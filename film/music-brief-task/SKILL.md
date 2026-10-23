---
name: music-brief-task
description: The answer format of the composer (after film/music-brief) and the lines of its brief: the world, earlier scores, the user's lead and feeling.
kind: fragment
---

## Answer
Return {"prompt","bpm","lead","mood","mood_vi"}. JSON only.

## World
The film's world: {{world}}

## Earlier
Earlier scores, the most recent last; never repeat their idea, nor the lead of the last two: {{earlier}}

## Lead
LEAD: {{lead}} (the user's choice: this instrument leads the score).

## Feeling
FEELING: {{mood}} (the user's choice: the score has this feeling's energy).
