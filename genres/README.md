# genres

The film and commercial genres a project is made in. The API finds them by listing this folder at boot (no list of
genres in its code), builds each one from its `SKILL.md` and stops with the file and the reason when one breaks the
format below. Genres are read only in the app: a genre is added or changed here.

## Layout

```
genres/
  <key>/SKILL.md              the genre (kind: genre); the folder name is its key
  <key>/router/SKILL.md       its skill's router (optional; always read with the modules)
  <key>/<module>/SKILL.md     one module of its skill
  short-drama/<part>/SKILL.md the craft the sd_* genres share (included by them), and cute-child
  guide/SKILL.md              how the genre's rules are handed to the writers and the crew
```

A folder here is a genre only when its `SKILL.md` has `kind: genre`; `short-drama/` and `guide/` are not.

## The genre: `<key>/SKILL.md`

Frontmatter (one `key: value` per line):

| key | value |
| --- | --- |
| `name` | the genre's key, the same as its folder (`family_drama`) |
| `description` | one line about the file |
| `kind` | `genre` |
| `category` | `film`, `commercial` or `short_drama` |
| `name_vi`, `name_en` | the names the app shows |
| `sort` | its place in the app's list (a number) |
| `active` | `true` or `false` (switched off: listed only when asked for all) |
| `music_bed`, `holds_moments` | optional, `true` or `false` |
| `beat_sheet` | optional: `comedy`, `drama` or `""` (straight to shots); absent, the API's own list decides |
| `default_aspect_ratio` | optional: `9:16`, `16:9` or `1:1` |
| `default_continuity` | optional: `anthology` or `serial` |
| `default_planned_episodes`, `default_episode_duration_seconds` | optional numbers |
| `default_shot_pace` | optional: `short`, `medium` or `long` |

An unknown key is an error (a typo would otherwise be ignored).

Sections, every one required except `Voice` (a section may be empty: `## Lighting` with nothing under it is ""):

- `## Description`: the app's description (Vietnamese).
- `## Structure`: the beats in order, each a `### <role>: <name shown to the user>` line followed by its guidance for
  the writers. Roles: `hook`, `setup`, `turn`, `escalation`, `climax`, `payoff`, `cliffhanger`.
- `## Hook`, `## Pacing`, `## Dialogue`, `## Avoid`: what the writers read.
- `## Camera`, `## Lighting`, `## Sound`: each crew department's conventions.
- `## Serial`: how a serial episode ends.
- `## Voice` (optional): how the lines are delivered, told to the video model with every line. Absent means the genre
  has no voice; present and empty means an empty one.
- `## Tones`: the tones the app offers, one `- tone` line each (no other lines).

## The skill: `<key>/router` and `<key>/<module>`

Each part is a fragment read whole. Module folders: `storytelling`, `genre-engine`, `dialogue`, `directing`, `sound`,
`video-prompt`, `quality-check` and `lighting` (read by the gaffer alone). A genre with modules has a router. Which
modules each step reads (planning, writing, a shot, camera, lighting, sound) is decided in the API (`SKILL_STAGES`);
a genre without a skill folder is guided by its sections alone.

The `sd_*` genres share one craft: their router and modules are `{{> genres/short-drama/<part>}}`, and their own
`genre-engine` may include `{{> genres/short-drama/cute-child}}`.

## The guide: `guide/SKILL.md`

The lines around a genre's rules: `## Story` (the writers' guide, laid out: a line whose values are empty is dropped),
`## Serial`, `## Crew`, and the small pieces they are made of (the genre's name with or without the tone, a beat, the
voice line).
