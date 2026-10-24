# Skills

The prompts the AI follows, as plain Markdown. Edit a file and the next video uses it: no code change, no rebuild in dev
(the server reads them on every request; in production they ship next to the server, see `npm run build` / Dockerfile).

- `storyboard/SKILL.md`: how every storyboard is written (shots, continuity, references, voice-over, safety).
- `formats/<id>/SKILL.md`: one per video type shown in the UI. Frontmatter: `label`, `description` (UI), `order`, and
  pipeline flags the code relies on (`composite: fan`, `product_last: false`). Sections:
  - `## Director` (who the AI is), `## Structure` (the order of the video and its rules), `## Voice-over`,
  - `## Prompt guide`: what a good initial prompt for this type says (used by "Tối ưu prompt").
  - `## Prompt samples`: example prompts, one `### Title` each (Vietnamese, written like a video-model prompt); the first three
    are the AI's style reference when it writes or improves a prompt. (The "Mẫu" gallery the user browses is `gallery/`.)
  Add a folder here to add a video type.
- `shot-prompt/SKILL.md`: the exact prompt each storyboard shot is rendered with (layout from Google's Veo prompt guide:
  style first, then scene, cast, `Dialogue:` with speaker and voice, `Audio:`). One `## Section` per line; a section
  without data for the shot is left out.
- `optimize-clip/SKILL.md`: "Tối ưu prompt" on Tạo: a rough idea -> a prompt for one picture or one clip (Veo layout), with
  the first/last frame and the [ảnh n] references shown to the AI.
- `optimize-prompt/SKILL.md`: turns the user's rough prompt (or nothing) plus the product into a strong initial prompt.
- In both optimize skills the text before the first `## ` is the system prompt; the `## …` sections below it are the
  parts the code puts together (the mode's rules, the style note, the labels above each photo, the user's message).

Placeholders filled by the code: `{{duration}}`, `{{min_shot_s}}`, `{{max_shot_s}}`, `{{min_shots}}`, `{{language}}`,
`{{transitions}}`, `{{director}}`, `{{structure}}`, `{{voiceover}}`, `{{format_label}}`, `{{prompt_guide}}`, `{{prompt_examples}}`.
Any other `{{key}}` (e.g. `{{product}}`) is left as is: it is how the storyboard names a reference image.
