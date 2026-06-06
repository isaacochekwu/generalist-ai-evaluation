# Instruction-Following Assessment Guide

A dedicated guide for evaluating whether an AI model has accurately and completely followed the instructions in a given prompt. Instruction adherence is one of the most critical quality signals in LLM evaluation.

---

## Why Instruction-Following Matters

A model can produce a beautifully written, factually accurate output and still fail completely if it didn't do what was asked. Instruction-following assessment is not about quality — it's about compliance. An evaluator's job is to check both independently.

---

## Taxonomy of Instruction-Following Failures

### Type 1: Complete Miss
The model does not attempt the task at all, or substitutes an entirely different task.

**Example prompt:** "Write a formal complaint letter about a delayed parcel."  
**Failure:** The model writes a casual email about tracking a package instead.

**Detection:** Read the prompt, then the first sentence of the output. Do they align in task type and register?

---

### Type 2: Partial Compliance
The model completes part of the instructions but ignores one or more requirements.

**Example prompt:** "Summarise this article in 3 bullet points, using simple language for a non-expert audience."  
**Failure:** The model writes 6 bullet points in technical language.

**Detection:** Create a checklist from the prompt — every explicit instruction is a checkbox. Tick each one in the output.

---

### Type 3: Format Non-Compliance
The model produces the right content but in the wrong format.

**Example prompt:** "List 5 advantages of remote work in a numbered list."  
**Failure:** The model writes 5 advantages in paragraph form.

**Detection:** Format requirements (list, table, paragraph, bullet, numbered, code block, etc.) should be the first thing you check.

---

### Type 4: Length Non-Compliance
The model ignores explicit length constraints.

**Example prompt:** "Write a one-paragraph summary."  
**Failure:** The model writes four paragraphs.

**Or:** "Write a detailed 500-word analysis."  
**Failure:** The model writes 80 words.

**Detection:** Word/paragraph count. If a constraint was given, measure it.

---

### Type 5: Tone/Register Non-Compliance
The model uses the wrong tone or level of formality.

**Example prompt:** "Explain quantum entanglement to a 10-year-old."  
**Failure:** The model uses graduate-level physics terminology.

**Detection:** Identify the target audience stated in the prompt. Read the output as if you are that audience. Would they understand it?

---

### Type 6: Constraint Violation
The model ignores specific constraints or exclusions.

**Example prompt:** "Write a product description without mentioning price or delivery times."  
**Failure:** The model mentions both price and delivery times.

**Detection:** List all "do not include" or "avoid" constraints from the prompt. Scan the output specifically for these.

---

### Type 7: Persona/Role Non-Compliance
The model fails to adopt a specified role or persona.

**Example prompt:** "Respond as a sceptical journalist questioning the claims in this press release."  
**Failure:** The model summarises the press release neutrally without any sceptical framing.

**Detection:** Identify any persona or role instruction. Does the output voice, tone, and stance reflect that role throughout?

---

## Instruction Parsing Method

For complex prompts, use this method before evaluating:

1. **Read the prompt once** — get the overall task
2. **Re-read and extract** every explicit instruction into a numbered list
3. **Score each instruction** as: ✅ Followed / ⚠️ Partially followed / ❌ Not followed
4. **Calculate compliance rate:** (✅ count) / (total instructions)
5. **Map to score:** 100% = 5, 80–99% = 4, 60–79% = 3, 40–59% = 2, <40% = 1

---

## Example Instruction Parse

**Prompt:** "Write a professional email to a client apologising for a project delay, explaining the cause was a supplier issue, keeping it under 150 words, and ending with a revised delivery date of next Friday."

| # | Instruction | Status |
|---|-------------|--------|
| 1 | Professional email format | ✅ |
| 2 | Apologise for delay | ✅ |
| 3 | Explain cause = supplier issue | ✅ |
| 4 | Under 150 words | ⚠️ (162 words) |
| 5 | End with revised delivery date = next Friday | ❌ (date not mentioned) |

**Compliance rate:** 3/5 explicit = 60% → Score: 3/5

---

## Implicit Instructions

Some instructions are implied rather than stated. Evaluators should flag — but not automatically penalise — implicit instruction violations. Document them in feedback notes.

**Examples of implicit instructions:**
- "Write an email" implies: use greeting and sign-off
- "Explain to a beginner" implies: define jargon before using it
- "Write a review" implies: include a clear recommendation

Implicit violations are feedback-worthy but should be weighted less heavily than explicit ones.

---

## Key Principle

> Instruction-following is binary at the instruction level — either a requirement was met or it wasn't. Quality is a separate judgment. A badly written output that follows all instructions scores higher on this dimension than a beautifully written output that ignores half of them.
