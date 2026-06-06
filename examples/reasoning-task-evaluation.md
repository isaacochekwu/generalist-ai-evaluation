# Example: Reasoning Task Evaluation

**Task Type:** Logical Reasoning / Problem Analysis  
**Evaluator:** Isaac Ochekwu, MBBS  
**Preference:** B >> A

---

## Prompt Given to AI

> A company has 3 candidates for a promotion: Alice, Bob, and Carol. Alice has more experience than Bob. Carol has more experience than Alice. Bob has been with the company longer than Carol. The promotion criteria states: experience is weighted at 70%, tenure at 30%. Who should get the promotion, and why? Show your working.

---

## Output A

> Based on the information provided, Carol should get the promotion. She has the most experience, which is an important factor for any promotion decision. Alice comes second, and Bob has the least experience. Experience matters a lot in the workplace, so Carol is the best choice.

---

## Output B

> **Step 1: Establish the rankings**
>
> From the prompt:
> - Experience ranking: Carol > Alice > Bob
> - Tenure ranking: Bob > Carol > Alice
>
> **Step 2: Assign scores using the weighting**
>
> For a 3-person ranking, I'll assign points: 1st = 3 pts, 2nd = 2 pts, 3rd = 1 pt.
>
> | Candidate | Experience (×0.7) | Tenure (×0.3) | Weighted Total |
> |-----------|------------------|--------------|----------------|
> | Alice | 2 × 0.7 = 1.40 | 1 × 0.3 = 0.30 | **1.70** |
> | Bob | 1 × 0.7 = 0.70 | 3 × 0.3 = 0.90 | **1.60** |
> | Carol | 3 × 0.7 = 2.10 | 2 × 0.3 = 0.60 | **2.70** |
>
> **Step 3: Conclusion**
>
> Carol scores highest at 2.70, followed by Alice at 1.70, and Bob at 1.60.
>
> **Carol should receive the promotion.** Her dominant experience advantage (weighted at 70%) outweighs Bob's tenure advantage. Even though Bob has been with the company longest, tenure counts for only 30% of the decision — insufficient to overcome his last-place experience ranking.

---

## Instruction Compliance Checklist

| Instruction | Output A | Output B |
|-------------|---------|---------|
| Identify who should get the promotion | ✅ (Carol) | ✅ (Carol) |
| Explain why | ⚠️ (generic — "experience matters") | ✅ (explicit weighted reasoning) |
| Show working | ❌ (no working shown) | ✅ (step-by-step with table) |
| Apply 70/30 weighting | ❌ (not applied) | ✅ (explicitly calculated) |
| Address all three candidates | ❌ (Bob barely mentioned) | ✅ (all three scored) |

**Output A compliance: 2/5 (40%) → Score: 2/5**  
**Output B compliance: 5/5 (100%) → Score: 5/5**

---

## Scoring

| Dimension | Output A | Output B |
|-----------|---------|---------|
| Instruction Adherence | 2/5 | 5/5 |
| Factual Accuracy | 4/5 | 5/5 |
| Reasoning & Coherence | 2/5 | 5/5 |
| Quality & Helpfulness | 1/5 | 5/5 |
| Safety & Appropriateness | 5/5 | 5/5 |
| **Total** | **14/25** | **25/25** |

---

## Preference: B >> A

**What Output A did well:**  
It reaches the correct conclusion (Carol) and identifies experience as the relevant factor. It is safe and appropriate.

**What Output A did poorly:**  
Output A does not show any working — the most explicit instruction in the prompt. It does not apply the 70/30 weighting at all, meaning the answer is correct by coincidence rather than method. It barely mentions Bob and ignores Alice's relative position. The reasoning provided ("experience matters a lot") is a generic assertion, not an analysis. If the tenure weighting had been higher and Bob were the correct answer, Output A would have gotten it wrong — because it isn't actually reasoning, it's concluding.

**What Output B did well:**  
Output B treats this as the structured reasoning problem it is. It explicitly establishes rankings for each criterion before scoring, applies the weighting quantitatively, and presents the results in a table that makes the comparison transparent. The conclusion follows demonstrably from the working — a reader can check every step. It also explains *why* Carol wins despite Bob's tenure advantage, which is the most instructive part of the reasoning.

**Decisive factor:**  
Output A guesses correctly. Output B reasons correctly. For an RLHF training signal, Output B is vastly more valuable — it teaches the model to show structured, weighted reasoning rather than jumping to conclusions. Output A reaching the right answer for the wrong reasons is actually a training risk: it could reinforce shortcut reasoning patterns.
