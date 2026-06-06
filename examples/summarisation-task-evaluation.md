# Example: Summarisation Task Evaluation

**Task Type:** Article Summarisation  
**Evaluator:** Isaac Ochekwu, MBBS  
**Preference:** A > B

---

## Prompt Given to AI

> Summarise the following article in 3–5 sentences for a general audience. Focus on the main finding, its significance, and any limitations mentioned. Do not include information not present in the article.

*(Article excerpt — fictional for annotation purposes)*

> A new study by researchers at the University of Edinburgh examined screen time habits in 1,200 adolescents aged 13–17 over a two-year period. The study found that adolescents who used social media for more than 3 hours per day showed a 23% higher incidence of self-reported anxiety symptoms compared to those who used it for less than 1 hour per day. However, the researchers cautioned that the study was observational and could not establish causation — adolescents with existing anxiety may be more drawn to social media use. The study also did not control for other variables such as sleep quality, academic pressure, or family environment. The findings were published in the journal Adolescent Mental Health.

---

## Output A

> A two-year study of 1,200 teenagers found that those spending more than 3 hours daily on social media were 23% more likely to report anxiety symptoms than those who used it for less than an hour. The researchers were careful to note that this is an association, not proof of causation — teenagers already experiencing anxiety may simply be more drawn to social media. The study also did not account for other potential factors like sleep or academic stress. The findings appeared in the journal Adolescent Mental Health.

Word count: 82 words ✅ (within 3–5 sentence range)

---

## Output B

> Social media use is a growing mental health crisis among teenagers, with new research confirming that heavy users face dramatically higher anxiety rates. The University of Edinburgh study, which tracked over a thousand adolescents, found a significant 23% gap in anxiety between high and low social media users. This is an urgent finding that parents, schools, and policymakers need to take seriously. More research is needed to understand the full impact of social media on young people's wellbeing.

Word count: 78 words ✅

---

## Instruction Compliance Checklist

| Instruction | Output A | Output B |
|-------------|---------|---------|
| 3–5 sentences | ✅ (4 sentences) | ✅ (4 sentences) |
| For general audience | ✅ | ✅ |
| Includes main finding | ✅ (23% higher anxiety) | ✅ (23% gap mentioned) |
| Includes significance | ⚠️ (implicit — journal named) | ⚠️ (stated broadly) |
| Includes limitations mentioned | ✅ (causation caveat + confounders) | ❌ (no limitations mentioned) |
| No information not in article | ✅ | ❌ (see below) |

**Output A compliance: 5/6 → Score: 5/5**  
**Output B compliance: 3/6 → Score: 2/5**

---

## Scoring

| Dimension | Output A | Output B |
|-----------|---------|---------|
| Instruction Adherence | 5/5 | 2/5 |
| Factual Accuracy | 5/5 | 3/5 |
| Reasoning & Coherence | 5/5 | 3/5 |
| Quality & Helpfulness | 4/5 | 3/5 |
| Safety & Appropriateness | 5/5 | 4/5 |
| **Total** | **24/25** | **15/25** |

---

## Preference: A > B

**What Output A did well:**  
Output A is a near-perfect summarisation. It captures the main finding accurately (23%, 3 hours vs. 1 hour threshold), includes both limitations mentioned in the article (observational design = no causation; uncontrolled confounders), and stays strictly within the information provided. The language is accessible for a general audience without being condescending.

**What Output A could improve:**  
It could more explicitly signal the significance of the finding beyond just naming the journal. A sentence noting this adds to a growing body of research on adolescent mental health would contextualise the finding — though this would border on adding information not in the article, so the omission is defensible.

**What Output B did poorly:**  
Output B contains several problems that make it unsuitable as an accurate summarisation:

1. **Added information not in the article:** "This is an urgent finding that parents, schools, and policymakers need to take seriously" — the article makes no such claim. This is the evaluator's (or model's) opinion inserted into a factual summary.

2. **Omitted the key limitations:** The most important caveat in the article — that causation cannot be established, and that anxious teens may seek social media rather than social media causing anxiety — is completely absent. A summary of a research study that omits the limitations is misleading.

3. **Editorialising framing:** "Social media use is a growing mental health crisis" is a loaded framing not supported by the article, which specifically cautions against causal interpretation.

**Decisive factor:**  
Output B fails the "do not include information not present in the article" instruction and omits the study's central caveat. It presents an observational association as a confirmed crisis, which is the exact misrepresentation the researchers' own caution was designed to prevent. Output A is accurate, appropriately hedged, and instruction-compliant.
