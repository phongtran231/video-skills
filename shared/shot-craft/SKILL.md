---
name: shot-craft
description: The rules every agent follows when it writes or rewrites a shot or a clip prompt.
kind: fragment
---

# Shot craft (for every agent that writes or rewrites a shot or its prompt)

The video model gets each shot as a prompt in sections, made of your words: SUBJECTS (who is in it), BACKGROUND (the place and its light), RULES (the shot's rules line and its motion line), TIMELINE (the opening frame, one line per timed beat, the ending), STYLE, SOUND. Nothing is added to your words and nothing is reworded, so write every field the way the model should read it.

## Long shots, few cuts
Every cut is a new drawing of the faces and the place. Size shots to the project's pace (about 10 seconds at the long pace). A look, a reaction, a detail or a single move is a 1-2 second beat inside a longer shot, never a shot of its own. A scene longer than one shot runs on into the next shot of the same place, the action carrying across the cut.

## Timed beats are a shot list
Each timed beat says: what the frame holds in that moment, with one focal point ("close on her hand on the bell", "both of them by the gate"); what moves, as a path from one place in the frame to another with a speed, never a pose; and who stays in the frame when someone enters or could be lost. Never where the camera stands (behind, over a shoulder, from the side). A key event of the story is framed medium or closer; a wide frame shows the people in the place and names its near, middle and far layers; scale is a comparison ("the figures reach only the first eave"), never an adjective.

## Acting: truthful, specific, held back (the film is only as good as its acting)
Played the way the beats asked, the cast looked like amateurs: big faces, waving hands, everyone frozen while one spoke. Screen acting is the opposite:
- Every line has a want and a hidden one: what the speaker wants from the other right now, and what they will not say. A beat says what they do to get it, never only the feeling ("she keeps her voice light and folds the card twice, so he cannot see her hands shake").
- A thought comes before a line, in the beat before it or in a glance at its very start (the look that lands, the moment of deciding to speak); then the line is said at the pace people really talk, never slowed down. A realisation is played in the eyes before anyone moves.
- Small and exact beats big and vague: a swallow, the jaw tightening, eyes that drop and come back, a hand stopping halfway. Never mugging, wide-eyed alarm, clutching the chest, throwing the arms out, a gasp to the camera, rolling eyes, an exaggerated smile.
- The listener acts as much as the speaker: they listen with the face and the eyes (a blink held too long, a slow nod that is not agreement), mouth closed, lips still. Nobody stands frozen like a statue.
- With two or more people in the frame, only the beat's owner (the speaker, or the one the beat is about) makes a large move (stands, walks, turns the body) or handles a prop; everyone else keeps small continuous motion only (a blink, a glance, a small shift of weight). A prop is then handled by one person in one simple hand action, or off-screen. When several people moved and handled things at once, props multiplied and people were drawn twice.
- Melodrama is big in what is at stake, not in the faces: the bigger the moment, the stiller and more precise the acting; the tears come at the end of the fight to hold them back, not at its start.
- Comedy (the genre says so) may push the faces; nothing else does.

## Feelings are shown by the body, and each move grows out of the last
- The video model cannot play "sad", "angry" or "scared": a beat says what the body does with it, the part and how much. Grief is the head lowering, the shoulders shaking a little, fingers tight on the hem of a sleeve; fear is a quick glance at the door, a hand closing on the table's edge, a step back; anger is the jaw set, the fists closed, the shoulders squared. Never a feeling word alone in a beat, the opening, the still or the ending.
- Name the part and the degree: "slowly lifts her right hand", "turns his head quickly toward the gate", "lowers her eyes a little". "She reacts" or "he moves" tells the model nothing.
- Each beat's move starts from where the last one left the body: "carried by the turn, she lifts the lantern", "from the pause, he raises his hand"; never a new move from a reset pose. A beat holds what the body can do in its seconds, nothing more.
- A feeling is one plain word and one physical anchor ("afraid: her hand stops on the latch"), never an idiom or a figure of speech: the model plays the words literally, and "her heart in her throat" or "cold feet" become pictures.
- An accident (a slip, a spill, a coat caught on a nail, a cup knocked over) is never what a beat ends on: write the deliberate action that the person does on purpose, or keep the accident off-screen and show its result already there (the tea already spilt on the table). Told to let a cup slip, the model staged it as a deliberate drop, and the moment read as anger.

## camera
One line: shot size, angle, ONE move with where it starts and where it ends ("slow push-in from medium to medium close-up on Lão Cẩu", "pan left to right from the gate to the altar") or static, lens and focus. A shot that covers an exchange may chain two smooth moves into one path at a consistent scale ("medium two-shot, slow pan from Tiểu Cẩu to Lão Cẩu"); never more.

## Face persistence and stable shot scale
The image model draws each shot's opening still from the character sheets, and the video model animates from that first frame. A face drifts or morphs whenever a single clip jumps drastically in scale (such as wide to close-up in one shot) or packs too many faces into the frame:
- Keep one stable shot scale within a single shot: stay at the opening still's scale or shift at most one neighbouring step ("medium to medium close-up", "wide tracking"). Never zoom or push in from a wide room all the way to a tight close-up in one clip; make a closer view its own shot with its own opening still at that size.
- In a drawn style (2D, anime, manhua, cartoon, watercolor), hold the camera distance steady or move gently parallel so the opening still's drawn face never rescales into a realistic or 3D face.
- At most two focal characters in onScreen in any shot where faces matter (three at most in a wide shot): the video model takes at most three reference images (the opening frame plus two character sheets), so a third character's sheet is dropped if three are on screen.
- When a character speaks or reacts, frame them at medium or medium close-up from the first frame of the shot, with their face in a clear front or three-quarter view; never turn a character 180 degrees from their back to their face mid-shot.
- Two people in one shot are told apart by what differs (hair, clothes, size, which side each sits on), never called twins or alike; never re-describe a character's face or age in the beats.

## Coverage inside one shot (an exchange: a line and who hears it)
When one shot covers a spoken exchange, keep both speakers at a readable medium or medium close-up scale so their faces hold from start to finish:
- Hold a two-shot where both faces read clearly, or pan smoothly at the same medium close-up distance from the speaker to the listener. Never write "CUT 1 / CUT 2" inside a shot.
- Whoever moves while the camera is on them moves across the frame or toward the other person, never straight into the lens: their face and shoulders stay in the frame. A shot never ends on a shoulder, a back or a body blocking the lens.

## Action continuity across cuts
Each shot is generated on its own without seeing the clip before or after it, so abrupt action jumps happen whenever two consecutive shots disagree on where a body or hand is at the cut:
- Within a scene, a shot's opening and still must match the exact spatial position, facing, posture and hand/prop placement of the previous shot's ending ("his right hand already resting on the brass bell on the altar"), viewed from the new camera angle (at least 30 degrees different).
- The first timed beat (starting at 0s) must begin directly from the opening frame's motion trajectory, never resetting to a neutral stand or repeating the start of an action the previous shot already played.
- A shot that carries on from the shot before (continues) says once, at its start, what is already done and what is under way: "the cup already set down by her hand, the letter already open; she is still turning toward the door". Its first beat carries on the movement under way. Told only the next action, the model played the shot before's last action again, and a cup already set down came back into a hand.
- Use cut_on_action only when the outgoing ending and incoming opening name the exact same continuous limb or body path from a new angle. Otherwise, let the outgoing gesture finish into a living follow-through state (cloth settling, a hand coming to rest, gaze shifting) and use a clean cut so independently generated shots never mismatch mid-swing.

## Scene transitions across locations
- The last shot of a scene settles its action on a clear visual beat and hands over with a deliberate effect chosen for the moment (dissolve, dip_black, fade_black, flash or zoom_in, varied across the episode; a plain cut only for a hard smash cut); never use cut_on_action, whip_pan, match_move or push_through at the end of a scene when the next scene moves to a different location.
- The first shot of a new scene in a new location opens cleanly from its planned starts state, already in the action, the place read around the people in it (wide enough to see who is where), never an empty establishing view, an arrival or a walk in, never carrying over motion blur or an unfinished gesture from the previous location.
- When the next scene continues in the same location, its first shot opens from the previous scene's ends state and changes camera size or angle by at least 30 degrees to avoid a jump cut.

## motion (one line, 25-50 words)
How THIS shot moves. A calm shot: one continuous performance already moving on the first frame, weight and follow-through, listeners blinking, glancing and shifting their weight, the camera's feel. An action shot: real speed, a quick wind-up and a clean stop, speed lines on the fastest moves, cloth and hair snapping, dust from every step, a half-second pause on the flash at the peak, the handheld camera following. A shot without people: what in the place keeps moving. A drawn style: "fully animated like a feature film, never stiff or held".

## rules (one line, 15-50 words)
What holds for the whole shot: who is in the frame and stays in it (by name, and that nobody else enters), who stays silent with their mouth closed while another speaks, and always that nothing is written on screen (with a line: it is only heard, never shown as subtitles or captions). With a line, also how it is said: "Tiểu Cẩu says his line in Vietnamese word for word, in one smooth flow from first word to last, clearly, at a pace a listener follows".

## Lines (nothing else tells the video model how to say them)
A line is spoken in the beat it sits in, and only there; the model starts it as that beat starts. A Vietnamese line said in pieces comes out with a word said twice ("Vệt vệt máu đỏ"), so give it room and one flow:
- The beat that carries a line starts on the line and lasts at least its speaking time: about 3 words a second plus one second ("Cha! Vệt máu đỏ chỉ còn cách tim ba tấc nữa thôi!", 12 words, needs a beat of 5 seconds). Count the words of every line. Two lines in one shot need both speaking times back to back: the answer's beat starts only after the first speaker's beat has its full time, so the shot is at least their sum (two 9-word lines: 2 × 4 = about 8 seconds). A line's beat is no longer than that: given more room, the model stretches the line to fill it, with long silences between its words, and the cast talk as slowly as children reading aloud ("Vanessa… don't… Not tonight" over four seconds). A shot with more time than its lines puts the rest in a beat of its own after the line, with no line in it (the other's reaction, a move, a held look), never inside the line's beat. When the lines of a shot do not fit its length (the longest shot included), the line that does not fit goes whole into the next shot, which carries on the same exchange in the same place; never cut a line short, squeeze its beat, or let the next speaker start before it is finished.
- In that beat the speaker does one small movement that goes on while speaking (turns the head, points, lifts a hand), standing in place: never walking or crossing the frame while speaking (a cat gliding into a doorway as she spoke barely moved her lips, and her line was seen on the dog), never a start-stop action, a gasp, a flinch or a breath before the first word. Whoever listens keeps their place with the mouth closed and the lips still, and listens with the face: shock is in the eyes and the stillness, never a gaping mouth.
- The speaker's mouth stays in plain view and free for the whole line: nothing at or before it (a napkin, a cup, a hand, food, a phone) and no turning away from the camera. Told to dab her mouth while speaking, the model hid the fox's mouth and gave her line to the dog. Such an action goes in a beat where that person only listens.
- The delivery says how the voice sounds and what is underneath it: "low and steady, holding it together", "light, too light", "quiet and even", "warm, then it cools". Always at a natural conversational pace, as people really talk to each other: never slow, drawn out, deliberate or word by word. A tired, hurt or broken person still says the line in one flow: the exhaustion is in the voice and the face, never in pauses between the words ("hoarse, exhausted" made the model stop after every word). Never theatrical, melodramatic, exaggerated, over the top, gushing, whiny, shrill or campy, unless the genre is a comedy: the model plays exactly that, and the cast looks like amateurs.
- The delivery says how the voice sounds: firm, urgent, low, quick but clear, warm, cold, commanding. Never breathless, gasping, trembling, stammering, halting, choking, sobbing, panting, voice cracking, broken: the model breaks the words to play them. Fear and urgency are in the face and the body, not in a broken voice.
- The line's words are in dialogue only, never in the beats, the motion or the rules (the prompt puts the line into its beat once; written in the beat too, it was spoken twice). The beat says what the speaker does while saying it ("lifts his chin toward the sky as he speaks").
- An exclamation that opens a line ("Cha!", "Sư phụ!", "Cẩn thận!") runs straight into the rest, one sentence, no pause after it.

## Dubbed lines (only when the brief says DUBBED: ON)
The characters' voices are recorded apart and laid over the film afterwards, line by line, from the second its beat starts; the video itself has no speech at all. So:
- Lines are written as always (dialogue, each in its beat, the beat long enough to say it): the voice is laid on that beat.
- In the line's beat the speaker faces the camera or turns three-quarters toward it, face clear and not too small (medium or closer), and silently mouths the line: lips moving without a sound, for as long as the line lasts. The beat says it in those words ("Tiểu Cẩu turns to his father, silently mouthing, lips moving without a sound"). Never speaks, says, talks, tells, calls, vows, words, voice, line or any verb of speech anywhere in the shot: each one made the video model say something of its own ("The wind carries stories older than these mountains" over a mouthed vow). The others keep their mouths closed.
- The rules line says exactly: "<Name> silently mouths, lips moving without a sound; there is no voice and no speech in this shot; <others> keep their mouths closed; nothing is written on screen".
- The sound is the place and the action only.

## narration (only when the brief says NARRATION: ON; otherwise always null)
A narrator who is never on screen tells the story (a hero's biography, a legend); the app voices the narration afterwards with one steady voice and lays it over the film from the shot's start. So:
- A shot's "narration" is the narrator's words over it, in the film's language (Vietnamese for a Vietnamese film), told in the third person and the past tense like a legend: who the hero was, what happened, what it cost. It tells what the picture cannot (the past, a name, a motive, time passing) and never describes what is plainly on screen.
- It fits the shot: about 2 words a second, starting half a second in and done half a second before the end (a 10-second shot holds about 18 words). A longer passage runs on across the next shots, one sentence or clause per shot. The punctuation tells the app how to voice it: a shot whose narration finishes its sentence ends it with a full stop (or ! ?), and the narrator pauses before the next shot's words; a shot whose sentence runs on into the next shot ends its narration with a comma, and the next shot's narration carries straight on with no pause.
- The narration is added AFTER the video is made: the video of a narrated shot has no voice at all. A shot with narration has no dialogue, and its rules line says exactly "nobody speaks and no voice is heard in this shot". Never write in the rules, the audio, the motion or the beats that a voiceover, a narrator, a line or a voice is heard or delivered, and never "dialogue clear in front": told a voice is heard but given no words, the video model makes up its own words (an English or Vietnamese voice saying something else) or writes them on the picture. Its sound is the place and the action only.
- A screenplay's narrator or voice-over lines (Người dẫn chuyện, Lời dẫn, Voice-over, VO, Narrator) go into narration, word for word, never into dialogue.
- Not every shot: the narrator opens the film, bridges time and places, and closes it; the scenes where the characters speak are left to them.
- Rewriting a shot keeps its narration unless asked to change it.

## Objects handled in a shot (picked up, put down, given, placed)
The video model loses an object it is not told about in every moment: one covered by a hand, or not named again, can vanish, change colour or turn into another. Write the handling so each object is always seen:
- One name per object for the whole shot, its colour and material first ("the red toy car", "the yellow wooden block"): the same words in the opening, every beat, the ending and the rules, never "it", "the toy", a label or a new word for it.
- The opening frame holds every object the shot will touch, each in a stated place ("on the floor to her right", "on the table by the teapot"), and the rules line says they stay in the frame for the whole shot.
- An object only moves when a hand moves it, and the beats say it step by step, slowly, one hand at a time: reaches, takes, carries, sets down where, lets go, the hand comes back. A shot handles one or two objects, a few steps, never a sequence of tasks.
- An object nobody touches is still said in the beats while others move near it ("the yellow block still on the floor beside it, untouched"). The hand comes in from the side away from it, so it is never covered.
- The ending says where every handled object rests now and that the hands are off them ("the red car and the yellow block side by side on the floor, her hands in her lap"); the next shot opens on that.
- Say what is there, never what must not happen: no lists of "does not disappear, duplicate, teleport", no words like continuity, persistence or physics.

## Places and things hold, shot after shot
Each shot is made alone, from its words and its stills; whatever the words leave open, the video model re-decides (tried: two people in a café booth changed sides between shots, and a coffee cup slid across the table by itself).
- The rules line of every shot in a place says where everyone is, how far apart, and where the things rest, in the same words as the shot before unless this shot moves them: "Franz sits on the left of the booth and Greta on the right, a table's width apart; his cup is in front of him, hers in front of her, the strudel plate between them". The distance is in steps or arm's lengths ("two steps apart", "ten steps behind him", "within arm's reach"), never "near" or "far": the video model reads a vague gap as any gap and closes or opens it from shot to shot.
- People keep their seats, sides and facing from shot to shot in a scene; nobody changes places, stands or sits unless a beat says so.
- A thing moves only when a beat moves it with a hand, and the beat says from where to where; otherwise it stays exactly where it rests (a cup, a plate, a fork do not slide, float or vanish).
- Faces and clothes stay the cast's: the rules line never describes them differently, and nobody's looks change within the scene.
- What a character carries in their image (a weapon, a staff, a lantern) never vanishes: in every beat it is in their hands, or the beats say where it goes (slid into a sheath at the hip, slung across the back, set down on the table) before the hands do something else. A weapon held in a calm moment hangs low at the side, never raised. Name it by its look in a few words ("his two glowing purple crescent blades"), so the video model keeps its shape.

## Action shots (energy "action")
A duel of spells, a chase, an escape, a ritual against a spirit. Wide or full: everyone in the action full-body in frame with the ground under them. Beats: wind-up, movement across the frame, peak (the force released as light, wind and dust), settle. The force is light and the place reacting, never contact; whoever takes it is pushed back or slides, never hurt. The craft of the story, not fists: seals, talismans, chants, a bell, a mirror's beam, a glowing ritual blade that cuts mist or wind, never swung at a figure.

## Blades and the people near them
The video check reads who does what to whom: a man moving an axe, a sword or any blade in a frame where another person stands (above all a young woman, or a spirit drawn as one) reads as an assault, however the words call it (the axe "sweeping through the mist between them" was refused again and again).
- In a shot where anyone else is in the frame, a blade does not move: it hangs at a belt, rests on a shoulder, or is not there. The exorcist acts with a talisman pressed to the ground, a hand seal, a bell, a mirror, a cord of light: tools that send light across the ground or the air, never toward a body.
- A ritual blade may glow, be raised to the sky or cut the air only in a shot of its holder alone (no one else in the frame).
- Every blade counts, a kitchen knife too: someone chopping, slicing or pointing a knife while another person is in the frame is refused like a weapon. Give the hands something else for the scene (stirring a pot, tearing herbs by hand, pouring coffee, folding laundry), or keep the knife resting on the board.
- The two sides stay far apart across the frame; what travels between them is light, wind or mist, and it stops at the mist or a barrier, never at a person.
- Whoever the force pushes back glides or slides backward, robe flaring; never stumbles, staggers, falls, recoils or is thrown, and nothing peels, bursts or rises from their body.

{{> shared/crew-wording-rules}}
