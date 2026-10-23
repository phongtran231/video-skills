---
name: identity-task
description: The answer format of the identity agent (after characters/identity) and the caption of each numbered image, with the age and look the story gives.
kind: fragment
---

## Answer
Return {"characters":[{"name","identity"}]}, one entry per image, name being the image's label exactly as given ("Character 1"). JSON only.

## Caption
Character {{number}}:

## Caption with age
Character {{number}}: (their age in the story: {{age}}; write this age, not the one the image seems to show)

## Caption with look
Character {{number}}: (their look in the story: {{look}})

## Caption with age and look
Character {{number}}: (their age in the story: {{age}}; write this age, not the one the image seems to show) (their look in the story: {{look}})
