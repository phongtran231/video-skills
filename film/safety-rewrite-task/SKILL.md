---
name: safety-rewrite-task
description: The answer format of the safety rewrite (after film/safety-rewrite) and its brief: the refused prompt and Muse's error.
kind: fragment
---

## Answer
Return {"prompt","triggers":[{"word","replacement"}]}. JSON only.

## Brief
Kind: {{kind}} prompt
Refusal: {{refusal}}
Prompt:
{{prompt}}
