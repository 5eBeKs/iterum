# Platform assets on the reporting date 2026-06-26

One reporting day, one valuation of every position held on it. The population is the positions held on the reporting date; the headline is net of short positions and covers securities positions only. Every figure below is rendered from the frozen claim register, each anchored to its claim id, and every caveat registered for a claim is reproduced verbatim in the appendix at the end of this report.

## R01 Сколько активов у платформы на **D**: по каждому фонду в его базовой валюте и суммарно в EUR? Сколько позиций, в скольких бумагах, валютах и классах активов?

Assets of the platform on the reporting date: each fund in its base currency and the total in EUR, with position, security, currency and asset-class counts, the price-row/master quote-currency disagreement, the accrued interest inside the total and the five disclosed populations as counts and shares of gross exposure.

## R02 Как соотносятся три разных «вселенные»: сколько бумаг в справочнике, сколько имеют историю цен, сколько реально удерживается хотя бы одним фондом на **D**?

The three universes compared: securities in the instrument master, securities with a price history on any date, and securities actually held on the reporting date.

## R03 Как активы на **D** распределены по классам активов, секторам, странам риска эмитента и валютам котировки? Какая доля приходится на длинные и короткие позиции?

Distribution of the assets by asset class, GICS sector, country of risk of the issuer and quote currency of the price row, and the long/short split with shares of gross exposure.

## R04 Сколько бумаг на **D** котируются в процентах от номинала, в пунктах индекса и в доходности? Какую долю стоимости портфелей они образуют и что происходит с этой долей, если применить неверный множитель?

Securities quoted in percent of par, in index points and in yield. The value of yield-quoted positions is not determinable from the export, which carries no curve; their share of portfolio value is not computable, and that share is stated as such rather than omitted. They are reported by quantity. Each convention's share is a share of the value of the valued positions, and the counterfactual with the wrong multiplier (k = one for every convention, the price read as a price per unit) is shown next to the correct shares.

### R01 funds in base currency

| Fund | Base currency | Assets |
| --- | --- | --- |
| FND001 | USD | <!-- claim:CLM-AUM-BASE-FND001:value -->410085231.95 |
| FND002 | EUR | <!-- claim:CLM-AUM-BASE-FND002:value -->1172182294.20 |
| FND003 | USD | <!-- claim:CLM-AUM-BASE-FND003:value -->723163327.64 |
| FND004 | GBP | <!-- claim:CLM-AUM-BASE-FND004:value -->674946337.62 |
| FND005 | USD | <!-- claim:CLM-AUM-BASE-FND005:value -->537945432.76 |
| FND006 | EUR | <!-- claim:CLM-AUM-BASE-FND006:value -->921007265.63 |
| FND007 | USD | <!-- claim:CLM-AUM-BASE-FND007:value -->1015269075.37 |
| FND008 | USD | <!-- claim:CLM-AUM-BASE-FND008:value -->705928493.73 |
| FND009 | EUR | <!-- claim:CLM-AUM-BASE-FND009:value -->1134181465.13 |
| FND010 | USD | <!-- claim:CLM-AUM-BASE-FND010:value -->889175886.28 |
| FND011 | USD | <!-- claim:CLM-AUM-BASE-FND011:value -->1230786090.45 |
| FND012 | EUR | <!-- claim:CLM-AUM-BASE-FND012:value -->833882134.07 |
| FND013 | EUR | <!-- claim:CLM-AUM-BASE-FND013:value -->968699705.09 |
| FND014 | USD | <!-- claim:CLM-AUM-BASE-FND014:value -->1118790642.06 |
| FND015 | GBP | <!-- claim:CLM-AUM-BASE-FND015:value -->794107751.63 |

Platform total in EUR, net of shorts: <!-- claim:CLM-AUM-EUR-TOTAL:value -->13551579083.03 EUR.

- positions held: <!-- claim:CLM-POSITIONS-COUNT:value -->2133 count.
- of which valued: <!-- claim:CLM-VALUED-POSITIONS-COUNT:value -->2094 count.
- of which quoted in yield: <!-- claim:CLM-YIELD-POSITIONS-COUNT:value -->39 count.
- distinct securities held: <!-- claim:CLM-SECURITIES-HELD-COUNT:value -->669 count.
- valuation currencies of the price rows: <!-- claim:CLM-VALUATION-CURRENCIES-COUNT:value -->10 count.
- asset classes: <!-- claim:CLM-ASSET-CLASSES-COUNT:value -->5 count.
- accrued interest inside the total: <!-- claim:CLM-ACCRUED-INTEREST-EUR-TOTAL:value -->31662714.31 EUR.

The master version valid on the reporting date names a quote currency for each instrument; the price row valued carries its own. The disagreement is published, never resolved silently in either direction:

- securities whose master version on the date names another quote currency than the price row: <!-- claim:CLM-CURRENCY-MISMATCH-SECURITIES-COUNT:value -->36 count.
- positions in such securities: <!-- claim:CLM-CURRENCY-MISMATCH-POSITIONS-COUNT:value -->116 count.
- value carried in those positions: <!-- claim:CLM-CURRENCY-MISMATCH-VALUE-EUR:value -->1017776997.48 EUR.

### R01 disclosed populations, counts and shares of gross exposure

| Population | Positions | Securities | Share of gross exposure |
| --- | --- | --- | --- |
| stale price | <!-- claim:CLM-STALE-PRICE-POSITIONS-COUNT:value -->42 | <!-- claim:CLM-STALE-PRICE-SECURITIES-COUNT:value -->14 | <!-- claim:CLM-STALE-PRICE-VALUE-SHARE-OF-GROSS:value -->0.022719 |
| evaluated price | <!-- claim:CLM-EVALUATED-PRICE-POSITIONS-COUNT:value -->87 | <!-- claim:CLM-EVALUATED-PRICE-SECURITIES-COUNT:value -->29 | <!-- claim:CLM-EVALUATED-PRICE-VALUE-SHARE-OF-GROSS:value -->0.033617 |
| suspended instrument | <!-- claim:CLM-SUSPENDED-POSITIONS-COUNT:value -->377 | <!-- claim:CLM-SUSPENDED-SECURITIES-COUNT:value -->121 | <!-- claim:CLM-SUSPENDED-VALUE-SHARE-OF-GROSS:value -->0.144414 |
| delisted instrument | <!-- claim:CLM-DELISTED-POSITIONS-COUNT:value -->414 | <!-- claim:CLM-DELISTED-SECURITIES-COUNT:value -->129 | <!-- claim:CLM-DELISTED-VALUE-SHARE-OF-GROSS:value -->0.227587 |
| closed fund | <!-- claim:CLM-CLOSED-FUND-POSITIONS-COUNT:value -->166 | <!-- claim:CLM-CLOSED-FUND-SECURITIES-COUNT:value -->166 | <!-- claim:CLM-CLOSED-FUND-VALUE-SHARE-OF-GROSS:value -->0.077442 |

Cross-check of the vendor stale flag against the data's own reading:

- positions whose price row carries the vendor stale flag: <!-- claim:CLM-STALE-FLAG-POSITIONS-COUNT:value -->40 count.
- positions whose close repeats the previous quoted close while the vendor flag is unset: <!-- claim:CLM-STALE-UNFLAGGED-POSITIONS-COUNT:value -->5 count.
- yield-quoted positions whose close is above the yield threshold: <!-- claim:CLM-YIELD-QUOTES-ABOVE-100-POSITIONS-COUNT:value -->28 count.

### R02 the three universes of securities

| Universe | Securities |
| --- | --- |
| In the instrument master, any version | <!-- claim:CLM-MASTER-SECURITIES-COUNT:value -->15600 |
| With a price row on any date | <!-- claim:CLM-PRICED-SECURITIES-COUNT:value -->845 |
| Held on the reporting date | <!-- claim:CLM-SECURITIES-HELD-COUNT:value -->669 |

### R03 distribution by asset class

| Asset class | Assets, EUR |
| --- | --- |
| CORP BOND | <!-- claim:CLM-AUM-EUR-BY-ASSET-CLASS-CORP-BOND:value -->977872021.74 |
| EQUITY | <!-- claim:CLM-AUM-EUR-BY-ASSET-CLASS-EQUITY:value -->10001058991.85 |
| ETF | <!-- claim:CLM-AUM-EUR-BY-ASSET-CLASS-ETF:value -->2382161291.22 |
| GOVT BOND | <!-- claim:CLM-AUM-EUR-BY-ASSET-CLASS-GOVT-BOND:value -->190486778.22 |

### R03 distribution by GICS sector

| Sector | Assets, EUR |
| --- | --- |
| COMM SERVICES | <!-- claim:CLM-AUM-EUR-BY-SECTOR-COMM-SERVICES:value -->410650686.02 |
| CONS DISC | <!-- claim:CLM-AUM-EUR-BY-SECTOR-CONS-DISC:value -->2469541352.23 |
| CONS STAPLES | <!-- claim:CLM-AUM-EUR-BY-SECTOR-CONS-STAPLES:value -->810614711.08 |
| ENERGY | <!-- claim:CLM-AUM-EUR-BY-SECTOR-ENERGY:value -->377869179.35 |
| FINANCIALS | <!-- claim:CLM-AUM-EUR-BY-SECTOR-FINANCIALS:value -->2494209145.31 |
| HEALTH CARE | <!-- claim:CLM-AUM-EUR-BY-SECTOR-HEALTH-CARE:value -->1672141537.16 |
| INDUSTRIALS | <!-- claim:CLM-AUM-EUR-BY-SECTOR-INDUSTRIALS:value -->1732300549.19 |
| INFO TECH | <!-- claim:CLM-AUM-EUR-BY-SECTOR-INFO-TECH:value -->1766696523.73 |
| MATERIALS | <!-- claim:CLM-AUM-EUR-BY-SECTOR-MATERIALS:value -->454696687.19 |
| REAL ESTATE | <!-- claim:CLM-AUM-EUR-BY-SECTOR-REAL-ESTATE:value -->340744212.18 |
| SOVEREIGN | <!-- claim:CLM-AUM-EUR-BY-SECTOR-SOVEREIGN:value -->58756804.87 |
| SUPRANATIONAL | <!-- claim:CLM-AUM-EUR-BY-SECTOR-SUPRANATIONAL:value -->107580893.53 |
| UTILITIES | <!-- claim:CLM-AUM-EUR-BY-SECTOR-UTILITIES:value -->855776801.17 |

### R03 distribution by country of risk of the issuer

| Country of risk | Assets, EUR |
| --- | --- |
| AU | <!-- claim:CLM-AUM-EUR-BY-COUNTRY-AU:value -->384512665.19 |
| BM | <!-- claim:CLM-AUM-EUR-BY-COUNTRY-BM:value -->288548582.88 |
| CA | <!-- claim:CLM-AUM-EUR-BY-COUNTRY-CA:value -->668950244.84 |
| CH | <!-- claim:CLM-AUM-EUR-BY-COUNTRY-CH:value -->586592010.33 |
| DE | <!-- claim:CLM-AUM-EUR-BY-COUNTRY-DE:value -->1035435020.53 |
| DK | <!-- claim:CLM-AUM-EUR-BY-COUNTRY-DK:value -->333499034.92 |
| ES | <!-- claim:CLM-AUM-EUR-BY-COUNTRY-ES:value -->158696930.05 |
| FR | <!-- claim:CLM-AUM-EUR-BY-COUNTRY-FR:value -->684899827.07 |
| GB | <!-- claim:CLM-AUM-EUR-BY-COUNTRY-GB:value -->1146942374.06 |
| HK | <!-- claim:CLM-AUM-EUR-BY-COUNTRY-HK:value -->512498173.54 |
| IE | <!-- claim:CLM-AUM-EUR-BY-COUNTRY-IE:value -->536078322.97 |
| IT | <!-- claim:CLM-AUM-EUR-BY-COUNTRY-IT:value -->898651037.37 |
| JP | <!-- claim:CLM-AUM-EUR-BY-COUNTRY-JP:value -->870828103.41 |
| KY | <!-- claim:CLM-AUM-EUR-BY-COUNTRY-KY:value -->619469091.33 |
| LU | <!-- claim:CLM-AUM-EUR-BY-COUNTRY-LU:value -->312741250.19 |
| NL | <!-- claim:CLM-AUM-EUR-BY-COUNTRY-NL:value -->487549328.79 |
| NO | <!-- claim:CLM-AUM-EUR-BY-COUNTRY-NO:value -->101908732.23 |
| SE | <!-- claim:CLM-AUM-EUR-BY-COUNTRY-SE:value -->645869820.17 |
| SG | <!-- claim:CLM-AUM-EUR-BY-COUNTRY-SG:value -->107183628.67 |
| US | <!-- claim:CLM-AUM-EUR-BY-COUNTRY-US:value -->3170724904.49 |

### R03 distribution by quote currency of the price row

| Quote currency | Assets, EUR |
| --- | --- |
| AUD | <!-- claim:CLM-AUM-EUR-BY-CURRENCY-AUD:value -->651027056.61 |
| CAD | <!-- claim:CLM-AUM-EUR-BY-CURRENCY-CAD:value -->414867706.33 |
| CHF | <!-- claim:CLM-AUM-EUR-BY-CURRENCY-CHF:value -->613578598.16 |
| DKK | <!-- claim:CLM-AUM-EUR-BY-CURRENCY-DKK:value -->61705999.82 |
| EUR | <!-- claim:CLM-AUM-EUR-BY-CURRENCY-EUR:value -->3515472396.25 |
| GBP | <!-- claim:CLM-AUM-EUR-BY-CURRENCY-GBP:value -->2403867835.80 |
| HKD | <!-- claim:CLM-AUM-EUR-BY-CURRENCY-HKD:value -->85105714.53 |
| JPY | <!-- claim:CLM-AUM-EUR-BY-CURRENCY-JPY:value -->38134100.38 |
| SEK | <!-- claim:CLM-AUM-EUR-BY-CURRENCY-SEK:value -->53684459.04 |
| USD | <!-- claim:CLM-AUM-EUR-BY-CURRENCY-USD:value -->5714135216.11 |

### R03 long and short

- long value: <!-- claim:CLM-LONG-VALUE-EUR:value -->15396703801.47 EUR.
- short value, negative: <!-- claim:CLM-SHORT-VALUE-EUR:value -->-1845124718.45 EUR.
- gross exposure, long plus the absolute short: <!-- claim:CLM-GROSS-EXPOSURE-EUR:value -->17241828519.92 EUR.
- long share of gross: <!-- claim:CLM-LONG-SHARE-OF-GROSS:value -->0.892986 proportion.
- short share of gross: <!-- claim:CLM-SHORT-SHARE-OF-GROSS:value -->0.107014 proportion.

### R04 quote conventions and the wrong multiplier

- securities quoted in percent of par: <!-- claim:CLM-SECURITIES-PERCENT-OF-PAR-COUNT:value -->132 count.
- securities quoted in index points: <!-- claim:CLM-SECURITIES-INDEX-POINTS-COUNT:value -->0 count.
- securities quoted in yield: <!-- claim:CLM-SECURITIES-YIELD-COUNT:value -->11 count.
- quantity of the yield-quoted positions: <!-- claim:CLM-YIELD-QUANTITY-TOTAL:value -->1968188.9500 units.
- value share of percent-of-par: <!-- claim:CLM-VALUE-SHARE-PERCENT-OF-PAR:value -->0.086216 proportion.
- value share of index points: <!-- claim:CLM-VALUE-SHARE-INDEX-POINTS:value -->0.000000 proportion.

The counterfactual reads every price as a price per unit, the multiplier error the convention column exists to prevent. Under it the percent-of-par convention swallows almost the whole portfolio value:

- total under the wrong multiplier, every convention priced as a price per unit: <!-- claim:CLM-AUM-EUR-TOTAL-WRONG-K:value -->129219100278.75 EUR.
- percent-of-par value share under the wrong multiplier: <!-- claim:CLM-VALUE-SHARE-PERCENT-OF-PAR-WRONG-K:value -->0.904169 proportion.

## Appendix: claim caveats, as the register carries them

The caveats below are the register's own words for the claims above. Every number inside them is either the claim-bound figure it names or an excluded label; the yield threshold is a parameter of the spec, not a published figure, and the register itself names it in words rather than digits.

- All figures relate to the reporting date 2026-06-26.
- yield-quoted positions are not valued: the export carries no curve, so their value is not determinable and they are reported by quantity.
- bonds are valued at their dirty price, the close plus the accrued interest of the price row.
- each position is valued in its price row's currency; the master version valid on the date names a different quote currency for some securities, and the disagreement is published rather than resolved in either direction.
- stale-priced positions, whose close is carried forward from an earlier day, are included and disclosed with the share of value they carry.
- positions at evaluated prices are included and disclosed with the share of value they carry.
- positions in suspended or delisted instruments are included and disclosed with the share of value they carry.
- positions of a closed fund are included and disclosed with the share of value they carry.
- some of these quotes are quoted above the yield threshold, a number outside the range of a yield; <!-- claim:CLM-YIELD-QUOTES-ABOVE-100-POSITIONS-COUNT:value -->28 positions

Rendered by src/release/build_release.py from the frozen registries.

```
python src/release/build_release.py --project . --out-dir release
```
