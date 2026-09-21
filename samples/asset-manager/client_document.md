# Что проверено в отчёте и что найдено

*Документ для читателя отчёта. Ничего не считает сам: каждое число и каждый статус взяты из записей проверки.*

Все 106 числа отчёта воспроизводятся из выгрузки независимым пересчётом.

Правила проверки зафиксированы 2026-09-20 11:04 UTC; после этого их никто не менял.

Проверка ещё не запечатана: этот документ описывает её текущее состояние.

## Что это за документ

Отчёт был написан по выгрузке данных. Каждое его число пересчитано из той же выгрузки отдельным кодом, который не видел, как считал автор отчёта, и сравнено с тем, что напечатано. Проверялись числа и слова, стоящие рядом с ними; всё остальное, что отчёт говорит словами, здесь не проверялось.

## Главное

- raw_data/questions.md writes the valuation formula as quantity_traded times close_px times k and omits accrued interest; the spec and the report value bonds at dirty price and publish accrued_interest_eur_total 31662714.31 EUR inside the headline.
- asset_classes_count is 5 over every held position because MONEY_MARKET is held, but MONEY_MARKET is YIELD-only so the R03 asset-class AUM table has four valued classes and never names MONEY_MARKET.
- On this dump every held security's master version valid on 2026-06-26 has the same attributes as the current version, so the current-versus-valid-version trap is not distinguishable on held rows; price-versus-master currency mismatch is (116 positions, 36 securities, 1017776997.48 EUR).
- INDEX_POINTS has 0 held securities, so the contract_multiplier path of k was never exercised on a valued row; R04 reports that count as 0.
- 1800 of 2133 reporting-date positions have quantity_traded different from quantity_settled; the valuation used quantity_traded as specified.
- решение подготовила модель, подписал Ilya: worker_analysis rewords the yield caveat in analysis/claim_register.json so it names the threshold without a bare figure, for example 'some of these quotes are quoted above the yield threshold, a number outside the range of a yield; 28 positions', leaving every rendered figure claim-bound; the threshold itself stays declared in audit/audit_spec.yaml inside the metric id yield_quotes_above_100_positions_count.

## Числа отчёта

Расхождения и неподтверждённые числа стоят первыми. Допуск: денежные суммы ±0,01, доли ±0,000001, счётчики точно.

| Где в отчёте | Число | Что означает | Пересчёт из выгрузки | Статус |
|---|---|---|---|---|
| строка 49 | 31662714.31 | accrued interest eur total (SUM(accrued_eur) over valued positions) | 31662714.31 | совпадает |
| строка 48 | 5 | asset classes count (COUNT DISTINCT asset_class) | 5 | совпадает |
| строка 25 | 410085231.95 | aum base fnd001 (SUM(value_base) over valued positions of the fund) | 410085231.95 | совпадает |
| строка 26 | 1172182294.20 | aum base fnd002 (SUM(value_base) over valued positions of the fund) | 1172182294.20 | совпадает |
| строка 27 | 723163327.64 | aum base fnd003 (SUM(value_base) over valued positions of the fund) | 723163327.64 | совпадает |
| строка 28 | 674946337.62 | aum base fnd004 (SUM(value_base) over valued positions of the fund) | 674946337.62 | совпадает |
| строка 29 | 537945432.76 | aum base fnd005 (SUM(value_base) over valued positions of the fund) | 537945432.76 | совпадает |
| строка 30 | 921007265.63 | aum base fnd006 (SUM(value_base) over valued positions of the fund) | 921007265.63 | совпадает |
| строка 31 | 1015269075.37 | aum base fnd007 (SUM(value_base) over valued positions of the fund) | 1015269075.37 | совпадает |
| строка 32 | 705928493.73 | aum base fnd008 (SUM(value_base) over valued positions of the fund) | 705928493.73 | совпадает |
| строка 33 | 1134181465.13 | aum base fnd009 (SUM(value_base) over valued positions of the fund) | 1134181465.13 | совпадает |
| строка 34 | 889175886.28 | aum base fnd010 (SUM(value_base) over valued positions of the fund) | 889175886.28 | совпадает |
| строка 35 | 1230786090.45 | aum base fnd011 (SUM(value_base) over valued positions of the fund) | 1230786090.45 | совпадает |
| строка 36 | 833882134.07 | aum base fnd012 (SUM(value_base) over valued positions of the fund) | 833882134.07 | совпадает |
| строка 37 | 968699705.09 | aum base fnd013 (SUM(value_base) over valued positions of the fund) | 968699705.09 | совпадает |
| строка 38 | 1118790642.06 | aum base fnd014 (SUM(value_base) over valued positions of the fund) | 1118790642.06 | совпадает |
| строка 39 | 794107751.63 | aum base fnd015 (SUM(value_base) over valued positions of the fund) | 794107751.63 | совпадает |
| строка 85 | 977872021.74 | aum eur by asset class corp bond (SUM(value_eur) over valued positions grouped by asset_class) | 977872021.74 | совпадает |
| строка 86 | 10001058991.85 | aum eur by asset class equity (SUM(value_eur) over valued positions grouped by asset_class) | 10001058991.85 | совпадает |
| строка 87 | 2382161291.22 | aum eur by asset class etf (SUM(value_eur) over valued positions grouped by asset_class) | 2382161291.22 | совпадает |
| строка 88 | 190486778.22 | aum eur by asset class govt bond (SUM(value_eur) over valued positions grouped by asset_class) | 190486778.22 | совпадает |
| строка 112 | 384512665.19 | aum eur by country au (SUM(value_eur) over valued positions grouped by country_of_risk) | 384512665.19 | совпадает |
| строка 113 | 288548582.88 | aum eur by country bm (SUM(value_eur) over valued positions grouped by country_of_risk) | 288548582.88 | совпадает |
| строка 114 | 668950244.84 | aum eur by country ca (SUM(value_eur) over valued positions grouped by country_of_risk) | 668950244.84 | совпадает |
| строка 115 | 586592010.33 | aum eur by country ch (SUM(value_eur) over valued positions grouped by country_of_risk) | 586592010.33 | совпадает |
| строка 116 | 1035435020.53 | aum eur by country de (SUM(value_eur) over valued positions grouped by country_of_risk) | 1035435020.53 | совпадает |
| строка 117 | 333499034.92 | aum eur by country dk (SUM(value_eur) over valued positions grouped by country_of_risk) | 333499034.92 | совпадает |
| строка 118 | 158696930.05 | aum eur by country es (SUM(value_eur) over valued positions grouped by country_of_risk) | 158696930.05 | совпадает |
| строка 119 | 684899827.07 | aum eur by country fr (SUM(value_eur) over valued positions grouped by country_of_risk) | 684899827.07 | совпадает |
| строка 120 | 1146942374.06 | aum eur by country gb (SUM(value_eur) over valued positions grouped by country_of_risk) | 1146942374.06 | совпадает |
| строка 121 | 512498173.54 | aum eur by country hk (SUM(value_eur) over valued positions grouped by country_of_risk) | 512498173.54 | совпадает |
| строка 122 | 536078322.97 | aum eur by country ie (SUM(value_eur) over valued positions grouped by country_of_risk) | 536078322.97 | совпадает |
| строка 123 | 898651037.37 | aum eur by country it (SUM(value_eur) over valued positions grouped by country_of_risk) | 898651037.37 | совпадает |
| строка 124 | 870828103.41 | aum eur by country jp (SUM(value_eur) over valued positions grouped by country_of_risk) | 870828103.41 | совпадает |
| строка 125 | 619469091.33 | aum eur by country ky (SUM(value_eur) over valued positions grouped by country_of_risk) | 619469091.33 | совпадает |
| строка 126 | 312741250.19 | aum eur by country lu (SUM(value_eur) over valued positions grouped by country_of_risk) | 312741250.19 | совпадает |
| строка 127 | 487549328.79 | aum eur by country nl (SUM(value_eur) over valued positions grouped by country_of_risk) | 487549328.79 | совпадает |
| строка 128 | 101908732.23 | aum eur by country no (SUM(value_eur) over valued positions grouped by country_of_risk) | 101908732.23 | совпадает |
| строка 129 | 645869820.17 | aum eur by country se (SUM(value_eur) over valued positions grouped by country_of_risk) | 645869820.17 | совпадает |
| строка 130 | 107183628.67 | aum eur by country sg (SUM(value_eur) over valued positions grouped by country_of_risk) | 107183628.67 | совпадает |
| строка 131 | 3170724904.49 | aum eur by country us (SUM(value_eur) over valued positions grouped by country_of_risk) | 3170724904.49 | совпадает |
| строка 137 | 651027056.61 | aum eur by currency aud (SUM(value_eur) over valued positions grouped by px_currency) | 651027056.61 | совпадает |
| строка 138 | 414867706.33 | aum eur by currency cad (SUM(value_eur) over valued positions grouped by px_currency) | 414867706.33 | совпадает |
| строка 139 | 613578598.16 | aum eur by currency chf (SUM(value_eur) over valued positions grouped by px_currency) | 613578598.16 | совпадает |
| строка 140 | 61705999.82 | aum eur by currency dkk (SUM(value_eur) over valued positions grouped by px_currency) | 61705999.82 | совпадает |
| строка 141 | 3515472396.25 | aum eur by currency eur (SUM(value_eur) over valued positions grouped by px_currency) | 3515472396.25 | совпадает |
| строка 142 | 2403867835.80 | aum eur by currency gbp (SUM(value_eur) over valued positions grouped by px_currency) | 2403867835.80 | совпадает |
| строка 143 | 85105714.53 | aum eur by currency hkd (SUM(value_eur) over valued positions grouped by px_currency) | 85105714.53 | совпадает |
| строка 144 | 38134100.38 | aum eur by currency jpy (SUM(value_eur) over valued positions grouped by px_currency) | 38134100.38 | совпадает |
| строка 145 | 53684459.04 | aum eur by currency sek (SUM(value_eur) over valued positions grouped by px_currency) | 53684459.04 | совпадает |
| строка 146 | 5714135216.11 | aum eur by currency usd (SUM(value_eur) over valued positions grouped by px_currency) | 5714135216.11 | совпадает |
| строка 94 | 410650686.02 | aum eur by sector comm services (SUM(value_eur) over valued positions grouped by gics_sector) | 410650686.02 | совпадает |
| строка 95 | 2469541352.23 | aum eur by sector cons disc (SUM(value_eur) over valued positions grouped by gics_sector) | 2469541352.23 | совпадает |
| строка 96 | 810614711.08 | aum eur by sector cons staples (SUM(value_eur) over valued positions grouped by gics_sector) | 810614711.08 | совпадает |
| строка 97 | 377869179.35 | aum eur by sector energy (SUM(value_eur) over valued positions grouped by gics_sector) | 377869179.35 | совпадает |
| строка 98 | 2494209145.31 | aum eur by sector financials (SUM(value_eur) over valued positions grouped by gics_sector) | 2494209145.31 | совпадает |
| строка 99 | 1672141537.16 | aum eur by sector health care (SUM(value_eur) over valued positions grouped by gics_sector) | 1672141537.16 | совпадает |
| строка 100 | 1732300549.19 | aum eur by sector industrials (SUM(value_eur) over valued positions grouped by gics_sector) | 1732300549.19 | совпадает |
| строка 101 | 1766696523.73 | aum eur by sector info tech (SUM(value_eur) over valued positions grouped by gics_sector) | 1766696523.73 | совпадает |
| строка 102 | 454696687.19 | aum eur by sector materials (SUM(value_eur) over valued positions grouped by gics_sector) | 454696687.19 | совпадает |
| строка 103 | 340744212.18 | aum eur by sector real estate (SUM(value_eur) over valued positions grouped by gics_sector) | 340744212.18 | совпадает |
| строка 104 | 58756804.87 | aum eur by sector sovereign (SUM(value_eur) over valued positions grouped by gics_sector) | 58756804.87 | совпадает |
| строка 105 | 107580893.53 | aum eur by sector supranational (SUM(value_eur) over valued positions grouped by gics_sector) | 107580893.53 | совпадает |
| строка 106 | 855776801.17 | aum eur by sector utilities (SUM(value_eur) over valued positions grouped by gics_sector) | 855776801.17 | совпадает |
| строка 41 | 13551579083.03 | aum eur total (SUM(value_eur) over valued positions) | 13551579083.03 | совпадает |
| строка 167 | 129219100278.75 | aum eur total wrong k (SUM(value_eur_wrong_k) over valued positions) | 129219100278.75 | совпадает |
| строка 65 | 166 | closed fund positions count (COUNT(*) over the disclosed population) | 166 | совпадает |
| строка 65 | 166 | closed fund securities count (COUNT DISTINCT sec_id over the disclosed population) | 166 | совпадает |
| строка 65 | 0.077442 | closed fund value share of gross (SUM(abs_value_eur) of the population over SUM(abs_value_eur) of all valued positions) | 0.077442 | совпадает |
| строка 54 | 116 | currency mismatch positions count (COUNT(*) where currency_mismatch = 1) | 116 | совпадает |
| строка 53 | 36 | currency mismatch securities count (COUNT DISTINCT sec_id where currency_mismatch = 1) | 36 | совпадает |
| строка 55 | 1017776997.48 | currency mismatch value eur (SUM(value_eur) where currency_mismatch = 1) | 1017776997.48 | совпадает |
| строка 64 | 414 | delisted positions count (COUNT(*) over the disclosed population) | 414 | совпадает |
| строка 64 | 129 | delisted securities count (COUNT DISTINCT sec_id over the disclosed population) | 129 | совпадает |
| строка 64 | 0.227587 | delisted value share of gross (SUM(abs_value_eur) of the population over SUM(abs_value_eur) of all valued positions) | 0.227587 | совпадает |
| строка 62 | 87 | evaluated price positions count (COUNT(*) over the disclosed population) | 87 | совпадает |
| строка 62 | 29 | evaluated price securities count (COUNT DISTINCT sec_id over the disclosed population) | 29 | совпадает |
| строка 62 | 0.033617 | evaluated price value share of gross (SUM(abs_value_eur) of the population over SUM(abs_value_eur) of all valued positions) | 0.033617 | совпадает |
| строка 152 | 17241828519.92 | gross exposure eur (SUM(abs_value_eur) over valued positions) | 17241828519.92 | совпадает |
| строка 153 | 0.892986 | long share of gross (SUM(abs_value_eur) of longs over SUM(abs_value_eur)) | 0.892986 | совпадает |
| строка 150 | 15396703801.47 | long value eur (SUM(value_eur) where quantity_traded > 0) | 15396703801.47 | совпадает |
| строка 77 | 15600 | master securities count (COUNT(*) over clean_data/securities_universe.csv) | 15600 | совпадает |
| строка 43 | 2133 | positions count (COUNT(*)) | 2133 | совпадает |
| строка 78 | 845 | priced securities count (COUNT(*) where has_price_history = 1) | 845 | совпадает |
| строка 46, строка 79 | 669 | securities held count (COUNT DISTINCT sec_id) | 669 | совпадает |
| строка 159 | 0 | securities index points count (COUNT DISTINCT sec_id where quote_convention = INDEX_POINTS) | 0 | совпадает |
| строка 158 | 132 | securities percent of par count (COUNT DISTINCT sec_id where quote_convention = PERCENT_OF_PAR) | 132 | совпадает |
| строка 160 | 11 | securities yield count (COUNT DISTINCT sec_id where quote_convention = YIELD) | 11 | совпадает |
| строка 154 | 0.107014 | short share of gross (SUM(abs_value_eur) of shorts over SUM(abs_value_eur)) | 0.107014 | совпадает |
| строка 151 | -1845124718.45 | short value eur (SUM(value_eur) where quantity_traded < 0) | -1845124718.45 | совпадает |
| строка 69 | 40 | stale flag positions count (COUNT(*) where is_stale = 1, the vendor flag, cross-checked against the data) | 40 | совпадает |
| строка 61 | 42 | stale price positions count (COUNT(*) over the disclosed population) | 42 | совпадает |
| строка 61 | 14 | stale price securities count (COUNT DISTINCT sec_id over the disclosed population) | 14 | совпадает |
| строка 61 | 0.022719 | stale price value share of gross (SUM(abs_value_eur) of the population over SUM(abs_value_eur) of all valued positions) | 0.022719 | совпадает |
| строка 70 | 5 | stale unflagged positions count (COUNT(*) where close repeats previous_close_px and is_stale = 0) | 5 | совпадает |
| строка 63 | 377 | suspended positions count (COUNT(*) over the disclosed population) | 377 | совпадает |
| строка 63 | 121 | suspended securities count (COUNT DISTINCT sec_id over the disclosed population) | 121 | совпадает |
| строка 63 | 0.144414 | suspended value share of gross (SUM(abs_value_eur) of the population over SUM(abs_value_eur) of all valued positions) | 0.144414 | совпадает |
| строка 47 | 10 | valuation currencies count (COUNT DISTINCT px_currency) | 10 | совпадает |
| строка 163 | 0.000000 | value share index points (SUM(value_eur) of INDEX_POINTS over SUM(value_eur)) | 0.000000 | совпадает |
| строка 162 | 0.086216 | value share percent of par (SUM(value_eur) of PERCENT_OF_PAR over SUM(value_eur)) | 0.086216 | совпадает |
| строка 168 | 0.904169 | value share percent of par wrong k (SUM(value_eur_wrong_k) of PERCENT_OF_PAR over SUM(value_eur_wrong_k)) | 0.904169 | совпадает |
| строка 44 | 2094 | valued positions count (COUNT(*) where is_valued = 1) | 2094 | совпадает |
| строка 45 | 39 | yield positions count (COUNT(*) where is_valued = 0) | 39 | совпадает |
| строка 161 | 1968188.9500 | yield quantity total (SUM(quantity_traded) over YIELD positions) | 1968188.9500 | совпадает |
| строка 71, строка 182 | 28 | yield quotes above 100 positions count (COUNT(*) where is_valued = 0 and close_px > 100) | 28 | совпадает |

- совпадает — число отчёта воспроизводится из выгрузки в пределах допуска
- не совпадает — в отчёте напечатано не то, что посчитано
- расходится в пределах порога — пересчёт дал другое число, и разница меньше порога существенности, объявленного до начала проверки
- не подтверждено — два независимых пересчёта разошлись; число не названо ни верным, ни неверным
- не показано в отчёте — число посчитано и проверено, но в отчёт не попало

## Что заметила независимая проверка

Последний шаг — отдельная проверка всей работы с чистого листа (grok-4.6). Её вердикт: пройдено. Замечания ниже — её слова, приведены как есть.

### Замечания

- raw_data/questions.md writes the valuation formula as quantity_traded times close_px times k and omits accrued interest; the spec and the report value bonds at dirty price and publish accrued_interest_eur_total 31662714.31 EUR inside the headline.
- asset_classes_count is 5 over every held position because MONEY_MARKET is held, but MONEY_MARKET is YIELD-only so the R03 asset-class AUM table has four valued classes and never names MONEY_MARKET.
- On this dump every held security's master version valid on 2026-06-26 has the same attributes as the current version, so the current-versus-valid-version trap is not distinguishable on held rows; price-versus-master currency mismatch is (116 positions, 36 securities, 1017776997.48 EUR).
- INDEX_POINTS has 0 held securities, so the contract_multiplier path of k was never exercised on a valued row; R04 reports that count as 0.
- 1800 of 2133 reporting-date positions have quantity_traded different from quantity_settled; the valuation used quantity_traded as specified.
- 236 held positions have issuer country_of_incorporation different from country_of_risk; the R03 country split uses country_of_risk.
- 3 valued positions carry the vendor is_stale flag while close does not equal previous_close_px; the disclosed stale population is the 42 close-repeats, not the 40 flags, and 5 close-repeats are unflagged.
- closed_fund_positions_count 166 is over valued positions of FND006; 3 further closed-fund positions are YIELD and sit in the yield counts instead of that disclosure.
- card_caveat_requirements in audit/release_surface_contract.json is empty, so register caveats are reproduced in an appendix rather than on the same table as each figure.
- Several proportion claims carry a percent render role with scale 100; the report did not use that role, so shares remain six-digit proportions such as 0.892986.
- No securities_price_per_unit_count metric exists in the spec; 526 held securities are PRICE_PER_UNIT and R04 does not count them as their own figure because the question asked percent-of-par, index points and yield.
- aum_base_* groups are in mixed USD, EUR and GBP and are not added back to the EUR headline; the R01 fund table Assets column is in each fund's base currency and must not be summed across rows.
- Several RESOLVED items in audit/human_decisions.yaml were reasoned by Claude under Ilya's delegation (currency_distribution_basis, long_short_basis, wrong_multiplier_counterfactual, issuer_country_basis, securities_universes, bond_price_basis); the report states the chosen rules without naming a person, so it does not pass those readings off as a solo human decision.
- The frozen metrics plan does not run a deterministic rule on is_short versus quantity sign, dirty_px identity, or universe flag values against prices and holdings; those were rebuilt here from raw and matched.
- handoff.json has no drift_since_review; absence of that field does not prove the clean and metrics scripts' filters still fit a later dump.
- Retry history and stale inputs are not in this handoff; a person reads them from audit_runner.py report, and this stage does not claim to have checked them.
- GLM-lane execution.model cannot be verified from launcher output; only the GLM stages' own result.json names their model.

## Полна ли выгрузка

Выгрузку не с чем было сверить: внешних итогов не объявлено. Все числа выше верны для выгрузки в том виде, в каком её прислали; что в ней было всё, эта проверка не утверждает.

## На каких определениях всё стоит

Прежде чем что-то считать, спорные вопросы были решены и записаны. Ниже — что решено, как и кем. Другое решение дало бы другие числа.

| Вопрос | Решено | Кем |
|---|---|---|
| В какой валюте число из строки цены: в валюте самой строки цены или в валюте котировки из справочника? | price_row_currency | Ilya |
| Распределение по валютам — по валюте, в которой оценена позиция, по валюте котировки из справочника или по базовой валюте фонда? | price_row_currency | решение подготовила модель, подписал Ilya |
| Доли длинных и коротких позиций считаются от валовой экспозиции или от чистой стоимости? | gross_exposure | решение подготовила модель, подписал Ilya |
| wrong_multiplier_counterfactual | k_equals_1_for_every_convention | решение подготовила модель, подписал Ilya |
| Страна для концентрации — страна риска эмитента или страна его регистрации? | country_of_risk | решение подготовила модель, подписал Ilya |
| Как определены «вселенные» бумаг: весь справочник, бумаги с ценами и бумаги в позициях? | master_any_version__priced_on_any_date__held_on_reporting_date | решение подготовила модель, подписал Ilya |
| Позиция на дату — это количество по дате сделки или по дате расчётов? | quantity_traded | Ilya |
| Атрибуты инструмента — конвенция котировки, множитель, класс, эмитент, валюта — берутся из версии, действовавшей на дату оценки, или из текущей? | version_valid_on_reporting_date | Ilya |
| Каким курсом стоимость переводится в базовую валюту фонда и в валюту отчёта? | mid_rate_on_valuation_date | Ilya |
| Как оценивать инструменты, котируемые в доходности, а не в цене? | not_valued_reported_by_quantity | Ilya |
| Облигации оцениваются по чистой цене или по грязной, с накопленным купонным доходом? | dirty_price | решение подготовила модель, подписал Ilya |
| Главный итог «активы» — это чистая стоимость, где короткие позиции со знаком минус, валовая экспозиция или только длинные позиции? | net_of_shorts | Ilya |
| Что входит в итог активов: только позиции в бумагах, бумаги и деньги, или все чистые активы фонда? | securities_positions_only | Ilya |
| Что делать с позициями, цена которых на дату повторяет цену прошлого дня? | value_and_disclose | Ilya |
| Что делать с позициями, оценёнными модельной ценой, а не рыночной котировкой? | value_and_disclose | Ilya |
| Как оценивать бумаги, у которых на дату статус «приостановлена» или «исключена из листинга»? | last_price_and_disclose | Ilya |
| Включать ли фонды со статусом «закрыт», у которых на дату остаются позиции? | include_and_disclose | Ilya |
| Если у бумаги на дату есть цены из нескольких источников, какой из них главный? | as_selected_in_price_file | Ilya |

Не относится к этому отчёту (со слов заказчика): AM-FEEDER-DUPLICATION — 07_funds holds no MASTER fund and FND009's master_fund_id is empty, so the duplication cannot be measured or excluded inside this export; the certification's red team said so; AM-SPLIT-EX-DATE — the audit is a single-date snapshot; no series is compared across an ex-date; AM-CORPORATE-ACTION-STATUS — the export carries no corporate actions file; AM-HEADLINE-BASIS — Ilya, 2026-09-14 -- не относится к этому аудиту; AM-ACCRUED-INTEREST — bonds are valued at dirty prices here (bond_price_basis: dirty_price), so no total is a clean-price total; the accrued interest inside the headline is published as accrued_interest_eur_total; AM-NET-UNITS — Ilya, 2026-09-14 -- не относится к этому аудиту; AM-BREAKDOWN-ADDS-BACK — Ilya, 2026-09-14 -- не относится к этому аудиту; AM-DISPLAY-ROUNDING — Ilya, 2026-09-14 -- не относится к этому аудиту; AM-PRICE-SOURCE-SHARE — Ilya, 2026-09-14 -- не относится к этому аудиту

## Вопросы, возникшие по ходу проверки

| Вопрос | Ответ | Кем |
|---|---|---|
| two frozen rules demand contradictory renderings of the same caveat; release_surface_gate requires the visible threshold bound to a claim (none exists) or wrapped (no allowed reason id), caveats_rendered requires it verbatim with digits; worker_release can satisfy either one, never both | worker_analysis rewords the yield caveat in analysis/claim_register.json so it names the threshold without a bare figure, for example 'some of these quotes are quoted above the yield threshold, a number outside the range of a yield; 28 positions', leaving every rendered figure claim-bound; the threshold itself stays declared in audit/audit_spec.yaml inside the metric id yield_quotes_above_100_positions_count. | решение подготовила модель, подписал Ilya |

## Что никто не пересчитывал

Проверки сами записали, чего они не касались. На эти места ни одно правило не смотрело.

| Проверка | Что | Почему |
|---|---|---|
| gate_metrics_machine | fund_id | every group is recomputed, and no check adds the groups back to a total |

## Как проходила проверка

Шаг за шагом: кто выполнял (код, модель или человек), с какой попытки прошло и что стоило.

| Шаг | Кто | Попыток | Итог |
|---|---|---|---|
| profile_sources | код | 1 | пройдено |
| gate0_machine | код | 1 | пройдено |
| gate0_semantic | модель (openrouter/z-ai/glm-5.3-flash) | 1 | пройдено |
| worker_clean | модель (openrouter/z-ai/glm-5.3-flash) | 1 | пройдено |
| gate_clean_machine | код | 1 | пройдено |
| gate_clean_auditor | модель (grok-4.6) | 1 | пройдено |
| worker_metrics | модель (openrouter/z-ai/glm-5.3-flash) | 1 | пройдено |
| gate_metrics_machine | код | 1 | пройдено |
| gate_metrics_auditor | модель (Grok 4.6) | 1 | пройдено |
| worker_analysis | модель (openrouter/z-ai/glm-5.3-flash) | 3 | пройдено |
| gate_claims_machine | код | 1 | пройдено |
| gate_claims_auditor | модель (grok-4.6) | 1 | пройдено |
| worker_release | модель (openrouter/z-ai/glm-5.3-flash) | 2 | пройдено |
| gate_release_machine | код | 1 | пройдено |
| gate_release_auditor | модель (grok-4.6) | 1 | пройдено |
| final_grok_redteam | модель (grok-4.6) | 1 | пройдено |
| client_document | код | 1 | RUNNING |

Запусков моделей: 16; стоимость: $5.25; шагов: 17.

## Что осталось на машине

Данные читали модели: Grok 4.6, grok-4.6, openrouter/z-ai/glm-5.3-flash. Каждое опубликованное число при этом пересчитано кодом без участия модели.

## Где искать подробности

Технические файлы проверки лежат рядом: реестр чисел `analysis/claim_register.json`, независимый пересчёт `audit/results/gate_claims_machine/evidence/independent_claim_recalc.json`, привязка напечатанных чисел `audit/results/gate_release_machine/evidence/release_surface_gate.json`, результат независимой проверки `final_grok_redteam`, журнал решений `audit/decisions`. Профиль grok-glm, ревизия 61b99d35338d1d59ec1aacf62d3298ce981d74c2; замок контрактов 2e99c7a2f5a9.
