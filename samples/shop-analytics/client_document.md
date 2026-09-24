# Что проверено в отчёте и что найдено

*Документ для читателя отчёта. Ничего не считает сам: каждое число и каждый статус взяты из записей проверки.*

Все 36 числа отчёта воспроизводятся из выгрузки независимым пересчётом.

Правила проверки зафиксированы 2026-09-23 16:01 UTC; после этого их никто не менял.

Проверка ещё не запечатана: этот документ описывает её текущее состояние.

## Что это за документ

Отчёт был написан по выгрузке данных. Каждое его число пересчитано из той же выгрузки отдельным кодом, который не видел, как считал автор отчёта, и сравнено с тем, что напечатано. Проверялись числа и слова, стоящие рядом с ними; всё остальное, что отчёт говорит словами, здесь не проверялось.

## Главное

- Открытый вопрос: Should the 87 orders tagged 'wholesale' (draft orders with payment terms, 14371.70 EUR net) count as shop sales in net sales, AOV and the customer base, as they do now, or be reported separately?
- Открытый вопрос: The repeat-customer rate counts repeats within the quarter only (0.233675). The export also holds sale orders from 29 to 31 December 2025, and counting those as history would give 0.239382. Do you confirm the within-quarter reading, and may the caveat say that these three December days are held but not counted, rather than that no earlier history exists?
- Открытый вопрос: Does your Shopify export always write customer emails in lower case, with no leading or trailing spaces? The customer count and the repeat-customer rate treat two spellings of one address as two customers.
- Открытый вопрос: Do you confirm that in your shop a partial refund never includes shipping? The export cannot show this, and refunds of 83507.42 EUR and net sales rely on it.
- Открытый вопрос: May the report state the export date (2026-04-04) and say that March figures and the refund rate are provisional until later refunds on March orders are recorded?

## Числа отчёта

Расхождения и неподтверждённые числа стоят первыми. Допуск: денежные суммы ±0,01, доли ±0,000001, счётчики точно.

| Где в отчёте | Число | Что означает | Пересчёт из выгрузки | Статус |
|---|---|---|---|---|
| строка 13 | 170.23 | aov (net_sales_total / orders_count (ratio of sums, never a mean of means)) | 170.23 | совпадает |
| строка 15 | 0.027263 | discount share (discounts_total / gross_sales_total) | 0.027263 | совпадает |
| строка 10 | 43677.95 | discounts total (SUM(Discount Amount) over sale orders) | 43677.95 | совпадает |
| строка 9 | 1602077.00 | gross sales total | 1602077.00 | совпадает |
| строка 8 | 1474891.63 | net sales total | 1474891.63 | совпадает |
| строка 35 | 51231.90 | net sales source shopify draft order | 51231.90 | совпадает |
| строка 26 | 458841.03 | net sales 2026 02 (SUM(net_sales) over sale orders with order_month = 2026-02 (Created at in shop time)) | 458841.03 | совпадает |
| строка 25 | 528930.40 | net sales 2026 01 (SUM(net_sales) over sale orders with order_month = 2026-01 (Created at in shop time)) | 528930.40 | совпадает |
| строка 27 | 487120.20 | net sales 2026 03 (SUM(net_sales) over sale orders with order_month = 2026-03 (Created at in shop time)) | 487120.20 | совпадает |
| строка 34 | 99157.00 | net sales source pos (SUM(net_sales) over sale orders with Source = pos (where the order was placed)) | 99157.00 | совпадает |
| строка 33 | 1324502.73 | net sales source web (SUM(net_sales) over sale orders with Source = web (where the order was placed)) | 1324502.73 | совпадает |
| строка 12 | 8664 | orders count (COUNT(DISTINCT Name) over sale orders) | 8664 | совпадает |
| строка 47 | 85738.08 | product sales nlo-bag-day | 85738.08 | совпадает |
| строка 63 | 18945.53 | product sales nlo-bag-dry | 18945.53 | совпадает |
| строка 57 | 50398.45 | product sales nlo-bne-wool | 50398.45 | совпадает |
| строка 56 | 64127.53 | product sales nlo-bsl-leg | 64127.53 | совпадает |
| строка 45 | 99507.22 | product sales nlo-bsl-top | 99507.22 | совпадает |
| строка 62 | 34023.56 | product sales nlo-btl-steel | 34023.56 | совпадает |
| строка 64 | 15336.25 | product sales nlo-cap-sun | 15336.25 | совпадает |
| строка 44 | 104474.86 | product sales nlo-flc-mid | 104474.86 | совпадает |
| строка 65 | 0.00 | product sales nlo-gft-sticker | 0.00 | совпадает |
| строка 58 | 47488.18 | product sales nlo-glv-touch | 47488.18 | совпадает |
| строка 42 | 243146.58 | product sales nlo-jkt-down | 243146.58 | совпадает |
| строка 41 | 254356.47 | product sales nlo-jkt-rain | 254356.47 | совпадает |
| строка 61 | 35271.60 | product sales nlo-lmp-head | 35271.60 | совпадает |
| строка 60 | 38747.78 | product sales nlo-mat-air | 38747.78 | совпадает |
| строка 43 | 107314.28 | product sales nlo-pnt-hike | 107314.28 | совпадает |
| строка 49 | 74433.62 | product sales nlo-pnt-shell | 74433.62 | совпадает |
| строка 59 | 42716.43 | product sales nlo-pol-carb | 42716.43 | совпадает |
| строка 17 | 1558399.05 | product sales total | 1558399.05 | совпадает |
| строка 50 | 67465.31 | product sales nlo-sck-hike | 67465.31 | совпадает |
| строка 48 | 84666.39 | product sales nlo-slp-down | 84666.39 | совпадает |
| строка 46 | 90240.93 | product sales nlo-tnt-solo | 90240.93 | совпадает |
| строка 14 | 0.092682 | refund rate | 0.092682 | совпадает |
| строка 11 | 83507.42 | refunds total | 83507.42 | совпадает |
| строка 16 | 0.233675 | repeat customer rate | 0.233675 | совпадает |

- совпадает — число отчёта воспроизводится из выгрузки в пределах допуска
- не совпадает — в отчёте напечатано не то, что посчитано
- расходится в пределах порога — пересчёт дал другое число, и разница меньше порога существенности, объявленного до начала проверки
- не подтверждено — два независимых пересчёта разошлись; число не названо ни верным, ни неверным
- не показано в отчёте — число посчитано и проверено, но в отчёт не попало

## Открытые вопросы

Проверка их подняла, но решить может только владелец данных. Пока ответа нет, числа выше стоят на правилах, записанных до счёта; ответ означает новую проверку и новую печать.

- Should the 87 orders tagged 'wholesale' (draft orders with payment terms, 14371.70 EUR net) count as shop sales in net sales, AOV and the customer base, as they do now, or be reported separately?
- The repeat-customer rate counts repeats within the quarter only (0.233675). The export also holds sale orders from 29 to 31 December 2025, and counting those as history would give 0.239382. Do you confirm the within-quarter reading, and may the caveat say that these three December days are held but not counted, rather than that no earlier history exists?
- Does your Shopify export always write customer emails in lower case, with no leading or trailing spaces? The customer count and the repeat-customer rate treat two spellings of one address as two customers.
- Do you confirm that in your shop a partial refund never includes shipping? The export cannot show this, and refunds of 83507.42 EUR and net sales rely on it.
- May the report state the export date (2026-04-04) and say that March figures and the refund rate are provisional until later refunds on March orders are recorded?

## Что заметила независимая проверка

Последний шаг — отдельная проверка всей работы с чистого листа (claude-opus-5-5). Её вердикт: пройдено. Замечания ниже — её слова, приведены как есть.

### Замечания

- This run used one vendor. The architect, all four workers, the five auditors and this red team are all claude-opus-5-5 contexts. A mistake this model is prone to could repeat on both sides of every check, so the chain of PASS results is not independent review. Only the machine gates, the frozen check plan, the control lock and the release surface gate check the work independently of the model.
- Writes over raw_data and the frozen machinery were blocked by permissions.deny only for the edit tools, not for the shell. The control lock would have caught a changed raw file only after the fact, so such a write was detectable, not impossible.
- The repeat-customer caveat on report.md and the dashboard says earlier history is not in the export. In fact the export holds 237 sale orders from 2025-12-29 to 2025-12-31. Under the owner's within-quarter reading those orders are deliberately not counted. Counting them as history would move the rate from 0.233675 to 0.239382, because 34 customers with one quarter order also ordered in those three days.
- In report.md, line 4 says all money is after discount codes. The Gross sales line (1602077.00 EUR) and the Discount codes line (43677.95 EUR) are before discount codes. Each line's own caveat is correct, but the page-level sentence overstates.
- No surface states the export date (2026-04-04) that 'refunds as recorded on the export date' refers to, and no surface says March is provisional. In the data, 8.04% of sale orders from 15 March onward are refunded, against 9.55% of earlier orders. The March net sales of 487120.20 EUR and the refund rate of 0.092682 are therefore likely to change as late refunds arrive.
- The draft-order channel is labelled 'Draft orders entered by staff'. That label could be read as the shop's staff orders, which are excluded. The 283 draft sale orders are 196 orders tagged 'phone order' (36860.20 EUR) and 87 tagged 'wholesale' (14371.70 EUR). The 33 staff or test draft orders of the quarter are outside the population.
- The 87 wholesale draft orders all carry payment terms, and they count as ordinary sales in net sales, AOV and the customer base. Leaving them out would lower net sales by 14371.70 EUR and move AOV from 170.23 to 170.28 EUR. Only test and staff tags are internal under the owner's reading.
- Refunds (83507.42 EUR) are goods only. They are 1309.70 EUR below the sum of Refunded Amount, which is the shipping returned on fully refunded orders. A reader comparing with Shopify's own refund total will see that gap.
- Product sales (1558399.05 EUR) are before refunds, so they exceed net sales (1474891.63 EUR) by exactly the goods refunds. Each product line says so, but the product ranking is not a ranking of goods the customers kept.
- Several points are checked by no checklib rule: the top-ten ranking, the channel names in words, the wording of the repeat-rate history caveat, and the page-level sentences of report.md. The top ten and the order of all products match my ranking; the two wording faults above are what this review found in those places.
- Emails are hashed exactly as exported, and no rule checks case or spaces before hashing. The repeat-customer rate (1392 of 5957 customers) therefore relies on the export already writing emails in lower case. Under the pseudonyms I could not check this.
- Partial refunds are treated as goods only because the spec says so for this shop. The data only shows that none of the 439 partial refunds in the population exceeds its order's Subtotal, so a partial refund that included shipping could not be detected.
- The release generator src/release/build_release.py is not among my inputs. That no business-number literal is in it rests on the release surface gate's zero issues and on gate_release_auditor's reading, not on my own inspection.

## Полна ли выгрузка

Числа отчёта сверены с выгрузкой. Сама выгрузка сверена с итогами из других документов: если в ней не хватает месяца или региона, итог это покажет, а пересчёт — нет.

| Итог | Заявлено | В выгрузке | Статус | Откуда итог |
|---|---|---|---|---|
| последняя дата Created at | 2026-04-03 | 2026-04-03 | совпадает | the Shopify admin's record of the two exports it wrote (из собственной системы клиента: доказывает, что выгрузка — всё, что есть в этой системе, а не всё, что было) |
| строк | 21687 | 21687 | совпадает | the Shopify admin's record of the two exports it wrote (из собственной системы клиента: доказывает, что выгрузка — всё, что есть в этой системе, а не всё, что было) |
| разных Name | 9659 | 9659 | совпадает | the Shopify admin's record of the two exports it wrote (из собственной системы клиента: доказывает, что выгрузка — всё, что есть в этой системе, а не всё, что было) |
| первая дата Created at | 2025-12-29 | 2025-12-29 | совпадает | the Shopify admin's record of the two exports it wrote (из собственной системы клиента: доказывает, что выгрузка — всё, что есть в этой системе, а не всё, что было) |
| сумма Total | 1770193.90 | 1770193.90 | совпадает | the Shopify admin's record of the two exports it wrote (из собственной системы клиента: доказывает, что выгрузка — всё, что есть в этой системе, а не всё, что было) |

## На каких определениях всё стоит

Прежде чем что-то считать, спорные вопросы были решены и записаны. Ниже — что решено, как и кем. Другое решение дало бы другие числа.

| Вопрос | Решено | Кем |
|---|---|---|
| Какой статус заказа считается продажей в отчётном периоде? | paid_any_status | решение подготовила модель, подписал Ilya |
| Как считать отменённые заказы? | excluded_from_population | решение подготовила модель, подписал Ilya |
| Как распознаются и куда деваются тестовые и внутренние заказы? | excluded_by_flag | решение подготовила модель, подписал Ilya |
| Что такое одна строка популяции: заказ или строка заказа? | one_row_per_order | решение подготовила модель, подписал Ilya |
| На какой базе считается ставка возвратов? | order_rows | решение подготовила модель, подписал Ilya |
| Как считается частичный возврат? | counts_as_refunded_order | решение подготовила модель, подписал Ilya |
| К какому периоду относится возврат: к периоду заказа или к периоду возврата? | order_period | решение подготовила модель, подписал Ilya |
| Что входит в сумму возврата: только товар, или и доставка, и комиссии? | goods_only | решение подготовила модель, подписал Ilya |
| Какая дата определяет принадлежность заказа периоду? | order_date | решение подготовила модель, подписал Ilya |
| Границы периода включительные с обеих сторон или конец исключён? | inclusive_both_ends | решение подготовила модель, подписал Ilya |
| В каком часовом поясе читается дата события? | export_local_date | решение подготовила модель, подписал Ilya |
| Как читается строка заказа, у которой несколько версий в выгрузке? | no_revisions_expected | решение подготовила модель, подписал Ilya |
| Что такое выручка в заголовке: до или после возвратов? | net_of_refunds | решение подготовила модель, подписал Ilya |
| Суммы в выручке с НДС или без? | vat_inclusive | решение подготовила модель, подписал Ilya |
| Сумма заказа берётся до или после скидок и промокодов? | after_discounts | решение подготовила модель, подписал Ilya |
| Плата за доставку входит в выручку? | excluded_from_revenue | решение подготовила модель, подписал Ilya |
| В какой валюте и по какому курсу суммируются заказы в разных валютах? | single_currency_export | решение подготовила модель, подписал Ilya |
| Где округляются суммы: по строке или в итоге? | round_totals_only | решение подготовила модель, подписал Ilya |
| Что такое один клиент? | normalised_email | решение подготовила модель, подписал Ilya |
| Как считать заказы без аккаунта (гостевые)? | matched_by_email | решение подготовила модель, подписал Ilya |
| Кто такой платящий клиент в знаменателе ставок? | at_least_one_sale_in_population | решение подготовила модель, подписал Ilya |
| Что такое количество в строке: штуки, упаковки или вес? | units_as_exported | решение подготовила модель, подписал Ilya |
| Что означает отрицательное количество или отрицательная сумма в строке? | negative_rows_are_defects | решение подготовила модель, подписал Ilya |
| Как считать строки с нулевой суммой? | kept_in_counts | решение подготовила модель, подписал Ilya |
| Что такое канал заказа? | sales_channel_column | решение подготовила модель, подписал Ilya |
| Как заказ относится к промокампании? | not_attributed | решение подготовила модель, подписал Ilya |
| Что делать с повторяющимся идентификатором заказа? | rows_are_line_items | решение подготовила модель, подписал Ilya |
| Как поступать, если выгрузка не покрывает весь отчётный период? | stop_on_gap | решение подготовила модель, подписал Ilya |
| Как считать строки с пустой суммой? | missing_amount_is_defect | решение подготовила модель, подписал Ilya |
| Что делать с колонками свободного текста (комментарии, адреса, заметки)? | quarantined_before_agents | решение подготовила модель, подписал Ilya |
| product_sales_basis | after_discounts_before_refunds | решение подготовила модель, подписал Ilya |
| discount_share_basis | discounts_over_gross_sales | решение подготовила модель, подписал Ilya |
| repeat_customer_basis | repeat_within_period | решение подготовила модель, подписал Ilya |
| aov_basis | net_sales_per_order | решение подготовила модель, подписал Ilya |

Не относится к этому отчёту (со слов заказчика): EC-FX-RATE-DATE — Ilya, 2026-09-23 (reasoned by Claude (claude-opus-5-5, architect subagent) under Ilya delegation for test runs) -- one currency, nothing is converted; EC-GMV-IS-NOT-REVENUE — Ilya, 2026-09-23 (reasoned by Claude (claude-opus-5-5, architect subagent) under Ilya delegation for test runs) -- one first-party store, no marketplace turnover; EC-UNITS-MIXED — Ilya, 2026-09-23 (reasoned by Claude (claude-opus-5-5, architect subagent) under Ilya delegation for test runs) -- every product is sold by the piece; there is no unit column; EC-BUNDLE-DOUBLE-COUNT — Ilya, 2026-09-23 (reasoned by Claude (claude-opus-5-5, architect subagent) under Ilya delegation for test runs) -- the catalogue has no bundles; EC-PROMO-ATTRIBUTION — Ilya, 2026-09-23 (reasoned by Claude (claude-opus-5-5, architect subagent) under Ilya delegation for test runs) -- no campaign figure is published

## Как проходила проверка

Шаг за шагом: кто выполнял (код, модель или человек), с какой попытки прошло и что стоило.

| Шаг | Кто | Попыток | Итог |
|---|---|---|---|
| profile_sources | код | 1 | пройдено |
| gate0_machine | код | 1 | пройдено |
| gate0_semantic | модель (claude-opus-5-5) | 1 | пройдено |
| worker_clean | модель (claude-opus-5-5) | 1 | пройдено |
| gate_clean_machine | код | 1 | пройдено |
| gate_clean_auditor | модель (claude-opus-5-5) | 1 | пройдено |
| worker_metrics | модель (claude-opus-5-5) | 1 | пройдено |
| gate_metrics_machine | код | 1 | пройдено |
| gate_metrics_auditor | модель (claude-opus-5-5) | 1 | пройдено |
| worker_analysis | модель (claude-opus-5-5) | 3 | пройдено |
| gate_claims_machine | код | 1 | пройдено |
| gate_claims_auditor | модель (claude-opus-5-5) | 1 | пройдено |
| worker_release | модель (claude-opus-5-5) | 1 | пройдено |
| gate_release_machine | код | 1 | пройдено |
| gate_release_auditor | модель (claude-opus-5-5) | 1 | пройдено |
| final_claude_redteam | модель (claude-opus-5-5) | 1 | пройдено |
| client_document | код | 1 | RUNNING |

Запусков моделей: 16; стоимость: $31.70; шагов: 17.

## Что осталось на машине

Данные читали модели: claude-opus-5-5. Каждое опубликованное число при этом пересчитано кодом без участия модели.

## Где искать подробности

Технические файлы проверки лежат рядом: реестр чисел `analysis/claim_register.json`, независимый пересчёт `audit/results/gate_claims_machine/evidence/independent_claim_recalc.json`, привязка напечатанных чисел `audit/results/gate_release_machine/evidence/release_surface_gate.json`, результат независимой проверки `final_claude_redteam`, журнал решений `audit/decisions`. Профиль claude-build, ревизия 3c5bb00bca099b1424fe4b78df8e575e6ae9e873; замок контрактов 1b9e81a4621d.
