# video-skills

Every text a model reads, as Markdown skills, shared by the short-film API (`short-firm-ai/api`) and Ad Studio
(`ad-video-test`). The apps only load a skill, fill its runtime values and send it: change the words here, not in code.

## Format

One skill per folder: `<group>/<name>/SKILL.md`.

```markdown
---
name: director
description: One line: what the skill is for.
kind: fragment
version: v2
---

The text the model reads.
```

- **Frontmatter**: `key: value` lines between `---` fences. `name` and `description` always; `kind: fragment` for a
  piece that is only used inside other prompts (a rule block, a brief line); `version` where the app stores which
  version a result was made with (see `characters/README.md`). Other keys are read by the app that needs them.
- **Text**: everything after the frontmatter, trimmed at both ends. It is sent as it is: `## ` lines, backticks and
  `${` are plain text. The whole text is returned unless the app asks for one `## Section` of it.
- **Includes** `{{> path}}`: replaced by the whole text of `<path>/SKILL.md` (its includes resolved too), exactly
  where it stands, so shared rules exist once (e.g. `{{> shared/shot-craft}}`). A cycle is an error.
- **Placeholders** `{{name}}`: a runtime value the app fills in. The API throws when a placeholder has no value, so
  only add one together with the code that fills it. (Ad Studio leaves unknown `{{key}}` as they are: it uses them to
  name reference images; see its own skills.)

## Folders

- `shared/`: fragments used by many skills (crew wording rules, shot craft, story lock, content safety, blocking,
  camera position, tag guides, locked look, character forms, the dubbed brief line).
- `film/`: the short-film pipeline: crew members (director, screenwriter, supervisor, cinematographer, gaffer, sound,
  extras, safety reviewer, prompt writer, frame fit), writers (screenplay, scene planner, idea optimizer, idea logic,
  series editor, beats), series rules, the Vietnamese dialogue editor, clip check, safety rewrite and music brief.
- `characters/`: identity lines, voices and one design skill per art-style preset (`design-<preset>`), the extra views and outfit pictures drawn from a main image.
- `images/`: what every still image is told to draw: character and prop references (framing, age line, clean-up
  of a user's photo), setting images, character, animal and model sheets, frame shape words, the safety pre-check.
- `social/`: Facebook captions, link and trend analysts.
- `autopilot/`: the Facebook Page autopilot (planner, writers, marketing team, music pick, brief lines).
- `genres/`: the genres (one `genres/<key>/SKILL.md` each, found by listing the folder), their skills (router and
  modules) and the guide around them; see `genres/README.md`.
- `ad/`: Ad Studio's skills (storyboard, shot prompt, the two "Tối ưu prompt" optimizers, one `formats/<id>/` per
  video type with its `styles.md`); see `ad/README.md`. Ad Studio has its own loader: no `{{> path}}` includes there,
  and unknown `{{key}}` stay as they are.

## How the apps pull it

The API pins a ref in `api/skills.lock` and copies that ref into `api/skills/` (gitignored):

```sh
pnpm skills:pull                                   # the pinned ref from skills.lock
SKILLS_REF=main pnpm skills:pull                   # another ref
SKILLS_SOURCE=../video-skills pnpm skills:pull     # a local checkout, for development
```

The API reads `SKILLS_DIR` (default `skills/` in its working directory), loads every skill it uses at boot and stops
with a clear message if one is missing. CI pulls before it builds and ships `skills/` inside the release, so the
server needs no access to this repo.

Ad Studio (`ad-video-test`) does the same with its own `skills.lock`: `npm run skills:pull` checks the ref out into
`.skills/` and the app reads `.skills/ad` (`SKILLS_SOURCE=../video-skills npm run skills:pull` links a checkout).

## Versioning

Releases are git tags (`v1.0.0`, `v1.1.0`, ...). To ship a change: commit here, tag it, then put the tag's commit sha in
the app's `skills.lock` and run `pnpm skills:pull`. A text change that should redo stored work (a character's voice or
design) also bumps that skill's `version`.
