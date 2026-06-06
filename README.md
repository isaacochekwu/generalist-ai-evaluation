# Generalist AI Evaluation Framework

**Author:** Isaac Ochekwu, MBBS | AI Evaluation Specialist  
**Focus:** LLM Output Quality • Instruction-Following Assessment • AI Safety & Content Review • RLHF Preference Ranking

---

## Overview

This repository documents my framework for evaluating general-purpose AI outputs — including writing, reasoning, summarisation, question-answering, and instruction-following tasks — across diverse domains.

While I specialise in medical AI evaluation (see [`medical-ai-evaluation-guidelines`](https://github.com/isaacochekwu/medical-ai-evaluation-guidelines)), I also work as a generalist AI evaluator, reviewing LLM outputs for quality, factual accuracy, safety, and alignment with user intent across non-medical domains.

This framework is domain-agnostic and applies to any LLM output type. It is the foundation I use before applying domain-specific overlays (such as clinical safety criteria for healthcare AI).

---

## Repository Structure

```
generalist-ai-evaluation/
├── README.md                                      ← You are here
├── evaluation-framework.md                        ← Core quality dimensions for any AI output
├── instruction-following-guide.md                 ← How to assess whether AI followed instructions
├── ai-safety-content-policy-review.md             ← Safety & policy compliance evaluation
├── hallucination-detection-general.md             ← Hallucination types across non-medical domains
├── examples/
│   ├── writing-task-evaluation.md                 ← Annotated writing task comparison
│   ├── reasoning-task-evaluation.md               ← Annotated reasoning/logic task evaluation
│   └── summarisation-task-evaluation.md           ← Annotated summarisation quality review
└── templates/
    └── general-evaluation-scorecard.md            ← Reusable scorecard for any evaluation task
```

---

## Who This Is For

- AI/ML teams building or fine-tuning general-purpose LLMs who need structured human evaluation criteria
- Hiring teams at Turing, Mercor, Micro1, Scale AI, or Surge AI reviewing my evaluator profile
- Fellow AI evaluators looking for a reusable quality framework

---

## My Evaluation Background

I evaluate AI outputs across two tracks:

**Generalist Track**
- Writing quality, coherence, tone, and instruction compliance
- Factual accuracy across non-medical domains
- Reasoning and logical consistency
- AI safety and content policy compliance
- RLHF preference ranking for general LLM outputs

**Medical Specialist Track**
- Clinical accuracy and hallucination detection in healthcare AI
- RLHF preference ranking for medical AI systems
- NER annotation for healthcare NLP pipelines
- See: [`medical-ai-evaluation-guidelines`](https://github.com/isaacochekwu/medical-ai-evaluation-guidelines)

---

## Contact

- **Email:** ochekwuisaac333@gmail.com
- **LinkedIn:** [linkedin.com/in/isaac-ochekwu](https://linkedin.com/in/isaac-ochekwu)
- **GitHub:** [github.com/isaacochekwu](https://github.com/isaacochekwu)
