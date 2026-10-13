# Design decisions

Short records of the choices that shaped the tool, and why.

## 1. Search for disconfirming evidence separately

**Problem.** With one search, results skewed toward studies that agreed with the claim, and scores were overconfident.

**Decision.** Run a second, independent search for null and contradicting findings, and feed both result sets into the same study-card and reasoning steps.

**Effect.** Verdicts became noticeably more balanced. This was the single most important change in the project.

## 2. Structured study cards before reasoning

**Decision.** Extract a structured card per source (design, main finding) before any causal reasoning happens.

**Why.** Reasoning over consistent, compact cards is more reliable than reasoning over raw web text, and it makes the "design ceiling" check possible.

**Lesson.** Extraction failed less often when the output schema was loose (fields as strings) and defined from a JSON example rather than a strict JSON Schema.

## 3. Checklist-driven reasoning

**Decision.** Ask the model to work through five named causal checks rather than give an open-ended judgement.

**Why.** It mirrors how an epidemiologist would actually appraise a causal claim, and it makes the verdict explainable and easier to debug.

## 4. Self-hosted instead of a managed platform

**Decision.** Run n8n on a VPS with Docker Compose and Caddy rather than n8n Cloud.

**Why.** It allows a custom domain, keeps the editor private, keeps costs predictable, and makes the planned local-inference setup possible.

## 5. Private editor, public front end

**Decision.** Only the static page and the webhook path are public. The n8n editor is bound to localhost and reached by SSH tunnel.

**Why.** Smallest possible public surface.

## 6. Hard limits on a free demo

**Decision.** A per-visitor cap, a global daily cap, an input length limit, a result cache, and a hard monthly spend limit with auto-reload off.

**Why.** A public LLM demo with no limits is an open tab on your API bill.

<!-- TODO (optional): add why GPT-5-mini was chosen -->
