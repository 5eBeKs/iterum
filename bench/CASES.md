# Planted defects

[Русская версия](CASES.ru.md)

Every defect the bench shows a reviewer: where it is planted, which zoo class it belongs to, and what is wrong, in a client's words. A case marked as a mirror plants the one mistake the machine corpus records as a gap.

| case | dataset | stage | class | what is wrong |
|---|---|---|---|---|
| `population_relabelled` | orders | claims | definition | The headline claim says its population is all orders, while the spec and its own caveats say delivered orders. |
| `basis_caveat_inverted` | orders | claims | definition | The refund-rate caveat names the wrong denominator: order rows instead of unique paying customers. |
| `period_shifted_in_claim` | orders | claims | definition | One country claim carries a two-month period while its value is the full quarter's. |
| `unit_relabelled` | orders | claims | definition | One country claim is labelled USD; every figure of the audit is EUR. |
| `claim_bound_to_wrong_metric` | orders | claims | provenance | The PL claim lists the DE metric as its source while its value and reference are PL's. |
| `unsupported_trend_in_caveat` | orders | claims | inference | A caveat asserts growth against a previous quarter no metric computes. |
| `answer_misreads_its_fact` | orders | claims | inference | The answer to R02 calls a 47% refund rate low, fewer than one order in ten. |
| `exclusion_reasons_swapped` | orders | claims | label | R04 attaches each exclusion count to the other rule: 26 rows 'outside period', 1 row 'not delivered'. |
| `question_restated_narrower` | orders | claims | answer | R02 is restated without the half that asks on which basis the rate is taken. |
| `value_hardcoded_in_code` | orders | claims | provenance | The analysis code writes the headline as a literal instead of reading the metrics registry; the number happens to be right. |
| `headline_relabelled_gross` | orders | release | label | The page calls net revenue 'Gross revenue'; the number is net of refunds. |
| `population_line_wrong` | orders | release | definition | The page's population line says all orders; every figure is over delivered orders. |
| `country_labels_swapped` | orders | release | label | On the dashboard the PL and DE cards carry each other's labels; values and claim ids are untouched. |
| `unsupported_trend_in_prose` | orders | release | inference | The page says revenue grew through the quarter; no monthly figure exists in the audit. |
| `sum_sentence_false` | orders | release | definition | The page says the country figures sum to the headline before refunds; both are net of refunds. |
| `refund_basis_misstated_on_page` | orders | release | definition | The page states the refund-rate denominator is order rows; it is unique paying customers. |
| `caveat_dropped_where_repeated` (mirrors `caveat_covered_by_another_figure`) | orders | release | qualification | The headline's caveat line no longer says net of refunds; only a sentence about the country table still does. |
| `m_interval_read_as_probability` | messy | claims | inference | The answer to R03 reads each 0.95 interval as a 95% probability that the true rate lies inside it. |
| `m_mix_caveat_inverted` | messy | claims | qualification | The partner completion rate's caveat says its interval also covers a change in the channel's country mix. |
| `m_causal_channel_answer` | messy | claims | inference | The answer to R04 explains the lower partner basket by customers' price sensitivity, which no data in the audit measures. |
| `m_dedup_rule_misstated` | messy | claims | definition | The answer to R02 says the first revision of an order is kept; the spec and the clean stage keep the last. |
| `m_shipping_answer_complete` | messy | claims | qualification | The answer to R05 calls the shipping total complete; about six per cent of its cells are blank, NaN or inf. |
| `m_completion_population_delivered` | messy | claims | definition | The direct completion rate says its population is delivered orders, over which a completion rate is always 1. |
| `m_question_dropped_uncertainty` | messy | claims | answer | R03 is restated without the half of the brief that asks how precisely each rate is known. |
| `m_effect_misnamed` | messy | claims | definition | The R04 test calls its effect size a proportion difference; a Welch test on order values reports Cohen's d. |
| `m_page_interval_certainty` | messy | release | inference | The page says each interval is where the true value lies with near certainty. |
| `m_page_causal_sentence` | messy | release | inference | The page explains the smaller partner baskets by bargain hunters, which nothing in the audit measures. |
| `m_population_line_all_rows` | messy | release | definition | The page's population line says every export row; the figures are over one row per order after deduplication. |
| `m_channel_labels_swapped_page` | messy | release | label | On the page the direct and partner completion lines carry each other's labels; the figures and anchors are untouched. |
| `m_dashboard_aov_labelled_revenue` | messy | release | label | On the dashboard the direct average order value card is labelled revenue. |
| `m_page_no_uncertainty` | messy | release | qualification | The page says the channel figures are measured over every order and carry no uncertainty, beside their intervals. |
