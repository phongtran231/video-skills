---
name: scene-plan
description: The scene planner's brief (its parts chosen by what the episode is made from), its repair round and the plan problems the code sends back.
---

## Screenplay
Screenplay:
{{idea}}

## Idea
Idea:
{{idea}}

## Head
Style: {{style}}
Language: {{language}}
Length: no set length; the episode is as long as its story takes, never padded to reach a length or cut to fit one. Each beat is played out in full (the wind-up, the action and its result, a line and its answer, the reaction seen), never two or three actions crammed into one beat, and never holds, stares or padding.

## Frame vertical
Frame: Vertical 9:16 (the genre line names exactly this frame).

## Frame square
Frame: Square 1:1 (the genre line names exactly this frame).

## Frame horizontal
Frame: Horizontal 16:9 (the genre line names exactly this frame).

## Limits
Shots run at most {{maxShotSeconds}}s; the project's shot pace is {{pace}}.
Use at most {{maxLocations}} distinct locations.
PINNED CHARACTERS (exact names; keep their looks):
{{characters}}
PINNED OBJECTS/PROPS (exact names; the user's own products or props):
{{objects}}

## Spine
STORY SPINE (moments by id; list in each scene's "moments" the ids it shows; every mustShow id in some scene):
{{spine}}

## Outline
APPROVED OUTLINE (follow it exactly: same facts, events, order, outcome, characters and places; group its beats into scenes):
{{outline}}

## Numbered beat sheet
BEAT SHEET (the episode's beats, numbered in order; a number is one beat, not a shot: the scene's director groups beats into longer shots). Give every beat number to exactly one scene in its "shots", contiguous and in order, a scene holding the beats of one place and time; its durationSeconds is the time its beats take on screen (their lines at about 3 words a second, and the action around them); "beats" is "".
{{beats}}

## Screenplay beats
SCREENPLAY BEATS (the author's shots; beats with the same shot number are one shot). Shot numbers and their seconds: {{shots}}.
Give every shot number to exactly one scene (the scene of the segment it sits in), contiguous and in order; a scene's durationSeconds is the sum of its shots' seconds; "beats" is "".
{{beats}}

## Beat sheet
BEAT SHEET (the episode's beats in order; group them into scenes and write each scene's "beats" from them; "shots" is []):
{{beats}}

## No beats
No screenplay beats: plan scenes by place, time jump and act; "shots" is [].

## Contract
LANGUAGE CONTRACT: title, logline, story, character names/roles/descriptions/personality, object names/descriptions/purpose, location names and scene descriptions in "{{language}}"; style, look, genre, appearance, imagePrompt, tags, locations[].description/props and every scene's light, beats, starts and ends in English.
OUTPUT: one JSON object with exactly these keys:
{"title","logline","story","style","look","genre",
 "characters":[{"name","formOf","role","description","appearance","personality","imagePrompt","tags":[],"outfits":[{"name","appearance"}]}],
 "objects":[{"name","description","purpose","imagePrompt","tags":[]}],
 "locations":[{"name","description","props":[]}],
 "scenes":[{"sceneNumber","location","description","durationSeconds","light","moments":[],"shots":[],"beats","starts","ends","wardrobe":[{"character","outfit"}]}]}

## Repair
{{brief}}
YOUR PREVIOUS ANSWER:
{{answer}}
That plan has these problems:
{{problems}}
Return the complete corrected JSON only, with exactly the required keys. Keep the same story, cast, places and scenes except where a fix requires a change.

## No scenes
scenes is empty: plan the film as one or more scenes

## Scene numbers
sceneNumber must run 1, 2, 3… in order (got {{numbers}})

## Shots in no scene
screenplay shot numbers {{shots}} are in no scene's "shots": put each one in the scene of the segment it belongs to

## Shot not in screenplay
shot number {{shot}} (scene {{scenes}}) is not in the screenplay beats: remove it

## Shot in several scenes
screenplay shot {{shot}} is in more than one scene (scenes {{scenes}}): keep it in exactly one

## Shot order
scenes' "shots" must run in the screenplay's order, each scene a contiguous run (expected {{expected}}; got {{got}})

## Pinned character
pinned character "{{name}}" is not in characters: list it with its exact name

## Pinned object
pinned object "{{name}}" is not in objects: list it with its exact name

## Moments in no scene
STORY SPINE mustShow moments {{moments}} are in no scene's "moments": list each id in the scene that shows it

## Too many locations
a {{seconds}}s film may use at most {{limit}} distinct locations (found {{found}}); set more scenes in the same places
