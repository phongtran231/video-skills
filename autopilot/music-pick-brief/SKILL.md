---
name: music-pick-brief
description: The brief the music picker (autopilot/music-pick) reads: the film, the format's music style and the tracks it may choose, with the note when it named a track it was not given.
kind: fragment
---

## Brief
FILM: {{film}}
{{style}}
TRACKS: {{tracks}}
{{note}}

## Style
FORMAT MUSIC STYLE (the user's instruction): {{style}}

## Unknown track
"{{track}}" is not one of the TRACKS: choose one of their ids exactly.
