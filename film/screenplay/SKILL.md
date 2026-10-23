---
name: screenplay
description: Reads the user's own screenplay as a beat sheet.
---

# Reading the user's screenplay

The user wrote this episode themselves, scene by scene. Turn it into a beat sheet that follows it faithfully: the director builds the shots on your beats, and the pipeline writes the video prompts (cast, places, light, voices) from them.

## Follow it exactly
- Every scene, in its order. Add no scene, drop no scene, merge none, invent no event, change no outcome. The cliffhanger stays the cliffhanger.
- Every spoken line (dialogue, voiceover, a line written inside a visual) is its own beat: line word for word in the screenplay's language, speaker the exact character name as the screenplay writes it (without titles or stage notes in brackets). A stage note in brackets becomes the delivery and the gag. Never shorten, paraphrase or merge a line: the story is in its words (a stolen head, a sect's name, a place at the foot of the mountain). A line of more than about 20 words becomes two beats, split only at a sentence end (". ", "! ", "? "), each with its own line, the same speaker, one after the other in the same shot; never split inside a sentence.
- The gag of a line beat carries the screenplay's own visual for that moment (hands clutching the head in shame, a cane sweeping a circle in the dirt), so the director keeps the body acting while the line is said; never only "he speaks".
- A scene with no line becomes 1-3 silent beats (speaker "", line "", delivery "") from its visual, in order.

## The story spine
When a STORY SPINE is given (the screenwriter read this screenplay before you), it decides what the story cannot lose. Every moment marked mustShow is one or more beats of its own, its gag written from the moment's "show" (the event at full force, in words that pass the safety checks: "a column of black mist rushes at Lão Cẩu; he swings the axe through it and golden sparks burst"), never a calmer version and never merged away. The screenplay's times are kept (see seconds); a mustShow moment is never merged into another beat's time. The spine never changes a line: lines stay word for word.

## shot: fewer, fuller shots
Number the shots from 1 and give every beat the number of the shot it is in. Each shot is one clip of at most the longest shot given below, generated on its own: every cut is a new drawing of the faces and the place, so the fewer cuts, the steadier the film. Aim every shot at the project's pace (given below): consecutive beats in the same place and the same continuous action share one shot until their seconds reach it.
- A framing the screenplay names on a beat ("Toàn cảnh", "Trung cảnh", "Cận cảnh", "Cực cận", wide, close-up) is how the camera sees that moment, not a cut: inside one shot it is a camera move from the beat before (push in from the wide to the close-up, pull back, tilt up from the hem to the collar, pan to the next person). Write that move in the beat's gag.
- Cut to a new shot only at a new place or scene heading, a time jump, a cut the screenplay spells out ("cut to", fast cuts), a jump the camera cannot travel in one move (from one person's face to someone far off-screen), or when the next beat does not fit the shot's time.
- A shot's lines must fit it: about 3 words a second, plus a moment. An exchange that does not fit goes on in the next shot.
- A beat longer than the longest shot is split at a natural point into shots of about that length, the action carried on.
A shot shorter than the pace is right only for a single beat standing alone (an insert, a reaction cut in on purpose), never as the default.

## Each beat
- gag: one English line, the visible action and acting of the beat (who does what, where, how it moves), starting the scene's first beat with its camera direction ("Camera: slow pan up from the water to the night sky.") and, when the scene has one, its key sound in a short clause ("Sound: bamboo flute, wind in the reeds."). Use the user's AI prompt of the scene as a visual reference (place, costume, props, light, mood), never its technical tags (8k, resolution, --ar, photorealistic, hyper-detailed, cinematic lighting) and never its art style: the project's style decides that.
- seconds: the screenplay's own time for the beat (its timestamp's end minus its start; a beat split in two shares it). The author timed the episode: keep it. Never shorten a beat to make the episode tighter, and never give a line less than it needs to be said (about 3 words a second plus 1 second; give it more when its stretch is too short). When the screenplay states no times, give each beat what its content needs (a line its speaking time plus a reaction, an action 3-6 seconds, a look 2-3 seconds).
- A beat's seconds are filled by its action, not by waiting: its gag says what moves for the whole stretch (the mist rolling in as the camera cranes down, the spirit's sleeves lifting, the lantern swinging), so a long beat is never a still frame.
- delivery: English, how the line is said ("whispering, alarmed", "slow, grave, smoke curling from his pipe").

## Safe wording
The image and video safety checks read words, not intent. Keep every scene's event at its full force (an attack still lands on something and is met; a binding still pins), but show its harmful detail by its effect, in visible wording (the spine's "show" already does this; follow it): a corpse is "a pale motionless figure", blood is left out (a pricked fingertip, a red thread), a scream is "a wide-open mouth, eyes wide", a monster lunging is "rises fast out of the water toward them", rotting hands are "pale hands", horror is "eerie", ominous is "moody". Lines in the screenplay's language stay word for word.

## Also return
- title: the episode's title from the screenplay ("" if none).
- durationSeconds: the screenplay's stated total length in seconds (the last scene's end time, or its stated length); 0 when it states none. The beats' seconds add up to about this.

Return {"title","durationSeconds","beats":[{"shot","speaker","line","delivery","gag","seconds"}]}. JSON only.

{{> shared/shot-craft}}
