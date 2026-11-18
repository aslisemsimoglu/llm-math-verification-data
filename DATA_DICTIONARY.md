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

## Additional evaluation evidence

Path: `evaluation/review/final_evidence/`

| File | Contents |
|---|---|
| `G01L_ALL_5460_EVIDENCE_BRIDGE.csv` | Original outcomes and supplementary evidence classifications |
| `G01L_BY_CONDITION_AND_EVIDENCE.csv` | Condition-level evidence summaries |
| `G01L_OPEN_R_107.csv` | Remaining unresolved responses |
| `G01L_SUMMARY.json` | Aggregate evidence counts and source checksums |
| `G01D_ALL_417_EVIDENCE_MATRIX.csv` | Intermediate evidence records for the original R cases |
| `G01F_84_RECORD_LEVEL_RESOLUTION.csv` | Record-level disagreement resolution |
| `G01G_203_RECORD_LEVEL_AUDIT.csv` | Assessment agreement audit |
| `G01I_ALL_110_POLICY_DECISIONS.csv` | Conservative decision-policy records |
| `reviewer_2_BLIND_287_EVALUATED.csv` | AI-assisted contextual assessment records |

The evidence bridge preserves the original automatic classifications.

| Assessment | Correct | Incorrect | Unresolved |
|---|---:|---:|---:|
| Deterministic verification | 119 | 11 | 0 |
| Contextual assessment and reconciliation | 145 | 35 | 107 |
| Total | 264 | 46 | 107 |

These records represent overlapping assessment stages and must not be concatenated as independent observations.

No independent human adjudication was performed. Supplementary classifications do not represent independently human-validated semantic accuracy.

Legacy reviewer and human-adjudication field names are retained as archival schema fields and do not imply human assessment.

The summary contains checksums for original source artifacts, including artifacts not distributed in this repository.
