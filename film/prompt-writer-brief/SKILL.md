---
name: prompt-writer-brief
description: The briefs of the prompt writer (film/prompt-writer) and the frame fit (film/frame-fit): a scene's shots to write, the note on shots left out, the prompt to fit to a picture, what was observed at the end of the shot before and the clip check's faults, and the narration marker on a shot.
kind: fragment
---

## Ask
Write the texts for the shots listed under WRITE; the other shots of the scene are there for what comes before and after.
FILM: {{film}}
SCENE: {{scene}}
ALL SHOTS OF THE SCENE: {{shots}}
{{notes}}
WRITE: {{write}}

## Left out
Shot {{shot}} was left out or came back incomplete: write all its texts (video, animate, still).

## Fit
THE PROMPT (written before the picture existed):
{{text}}

## Observed end
OBSERVED END OF THE SHOT BEFORE (what the clip checker saw in its last frames; it overrides the plan):
{{end_state}}

## Rejected
THE CLIP CHECK FOUND FAULTS IN THE SHOT BEFORE, so the picture is not usable; write the shot to be made without it:
{{faults}}

## Opening picture
THE PICTURE the video starts on:

## Narration
a narrator is laid over this shot later: nobody speaks in it
