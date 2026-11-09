# Review and Screening Data

These files describe automatically identified cases requiring
additional assessment.

## review_required_417.csv

The complete set of 417 cases labeled R by the primary
automatic-verification protocol. R denotes review-required,
not necessarily mathematically incorrect.

The adjudication fields are unpopulated in this source.
The file must not be interpreted as a finalized manual review.

## triage_candidates_417.csv

Rule-based triage metadata for the same 417 cases.
Candidate labels are preliminary diagnostic information,
not independently verified correctness judgments.

## conservative_screening_289.csv

A subset of 289 review-required records processed by
additional conservative screening rules.

Screening categories indicate whether a case could be
resolved by the implemented rule set or required further
assessment. They are not final human annotations.

## Interpretation

Do not combine these files by concatenating rows:
they contain overlapping observations.

The shared identifiers are condition, test_index,
and question_id.

Original records are preserved without modifications.
