# characters

- `identity`: the line that ties a character's name to their reference image in every clip prompt, written by looking
  at the image itself, so it names what the video model will see.
- `voice`: the line that tells the video model how a character sounds, given with every line they speak.
- `design-<preset>`: one per art-style preset (`cartoon_3d`, `cartoon_2d`, `manhua_horror`, `storybook`,
  `painted_anime`, `watercolor_sketch`, `animal_3d`): turns a character's role, personality and notes into a look made
  for that style, before the character is drawn. `preset` in the frontmatter is the project's `art_style.preset`.

## version

The API stores the version a character was made with (`voice` as the voice's skill, `design-*` as the marker
`cartoon_3d:v2`). A stored result made under another version is made again, so bump `version` when a text change
should redo existing characters.

Voice history:
- v2: a habit is in how the voice sounds, never in the words (v1's "stammers" repeated words).
- v3: every voice speaks with clear diction (breathy, whispery or gravelly voices made some Vietnamese lines hard to
  understand).
- v4: no voice is fast (a nervous young man cast "rushed and uneven" said 49 words in 8 seconds); nerves and energy are
  in the rhythm and the colour, never the speed.
- v5: a line flows in one breath; nothing comes before or inside it ("halting", "watchful pauses" made the video model
  start a word, stop, and say it again).
- v6: no tight throat, tremble or breathiness either; nerves are in the attitude, never a broken voice.
- v7: a screen actor's voice, never a performance of one ("theatrically seductive" made the cast sound like amateurs).
- v8: a natural conversational pace ("slow and measured" voices talked like children reading aloud).

Design history:
- cartoon_3d v2: v1's "ugly-cute" came out scary (realistic skin, scars, bolts, spindly limbs): soft and lovable now.
