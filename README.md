# Grounded Distractor Probing: A Diagnostic Protocol for Hard-Distractor Sensitivity in VLM Multiple-Choice Evaluation

> [!IMPORTANT]
> 🎉 **Accepted at CIKM 2026**

**[Project Page](https://owinhun.github.io/GDP/)** · **[Paper PDF](./csp3510_Grounded_Distractor_Probing_A_Diagnostic_Protocol_for_Hard_Distractor_Sensitivity_in_VLM_Multiple_Choice_Evaluation.pdf)**

**Seunghun Oh · Ganghyeon Jeong · Unsang Park**  
Computer Vision and Image Processing (CVIP) Lab, Sogang University

This is the official project repository for **Grounded Distractor Probing (GDP)**, a diagnostic protocol for analyzing how vision–language models (VLMs) respond to **same-type, visually plausible near-miss distractors** in multiple-choice visual question answering. GDP is an **evaluation protocol**, not a new VLM or a universally effective prompting method.

## Overview

Standard multiple-choice accuracy can hide whether a VLM selects the correct answer using fine-grained visual evidence or easier cues from answer options. GDP keeps the image, question, and reference answer fixed while comparing three matched conditions:

| Condition | What changes? | What it helps diagnose |
| --- | --- | --- |
| **Original** | The original answer options are retained. | Baseline response to the original item. |
| **Permutation control** | The option order changes, without changing option meanings. | Sensitivity to option position or formatting. |
| **Hard distractor** | An incorrect option is replaced by a same-type, visually plausible near miss. | Sensitivity to fine-grained visual evidence. |

The manually reviewed **GDP-Slice** contains **98 diagnostic items** selected from the VMCBench development data, covering tasks related to **TextVQA, InfoVQA, DocVQA, ChartQA, and RealWorldQA**. A separately constructed **GDP-v2-lite** is used as a supplementary scale check, not as a replacement for the manually reviewed diagnostic slice.

GDP also compares **direct**, **evidence-first**, and **answer-first** prompting as controlled interventions. The central finding is **model dependence**: evidence-first prompting does not uniformly improve hard-distractor performance. Reported response patterns differ across LLaVA-style, Qwen2.5-VL, and InternVL2.5 models.

## Method

1. **Construct near-miss alternatives.** For each selected image–question–answer item, prepare a visually plausible wrong answer of the same semantic type as the correct answer. Examples include a nearby number, a slightly different clock reading, or a different object count.
2. **Build matched conditions.** Evaluate the original item, an option-order permutation control, and the item with one hard distractor, holding the image, question, and correct answer fixed.
3. **Apply controlled prompting interventions.** Compare direct answering with evidence-first and answer-first variants. These prompts are diagnostic probes rather than a proposed universal prompting improvement.
4. **Analyze paired behavior.** Examine accuracy, changes in hard-distractor selection, and paired response patterns. The paper reports diagnostic measures including **HSIG** and **ΔHDsel**, together with **McNemar tests** and **bootstrap confidence intervals**.
5. **Check scope.** Interpret the carefully reviewed 98-item GDP-Slice as a diagnostic set, and use GDP-v2-lite for supplementary scale validation rather than claiming it is an interchangeable benchmark.

For protocol definitions, exact statistics, experimental settings, and limitations, consult the [camera-ready paper](./csp3510_Grounded_Distractor_Probing_A_Diagnostic_Protocol_for_Hard_Distractor_Sensitivity_in_VLM_Multiple_Choice_Evaluation.pdf).

## Installation and Reproduction

**Status: code and data are not yet publicly available in this repository.** The repository currently contains the paper and project materials; there is not yet a runnable installation, a tested dependency list, or a reproduction command. Please do not treat the following checkout step as a working implementation:

```bash
git clone https://github.com/owinhun/GDP.git
cd GDP
```

The release is planned to include the reviewed GDP-Slice data, prompt templates, model-specific inference scripts, metric computation, and reproduction instructions. Exact environment requirements and commands will be documented **when those artifacts are uploaded and verified**.

## Release Status

- [x] Camera-ready paper available
- [x] Project page available via GitHub Pages
- [ ] GDP-Slice (98-item diagnostic data) released
- [ ] Direct / evidence-first / answer-first prompt templates released
- [ ] VLM inference scripts and dependency specifications released
- [ ] Evaluation metrics and statistical analysis scripts released
- [ ] End-to-end reproduction instructions validated

## News

- **August 2026** — Accepted at the **35th ACM International Conference on Information and Knowledge Management (CIKM 2026)**.

## Acknowledgements

For the authoritative acknowledgement and funding disclosures, please refer to the [camera-ready manuscript](./csp3510_Grounded_Distractor_Probing_A_Diagnostic_Protocol_for_Hard_Distractor_Sensitivity_in_VLM_Multiple_Choice_Evaluation.pdf).
This work was supported by the Institute of Information & Communications Technology Planning & Evaluation (IITP) grant funded by the Korea government (MSIT) (No. RS-2024-00438027, Development of an intelligent security and risk response system based on multi-modal data integration analysis), and by the Artificial Intelligence Innovation Graduate School (Sogang University) grant funded by the Korea government (MSIT) (No. RS-2026-25547954).


## Contact

Questions about this research or repository: **Seunghun Oh** — [gnsgus190@sogang.ac.kr](mailto:gnsgus190@sogang.ac.kr)

## Citation

The citation below is **provisional**. Replace it with the official ACM BibTeX entry when published.

```bibtex
@inproceedings{oh2026grounded,
  title     = {Grounded Distractor Probing: A Diagnostic Protocol for Hard-Distractor Sensitivity in VLM Multiple-Choice Evaluation},
  author    = {Oh, Seunghun and Jeong, Ganghyeon and Park, Unsang},
  booktitle = {Proceedings of the 35th ACM International Conference on Information and Knowledge Management},
  year      = {2026},
  note      = {Accepted at CIKM 2026; provisional citation}
}
```
