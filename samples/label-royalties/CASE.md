# A band's royalties and its label advance: paid right, recouped when, owed to whom

[Русская версия](CASE.ru.md)

A band of three and its producer. Their EP is out through one distributor, and the money comes straight
to the band. Their album came out under a label deal: the label paid a €15,000 advance, collects the
album's income from a second distributor, keeps half, and puts the band's half against the advance until
it is paid back. Only then does the band see album money. Eighteen months in, the band asks three
questions: **were we paid right, is the advance paid back yet, and who of us is owed what?**

## The answer

**The advance was paid back in the first quarter of 2026, not in the second, and the label owes the band
€2,410.15.** The label's statements got two things wrong:

- **In the second quarter of 2025 the label kept 55%** of the receipts where the contract says 50%. The band's
  share came out €410.15 short, and all of it went to the advance.
- **In the third quarter of 2025 it put an extra €2,000 back on the advance**, a line called "advance
  recoupment" on top of the band's share, which had already gone against it.

Without the two, the band's share covered the advance by 31 March 2026. €367.84 was due on 15 May and
nothing was paid; for the second quarter €2,708.60 was due and €666.29 was paid.

| Quarter | Receipts | Advance left, by the label | Advance left, by the recount | Payable, label | Payable, recount | Paid |
|---|---:|---:|---:|---:|---:|---:|
| 2025 Q1 | 0.00 | 15,000.00 | 15,000.00 | — | — | — |
| 2025 Q2 | 8,203.06 | 11,308.62 | 10,898.47 | — | — | — |
| 2025 Q3 | 8,722.93 | 8,947.16 | 6,537.01 | — | — | — |
| 2025 Q4 | 7,476.73 | 5,208.80 | 2,798.65 | — | — | — |
| 2026 Q1 | 6,332.99 | 2,042.31 | **0.00** | 0.00 | **367.84** | 0.00 |
| 2026 Q2 | 5,417.21 | 0.00 | 0.00 | 666.29 | **2,708.60** | 666.29 |

The gap between the two columns opens in the second quarter of 2025 and never closes, which is how an
advance stays unpaid on paper after it has been paid in fact.

## Were the distributors right

Every dollar the EP's distributor reported, $10,556.27, reached the band's account in eighteen monthly
withdrawals, €9,639.32. The label's receipts equal the album distributor's earnings in every quarter.
Four things are not right:

| What | Where | Amount |
|---|---|---:|
| A month reported twice | Album distributor: Deezer's July 2025 sales, reported again in October | +$150.35 |
| A month never reported | EP distributor: Apple Music's June 2025, every track | about $143 |
| A deduction larger than the month it names | EP distributor: Spotify, *Glass Coast*, November 2025: 38,400 streams in the US and 16,200 in the UK, where the month counted 5,555 and 3,810 | −$174.72 |
| A conversion beyond the agreed margin | the withdrawal of 30 September 2025, 3.4% below the reference rate | −€7.60 |

Deezer's double report is in the label's receipts, and so in the band's recoupment: the doubled receipts
paid the advance back sooner, and €68.48 of the €2,410.15 rests on them. A distributor usually takes a
double back, and when this one does, the label will deduct that €68.48 from a later statement.

The EP distributor's deduction takes more streams than the month it names counted in those countries,
and its statement gives no reason. A take-back of streams judged artificial can look like this, but only
the distributor can say what it is for and which months it covers.

## Who is owed what

The EP is shared 34/33/33 among the three; the album 30/30/30, with 10% to the producer. The label's debt is
shared the way the album is:

| Member | From the EP, received | From the album, received | Owed by the label |
|---|---:|---:|---:|
| Mara Keller | 3,277.37 | 199.89 | 723.05 |
| Jonas Brandt | 3,180.98 | 199.89 | 723.05 |
| Teo Vasić | 3,180.97 | 199.88 | 723.04 |
| Lena Ortiz, producer | — | 66.63 | 241.01 |
| **Together** | **9,639.32** | **666.29** | **2,410.15** |

Each column is split by the largest remainder, so the cents add up to the total the members share; a
cent left over goes to the member the split sheet names first.

## Why this is not a spreadsheet afternoon

Seven files in two currencies. The EP's statement has 2,570 rows, each one a store, a track, a country and two
months: the month it was sold and the month it was reported, three months apart for one store and two for
the others. The album's has 4,080 rows in another layout. The label's statement is one line a quarter, and it is
the only view of the advance the band ever gets. Checking it means rebuilding it: the distributor's rows posted
in the quarter, the contract's rate on the quarter's last business day, the 50%, and the advance carried from
quarter to quarter. One wrong line in 2025 moves every balance after it.

## Rules written down before counting

- A store reports each month of sales once: a repeat is a duplicate, a missing month a gap, a negative row a deduction.
- Every dollar the EP's distributor reports is withdrawn; a conversion within 1.5% of the day's reference rate is the bank's agreed margin.
- The label's receipts are the album distributor's earnings posted in the quarter, converted at the reference rate of the quarter's
  last business day less at most 1%; the label keeps 50%; the band's 50% goes to the advance until it is recouped, then is paid 45 days
  after the quarter ([`contract_terms.json`](contract_terms.json)).
- The members share each release by the [split sheet](split_sheet.csv).

## What the client receives

- [**The royalty document**](royalties-document.pdf) (3 pages): the answer, the advance quarter by quarter as a chart and a table,
  what the label's statements get wrong, the distributors' findings, a statement for each member, what to do, the rules and the
  files' fingerprints.
- [**The workbook**](royalties.xlsx): the timeline, the label's and the distributors' findings, every withdrawal against the reference
  rate, the members.
- For a band or a small label with a catalogue, the same recount every quarter, with the advance carried forward.

## What this case is, and is not

The band, the tracks, the rates, the reference rates and the contract are invented, and the disagreements were planted on purpose. The
distributors' column sets are modelled on DistroKid's and TuneCore's downloads and are illustrative. The code that reconciles reads only
the files, but it was written by the same person who planted the disagreements, so this case shows the method and what a client
receives; it is not a blind test. Every planted disagreement is in the protocol.

---

*Files in this folder, for readers on GitHub.* The seven source files are the ones reconciled, byte for byte: the EP distributor's
[statement](distributor_a_2025-01_2026-06.tsv), the album distributor's [report](distributor_b_album_2025-01_2026-06.csv), the label's
[statements](label_statements.csv), the band's [account](band_account.csv), the split sheet, the [reference rates](reference_rates_usd_eur.csv)
and the contract's terms. The document lists every file's SHA-256.
