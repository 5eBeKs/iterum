# A fund factsheet whose top 10 does not reproduce from the fund's own holdings

[Русская версия](CASE.ru.md)

This one is not synthetic. Both documents are public and come from the same
issuer: the September 2026 factsheet of the iShares Core MSCI Europe UCITS ETF
EUR (Acc), ticker SMEA, and the fund's full holdings file, which iShares
publishes by date.

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

Ten of the eleven do not reproduce. Because the factsheet names two dates, the
same figures were then recounted from the holdings file of 3 September. They do
not reproduce from that one either.

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
| Top 10, total | 21.02 | 20.98 | 21.15 |

Weights in percent of the market value of every line of the file, as iShares
itself computes the file's weight column; that basis is one of the readings the
owner ruled before any counting. The 31 August column is the sealed check. The
3 September column is a direct recount from the second file, not a sealed run.

**What this does and does not say.** It does not say iShares made a mistake. It
says the printed weights cannot be recomputed from the issuer's own published
holdings on either date the factsheet names. They may rest on another basis or
another day the document does not name; the document does not say which.

**The holdings count.** The factsheet prints *Number of Holdings: 396*. The file
has 387 share lines on both dates, and 387 share lines plus 9 cash lines make 396
on both dates. Whether 396 is right depends on what counts as a holding. That was
the owner's ruling to make before the check, and it is printed in the document
with the owner's name: shares only, so the count cannot be confirmed.

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

```powershell
Get-FileHash verification_report.md -Algorithm SHA256
```

The digest must be `385ab7aed78017eb0ecf7c79dca4da8ff4710628caf6487ad0c51e879daa945a`,
the line for `deliverable/verification_report.md` in the receipt.
