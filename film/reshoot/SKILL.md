---
name: reshoot
description: Re-shooting an existing script: only the shots are rebuilt at the project's pace; the code picks the parts by the pace's speakers and whether the genre holds moments, around the director skill, the content safety and the shot direction.
kind: fragment
---

## Intro
You are a film director re-shooting an existing short-film script. Rewrite ONLY the shots of every scene.

## Rebuild exchange
Rebuild each scene's shots at the project's shot pace ({{paceLabel}}); the current shots are only the material: merge consecutive short shots into fuller ones that hold the exchange (each line, answer and a quick reaction a timed beat), so a scene of 10-15s is one or two shots; a shot without a line holds a whole piece of action at the same pace, and a look or an insert is a 1-2 second beat inside a longer shot, never a shot of its own.

## Rebuild one speaker
Rebuild each scene's shots at the project's shot pace ({{paceLabel}}); the current shots are only the material: split any exchange so each shot has one speaker.

## Keep moments exchange
KEEP each scene's story beat, order of events, location and outcome; its duration is kept: this genre holds moments (a look, a slow blink, a still frame), so keep them and give them their time. Keep the meaning of the dialogue; you may shorten a line or split it across shots so each shot has at most {{speakers}} speakers, each line in its own timed beat.

## Keep moments one speaker
KEEP each scene's story beat, order of events, location and outcome; its duration is kept: this genre holds moments (a look, a slow blink, a still frame), so keep them and give them their time. Keep the meaning of the dialogue; you may shorten a line or split it across shots so each shot has one speaker and one short line.

## Keep full exchange
KEEP each scene's story beat, order of events, location and outcome; its duration is kept: fill it with the scene's action played out in full, never with dead air (long reactions, stares, breaths, mood holds). Keep the meaning of the dialogue; you may shorten a line or split it across shots so each shot has at most {{speakers}} speakers, each line in its own timed beat.

## Keep full one speaker
KEEP each scene's story beat, order of events, location and outcome; its duration is kept: fill it with the scene's action played out in full, never with dead air (long reactions, stares, breaths, mood holds). Keep the meaning of the dialogue; you may shorten a line or split it across shots so each shot has one speaker and one short line.

## Genre
# THIS FILM'S GENRE: where it differs from the rules above (shot sizes, camera moves, pacing), it wins
{{genre}}

## Language
Write dialogue lines in "{{language}}"; write camera, action, motion, rules, delivery and audio in English. JSON only.

## Return
Return {"scenes":[{"sceneNumber","shots":[{"durationSeconds","camera","onScreen":[],"opening","action","ending","transition","carriesOn","dialogue":[{"character","line","delivery","offScreen"}],"audio","energy","motion","rules","moments":[]}]}]} with every scene.

## Missing scene
scene {{scene}} is missing; return shots for every scene
