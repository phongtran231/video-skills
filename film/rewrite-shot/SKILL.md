---
name: rewrite-shot
description: Rewriting one shot in its place in the edit, around the director, extras, blocking, content safety and shot direction skills; the user's note or none, and the length check sent back.
kind: fragment
---

## Intro
You are the director of this film. Rewrite ONE shot (the target) so it plays better, keeping it in its place in the edit.

## Keep
KEEP: its story beat, its scene and location, and the hand-over with its neighbours: it opens from the previous shot's ending and transition and ends set up for the next shot's opening. Change only what the user asks (if anything) and what breaks the rules below. Its durationSeconds is yours to choose: as long as what it holds (its lines said whole at the pace people talk, about 3 words a second, the answer right after the line before; its action as long as it takes), at most {{maxShotSeconds}}, never stretched to fill time.

## Keep lines
KEEP its dialogue lines and its narration word for word, whatever their length: the dialogue word limits below are for writing a new line, never for cutting one that is there. Change a line only when the user's note asks for it; size the beat that carries a line to the time it takes to say.

## Language
Write the dialogue line in "{{language}}"; write camera, opening, action, ending, motion, rules, delivery and audio in English.

## Scene lines
background, layout, focus and opposite: the scene's lines (see the assistant director below), kept as they are unless missing or the user asks to change them. blocking: this shot's camera side, the place its camera line is filmed from. JSON only.

## Note
What the user wants changed: {{guidance}}

## No note
The user gave no note: fix what breaks the rules and make it play better.

## Return
Return {"shot":{"durationSeconds","camera","onScreen":[],"opening","action","ending","transition","carriesOn","dialogue":[{"character","line","delivery","offScreen"}],"audio","energy","motion","rules","moments":[]},"background","layout","focus","opposite","blocking":{"side","facing":[],"note"}}.

## Too long
shot.durationSeconds is at most {{seconds}}, the longest the video model makes
