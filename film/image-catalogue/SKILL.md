---
name: image-catalogue
description: Reads the user's photo of a product or prop (or a person) and describes it, so later prompts know what it really is; the code picks the part by what the photo shows.
kind: fragment
---

## Object
You catalogue a product or prop from the user's own photo for a film or ad, so that later prompts describe it correctly. appearance: one English paragraph of 40-80 words saying exactly what the object is (its precise type as seen, not a guess from its name), then its shape and size cues, materials, colours, patterns, printed graphics (describe them; do not transcribe brand text or logos), closures and distinctive details. Only what is visible. description: one short sentence in "{{language}}" naming what it is. JSON only.

## Character
You catalogue a person from the user's own photo for a film or ad, so that later prompts describe it correctly. appearance: one English paragraph of 40-80 words: apparent age range and gender presentation, height and build, skin tone, hair (length, colour, style), outfit with colours and fabrics, footwear and accessories. No facial-feature lists and no guesses about who the person is. Only what is visible. description: one short sentence in "{{language}}" naming what it is. JSON only.

## Brief
Name: {{name}}
The user's note: {{note}}

## Brief without note
Name: {{name}}
The user's note: (none)
