---
name: mo_lei_tau-video-prompt
description: The Mo lei tau nonsense comedy (Stephen Chow style) genre skill's video-prompt module.
kind: fragment
---

# Module: Video prompt

# 36. VIDEO PROMPT STRUCTURE

Every generated video prompt should preferably follow:

```text
[SHOT TYPE]

[SUBJECT + APPEARANCE]

[EXACT ACTION]

[ACTING + FACIAL EXPRESSION]

[CAMERA]

[CAMERA MOVEMENT]

[ENVIRONMENT]

[LIGHTING]

[VISUAL STYLE]

[TIMING]

[DIALOGUE]

[SOUND]

[COMEDIC INTENTION]
```

---

# 37. DO NOT OVERWRITE THE PROMPT

Do not fill prompts with meaningless adjectives.

BAD:

```text
Ultra cinematic beautiful amazing incredible masterpiece
high quality stunning professional epic gorgeous...
```

Prefer concrete instructions:

```text
Medium-wide shot.

The exhausted shopkeeper stands behind the counter,
trying to appear completely serious.

He slowly raises one eyebrow.

Camera performs a very subtle push-in.

The customer continues talking without noticing.

Hold for one second after the customer finishes.

The shopkeeper quietly says:
"...What?"

Deadpan delivery.

No exaggerated facial animation.

Natural room tone.

Sudden silence immediately after the line.
```

---

# 68. FINAL PROMPT QUALITY RULE

Prefer:

```text
SPECIFIC
VISUAL
PHYSICAL
TEMPORAL
ACTING-ORIENTED
CAMERA-AWARE
CAUSE-AND-EFFECT
```

Avoid:

```text
VAGUE
ABSTRACT
ADJECTIVE-HEAVY
PLOT-SUMMARY-ONLY
"MAKE IT FUNNY"
"MAKE IT CINEMATIC"
```

Never rely on:

> "Make this funny."

Instead describe exactly **why the moment is funny**.

---

# 69. FINAL PROMPT EXAMPLE

Input:

```text
A poor guy tries to impress a girl at a restaurant.
```

Do NOT output a generic prompt.

Build the comedy first.

### Comedy structure

```text
Goal:
He wants to appear wealthy and sophisticated.

Expectation:
Elegant romantic dinner.

Contradiction:
He clearly cannot afford the restaurant.

Interruption:
The waiter brings an absurdly expensive dish.

Escalation:
He pretends he ordered it.

Escalation:
The waiter asks him to confirm the wine.

Escalation:
He confidently chooses the most expensive wine.

False resolution:
The girl appears impressed.

Reversal:
She reveals she owns the restaurant.

Final payoff:
She quietly tells the waiter:
"Put everything on his bill."

He freezes.

The waiter smiles.

```

### Shot structure

```text
SHOT 01
Elegant restaurant.
Hero sits upright, pretending to be wealthy.
Subtle push-in.

SHOT 02
Waiter places an enormous luxury dish on the table.
Hero's eyes widen.
He immediately hides his reaction.

SHOT 03
Hero confidently gestures toward the dish.
"Exactly what I ordered."

SHOT 04
Close-up of the bill.
His smile slowly disappears.

SHOT 05
He tries to hide the bill under his plate.

SHOT 06
The girl calmly picks it up.

SHOT 07
She looks at him.
Pause.

"I own this restaurant."

SHOT 08
Extreme close-up.
Hero freezes.

SHOT 09
She smiles politely.
"Enjoy your dinner."

SHOT 10
Cut to waiter placing an even larger bill on the table.

Hero slowly looks at camera.

CUT.
```

The humor comes from:

```text
status
+
pretending
+
escalation
+
misunderstanding
+
reaction
+
reversal
+
final visual payoff
```
