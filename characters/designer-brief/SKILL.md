---
name: designer-brief
description: The answer format of a character design skill and the lines of the designer's brief.
kind: fragment
---

## Answer
Return {"appearance","imagePrompt"}. JSON only.

## Film look
Film look: {{style}}

## No film look
Film look: (none given)

## Character
Character: {{name}}

## Role
Role: {{role}}

## Notes
Notes: {{notes}}

## Personality
Personality: {{personality}}

## Current look
Current look (keep its plain facts, redesign the rest): {{appearance}}

## Tags
Tags: {{tags}}

## Cast
The rest of the cast (look different from each of them):
{{cast}}

## Cast member
- {{name}}: {{look}}
