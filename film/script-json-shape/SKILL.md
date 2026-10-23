---
name: script-json-shape
description: The script's explicit JSON output shape and which fields are written in the film's language, for gateways that do not enforce the JSON schema.
kind: fragment
---

OUTPUT: one JSON object with exactly these keys and no others:
{"title","logline","story","style","look","genre","durationSeconds",
 "characters":[{"name","formOf","role","description","appearance","personality","imagePrompt","tags":[],"outfits":[{"name","appearance"}]}],
 "objects":[{"name","description","purpose","imagePrompt","tags":[]}],
 "locations":[{"name","description","props":[]}],
 "scenes":[{"sceneNumber","location","description","durationSeconds","wardrobe":[{"character","outfit"}],
   "shots":[{"durationSeconds","camera","onScreen":[],"opening","action","ending","transition","carriesOn","dialogue":[{"character","line","delivery","offScreen"}],"audio","energy","motion","rules","moments":[]}]}]}
Write title, logline, story, character names/roles/descriptions/personality, object names/descriptions/purpose, location names, scene descriptions and dialogue lines in "{{language}}".
Write the visual-production fields in English, because image and video models read them: style, look, genre, appearance, imagePrompt, locations[].description, locations[].props, camera, opening, still, action, ending, motion, rules, delivery, audio and tags.
style: copy the given Style exactly; do not add framing, aspect ratio, film grain or realism terms.
look: one English line of cinematography for the whole film, opening every clip prompt: lens, light direction, quality and colour for the time of day, depth of field, colour grade and atmosphere, e.g. "Cinematic film shot, 35mm anamorphic lens, golden-hour backlight with volumetric sun rays and soft lens flare, shallow depth of field, rich warm color grade, light sea haze". It suits the style (an animation style still gets lens and light) and never names a film, studio or brand.
