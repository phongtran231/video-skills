---
name: script-repair
description: The repair round of the one-call script writer: the problems found in its draft (or the schema errors), then what to return.
kind: fragment
---

## Problems
That script has these problems:
{{problems}}
Return the complete corrected JSON only, with exactly the required keys and no others. Keep the same story, cast and scenes except where a fix requires a change. Write style, appearance, imagePrompt, camera, action, delivery and audio in English.

## Schema
That JSON does not match the required schema:
{{issues}}
Return the complete corrected JSON only, with exactly the required keys and no others. Keep the same story, cast and scenes except where a fix requires a change. Write style, appearance, imagePrompt, camera, action, delivery and audio in English.
