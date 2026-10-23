---
name: script-writer-brief
description: The user's brief for the one-call script writer: the layout (Brief) and the parts the code picks by the project's frame, beats and language. Empty values leave their line empty.
kind: fragment
---

## Brief
{{series}}
{{genre}}
Idea: {{idea}}
Style: {{style}}
Length: no set length; the episode is as long as its story takes, never padded to reach a length or cut to fit one. Each beat is played out in full (the wind-up, the action and its result, a line and its answer, the reaction seen), never two or three actions crammed into one beat, and never holds, stares or padding.
{{frame}}
{{beats}}
Language: {{language}}
{{languageRequirement}}
PINNED CHARACTERS:
{{characters}}
PINNED OBJECTS/PROPS:
{{objects}}
{{spine}}
{{outline}}
Use at most {{maxLocations}} distinct locations.
Write the story and scene-by-scene script. Add only the characters (at most 6 in total) and props the story needs beyond the pinned ones; a single character is fine. Never add helpers, onlookers or crew the idea does not ask for, and if the idea says a character is alone (alone, solo, một mình), nobody else appears.
{{> film/script-json-shape}}

## Frame 9:16
Frame: Vertical 9:16 (the genre line names exactly this frame; compose every shot for it)

## Frame 1:1
Frame: Square 1:1 (the genre line names exactly this frame; compose every shot for it)

## Frame 16:9
Frame: Horizontal 16:9 (the genre line names exactly this frame; compose every shot for it)

## Screenplay beats
SCREENPLAY BEATS (the user's own screenplay, scene by scene, with its own cutting; build the shot list on it): beats with the same shot number are ONE shot, each beat one timed beat of its timeline in order, its line word for word by its speaker; never split a shot number into several shots and never merge two shot numbers. Write exactly {{shots}} shots, sized to their beats' seconds (at most {{maxShotSeconds}}s each). Add no other shots. Scenes: one per place or time jump. THE LINES ARE THE SCREENPLAY'S: copy each one word for word, whatever its length; never shorten, paraphrase, merge or drop a line (the word limits of the dialogue rule do not apply here), and size the shot to its lines instead (about 3 words a second, plus 2 seconds), up to the longest shot. THE TIMES ARE THE SCREENPLAY'S: each shot's durationSeconds is the sum of its beats' seconds (up to the longest shot); the dead-air, shot-length and reaction limits of the rules above never shorten it. Fill the time with movement that carries the beat (the mist rolling, the camera craning, the sleeves lifting), never a still frame. Each beat's gag names what the body does while the line is said: keep that action in the shot (a cane sweeping a circle in the dirt, hands clutching the head), never reduce a beat to "he speaks". A NARRATOR'S line (its speaker is the narrator: Voiceover, VO, Narrator, Người dẫn chuyện, Lời dẫn) is never dialogue: when the film is told by a narrator (NARRATION: ON) it goes word for word into that shot's "narration" field and nobody speaks it in the shot.
{{beats}}

## Beat sheet
BEAT SHEET (the episode's beats, already written; build the shot list on it): {{bitRule}} A beat's line is a shot's dialogue, word for word, by that speaker; its gag is that beat's action in the shot's timeline. A NARRATOR'S line (its speaker is the narrator: Voiceover, VO, Narrator, Người dẫn chuyện, Lời dẫn) is never dialogue: when the film is told by a narrator (NARRATION: ON) it goes word for word into that shot's "narration" field and nobody speaks it in the shot. Size each shot to its lines and gags. Add no other shots, except at most one opening shot that already starts the first joke. Scenes: one per place or time jump; the whole bit in one place and continuous time is ONE scene (ignore the usual scene count).
{{beats}}

## No beats
Scenes: one per place or time jump.

## Language vi
LANGUAGE REQUIREMENT: All dialogue character names and dialogue lines must be in Vietnamese, except proper names. Do not include English dialogue.

## Language other
LANGUAGE REQUIREMENT: All dialogue character names and dialogue lines must use the requested language.

## Outline
APPROVED OUTLINE (follow it exactly: same facts, events, order, outcome, characters and locations; group its beats into scenes and shots; add nothing that contradicts it):
{{outline}}
