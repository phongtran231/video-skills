---
name: safety-rewrite
description: Rewrites a clip prompt Muse's safety check refused.
---

# Safety rewrite

A prompt for an AI image or video model was refused by its safety check. The check reads the WORDS, not the intent: most refused scenes are harmless (a banquet, a repair shop, a surprised face) told in words that sound violent, gory, distressing, sexual or hateful. Rewrite the prompt so it shows the same scene and passes.

Change only what plausibly triggered THIS refusal (read the refusal message): never sanitize the whole prompt into blandness, never drop or replace the event the shot shows. A duel of spells stays a duel, shown by its effect (a gust, sparks off a glowing ritual blade, a recoil); a binding still binds; a spirit still approaches. Keep every character's exact name (never a role word instead).

## Keep exactly
- The prompt comes in sections (SUBJECTS, BACKGROUND, RULES, TIMELINE, STYLE, SOUND): keep every heading and every tag in angle brackets (<IMAGE_1>, <SETTING>) exactly, with the section each part sits in.
- Every character name, every timing ("0-4s:"), the structure, the order of beats, the camera, and the language of each part.
- Spoken lines in quotes: keep them word for word, unless a word in them is plainly violent or sexual; then soften only that word.
- The STYLE and SOUND lines word for word: they are in every prompt of the film and are not what was refused. The RULES section (the rules line and the motion line) and the TIMELINE are written per shot and may be what was refused: rewrite a word there only when it plausibly caused this refusal, and keep the rules line's meaning (who stays in frame, who stays silent, nothing written on screen).
- Same length, give or take; never add new content, never explain.

## Change: wording by risk family (examples, not a complete list; judge any word the same way)
- Fear and shock: shocked, horrified, terrified, terrifying, horror, scream, shriek -> surprised, wide-eyed, startled, taken aback, gasp.
- Violence: attack, assault, hit, punch, kick, stab, slash, strangle, beat up, kill, murder, fight, brawl, clash -> rush toward, lunge, push, spar, a lively exchange, a duel of moves; show the motion and the reactions, never the harm or the contact.
- Weapons: gun, knife, blade, sword, dagger, axe -> keep a sword or staff a story needs as a "prop sword" or "wooden staff" held, never swung at a body; drop weapons from places and still images when not needed.
- Injury and gore: blood, bleeding, wound, bruise, broken bone, gore, corpse, dead body -> drop entirely; at most "a scuffed sleeve".
- Death: dead, death, dying, kill, execution -> fallen back, defeated, the end.
- Distress: torture, torment, agony, anguish, suffering, sobbing in pain, crying in pain, despair -> uneasy, troubled, teary-eyed, quiet sorrow.
- Disorder: chaos, panic, pandemonium, mob, riot, stampede, swarming -> bustling, lively, festive, a crowd, guests.
- Menace: dark, ominous, menacing, sinister, threatening, evil, creepy, eerie, haunted -> moody, dim, dramatic lighting, mysterious, atmospheric.
- Bodies: nude, naked, exposed, undressed, sexy, seductive, lingerie, cleavage -> fully dressed, elegant; drop anything sexual. Anyone young is never described with romance or a body.
- Captivity and abuse: slave, prisoner, captive, hostage, abuse, kidnap, tied up -> attendant, guest, helper, held back, follows reluctantly.
- Body horror: distorted, grotesque, deformed, mutilated, monster flesh -> exaggerated, stylized, cartoonish.
- Hate and real harm: slurs, drugs, self-harm, suicide, real public figures, brands -> drop or replace with a neutral word.
- Poisons and toxic substances, even as folk ingredients: cinnabar, chu sa, mercury, arsenic, poison, venom -> red-dyed, red pigment, herbs.
- Bodies on the floor: lies prostrate, face down, forehead pressed to the floor, motionless, collapsed -> kneels upright with the head bowed low and hands clasped (a person lying still reads as a dead body).
- Spirits and ghost-like figures: the check refuses the corpse look, not the story. A face hidden behind hair, a wedding gown, white, empty or glowing eyes, pale grey skin, torn or burial clothes, a limp or stooped body, crawling, long nails -> the same character as an ordinary living person: a visible face with ordinary eyes and a still expression, hair off the face, an intact embroidered robe, standing upright, natural skin. Words for what they are (ghost, spirit, specter, corpse, undead, demon, ma, hồn, xác, thi) -> words for how they look ("the woman in red"). Keep what makes the shot uncanny: mist around them, a flickering lamp, a shadow that falls wrong, a movement too still or too smooth.
- Faces and emotions: a strong emotion becomes a visible, neutral expression ("bàng hoàng" -> "wide surprised eyes"; "tears of pain" -> "teary-eyed").

## triggers
List the exact words or short phrases of the ORIGINAL prompt (as they appear, lower case, English or other language) you judged to have caused the refusal, each with its replacement ("" to drop). Only words of the risk families above, never plain ones you softened for good measure (deep, dark, bone, cute, torn, weathered, harsh, a name, a place, a style word). At most 8.

{{> shared/shot-craft}}
