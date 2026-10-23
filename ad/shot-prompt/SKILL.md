---
name: shot-prompt
description: Turns one storyboard shot into the prompt the video model renders.
---

Layout from Google's Veo prompt guide (deepmind.google/models/veo/prompt-guide), which Grok Imagine reads the same way:
the kind of video and its style first, then where, what happens and how it is filmed, who is in it, the dialogue
attributed to its speaker with how they sound, and the sounds in an Audio part of their own.

How this file is used: every `## Section` below is one line of the prompt, in this order. A section is left out when
one of its placeholders has nothing for this shot (no line to say, no camera note, no product photo…). A section
whose placeholder is a list is repeated once per item. Placeholders:
{{aspect}} {{look}} {{location}} {{opening}} (a cut) or {{carried_opening}} (carries on), {{action}} {{camera}} {{ending}} {{cast}}
{{speaker}} {{language}} {{voice}} {{oncamera_line}} {{voiceover_line}} {{audio}} {{dialogue_note}}
{{product_tag}} {{reference_tags}} (list).
`<IMAGE_n>` are the reference photos sent with the shot, `<AUDIO_0>` the chosen voice.

## Style
Realistic {{aspect}} video ad shot{{look}}.

## Location
Location: {{location}}.

## Opening
Opening frame: {{opening}}.

## Carried-on opening
The shot starts exactly on <IMAGE_0> (the previous shot's last frame) and carries on from it: {{carried_opening}}.

## Action
{{action}}.

## Camera
Camera: {{camera}}.

## Last frame
Last frame: {{ending}}.

## Cast
Recurring cast (only those this shot shows): {{cast}}.

## Dialogue on camera
Dialogue: {{speaker}}, looking into the camera and speaking {{language}}{{voice}}, starting right at the beginning of the shot with no pause, lively and expressive with natural gestures, at a clear natural speed with clear pronunciation, lips in sync: "{{oncamera_line}}"

## Dialogue voice-over
Dialogue: Voice-over, off screen, in {{language}}{{voice}}, starting right at the beginning of the shot with no pause, lively and expressive, at a clear natural speed with clear pronunciation: "{{voiceover_line}}"

## Audio
Audio: {{audio}}{{dialogue_note}}. No background music.

## No text
No captions, no subtitles, no on-screen text.

## Keep the product
Keep the product exactly as in {{product_tag}}: same shape, colors, logo and label; a label or logo stays facing the camera, steady and sharp, never redrawn in motion.

## Keep each product photo
Keep {{reference_tags}} exactly as pictured: same cut, colours, pattern and details.
