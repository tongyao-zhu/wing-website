---
title: "Minimal Code Editing with LLMs"

summary: Measuring and reducing unnecessary changes in LLM code repair while preserving correctness.
abstract: "Correct code repairs can still introduce unnecessary changes. We study over-editing using 400 BigCodeBench problems with controlled corruptions and known minimal repairs, measuring functional success, excess edit distance, and added cognitive complexity. Preservation prompts reduce unnecessary changes, while reinforcement learning offers the strongest tested trade-off between edit fidelity, generalization to unseen corruption patterns, and retention of broader coding ability."

tags: ["Code Repair", "LLMs", "Reinforcement Learning"]
year: 2026
date: '2026-09-03'
all_day: true
featured: true
image:
  caption: 'A one-line bug and its minimal repair compared with larger model-generated patches. Every patch shown passes the tests, but edit fidelity varies widely.'
  focal_point: Center
url_pdf: 'https://arxiv.org/pdf/2609.04061'
url_code: 'https://github.com/nreHieW/over-editing'
authors: ["tongyao", "weihern", "min"]

---
A code repair can pass every test while changing far more than the bug requires. In this project, we study over-editing: unnecessary rewrites that increase review effort and disturb an existing implementation. Our EMNLP 2026 paper, [When Models Edit Too Much: On the Fidelity of Minimal Code Edits](https://arxiv.org/abs/2609.04061), introduces a controlled evaluation framework built from 400 BigCodeBench problems. Injected local corruptions provide known minimal repairs, allowing us to measure correctness alongside excess edit distance and added cognitive complexity. Asking models to preserve the original code reduces average excess edit distance from 0.195 to 0.131, lowers added complexity by 26.6%, and improves Pass@1 by 2.3 percentage points.

The project brings together Tongyao Zhu, Wei Hern Lim, and Prof. Min-Yen Kan, building on Wei Hern's final-year project at WING. Beyond prompting, we investigate whether models can learn to make minimal repairs. Supervised fine-tuning overfits to familiar corruption patterns, while reinforcement learning offers the strongest tested balance between correctness, edit fidelity on unseen corruption patterns, and retention of broader coding ability. These results establish edit fidelity as a measurable and learnable dimension of code-repair quality, helping models preserve the implementation around a local bug.
