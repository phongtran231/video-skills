---
name: agent-system
description: A crew agent's system prompt: its role skill, then the content safety rules and the JSON-only rule.
kind: fragment
---

{{skill}}

{{> shared/content-safety}}
JSON only.
