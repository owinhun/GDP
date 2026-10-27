# Grounded Distractor Protocol (GDP): Diagnosing Model-Dependent Intervention Effects under Hard Distractors in MCQ-Based Vision-Language Model Evaluation

> [!IMPORTANT]
> 🎉 **Accepted at CIKM 2026**

[arXiv]()
[Project Page]()
[Paper PDF](https://github.com/owinhun/GDP/blob/main/csp3510_Grounded_Distractor_Probing_A_Diagnostic_Protocol_for_Hard_Distractor_Sensitivity_in_VLM_Multiple_Choice_Evaluation.pdf)

by Seunghun Oh, Ganghyeon Jeong, Unsang Park

This is the official implementation of **Grounded Distractor Protocol (GDP)**, a *matched three-condition diagnostic protocol* that evaluates how vision-language models respond to **same-type, visually plausible hard distractors** under controlled prompting interventions.

---

### Overview

Multiple-choice evaluation for vision-language models (VLMs) increasingly relies on stronger distractors, but a single accuracy score cannot distinguish whether models truly use **fine-grained visual evidence** or rely on coarse cues.

**GDP** instantiates a matched (original, permutation-control, hard-distractor) protocol over a manually reviewed **98-item diagnostic slice (GDP-Slice)** and probes evidence-first prompting as a **controlled diagnostic intervention**—not a new prompting method.

We find that the same evidence-first intervention is **not universally beneficial**: LLaVA-style models improve, while Qwen2.5-VL and InternVL2.5 show **opposite, negative effects**. Answer-first controls further suggest that these model-dependent effects reflect **different intervention mechanisms**, rather than a uniform prompting benefit.

---

### News

- **August 2026** — Our paper was accepted at the **35th ACM International Conference on Information and Knowledge Management (CIKM 2026)**. 🎉

---

### Release Status

🚧 **This repository is being prepared for public release.**

The code, GDP-Slice dataset, and prompt templates will be released soon.

Planned contents:

- [ ] GDP-Slice: 98-item diagnostic slice with hard distractors
- [ ] Prompt templates: direct, evidence-first, and answer-first
- [ ] Inference scripts for four evaluated VLMs
- [ ] Metric computation: HSIG, ΔHDsel, McNemar tests, and bootstrap confidence intervals
- [ ] Reproduction scripts

---

### Installation

Installation instructions will be added with the code release.

---

### Method

A detailed description of the GDP construction and evaluation pipeline will be added with the public release.

---

### Acknowledgements

Acknowledgements will be added in the camera-ready release.

---

### Questions

For questions about the paper or repository, please contact Seunghun Oh at [gnsgus190@sogang.ac.kr](mailto:gnsgus190@sogang.ac.kr).

---

### Citation

Please use the following provisional citation. The official ACM BibTeX entry will be added once the proceedings become available.

```bibtex
@inproceedings{oh2026gdp,
  title     = {Grounded Distractor Protocol ({GDP}): Diagnosing Model-Dependent Intervention Effects under Hard Distractors in {MCQ}-Based Vision-Language Model Evaluation},
  author    = {Oh Seunghun and Ganghyeon Jeong and Park Unsang},
  booktitle = {Proceedings of the 35th ACM International Conference on Information and Knowledge Management},
  year      = {2026},
  note      = {Accepted at CIKM 2026}
}
