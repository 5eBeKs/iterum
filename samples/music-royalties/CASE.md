# A band's royalties: was it paid right, and who is owed what

[Русская версия](CASE.ru.md)

A four-person project, a band of three and their producer, releases through a distributor, withdraws its
balance every month into a shared account, pays its manager and shares out the rest every quarter. After
six months the band asks two questions: were we paid everything the stores reported, and did each of us
get our share?

## What was compared

| File | What it is | Rows |
|---|---|---:|
| [`distributor_statement_2026H1.tsv`](distributor_statement_2026H1.tsv) | The distributor's detailed statement, January–June 2026 reporting dates: store, track, country, month of sale, streams, earnings in USD | 2,594 |
| [`band_account_2026H1.csv`](band_account_2026H1.csv) | The band's bank account: withdrawals with the original USD amount and the rate, the manager's commission, the quarterly payouts | 18 |
| [`split_sheet.csv`](split_sheet.csv) | Who owns what share of each track | 35 |
| [`reference_rates_usd_eur.csv`](reference_rates_usd_eur.csv) | A reference USD→EUR rate for every business day | 137 |

All four are synthetic. The statement is modelled on the detailed download of a distributor such as
DistroKid, one row per reporting date, store, track and country, with the month of the sale beside the
month it was reported; its columns are illustrative, because that distributor changed its layout in July
2025. The files were generated and then given, on purpose, the kinds of disagreement a real band's have.
The reconciliation code reads the files and nothing else. It was written by the same person
who planted the disagreements, so this case shows the method and what a client receives; it is not
a blind test.

## Rules agreed before counting

- **A store reports each month of sales once.** The same row under two reporting dates is a duplicate; a
  month missing between a store's first and last reported months is a gap.
- **Negative rows are the distributor's deductions**, and are listed rather than netted away.
- **Every dollar reported is withdrawn**, matched to the statement month by month.
- **The bank may convert up to 1.5% below the day's reference rate**; beyond that is a cost to raise.
- **The manager takes 15%** of each withdrawal as it arrives in euros.
- **Each quarter's payouts share out what arrived in that quarter after the 15%**, track by track by the
  split sheet: album tracks 30/30/30 with 10% to the producer, the single 34/33/33 among the three.

## Were we paid right

Every dollar the statement reports, $8,717.02, reached the account in five withdrawals; March was not
withdrawn, and April's withdrawal covers both months. Four things are not right:

| What | Where | Amount |
|---|---|---:|
| A month never reported | Apple Music, sales of February, every track | about $467 (average of January and March) |
| A month reported twice | Deezer, sales of February, in the April and again in the May statement | +$95.15 |
| Streams taken back as artificial | Spotify, *Summer Static*, sales of March, US and GB, in the June statement | −$191.52 |
| A conversion beyond the agreed margin | the withdrawal of 29 May, 3.1% below the reference rate | −€19.03 |

## Who is owed what

| Member | Owed for the half year | Paid | Difference |
|---|---:|---:|---:|
| Mara Keller | 2,073.84 | 1,989.58 | −84.26 |
| Jonas Brandt | 2,058.03 | 1,984.21 | −73.82 |
| Teo Vasić | 2,058.03 | 1,984.21 | −73.82 |
| Lena Ortiz, producer | 511.95 | 602.23 | +90.28 |
| **Together** | **6,701.85** | **6,560.23** | **−141.62** |

The first quarter was paid exactly as owed. Two things went wrong in the second:
- **The manager took 20% of the 30 April withdrawal**, €566.50 where the contract gives €424.87. The €141.63
  above it is exactly what the four are short together.
- **The single was shared out on the album's split.** The producer was paid 10% of *Summer Static*, a track
  she is not on, and the other three were paid 30% of it each instead of 34/33/33.

## From the stores to the members, EUR

| | EUR |
|---|---:|
| Withdrawn from the distributor, $8,717.03 converted | 7,884.53 |
| (at the day's reference rates it would have been €7,975.87; the bank kept €91.34, of which €19.03 beyond the agreed margin) | |
| Manager's commission, of which €141.63 above the contract | −1,324.31 |
| Paid to the four members | −6,560.23 |
| **Left in the account** | **−0.01** |

The cent is rounding in the payouts. Every line is a sum of rows of one of the files.

## What the band does next

- **Ask the distributor about Apple Music's February.** No track has a single February stream from Apple
  Music, where January and March have hundreds of dollars each.
- **Keep $95.15 aside.** Deezer's February was paid twice; a distributor usually takes such a double back.
- **Look at who promoted *Summer Static* in March.** Spotify took back 59,850 streams as artificial; the next
  time can mean the track is removed.
- **Ask the manager to return €141.63**, and the producer to return €90.28, and pay the three the rest of what
  they are owed: Mara €84.26, Jonas and Teo €73.82 each.
- **Ask the bank about 29 May.** Every other conversion was 0.8% below the reference rate; that one was 3.1%.

## What was planted, and what was found

Checked against the planted list: all six planted disagreements are in the
protocol, with the right store, month, track and amount, and so is the month nobody withdrew.

## What the client receives

- The protocol: what the statement and the account say, every disagreement with both values, and the
  table from the stores to each member.
- The member table, for sharing inside the band.
- For a band or a small label with a catalogue, the same check every quarter.

---

*Files in this folder, for readers on GitHub.* The four files are the ones reconciled, byte for byte. The
names, the tracks, the rates and the reference rates are invented; the reference rates are not any central
bank's.
