# Reviewer bench

Records: 554. Profiles: claude-build, glm-build, gpt-build, grok-build.

## orders: claims stage, gate_claims_auditor

| case | claude-build | glm-build | gpt-build | grok-build |
|---|---|---|---|---|
| clean | clean_pass/clean_pass/clean_pass $1.59 | clean_pass/clean_pass/clean_pass $0.01 | clean_pass/clean_pass/clean_pass $0.00 | clean_pass/clean_pass/clean_pass $0.57 |
| population_relabelled | blocked/blocked/blocked/blocked/blocked $1.66 | blocked/blocked/blocked/blocked $0.01 | blocked/blocked/blocked $0.00 | blocked/blocked/blocked/blocked $0.42 |
| basis_caveat_inverted |  |  |  |  |
| period_shifted_in_claim | blocked/blocked/blocked/blocked/blocked $1.66 | blocked/blocked/blocked/blocked $0.01 | blocked/blocked/blocked $0.00 | blocked/blocked/blocked/blocked $0.47 |
| unit_relabelled |  |  |  |  |
| claim_bound_to_wrong_metric |  |  |  |  |
| unsupported_trend_in_caveat | blocked/blocked/blocked/blocked/blocked $1.48 | blocked/blocked/blocked/blocked $0.01 | blocked/blocked/blocked $0.00 | blocked/blocked/blocked/blocked $0.42 |
| answer_misreads_its_fact | blocked/blocked/blocked/blocked/blocked $1.63 | blocked/blocked/blocked/blocked $0.01 | blocked/blocked/blocked $0.00 | blocked/blocked/blocked/blocked $0.47 |
| exclusion_reasons_swapped | blocked/blocked/blocked/blocked/blocked $1.52 | blocked/blocked/blocked/blocked $0.01 | blocked/blocked/blocked $0.00 | blocked/blocked/blocked/blocked $0.38 |
| question_restated_narrower | blocked/blocked/blocked/blocked/blocked $1.73 | warned/warned/warned/blocked/warned $0.01 | missed/blocked/blocked $0.00 | blocked/blocked/blocked/blocked $0.48 |
| value_hardcoded_in_code | blocked/blocked/blocked $1.86 | warned/missed/missed $0.01 | missed/missed/missed $0.00 | blocked/blocked/blocked $0.56 |

## orders: release stage, gate_release_auditor

| case | claude-build | glm-build | gpt-build | grok-build |
|---|---|---|---|---|
| clean | clean_pass/clean_pass/clean_pass $1.85 | clean_pass/clean_pass/clean_pass $0.01 | clean_blocked/clean_pass/clean_pass $0.00 | clean_pass/clean_pass/clean_pass $0.64 |
| headline_relabelled_gross | blocked/blocked/blocked/blocked/blocked $1.62 | blocked/blocked/blocked/blocked $0.01 | blocked/blocked/blocked $0.00 | blocked/blocked/blocked/blocked $0.49 |
| population_line_wrong | blocked/blocked/blocked/blocked/blocked $1.62 | blocked/blocked/blocked/blocked $0.01 | blocked/blocked/blocked $0.00 | blocked/blocked/blocked/blocked $0.46 |
| country_labels_swapped | blocked/blocked/blocked $1.69 | blocked/blocked/blocked $0.01 | blocked/blocked/blocked $0.00 | blocked/blocked/blocked $0.54 |
| unsupported_trend_in_prose | blocked/blocked/blocked/blocked/blocked $1.54 | warned/blocked/blocked/blocked/blocked $0.01 | blocked/blocked/blocked $0.00 | blocked/blocked/blocked/blocked $0.58 |
| sum_sentence_false | blocked/blocked/blocked/blocked/blocked $1.61 | blocked/blocked/blocked/blocked $0.01 | blocked/blocked/blocked $0.00 | blocked/blocked/blocked/blocked $0.57 |
| refund_basis_misstated_on_page |  |  |  |  |
| caveat_dropped_where_repeated | blocked/blocked/blocked/blocked/blocked $1.59 | blocked/blocked/blocked/blocked $0.02 |  | blocked/blocked $0.71 |

## orders: final stage, final red team

Each defect planted in its own stage, passed by that stage's auditor (a fake agent), and shown to the final red team.

| case | claude-build | glm-build | gpt-build | grok-build |
|---|---|---|---|---|
| clean | clean_pass $4.42 | clean_pass $0.07 |  |  |
| population_relabelled | blocked/blocked/blocked/blocked $3.95 | blocked/blocked $0.05 |  | blocked $0.46 |
| basis_caveat_inverted |  |  |  |  |
| period_shifted_in_claim | blocked/blocked/blocked/blocked $3.64 | blocked/blocked $0.06 |  | blocked $0.36 |
| unit_relabelled |  |  |  |  |
| claim_bound_to_wrong_metric |  |  |  |  |
| unsupported_trend_in_caveat |  |  |  |  |
| answer_misreads_its_fact | blocked/blocked/blocked/blocked $3.58 | blocked/blocked $0.08 |  | blocked $0.51 |
| exclusion_reasons_swapped | blocked/blocked/blocked/blocked $3.77 | blocked/blocked $0.05 |  | blocked $0.50 |
| question_restated_narrower | blocked/blocked/warned/blocked $4.54 | warned/warned/warned $0.07 |  |  |
| value_hardcoded_in_code |  |  |  |  |
| headline_relabelled_gross | blocked/blocked/blocked/blocked $4.13 | blocked/blocked $0.05 |  |  |
| population_line_wrong | blocked/blocked/blocked/blocked $4.03 | blocked/blocked $0.04 |  |  |
| country_labels_swapped |  |  |  |  |
| unsupported_trend_in_prose | blocked/blocked/blocked/blocked $3.94 | blocked/blocked/blocked $0.06 |  |  |
| sum_sentence_false | blocked/blocked/blocked/blocked $3.77 | blocked/blocked $0.05 |  |  |
| refund_basis_misstated_on_page |  |  |  |  |
| caveat_dropped_where_repeated | blocked/blocked/blocked/blocked $3.73 | blocked/blocked $0.06 |  | blocked $0.35 |

## messy: claims stage, gate_claims_auditor

| case | claude-build | glm-build | gpt-build | grok-build |
|---|---|---|---|---|
| clean | clean_blocked $2.74 | clean_pass $0.02 |  |  |
| m_interval_read_as_probability | blocked/blocked/blocked/blocked/blocked/blocked/blocked $2.71 | blocked/blocked/blocked $0.02 |  | blocked/blocked $0.69 |
| m_mix_caveat_inverted | blocked/blocked/blocked/blocked/blocked/blocked/blocked $2.82 | blocked/blocked/blocked $0.03 |  | blocked/blocked $0.71 |
| m_causal_channel_answer | blocked/blocked/blocked/blocked/blocked/blocked/blocked $2.75 | blocked/blocked/blocked $0.02 |  | blocked/blocked $0.71 |
| m_dedup_rule_misstated | blocked/blocked/blocked/blocked/blocked/blocked/blocked $2.74 | blocked/blocked/blocked $0.02 |  | blocked/blocked $0.61 |
| m_shipping_answer_complete | blocked/blocked/blocked/blocked/blocked/blocked/blocked $2.45 | blocked/blocked/blocked $0.02 |  | blocked/blocked $0.72 |
| m_completion_population_delivered | blocked/blocked/blocked/blocked/blocked/blocked/blocked $2.87 | blocked/missed/warned/blocked/blocked $0.02 |  | blocked/blocked $0.75 |
| m_question_dropped_uncertainty | blocked/warned/blocked/blocked/blocked/blocked/blocked $2.98 | warned/missed/missed/warned/warned $0.02 |  | blocked/blocked $0.80 |
| m_effect_misnamed | blocked/blocked/blocked/blocked/blocked/blocked/blocked $2.85 | blocked/blocked/blocked $0.02 |  | blocked/blocked $0.68 |

## messy: release stage, gate_release_auditor

| case | claude-build | glm-build | gpt-build | grok-build |
|---|---|---|---|---|
| clean | clean_blocked $2.35 | clean_blocked $0.02 |  |  |
| m_page_interval_certainty | blocked/blocked/blocked/blocked/blocked/blocked/blocked $2.47 | blocked/blocked/blocked $0.02 |  | blocked/blocked $0.62 |
| m_page_causal_sentence | blocked/blocked/blocked/blocked/blocked/blocked/blocked $2.28 | blocked/blocked/blocked $0.02 |  | blocked/blocked $0.54 |
| m_population_line_all_rows | blocked/blocked/blocked/blocked/blocked/blocked/blocked $2.15 | blocked/blocked/blocked $0.03 |  | blocked/blocked $0.56 |
| m_channel_labels_swapped_page | blocked/blocked/blocked/blocked/blocked/blocked/blocked $2.16 | blocked/blocked/blocked $0.02 |  | blocked $0.71 |
| m_dashboard_aov_labelled_revenue | blocked/blocked/blocked/blocked/blocked/blocked/blocked $2.49 | blocked/blocked/blocked $0.03 |  | blocked $0.57 |
| m_page_no_uncertainty | blocked/blocked/blocked/blocked/blocked/blocked/blocked $2.32 | blocked/blocked/blocked $0.02 |  | blocked $0.61 |

## messy: final stage, final red team

Each defect planted in its own stage, passed by that stage's auditor (a fake agent), and shown to the final red team.

| case | claude-build | glm-build | gpt-build | grok-build |
|---|---|---|---|---|
| clean | clean_blocked $7.76 | clean_blocked $0.10 |  |  |
| m_interval_read_as_probability | blocked/blocked/blocked/blocked $5.99 | blocked/blocked $0.10 |  |  |
| m_mix_caveat_inverted | blocked/blocked/blocked/blocked $5.84 | blocked/blocked $0.09 |  |  |
| m_causal_channel_answer | blocked/blocked/blocked/blocked $5.75 | blocked $0.08 |  |  |
| m_dedup_rule_misstated | blocked/blocked/blocked/blocked $5.82 | blocked/blocked $0.11 |  |  |
| m_shipping_answer_complete | blocked/blocked/blocked/blocked $6.49 | blocked $0.08 |  |  |
| m_completion_population_delivered | blocked/blocked/blocked/blocked $7.02 | blocked/blocked/blocked $0.10 |  |  |
| m_question_dropped_uncertainty | blocked/blocked/blocked/blocked $7.10 | blocked/blocked/blocked $0.10 |  |  |
| m_effect_misnamed | blocked/blocked/blocked/blocked $6.11 | warned/blocked/blocked $0.08 |  |  |
| m_page_interval_certainty | blocked/blocked/blocked $5.49 | blocked $0.06 |  |  |
| m_page_causal_sentence | blocked/blocked/blocked $5.39 | blocked $0.11 |  |  |
| m_population_line_all_rows | blocked/blocked/blocked $5.80 | blocked $0.08 |  |  |
| m_channel_labels_swapped_page | blocked/blocked/blocked $5.44 | blocked $0.05 |  |  |
| m_dashboard_aov_labelled_revenue | blocked/blocked/blocked $6.49 | blocked $0.08 |  |  |
| m_page_no_uncertainty | blocked/blocked/blocked $5.98 | blocked $0.19 |  |  |

## Workers: one launch, judged by the runner's verify and the stage's machine gate

| profile | stage | launches | gate pass | gate fail | not verified | mean cost | mean wall s |
|---|---|---|---|---|---|---|---|
| claude-build | clean | 1 | 1 | 0 | 0 | $1.74 | 215 |
| claude-build | metrics | 1 | 1 | 0 | 0 | $2.44 | 356 |
| claude-build | analysis | 1 | 1 | 0 | 0 | $2.93 | 348 |
| claude-build | release | 1 | 1 | 0 | 0 | $3.58 | 491 |
| glm-build | clean | 1 | 1 | 0 | 0 | $0.01 | 219 |
| glm-build | metrics | 1 | 1 | 0 | 0 | $0.03 | 138 |
| glm-build | analysis | 1 | 1 | 0 | 0 | $0.05 | 250 |
| glm-build | release | 1 | 1 | 0 | 0 | $0.03 | 138 |
| gpt-build | clean | 1 | 1 | 0 | 0 | $0.00 | 496 |
| gpt-build | metrics | 1 | 1 | 0 | 0 | $0.00 | 13876 |
| gpt-build | analysis | 1 | 0 | 0 | 1 | $0.00 | 303 |
| gpt-build | release | 1 | 1 | 0 | 0 | $0.00 | 300 |
| grok-build | clean | 1 | 1 | 0 | 0 | $0.53 | 660 |
| grok-build | metrics | 1 | 1 | 0 | 0 | $0.66 | 829 |
| grok-build | analysis | 1 | 1 | 0 | 0 | $0.68 | 672 |
| grok-build | release | 1 | 1 | 0 | 0 | $0.67 | 534 |

## Totals

False blockers and false warnings are counted on the clean control, where nothing was planted. Other blockers are a reviewer's blocking issues on a planted case that name nothing of the defect; records from before they were kept show a dash.

| profile | dataset | stage | cases | blocked | warned | missed | false blockers | false warnings | other blockers | mean cost | mean wall s |
|---|---|---|---|---|---|---|---|---|---|---|---|
| claude-build | orders | claims | 33 | 33 | 0 | 0 | 0 over 3 | 8 over 3 | 0 over 12 | $1.63 | 178 |
| claude-build | orders | release | 28 | 28 | 0 | 0 | 0 over 3 | 16 over 3 | 2 over 13 | $1.63 | 213 |
| claude-build | orders | final | 40 | 39 | 1 | 0 | 0 over 1 | 9 over 1 | 0 over 40 | $3.92 | 381 |
| claude-build | messy | claims | 56 | 55 | 1 | 0 | 2 over 1 | 9 over 1 | 38 over 56 | $2.77 | 243 |
| claude-build | messy | release | 42 | 42 | 0 | 0 | 4 over 1 | 6 over 1 | 50 over 42 | $2.31 | 240 |
| claude-build | messy | final | 50 | 50 | 0 | 0 | 5 over 1 | 9 over 1 | 171 over 50 | $6.12 | 633 |
| glm-build | orders | claims | 28 | 21 | 5 | 2 | 0 over 3 | 1 over 3 | 0 over 7 | $0.01 | 159 |
| glm-build | orders | release | 24 | 23 | 1 | 0 | 0 over 3 | 5 over 3 | 3 over 9 | $0.01 | 207 |
| glm-build | orders | final | 22 | 19 | 3 | 0 | 0 over 1 | 10 over 1 | 1 over 22 | $0.06 | 934 |
| glm-build | messy | claims | 28 | 21 | 4 | 3 | 0 over 1 | 2 over 1 | 0 over 28 | $0.02 | 285 |
| glm-build | messy | release | 18 | 18 | 0 | 0 | 2 over 1 | 5 over 1 | 13 over 18 | $0.02 | 343 |
| glm-build | messy | final | 23 | 22 | 1 | 0 | 2 over 1 | 8 over 1 | 18 over 23 | $0.10 | 1203 |
| gpt-build | orders | claims | 21 | 17 | 0 | 4 | 0 over 3 | 1 over 3 | - | $0.00 | 915 |
| gpt-build | orders | release | 15 | 15 | 0 | 0 | 1 over 3 | 6 over 3 | - | $0.00 | 1863 |
| grok-build | orders | claims | 27 | 27 | 0 | 0 | 0 over 3 | 9 over 3 | 0 over 6 | $0.47 | 521 |
| grok-build | orders | release | 21 | 21 | 0 | 0 | 0 over 3 | 13 over 3 | 0 over 6 | $0.56 | 627 |
| grok-build | orders | final | 5 | 5 | 0 | 0 | 0 over 0 | 0 over 0 | 0 over 5 | $0.44 | 585 |
| grok-build | messy | claims | 16 | 16 | 0 | 0 | 0 over 0 | 0 over 0 | 13 over 16 | $0.71 | 726 |
| grok-build | messy | release | 9 | 9 | 0 | 0 | 0 over 0 | 0 over 0 | 5 over 9 | $0.59 | 743 |
