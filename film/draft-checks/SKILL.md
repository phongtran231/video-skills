---
name: draft-checks
description: The problems the code finds in a writer's draft or a shot list (structure, names, lengths, English fields), one section each, sent back to the writer for its repair round. The scene writer tells small problems from big ones by their words (isMinor in scenes/scene-writer.ts: "has N words; keep it to", "camera has N moves", "characters on screen", "a speaking shot is a medium shot or closer", "timed beats; a Ns shot fits", ".action says", "has no line but runs", "needs at least Ns to be spoken in full"): change those wordings together with it.
kind: fragment
---

## Speech time
{{at}} is {{seconds}}s but its lines need at least {{needed}}s to be spoken in full, one after the other (about {{wordsPerSecond}} words a second, plus a moment around each line): make the shot longer (take the time from a shot without dialogue), each line's beat as long as its line, or move a whole line into the next shot; never cut a line short

## Shot count
The SCREENPLAY BEATS have {{wanted}} shot numbers, so the shot list must have exactly {{wanted}} shots (one per shot number, its beats as timed beats); it has {{written}}.

## Missing lines
The BEAT SHEET's lines must each be one shot's dialogue, word for word, by its speaker (a narrator's line goes in that shot's narration instead); {{count}} are missing: {{lines}}

## Pinned object
pinned object "{{name}}" is the user's own product/prop and appears in no shot: put "{{name}}" (exact name) in onScreen of the shots that show it, and remove any invented object that stands in for it

## Pinned character
pinned character "{{name}}" appears in no shot: put "{{name}}" (exact name) in onScreen of the shots that show them

## Not English
{{field}} must be written in English: "{{text}}"

## Appearance empty
{{field}}.appearance is empty; write the locked profile

## Appearance is style
{{field}}.appearance is style text; describe the person (age, build, skin tone, hair, outfit), not the style

## Form of unknown
{{field}}.formOf "{{formOf}}" is not the name of another character

## Other form
{{field}} appearance/imagePrompt mentions another form; describe only this form, and list the other form as its own character with formOf "{{name}}"

## Appearance lighting
{{field}}.appearance must describe only body, face, hair and clothes, not lighting

## Unknown location
scene {{scene}}.location "{{location}}" is not one of the locations; use a locations[].name exactly, or add that place to locations

## Too many locations
a {{seconds}}s film may use at most {{limit}} distinct locations (found {{found}}); merge scenes into fewer places

## Repeat shots
scene {{scene}} shots {{first}} and {{second}} show the same thing ({{people}}, no lines, about the same framing, {{seconds}}s together): merge them into ONE shot whose timeline holds both beats (the camera may move between them), or make the second a clearly different framing or event

## Repeat shots of nobody
scene {{scene}} shots {{first}} and {{second}} show the same thing (nobody, no lines, about the same framing, {{seconds}}s together): merge them into ONE shot whose timeline holds both beats (the camera may move between them), or make the second a clearly different framing or event

## Unknown on screen
{{at}}.onScreen "{{name}}" is not a character or prop name

## Too many speakers exchange
{{at}} has {{speakers}} speakers; keep at most {{allowed}} per shot (an exchange), each line in its own timed beat

## Too many speakers one
{{at}} has {{speakers}} speakers; keep one speaker per shot and move the reply to the next shot

## Off screen in frame
{{at}}: {{name}}'s line is offScreen but {{name}} is in onScreen; either take them out of onScreen (the voice comes from out of frame) or set offScreen false

## Listener talks
{{at}}: {{name}} talks or opens their mouth in opening/action, but the line belongs to {{speaker}}; only the speaker's mouth moves in a shot (others listen silently); give {{name}}'s words their own shot

## Silent shot talks
{{at}}: {{name}} talks or opens their mouth in opening/action, but the shot has no dialogue line; write the line in dialogue or keep them silent

## Crowded line
{{at}} has a line and {{count}} characters on screen; a speaking shot shows the speaker and at most one other character (keep the others out of the frame)

## Crowded
{{at}} has {{count}} characters on screen; keep at most three in a shot (faces of more drift), and split the rest into their own shots

## Wide line
{{at}} has a line but its camera is "{{camera}}"; a speaking shot is a medium shot or closer, so the face holds and the lips read

## Long line
{{at}}.dialogue line by "{{speaker}}" has {{words}} words; keep it to about {{maxLineWords}} words

## Unknown speaker
{{at}}.dialogue speaker "{{speaker}}" is not a character name

## Speaker off screen
{{at}}.dialogue speaker "{{speaker}}" is not in onScreen

## Too long
{{at}}.{{field}} has {{words}} words; keep it to {{max}} or fewer (one clear visible action, no adjectives piled up)

## No timed beats
{{at}}.action has no timed beats; write it as a timeline from 0s to {{seconds}}s ("0-1s: Setup: …; 1-{{middle}}s: Action: …; …"), with any line said in its beat

## Too many beats one
{{at}} is {{seconds}}s with {{beats}} timed beats; a {{seconds}}s shot fits {{budget}} (one action or one reaction): write its beats for this length from the start, never squeeze a longer shot's beats into it

## Too many beats several
{{at}} is {{seconds}}s with {{beats}} timed beats; a {{seconds}}s shot fits {{budget}} (a short setup, one action and a quick reaction): write its beats for this length from the start, never squeeze a longer shot's beats into it

## Beats not back to back
{{at}} beats must run back to back from 0s to {{seconds}}s (e.g. "0-1s: …; 1-{{middle}}s: …; {{middle}}-{{seconds}}s: …")

## Vague
{{at}}.action says "{{word}}": write the exact visible action instead (who does what with which hand, object or face), never that it is funny or dramatic

## Camera moves
{{at}}.camera has {{count}} moves ({{moves}}); keep it static or one slow move

## Short shot long line
{{at}} is {{seconds}}s and its line has {{words}} words; a shot of {{shortShotSeconds}}s or less fits one short line of {{shortLineWords}} words at most: shorten it or make the shot longer

## Still empty
{{at}}.still is empty; write the storyboard image the shot's video starts on

## Empty place
scene {{scene}} shot {{shot}} shows nobody and has no line but runs {{seconds}}s: an empty place runs at most {{emptyShotSeconds}}s; give the time it loses to the shots with action or lines, or put a character in it

## Then chain
scene {{scene}} shot {{shot}}.action chains {{count}} actions with "then" (pose after pose renders robotic): rewrite each beat as one continuous gesture with overlapping actions joined by while or as, and a secondary motion that keeps going (cloth, hair, smoke)
