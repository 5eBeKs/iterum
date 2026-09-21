# Что проверено в отчёте и что найдено

*Документ для читателя отчёта. Ничего не считает сам: каждое число и каждый статус взяты из записей проверки.*

Все 6 числа отчёта воспроизводятся из выгрузки независимым пересчётом.

Правила проверки зафиксированы 2026-09-16 12:25 UTC; после этого их никто не менял.

Проверка ещё не запечатана: этот документ описывает её текущее состояние.

## Что это за документ

Отчёт был написан по выгрузке данных. Каждое его число пересчитано из той же выгрузки отдельным кодом, который не видел, как считал автор отчёта, и сравнено с тем, что напечатано. Проверялись числа и слова, стоящие рядом с ними; всё остальное, что отчёт говорит словами, здесь не проверялось.

## Главное

- Six in-quarter orders (M006912, M008447, M015636, M016369, M035357, M037901) each have two revisions with the same updated_at, and the status differs: cancelled or pending in the earlier row, delivered in the later one. …
- The stage prompt asks the summary to say every context in this pipeline is one model. The execution blocks of the results in this stage's inputs show two models: openrouter/z-ai/glm-5.3-flash for gate0_semantic and the four workers, and claude-opus-5 for the four gate auditors and this red-team. …
- The unpublished shipping_total of 37792722.50 is a faithful reading of the column in the declared locale, not a locale misread. Every in-population cell matched one of eight notations. …
- release/report.md line 85 points the reader to the metric registry for the shipping total as a lower bound. No figure is shown, and the lower-bound statement holds: 2648 unreadable cells were zeroed and no parsed value is negative. …
- Both completion-rate claims and their dashboard cards carry the quarter-wide population string 'orders placed inside the quarter, one row per order' rather than naming the channel. …

## Числа отчёта

Расхождения и неподтверждённые числа стоят первыми. Допуск: денежные суммы ±0,01, доли ±0,000001, счётчики точно.

| Где в отчёте | Число | Что означает | Пересчёт из выгрузки | Статус |
|---|---|---|---|---|
| строка 7 | 3023296.61 | net revenue (SUM(gross_amount - refund_amount) WHERE status = delivered) | 3023296.61 | совпадает |
| строка 19 | 44531 | orders in period (COUNT(order_id) after deduplication) | 44531 | совпадает |
| строка 29 | 0.724397 | completion rate direct / completion ci low direct / completion ci high direct | 0.724397 | совпадает |
| строка 42 | 0.604746 | completion rate partner / completion ci low partner / completion ci high partner | 0.604746 | совпадает |
| строка 55 | 110.64 | aov direct / aov ci low direct / aov ci high direct | 110.64 | совпадает |
| строка 70 | 87.27 | aov partner / aov ci low partner / aov ci high partner | 87.27 | совпадает |

- совпадает — число отчёта воспроизводится из выгрузки в пределах допуска
- не совпадает — в отчёте напечатано не то, что посчитано
- не подтверждено — два независимых пересчёта разошлись; число не названо ни верным, ни неверным
- не показано в отчёте — число посчитано и проверено, но в отчёт не попало

## Что заметила независимая проверка

Последний шаг — отдельная проверка всей работы с чистого листа (claude-opus-5). Её вердикт: пройдено. Замечания ниже — её слова, приведены как есть.

### Замечания

- Six in-quarter orders (M006912, M008447, M015636, M016369, M035357, M037901) each have two revisions with the same updated_at, and the status differs: cancelled or pending in the earlier row, delivered in the later one. keep_latest_by_timestamp cannot choose between the two rows, so only file order decides (dedup_rule latest_revision_wins, raw_latest keep last). The published figures follow that declared rule and reproduce. But the duplicate_order_rule entry in human_decisions.yaml is justified by the claim that every revision is appended with a later updated_at, which is false for these six. No gate or auditor surfaced this. Resolving the tie the other way would move 10 of the 12 published values beyond tolerance: net revenue 3022518.62 instead of 3023296.61, completion direct 0.724235 instead of 0.724397, completion partner 0.604645 instead of 0.604746, and aov 110.63 and 87.26. A human should confirm that file order is the intended tie-break (evidence/redteam_recompute.json dedup.tie_cases and sensitivity_tie_break_first_row).
- The stage prompt asks the summary to say every context in this pipeline is one model. The execution blocks of the results in this stage's inputs show two models: openrouter/z-ai/glm-5.3-flash for gate0_semantic and the four workers, and claude-opus-5 for the four gate auditors and this red-team. The summary states the observed split instead of the templated sentence.
- The unpublished shipping_total of 37792722.50 is a faithful reading of the column in the declared locale, not a locale misread. Every in-population cell matched one of eight notations. Comma-decimal cells without a group run from 2.03 to 999.77, space- or U+00A0-grouped cells from 1000.23 to 1799.82, and plain and EUR-suffixed cells from 2.20 to 1799.99. Stripping every separator would have given 3779272250.00. The roughly 849 EUR per order that the release auditor asked the red-team to confirm is what the export itself says.
- release/report.md line 85 points the reader to the metric registry for the shipping total as a lower bound. No figure is shown, and the lower-bound statement holds: 2648 unreadable cells were zeroed and no parsed value is negative. Still, sending a reader to a figure the spec marks publish: never is wording worth tightening.
- Both completion-rate claims and their dashboard cards carry the quarter-wide population string 'orders placed inside the quarter, one row per order' rather than naming the channel. The card title, the n of 24597 or 19934 and the whole-channel denominator caveat beside the figure say which orders are counted, so the figure is not misread, but the population field alone is imprecise; gate_claims_auditor raised the same point.
- The worker_metrics carry and gate_metrics_auditor both state that the AOV bounds labelled student were computed with the normal quantile. With the Student t quantile at df 17817 (1.9600971) and df 12054 (1.9601608), all four bounds round to the published 2-decimal values, so the page is exact. The label is not literally the executed method, though, and the two would diverge for small groups.
- Neither surface says in words that the completion numerator is delivered orders, or that orders still pending at export count as not completed. The denominator caveat is present. Pending shares are flat by month (0.171212, 0.166565, 0.166858), and the last week of the quarter shows no build-up (0.153309), so a truncated tail does not distort the rate. No rule checks this wording.
- Where no deterministic rule in check_plan.json stands, only auditor judgement checks the work; each such place was verified here. (1) Ties between revisions with the same updated_at are covered by no rule (first warning). (2) truncated_period_policy stop_on_gap: ec-truncated-export maps to enum_values and population_matches, which cannot see a missing day; 90 of 90 days have orders, 426 to 581 per day. (3) date_format checks shape only; the month-first reading of slashed dates gives 0 mismatches over 2371 rows where day-first would differ, and 0 Z timestamps change date in Europe/Warsaw. (4) The renamed customer_id, country and order_date and the shipping_cost values have 0 mismatches over 44531 rows. (5) The report's 'n =' and '0.95 interval' labels are exempt from binding; all four equal the recount and the plan. (6) The R03 and R04 statistics reproduce and are unpublished. This is more than the machine gates cover but within what one final stage can carry.
- audit/tools is not among this stage's inputs, so the release gate's code was not inspected for slicing or magnitude filters; its output was checked instead. The digit runs on the comment-stripped report after the contract's three text exclusions, plus every digit-bearing dashboard leaf outside $.period, come to 36 numbers, and that is exactly the set release_surface_gate.json bound. release/ holds only the three declared surfaces, and no UNVERIFIED_CLAIM marker exists anywhere.
- audit/schemas/carry.schema.json is not among this stage's inputs, so the carries were checked against the fields the common contract names (step_id, context_id, attempt, updated_at, grain, periods, populations, pitfalls, do_not_reread, must_reread), not validated against the schema file. All four carries have those fields and no BOM, and each matches its result's context_id and attempt.
- Each worker carry lists its own audit/results/<step>/** evidence under do_not_reread, and the worker_analysis carry also lists audit/results/gate_claims_machine/**. That hides no contract, and the carries' facts agree with the recount, but the common contract meant that field for stage outputs and working data outside audit/**.
- The deviations workers reported in their own results change no number. worker_analysis ran a repo-wide content search that displayed matched lines from audit/.runner/state.json and from a superseded gate_claims_auditor result, both outside its inputs; it disclosed this isolation lapse and adopted nothing. worker_release used one-line python -c reads and shell redirects and self-ran gate_release_document, whose current result was read here and agrees with this recount. worker_metrics' attempt-1 fix and worker_clean's two notes are format-only. Every figure the workers produced reproduces from quarantine/orders.csv.
- analysis/answers/R03.json and R04.json record p_value 0.0. For R03 the two-sided p is on the order of 1e-156, which underflows in a 1 - cdf computation. Neither value is on a surface, so no published figure is affected, but either should read as below a bound if it is ever shown.
- audit/decisions/ holds no file, so the decision log reviewed was audit/human_decisions.yaml. Every RESOLVED entry that governs a number is applied in the registry and visible to the reader as a caveat or the period line: sale_status_basis, cancelled_order_policy, refund_sign_policy, shipping_fee_treatment, missing_amount_policy, period by order_month inclusive, and rounding once at display. The NOT_APPLICABLE entries fit an export with no test, tax, discount, promo or unknown-channel column.
- No instruction-like stem appears in the claim register, answers, metric registry, release surfaces, carries or any stage result among this stage's inputs. The manifest's top_tokens are twelve single tokens, not sentences. The quarantined column was not opened, and this result quotes no free text.
- The handoff's instructions field describes orchestrator commands (plan-spawn, record-spawn, register-context). They are launcher steps, not red-team work, and were not run.
- Reads and commands outside the forms this prompt names: (1) a grep over audit/results/gate0_machine/result.json, which the gate_*_machine input glob does not match; it showed the gate summary and its step_models_match_spec lines, and nothing in this verdict rests on it, since the model split above comes from execution blocks inside the inputs; (2) a wc -c size listing that included that file and the two data files; (3) a read of the dispatched prompt at audit/.runner/prompts/FINAL_CLAUDE_REDTEAM.md; (4) date -u for created_at; (5) four runs of python audit/results/final/evidence/redteam_recompute.py while fixing two bugs in that script; (6) python audit/results/final/evidence/validate_result.py, which checks this file's JSON shape and writes nothing. A compound cd-and-cat listing and two python -c one-liners were refused by the client before they ran. The only files written are the two scripts, the recompute's JSON output and this result.

## На каких определениях всё стоит

Прежде чем что-то считать, спорные вопросы были решены и записаны. Ниже — что решено, как и кем. Другое решение дало бы другие числа.

| Вопрос | Решено | Кем |
|---|---|---|
| dedup_rule | latest_revision_wins | latest_revision_wins |
| date_input_formats | iso_dotted_slashed_month_first_and_iso8601 | the slashed form is month-first |
| shipping_locale | space_thousands_comma_decimal | space thousands |
| refund_sign_policy | exclude_negative_refunds | a negative refund excludes the order |
| Что делать с колонками свободного текста (комментарии, адреса, заметки)? | quarantined_before_agents | решение подготовила модель, подписал Ilya |
| Какой статус заказа считается продажей в отчётном периоде? | delivered_only | решение подготовила модель, подписал Ilya |
| Как считать отменённые заказы? | excluded_and_counted | решение подготовила модель, подписал Ilya |
| Что такое одна строка популяции: заказ или строка заказа? | one_row_per_order | решение подготовила модель, подписал Ilya |
| Как считается частичный возврат? | amount_only | решение подготовила модель, подписал Ilya |
| К какому периоду относится возврат: к периоду заказа или к периоду возврата? | order_period | решение подготовила модель, подписал Ilya |
| Что входит в сумму возврата: только товар, или и доставка, и комиссии? | goods_only | решение подготовила модель, подписал Ilya |
| Какая дата определяет принадлежность заказа периоду? | order_date | решение подготовила модель, подписал Ilya |
| Границы периода включительные с обеих сторон или конец исключён? | inclusive_both_ends | решение подготовила модель, подписал Ilya |
| В каком часовом поясе читается дата события? | export_local_date | решение подготовила модель, подписал Ilya |
| Как читается строка заказа, у которой несколько версий в выгрузке? | latest_version_wins | решение подготовила модель, подписал Ilya |
| Что такое выручка в заголовке: до или после возвратов? | net_of_refunds | решение подготовила модель, подписал Ilya |
| Плата за доставку входит в выручку? | excluded_from_revenue | решение подготовила модель, подписал Ilya |
| В какой валюте и по какому курсу суммируются заказы в разных валютах? | single_currency_export | решение подготовила модель, подписал Ilya |
| Где округляются суммы: по строке или в итоге? | round_totals_only | решение подготовила модель, подписал Ilya |
| Что такое канал заказа? | sales_channel_column | решение подготовила модель, подписал Ilya |
| Что делать с повторяющимся идентификатором заказа? | keep_latest_by_timestamp | решение подготовила модель, подписал Ilya |
| Как поступать, если выгрузка не покрывает весь отчётный период? | stop_on_gap | решение подготовила модель, подписал Ilya |
| Как считать строки с пустой суммой? | missing_amount_excluded | решение подготовила модель, подписал Ilya |

Не относится к этому отчёту (со слов заказчика): EC-TEST-ORDERS — Ilya, 2026-09-16 (reasoned by Claude (claude-opus-5)) -- no test flag in the export; EC-GMV-IS-NOT-REVENUE — Ilya, 2026-09-16 (reasoned by Claude (claude-opus-5)) -- one first-party shop, no marketplace turnover; EC-REFUND-AFTER-PERIOD — Ilya, 2026-09-16 (reasoned by Claude (claude-opus-5)) -- a refund sits on its order's row with no date of its own; EC-PARTIAL-REFUND-COUNT — Ilya, 2026-09-16 (reasoned by Claude (claude-opus-5)) -- no refund count is published; EC-VAT-INCLUSIVE-PRICE — Ilya, 2026-09-16 (reasoned by Claude (claude-opus-5)) -- no tax column; EC-DISCOUNT-BEFORE-AFTER — Ilya, 2026-09-16 (reasoned by Claude (claude-opus-5)) -- no catalogue price in the export; EC-MIXED-CURRENCIES — Ilya, 2026-09-16 (reasoned by Claude (claude-opus-5)) -- one currency, EUR; EC-FX-RATE-DATE — Ilya, 2026-09-16 (reasoned by Claude (claude-opus-5)) -- nothing is converted; EC-ROUNDING-DRIFT — Ilya, 2026-09-16 (reasoned by Claude (claude-opus-5)) -- no breakdown is published as the parts of a total; EC-PROMO-ATTRIBUTION — Ilya, 2026-09-16 (reasoned by Claude (claude-opus-5)) -- no campaign figure is published

## Что никто не пересчитывал

Проверки сами записали, чего они не касались. На эти места ни одно правило не смотрело.

| Проверка | Что | Почему |
|---|---|---|
| gate_metrics_machine | completion_ci_low_direct | no check of this gate recomputes it from source |
| gate_metrics_machine | completion_ci_high_direct | no check of this gate recomputes it from source |
| gate_metrics_machine | aov_ci_low_direct | no check of this gate recomputes it from source |
| gate_metrics_machine | aov_ci_high_direct | no check of this gate recomputes it from source |
| gate_metrics_machine | completion_ci_low_partner | no check of this gate recomputes it from source |
| gate_metrics_machine | completion_ci_high_partner | no check of this gate recomputes it from source |
| gate_metrics_machine | aov_ci_low_partner | no check of this gate recomputes it from source |
| gate_metrics_machine | aov_ci_high_partner | no check of this gate recomputes it from source |

## Как проходила проверка

Шаг за шагом: кто выполнял (код, модель или человек), с какой попытки прошло и что стоило.

| Шаг | Кто | Попыток | Итог |
|---|---|---|---|
| profile_sources | код | 1 | пройдено |
| gate0_machine | код | 1 | пройдено |
| gate0_semantic | модель (openrouter/z-ai/glm-5.3-flash) | 2 | пройдено |
| worker_clean | модель (openrouter/z-ai/glm-5.3-flash) | 1 | пройдено |
| gate_clean_machine | код | 1 | пройдено |
| gate_clean_auditor | модель (claude-opus-5) | 1 | пройдено |
| worker_metrics | модель (openrouter/z-ai/glm-5.3-flash) | 2 | пройдено |
| gate_metrics_machine | код | 1 | пройдено |
| gate_metrics_auditor | модель (claude-opus-5) | 1 | пройдено |
| worker_analysis | модель (openrouter/z-ai/glm-5.3-flash) | 3 | пройдено |
| gate_claims_machine | код | 1 | пройдено |
| gate_claims_auditor | модель (claude-opus-5) | 1 | пройдено |
| worker_release | модель (openrouter/z-ai/glm-5.3-flash) | 2 | пройдено |
| gate_release_machine | код | 1 | пройдено |
| gate_release_auditor | модель (claude-opus-5) | 1 | пройдено |
| final_claude_redteam | модель (claude-opus-5) | 1 | пройдено |
| client_document | код | 1 | RUNNING |

Запусков моделей: 18; стоимость: $23.53; шагов: 17.

## Что осталось на машине

Данные читали модели: claude-opus-5, openrouter/z-ai/glm-5.3-flash. Каждое опубликованное число при этом пересчитано кодом без участия модели.

## Где искать подробности

Технические файлы проверки лежат рядом: реестр чисел `analysis/claim_register.json`, независимый пересчёт `audit/results/gate_claims_machine/evidence/independent_claim_recalc.json`, привязка напечатанных чисел `audit/results/gate_release_machine/evidence/release_surface_gate.json`, результат независимой проверки `final_claude_redteam`, журнал решений `audit/decisions`. Профиль claude-glm, ревизия e48d886bfa57d117a057de02afe315778e297dc8; замок контрактов 75159777ecaf.
