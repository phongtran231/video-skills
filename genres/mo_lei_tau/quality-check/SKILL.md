---
name: mo_lei_tau-quality-check
description: The Mo lei tau nonsense comedy (Stephen Chow style) genre skill's quality-check module.
kind: fragment
---

# Module: Quality check

# 66. COMEDY QUALITY CONTROL

Before output, score each category from 0–2.

```text
EXPECTATION            0 / 1 / 2
INTERRUPTION           0 / 1 / 2
ESCALATION             0 / 1 / 2
REVERSAL               0 / 1 / 2
PAYOFF                 0 / 1 / 2
CHARACTER CONTRAST     0 / 1 / 2
REACTION               0 / 1 / 2
TIMING                 0 / 1 / 2
VISUAL COMEDY          0 / 1 / 2
DIALOGUE COMEDY        0 / 1 / 2
CAMERA COMEDY          0 / 1 / 2
SOUND COMEDY           0 / 1 / 2
CALLBACK               0 / 1 / 2
CAUSALITY              0 / 1 / 2
SURPRISE               0 / 1 / 2
```

Maximum:

```text
30
```

Interpretation:

```text
26–30 = Strong comedy sequence
21–25 = Good
16–20 = Needs refinement
<16   = Rewrite the comedic structure
```

---

# 67. VIDEO GENERATION QUALITY CONTROL

Check:

```text
Is the main subject unambiguous?

Is the primary action physically achievable?

Is the camera movement clear?

Is the shot too complicated?

Are there too many characters?

Are character identities stable?

Is the environment consistent?

Is dialogue short enough?

Is the action visually observable?

Does the camera actually capture the joke?

Is there a clear beginning and ending?

Could this shot realistically be generated?
```

If a shot contains too many actions:

> SPLIT THE SHOT.

---

# 71. MOST IMPORTANT RULE

The agent must think like a director, not a prompt writer.

A prompt writer describes:

> "A man falls down."

A director thinks:

> "Why does he fall? What does he believe is happening? What does the audience expect? How long should we hold before the fall? Should we show the fall or cut to the consequence? Who sees it? Who pretends not to see it? What reaction makes it funnier? What does the fall cause next?"

The goal is not:

```text
MORE ADJECTIVES
```

The goal is:

```text
BETTER COMEDIC CAUSALITY
+
BETTER TIMING
+
BETTER ACTING
+
BETTER CAMERA
+
BETTER EDITING
+
BETTER PAYOFF
```
