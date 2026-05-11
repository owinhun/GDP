# Grounded Distractor Protocol (GDP)

> Diagnosing Model-Dependent Intervention Effects under Hard Distractors 
> in MCQ-Based Vision-Language Model Evaluation

## Overview

GDP is a matched original/permutation/hard evaluation protocol designed to 
diagnose how vision-language models (VLMs) respond to same-type, visually 
plausible near-miss distractors under controlled interventions.

This repository accompanies our paper submitted to CIKM 2026.

## Key Findings

- Hard distractor sensitivity exhibits **model-dependent** patterns that 
  cannot be explained by generic option-position bias alone.
- Evidence-first prompting is **not a universal improvement**: LLaVA family 
  models benefit, while Qwen2.5-VL and InternVL2.5 show negative effects.
- Answer-first follow-up controls suggest that the model-dependent effects 
  reflect differences in intervention mechanisms, not just performance.

## Status

🚧 **This repository is under construction.** 

Code, GDP-Slice dataset, and prompt templates will be released upon 
publication of the paper.

## Planned Contents

- [ ] GDP-Slice: 98-item diagnostic slice with hard distractors
- [ ] Prompt templates (direct, evidence-first, answer-first)
- [ ] Inference scripts for 4 evaluated VLMs
- [ ] Metric computation (HSIG, ΔHDsel, statistical tests)
- [ ] Reproduction scripts

## Citation

Citation information will be added upon publication.

## Contact

Will be added upon de-anonymization.

## License

MIT License (planned)
