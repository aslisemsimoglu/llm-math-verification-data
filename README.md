
# Mathematical Answer Verification: Experimental Data

## Overview

This repository provides datasets, model-generated responses, training records, and evaluation results from a controlled experimental study of parameter-efficient fine-tuning for mathematical answer verification.

## Experimental Design

- **Models:** Qwen2.5-1.5B-Instruct and Qwen2.5-Math-1.5B-Instruct
- **Method:** Quantized Low-Rank Adaptation (QLoRA)
- **Training-set sizes:** 100, 300, 600, and 900
- **Random seeds:** 42, 123, and 2026
- **Fine-tuned configurations:** 24
- **Baseline configurations:** 2
- **Test questions per configuration:** 210
- **Total evaluated responses:** 5,460

## Repository Structure

| Directory | Contents |
|---|---|
| `data/splits/` | Training subsets, validation data, and fixed test data |
| `experiments/runs/` | Training metrics and checkpoint-selection records |
| `experiments/summary/` | Experimental configuration and aggregate results |
| `evaluation/predictions/` | Model-generated responses |
| `evaluation/scoring/` | Record-level verification outcomes |
| `evaluation/summary/` | Aggregated evaluation results |
| `evaluation/review/` | Review-required cases and screening records |
| `statistics/` | McNemar tests and bootstrap analyses |
| `pilot/` | Exploratory evaluation on additional problem templates |

## Evaluation Results

The primary automatic-verification procedure produced the following outcomes:

| Classification | Count |
|---|---:|
| Correct (C) | 4,077 |
| Wrong (W) | 966 |
| Review-required (R) | 417 |
| **Total** | **5,460** |

The review-required category denotes responses for which the automatic procedure did not establish a definitive correctness judgment.

Review and screening records are provided separately from the primary evaluation results.

## Data Documentation

The `DATA_DICTIONARY.md` file describes the principal variables and evaluation records.

The `SHA256SUMS.csv` file provides SHA-256 checksums for verifying file integrity.

## Reproducibility

The repository includes the dataset partitions, recorded model outputs, experimental metrics, checkpoint-selection information, and evaluation artifacts used in the study.

Pretrained model weights, fine-tuned adapter weights, and the complete executable training environment are not distributed in this repository.

## Citation

**Dataset title:** Mathematical Answer Verification: Experimental Data

**Creators:** Aslı Şemşimoğlu and Celal Onur Gökçe

**Year:** 2026

A version-specific DOI and recommended citation will be available through the associated Zenodo record.
