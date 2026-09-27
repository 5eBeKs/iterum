# A fund factsheet whose top 10 does not reproduce from the fund's own holdings

[Русская версия](CASE.ru.md)

This one is not synthetic. Both documents are public and come from the same
issuer: the factsheet of the iShares Core MSCI Europe UCITS ETF EUR (Acc), ticker
SMEA, for August 2026, published in September, and the fund's full holdings
file, which iShares publishes by date.

The factsheet says of itself: *"Performance, Portfolio Breakdowns and Net Asset
information as at: 31-Aug-2026. All other data as at 03-Sep-2026."* The check
took the factsheet as the report and the holdings file of 31 August 2026 as the
data: 405 lines, 387 of them shares.

**No model read either file.** The code that reads this holdings file was written
and reviewed on an earlier run and frozen; this run executed it and compared.
Of the 52 figures on the list, 11 can be recomputed from a holdings file: the
ten largest positions' weights and their sum. The other 41 — returns, fees, net
assets, beta — cannot, and the document says why for each one.

## What turned up

Ten of the eleven do not reproduce at the precision the factsheet prints them.
Because the factsheet names two dates, the same figures were then recounted from
the holdings file of 3 September, and none of the eleven reproduces from that one.

**On the tolerance.** The sealed document prints ±0.01 beside each weight, but it
compares the weights at the printed precision, which is stricter. Held to ±0.01 of
the unrounded weights instead, nine of the eleven still differ: Banco Santander,
1.45 against 1.458, is the one more that would pass, and HSBC, Shell and
AstraZeneca are outside by 0.012 to 0.014 points.

| Position | Factsheet | Holdings, 31 Aug | Holdings, 3 Sep |
|---|---:|---:|---:|
| ASML HOLDING | 4.61 | 4.55 | 4.47 |
| HSBC HOLDINGS PLC | 2.46 | 2.47 | 2.53 |
| ROCHE PS PAR AG | 2.13 | **2.13** | 2.16 |
| NOVARTIS AG | 1.92 | 1.94 | 2.07 |
| SHELL PLC | 1.74 | 1.75 | 1.87 |
| NESTLE SA | 1.72 | 1.75 | 1.73 |
| SIEMENS N AG | 1.71 | 1.67 | 1.58 |
| ASTRAZENECA PLC | 1.69 | 1.70 | 1.73 |
| SAP | 1.59 | 1.56 | 1.52 |
| BANCO SANTANDER | 1.45 | 1.46 | 1.49 |
| Top 10, total | 21.02 | 20.98 | 21.13 |

The factsheet's total is the sum of its printed weights; the two file totals are sums of the
unrounded weights, which is why 21.13 is not the sum of the rounded column above it. Weights in
percent of the market value of every line of the file, as iShares
itself computes the file's weight column; that basis is one of the readings the
owner ruled before any counting. The 31 August column is the sealed check. The
3 September column is a direct recount from the second file, not a sealed run.

**What this does and does not say.** It does not say iShares made a mistake. It
says that from the issuer's own published holdings ten of the eleven printed
figures cannot be recomputed on 31 August and none on 3 September, the two dates
the factsheet names. They may rest on another basis or
another day the document does not name; the document does not say which.

**The holdings count.** The factsheet prints *Number of Holdings: 396*. The file
has 387 share lines on both dates, and 387 share lines plus 9 cash lines make 396
on both dates. The sealed document marks 396 *cannot be verified*, and the reason it gives is the date: the
factsheet counts holdings as at 3 September, and the check was over the 31 August file. Under the
owner's ruling a holding is a share line, and on either date that makes 387; 396 is reached only if
the 9 cash lines count as holdings too.

## The second date also moved the file

In the 3 September file the currency forwards come as several lines with the same
ticker and the same name — two or three per currency. The checks certified on the
31 August file take ticker plus name to identify a line, and on the new file they
stopped instead of pairing lines they could not tell apart. For a check repeated
every month that is the behaviour wanted: a file whose shape moved is refused, not
passed.

## Files

| File | What it is |
|---|---|
| [verification_report.md](verification_report.md) | the sealed document: every figure with its status, what could not be verified and why, the rulings made before counting |
| [receipt.md](receipt.md) | SHA-256 of the files the check covered, written outside the working folder at the seal |

The iShares files are not in this repository: they are the issuer's, not ours to
republish. The factsheet is at
[ishares.com](https://www.ishares.com/gls-download/literature/fact-sheet/smea-ishares-core-msci-europe-ucits-etf-eur-acc-fund-fact-sheet-en-gb.pdf)
(iShares replaces it every month); the holdings files are served by date, for
[31 August](https://www.ishares.com/varnish-api/uk-retail01-product-data/product-data/api/v1/get-fund-document?appType=PRODUCT_PAGE&appSubType=ISHARES&targetSite=ishares-uk&locale=en_GB&portfolioId=251861&userType=individual&asOfDate=20260831&component=holdings)
and
[3 September](https://www.ishares.com/varnish-api/uk-retail01-product-data/product-data/api/v1/get-fund-document?appType=PRODUCT_PAGE&appSubType=ISHARES&targetSite=ishares-uk&locale=en_GB&portfolioId=251861&userType=individual&asOfDate=20260903&component=holdings).
The receipt lists the digest of the 31 August file as it was checked, so a copy
downloaded today can be compared with it.

**The versions checked.** The factsheet link now serves a later month, so the
versions this case was checked against are named by their bytes:

| Document | As at | Downloaded | Bytes | SHA-256 |
|---|---|---|---:|---|
| Factsheet, `smea-ishares-core-msci-europe-ucits-etf-eur-acc-fund-fact-sheet-en-gb.pdf`, headed "August 2026" | 31 Aug 2026; other data 3 Sep 2026 | 21 Sep 2026 | 380,083 | `8d10940581f503a51db6a1b4382e0908131a227bea53ec66134e538647c8032c` |
| Holdings file, `SMEA_holdings.csv`, the sealed check's data | 31 Aug 2026 | 21 Sep 2026 | 60,265 | `1522469665017d604661a567440380356a687a045f2b0842f4ba8e6e05599819` |
| Holdings file, `SMEA_holdings.csv`, the direct recount | 3 Sep 2026 | by 23 Sep 2026 | 60,896 | `c6c999d5a2a6f2297251a5133e4d602bd12dd6d907a3efb70eb083af2dc6b63c` |

Copies of the three are kept with the case's working files; they are not republished here.

```powershell
Get-FileHash verification_report.md -Algorithm SHA256
```

The digest must be `385ab7aed78017eb0ecf7c79dca4da8ff4710628caf6487ad0c51e879daa945a`,
the line for `deliverable/verification_report.md` in the receipt.
