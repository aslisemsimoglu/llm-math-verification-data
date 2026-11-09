# Data Dictionary

## Primary scoring file

Path: `evaluation/scoring/scored_predictions.csv`

| Column | Description |
|---|---|
| `condition` | Experimental configuration identifier |
| `model` | Language-model family |
| `seed` | Experimental random seed |
| `training_size` | Training-set size |
| `test_index` | Position within the fixed test set |
| `question_id` | Question identifier |
| `category` | Mathematical problem category |
| `difficulty` | Dataset difficulty label |
| `template_id` | Problem template identifier |
| `question` | Mathematical question |
| `reference_answer` | Reference answer |
| `generated_text` | Recorded model response |
| `auto_class` | Automatic outcome: C, W, or R |
| `auto_reason` | Recorded automatic-verification reason |
| `format_compliant` | Recorded response-format compliance flag |
| `semantic_class` | Derived classification; not independent annotation |
| `generated_tokens` | Recorded number of generated tokens |
| `reached_generation_limit` | Whether the generation limit was reached |

## Review data

`review_required_417.csv` contains the complete set of
review-required records.

`triage_candidates_417.csv` contains preliminary
rule-based screening information for those records.

`conservative_screening_289.csv` contains an overlapping
289-record subset processed by conservative rules.

These files must not be concatenated or interpreted as
independent samples.

## Statistical files

`G03_EXACT_MCNEMAR.csv` contains recorded exact McNemar
test results.

`G03_TEMPLATE_CLUSTER_BOOTSTRAP.csv` contains recorded
template-cluster bootstrap results.

Statistical interpretation should follow the methods and
comparison definitions associated with these records.

## Pilot records

The pilot directory contains exploratory materials and
separate model outputs. Pilot observations should not be
added to the 5,460 primary evaluation records.
