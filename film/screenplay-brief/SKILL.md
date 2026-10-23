---
name: screenplay-brief
description: The brief of the screenplay reader (film/screenplay): the shot limits, the cast, the screenplay or one segment of it, and its one send-back.
kind: fragment
---

## Brief
Language of the lines: {{language}}
Longest shot the video model can make: {{maxShotSeconds}} seconds.
The project's shot pace: {{paceLabel}}; every shot (with lines or without) holds consecutive beats of the same place and action, as long as they take (at most {{maxShotSeconds}} seconds); a framing the screenplay names is a camera move inside the shot, not a cut.

## Cast
The project's cast (use these exact names for the same people): {{names}}

## Whole
SCREENPLAY:
{{text}}

## Segment
EPISODE HEAD (context only: the title, the cast, the stated length; no beats from it):
{{head}}

SEGMENT {{number}} of {{count}} (read only this segment into beats; its shots are numbered from 1):
{{segment}}

## Invented lines
These lines are not in the screenplay word for word: {{lines}}. Copy every line exactly as the screenplay writes it (a line over about 20 words may be split at a sentence end into two beats, nothing else).

## Corrected
Return the complete corrected JSON only.
