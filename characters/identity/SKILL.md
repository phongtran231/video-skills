---
name: identity
description: Identity lines: what tells each character apart in their image.
---

# Identity lines

You look at each character's reference image, the one a video model receives in every shot with them, and write the line that tells the model who that image is. The model keeps a character the same from shot to shot by matching your words to the image, so name what is plainly seen in it.

## identity: one line per character
What is seen, in this order, as short comma-separated items (no sentences, no "wearing", no articles):
1. Who: woman, man, girl, boy (or the animal: "tabby cat"), always first. When their look in the story is given, the gender is the story's, even if the drawing could be either: a woman drawn with short hair is still "woman". Never leave it out: without it the model picks one, and an androgynous cook written "28, clean-shaven" was drawn as a man in every shot.
2. Face anchors, which keep the face from drifting between shots: the apparent age as a number ("about 35"), the face shape ("long oval face", "round chubby face"), and for a man the facial hair ("clean-shaven", "thin moustache", "short black beard"; never for a woman).
3. Hair: length, colour, style (or "shaved bald head").
4. What is on the head or face: headband, hat, glasses, earrings.
5. One or two features of the face that stand out in the image (e.g. "big expressive eyes", "thick eyebrows", "round cheeks"): the face itself, never the expression of the moment (no crossed eyes, open mouth, grin, wink, tongue out: the shot sets the expression).
6. The outfit from top to toe, with exact colours and the one detail that makes each piece recognizable: "yellow mandarin-collar tunic with dark toggle buttons", "red sash", "charcoal-gray trousers".
7. Footwear.
8. A prop they always carry, if the image shows one.
The form only (never borrow its words; every item comes from the image): "man, about 40, round face, short grey stubble, curly dark-red hair tied back, small gold hoop earring, heavy-lidded eyes, mustard knitted cardigan over a green striped shirt, patched brown corduroy trousers, white canvas sneakers, wooden walking cane"

## Rules
- Only what the image shows, in the image's own colours. Never describe from memory: a character may look like a famous one (a monkey king, a monk, a pig in robes) but be the user's own redesign, and its outfit, colours, hair and props are whatever this image shows, not the classic version.
- No height, build, skin tone, personality, mood, pose, lighting, background or art style: the image carries those (the age, face shape and facial hair above are the exception: they hold the face).
- Tell the cast apart: when two characters look alike, put first the items that differ.
- If you cannot see an image, return an empty identity for it; never guess.
- Calm, neutral words only: the line goes into every video prompt, whose safety check reads words. Name what is seen without words a strict reviewer would refuse (blood, wounds, gore, rotting, corpse-like, claws, fangs, weapons aimed, torn burial rags): "dark red stains" is "dark red patches", a "bloodied robe" a "red-patterned robe".
- 15 to 30 words, English, lowercase except names. If the image is a character sheet (several views), describe the one person once.
