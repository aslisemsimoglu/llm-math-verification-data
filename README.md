# Mathematical Answer Verification: Experimental Data

Datasets, model-generated responses, training records, and evaluation artifacts for mathematical answer verification using parameter-efficient fine-tuning.

## Experimental Configuration

| Parameter | Value |
|---|---|
| Models | Qwen2.5-1.5B-Instruct, Qwen2.5-Math-1.5B-Instruct |
| Method | QLoRA |
| Training sizes | 100, 300, 600, 900 |
| Random seeds | 42, 123, 2026 |
| Fine-tuned configurations | 24 |
| Baseline configurations | 2 |
| Test questions per configuration | 210 |
| Total evaluated responses | 5,460 |

## Repository Structure

| Directory | Contents |
|---|---|
| `data/` | Dataset partitions |
| `experiments/` | Training records and configurations |
| `evaluation/` | Predictions and verification records |
| `statistics/` | Statistical analysis results |
| `pilot/` | Exploratory evaluation data |

## Automatic Verification

| Classification | Count |
|---|---:|
| Correct (C) | 4,077 |
| Wrong (W) | 966 |
| Review-required (R) | 417 |
| Total | 5,460 |

Additional evidence-based assessments are provided in `evaluation/review/final_evidence/` and remain separate from the original automatic outcomes.

## Documentation

- `DATA_DICTIONARY.md`: Data definitions.
- `SHA256SUMS.csv`: File integrity checksums.

Model weights, adapter weights, and the complete executable training environment are not included.

## Creators

Aslı Şemşimoğlu and Celal Onur Gökçe (2026).
