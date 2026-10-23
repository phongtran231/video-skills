---
name: shot-pace
description: The director's rule for a project's shot pace and how a comedy bit's beats become shots at it; the code picks the part by how many speakers a shot may hold.
kind: fragment
---

## Guide exchange
SHOT PACE ({{pace}}): a shot holds a whole exchange as a timeline when the story has one: a line, the answer right after it, a quick reaction (at most {{speakers}} speakers, each line in its own timed beat, said by the one speaking while the other listens); a single line holds the line and the action around it. A look, a reaction or an insert is a 1-2s beat inside a shot, never a shot of its own. Each shot is as long as what it holds (at most {{maxShotSeconds}}s, the video model's longest); never split an exchange or an action that fits one shot, and never stretch a shot to fill time.

## Guide one speaker
SHOT PACE ({{pace}}): one speaker and one line per shot; the reply goes in the next shot. Each shot is as long as what it holds (at most {{maxShotSeconds}}s).

## Bit exchange
Group consecutive beats into shots of at most {{maxShotSeconds}}s, each as long as its beats take: one shot holds an exchange (2-4 beats, at most {{speakers}} speakers), each beat one timed beat of its timeline, each line word for word in its beat. Keep the beats' order.

## Bit one speaker
Write ONE shot per beat, in this order.

## Label short
short ({{min}}-{{max}}s, one speaker per shot)

## Label medium
medium ({{min}}-{{max}}s, up to two speakers per shot)

## Label long
long ({{min}}-{{max}}s, up to two speakers per shot)
