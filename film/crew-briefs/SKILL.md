---
name: crew-briefs
description: The crew members' tasks and the fixed lines of their briefs (the genre header, the neighbouring scenes, the safety review, the story supervisor's opening).
kind: fragment
---

## Extras task
Write the layout (with where the cast sit), focus, opposite and background of every scene (scene numbers as given). Return {"scenes":[{"scene","layout","focus","opposite","background"}]}.

## Cinematographer task
Write the camera line and the blocking of every shot (scene and shot numbers as given), and the look for the whole film. Return {"look","shots":[{"scene","shot","camera","side","facing":[],"note"}]}.

## Gaffer task
Write one stable lighting baseline for every scene and optional motivated lighting cues for shots where the physical light changes. Return {"scenes":[{"scene","lighting"}],"shots":[{"scene","shot","lighting"}]}; return an empty shots array when no cue is needed.

## Sound task
Write the ambience of every scene and the effects of every shot (scene and shot numbers as given). Return {"scenes":[{"scene","ambience"}],"shots":[{"scene","shot","audio"}]}.

## Genre
# THIS FILM'S GENRE: where it differs from the rules above, it wins
{{rules}}

## One scene
Work on scene {{scene}} only. previousScene and nextScene are the neighbouring scenes' boundaries, for continuity across the cut: do not write them.

## Supervisor neighbours
NEIGHBOURS (do not rewrite them; this scene must join them): {{neighbours}}

## Safety
Review every field below and return only what you changed.
{{film}}

## Story with spine
Watch the whole episode against the screenwriter's spine; return the problems you find and the shots you rewrote.
{{film}}

## Story without spine
Watch the whole episode (there is no spine: take the story from the title, the story summary and the scenes); return the problems you find and the shots you rewrote.
{{film}}
