---
name: view-line
description: A shot's view line, written from the cinematographer's blocking: where the camera stands, where the scene's focus is in the frame and which way the cast face. The openings "Camera in front, filming head-on" and "Camera at the side" are read back by the code (saved views are matched on them): keep them, and keep every line opening with "Camera at" or "Camera in".
kind: fragment
---

## Facing camera one
{{headOn}}: {{who}} faces the camera; behind them is {{behind}}

## Facing camera many
{{headOn}}: {{who}} face the camera; behind them is {{behind}}

## From behind
Camera at the back, looking toward {{focus}}: {{who}} seen from behind, facing {{focus}} ahead in the distance

## Focus frame left
{{sideOn}}: {{focus}} at the left edge of frame; {{who}} in profile, facing frame left toward it

## Focus frame right
{{sideOn}}: {{focus}} at the right edge of frame; {{who}} in profile, facing frame right toward it

## Everyone
everyone in frame

## Far side
the far side of the place

## Toward
{{verb}} toward {{focus}}
