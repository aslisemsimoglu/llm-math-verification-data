# Mathematical Answer Verification: Experimental Data

## Overview

This repository contains experimental datasets, model outputs,
training records, and evaluation artifacts from a controlled
study of parameter-efficient language-model adaptation for
mathematical answer generation and verification.

The archive is organized to support independent inspection
of the experimental design, model responses, and reported
automatic-verification outcomes.

## Experimental configuration

- Model families: Qwen2.5-1.5B-Instruct and
  Qwen2.5-Math-1.5B-Instruct
- Adaptation: quantized parameter-efficient fine-tuning
- Training sizes: 100, 300, 600, and 900
- Random seeds: 42, 123, and 2026
- Adapted configurations: 24
- Baseline configurations: 2
- Fixed test questions per configuration: 210
- Total primary evaluation records: 5,460

## Repository contents

| Directory | Description |
|---|---|
| `data/splits/` | Dataset partitions and seeded training subsets |
| `experiments/runs/` | Training metrics and checkpoint-selection records |
| `experiments/summary/` | Experiment-level summaries |
| `evaluation/predictions/` | Raw outputs for 26 evaluation configurations |
| `evaluation/scoring/` | Record-level automatic evaluation |
| `evaluation/summary/` | Aggregated evaluation results |
| `evaluation/review/` | Review queues and conservative screening artifacts |
| `statistics/` | Paired statistical comparisons and bootstrap results |
| `pilot/` | Exploratory novel-template evaluation materials |

## Primary automatic-verification outcomes

Across 5,460 evaluated responses:

- Correct (C): 4,077
- Wrong (W): 966
- Review-required (R): 417

R indicates that the automatic verification procedure did
not establish a definitive outcome. It does not itself
indicate mathematical incorrectness.

Review queues and screening candidates are not final
independent human adjudications.

## Data interpretation

The `auto_class` field records the primary automatic
verification outcome. The `semantic_class` field in the
distributed scoring file mirrors the associated automatic
classification and must not be treated as independent
human verification.

The primary evaluation, review screening, and exploratory
pilot are distinct analytical components.

## Integrity

`SHA256SUMS.csv` provides cryptographic hashes for
checking the integrity of the archived files.

## Reproducibility scope

This archive preserves datasets, recorded outputs, training
metrics, and evaluation results. It does not contain model
weights or a complete executable reconstruction of the
training and inference environment.

## Attribution and license

Formal citation information and reuse permissions will be
finalized before public release.
