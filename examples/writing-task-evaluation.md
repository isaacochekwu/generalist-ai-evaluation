# Example: Writing Task Evaluation

**Task Type:** Persuasive Email Writing  
**Evaluator:** Isaac Ochekwu, MBBS  
**Preference:** B > A

---

## Prompt Given to AI

> Write a professional email from a project manager to a client, explaining that the project deadline has been pushed back by two weeks due to unexpected technical issues. The tone should be apologetic but confident. Keep it under 200 words. End with a clear revised deadline and a next steps statement.

---

## Output A

> Subject: Project Update
>
> Hi [Client],
>
> I hope you're doing well. I'm writing to let you know that unfortunately we've run into some technical difficulties that have impacted our timeline. We're working hard to resolve these issues as quickly as possible.
>
> We're going to need a bit more time to complete the project to the standard you expect from us. We appreciate your understanding and patience during this time.
>
> Please don't hesitate to reach out if you have any questions.
>
> Best regards,
> [Project Manager]

---

## Output B

> Subject: Project Timeline Update — Revised Delivery Date
>
> Dear [Client Name],
>
> I want to be upfront with you: we have encountered unexpected technical issues during the integration phase that have impacted our original schedule. I sincerely apologise for the disruption this causes to your planning.
>
> We have resolved the root cause and our team is back on track. The revised delivery date is **[date — two weeks from original deadline]**.
>
> As a next step, I will send you a progress update every three days until delivery to keep you fully informed.
>
> Thank you for your continued trust in our team.
>
> Best regards,
> [Project Manager]

Word count: 104 words ✅

---

## Instruction Compliance Checklist

| Instruction | Output A | Output B |
|-------------|---------|---------|
| Professional email format | ✅ | ✅ |
| Explains deadline pushed back 2 weeks | ❌ (vague — "a bit more time") | ✅ |
| Explains cause = technical issues | ⚠️ (mentioned but vague) | ✅ (integration phase specified) |
| Apologetic tone | ⚠️ (implied but weak) | ✅ (explicit apology) |
| Confident tone | ❌ (uncertain and hedging throughout) | ✅ (resolved, back on track) |
| Under 200 words | ✅ | ✅ |
| Clear revised deadline stated | ❌ (not stated) | ✅ |
| Next steps statement | ❌ (not included) | ✅ |

**Output A compliance: 3/8 (38%) → Score: 2/5**  
**Output B compliance: 8/8 (100%) → Score: 5/5**

---

## Scoring

| Dimension | Output A | Output B |
|-----------|---------|---------|
| Instruction Adherence | 2/5 | 5/5 |
| Factual Accuracy | 4/5 | 4/5 |
| Reasoning & Coherence | 3/5 | 5/5 |
| Quality & Helpfulness | 2/5 | 5/5 |
| Safety & Appropriateness | 5/5 | 5/5 |
| **Total** | **16/25** | **24/25** |

---

## Preference: B > A

**What Output A did well:**  
It uses a professional email format and avoids any safety or tone issues. It is polite and inoffensive.

**What Output A did poorly:**  
Output A fails on almost every specific instruction. It never states the two-week delay explicitly — "a bit more time" is not actionable for a client who needs to adjust their plans. It does not include a revised deadline, no next steps, and the tone is apologetic without being confident, which was specifically requested. The subject line "Project Update" gives the client no useful information before opening the email.

**What Output B did well:**  
Output B executes every instruction precisely. The subject line signals urgency and content immediately. The apology is explicit and sincere. The confidence comes through in "we have resolved the root cause." The revised deadline is clearly stated (even if placeholder). The next steps commitment (progress updates every three days) is specific and reassuring. It stays well under 200 words while being substantive.

**What Output B could improve:**  
The revised deadline uses a placeholder rather than a calculated date — in a real task with a specified original deadline, this would need to be filled in. Minor note; not a quality failure in a template context.

**Decisive factor:**  
Output A is a generic apologetic email that ignores half the instructions. Output B is a professional, complete, client-ready communication that satisfies every requirement. The difference is not tone — it's execution.
