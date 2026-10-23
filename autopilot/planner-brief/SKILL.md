---
name: planner-brief
description: The brief the autopilot planner (autopilot/planner) reads: the Page, the day, each format's world and the image slots to fill.
kind: fragment
---

## Brief
PAGE: {{page}}
DATE: {{date}}
{{videosOff}}

{{formats}}

SLOTS:
{{slots}}

## Slot
- {{time}}: FORMAT "{{format}}"

## Slot with kind
- {{time}}: FORMAT "{{format}}"
  KIND: {{kind}} (key {{key}})
  KIND BRIEF: {{brief}}
  PICTURES: {{images}}

## Format
FORMAT "{{name}}"
{{description}}
{{genre}}
{{style}}
{{imageStyle}}
{{kinds}}
CHARACTERS:
{{characters}}
RECENT EPISODES:
{{episodes}}
PAST IDEAS:
{{ideas}}

## Description
DESCRIPTION: {{description}}

## Genre
GENRE: {{genre}}

## Style
STYLE: {{style}}

## Image style
IMAGE STYLE: {{imageStyle}}

## Post kinds
POST KINDS: the user's own, one given with each slot below
CAPTION LANGUAGE: {{language}}
CAPTION VOICE: {{voice}}

## Content types
CONTENT TYPES: {{types}}
{{gallery}}

## Gallery size
GALLERY SIZE: {{size}} pictures

## Any type
(any)

## No voice
(none given)

## No characters
(none listed)

## None
(none)
