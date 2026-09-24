# Iterum

*Every number of an analytical report, checked against the data it came from.*

[Русская версия](README.ru.md)

Iterum checks the figures of an analytical report against the data they came from, and hands
you a document that says, for every figure, whether it holds.

## What you can order

| You have | You get | Example |
|---|---|---|
| A report or a deck with figures, written by an analyst or by an AI, and the export it was written from | Every figure of the agreed list recomputed from the export: it matches; it does not, with both values and the difference; or it cannot be checked, and why. The definitions it rests on, and a sealed receipt | [An AI's sales report](samples/ai-report/CASE.md): 27 of 35 checkable figures right, 8 off through one hidden assumption. [A fund factsheet](samples/etf-smea/CASE.md): its top 10 does not reproduce from the issuer's own holdings |
| Two files that should agree: orders and payments, a ledger and a bank statement | Every difference with both values and its kind, and a bridge from one total to the other | [A reconciliation protocol](samples/reconciliation/PROTOCOL.md) |
| A Shopify orders export and a question: how did the quarter go? | A sales report on a fixed menu, every figure recomputed, and the questions only you can answer. Later months are checked by the frozen code, with no model | [A quarter of a Shopify shop](samples/shop-analytics/CASE.md): 36 of 36, and five questions for the owner |

Before any counting you answer a short written list of definitions: what counts as a sale, VAT,
shipping, which date. No calls. How to order: [the verify check](samples/verify.md) for an export of
a kind already covered, [the full analysis](samples/llm.md) for a new one.

## How the check works

Every figure the report prints is either recomputed from the raw export by code that never saw how
the report's author computed it and compared with what is printed, or named in the document as not
recomputed, with the reason -- the bounds of an estimate's interval, for one, are read by a
reviewer rather than recomputed. The words beside the figures -- what a number counts, over which
rows, with which caveats, what it is said to prove -- are read by independent model reviewers. What
was found is sealed: the reader receives a document saying what was checked and what was found, and
a receipt with the digest of every file, which anyone can check without Iterum.

This repository is the evidence: what the checks stop, what they miss, and what that costs. The
system itself is not published here. Tables and records name it by its working name, MAX v2.

## What is checked, and by what

Three layers, in the order a defect meets them.

| Layer | What it is | What it stops |
|---|---|---|
| **Machine gates** | Deterministic code, the same on every run, free | A figure that is not what the rows give; rows lost, altered or never sent; a number printed under no claim; a figure hard-coded instead of computed |
| **Stage auditors** | One model review per stage, over the stage's own output | A right number under a wrong name; a population or basis stated wrongly; a caveat lost or inverted; a trend or a cause no number measures |
| **Final red team** | One model review of the whole run, after every auditor passed | What an auditor let through |

Before anything runs, the definitions a gate cannot decide -- what counts as revenue, which rows
are in the population, how large a difference is immaterial -- are answered by a person and
recorded with their name. A gate recomputes the reading it is given; a wrong reading is caught by
asking, not by arithmetic.

## What each layer stops: the defect zoo

[`zoo/ZOO.md`](zoo/ZOO.md) puts every defect we know into one table: 38 mistakes planted into the
machine corpus and 30 planted for model reviewers, in eight classes named for what a client would
get wrong.

| Class | What the reader gets wrong | Stopped first by |
|---|---|---|
| figure | a number is not what the rows give | machine |
| composition | rows lost, altered or never sent | machine |
| provenance | where a number came from | machine |
| definition | right arithmetic under a reading nobody asked for | mostly reviewers |
| label | the right number under another figure's name | machine or reviewers |
| qualification | the limit on reading a figure lost or inverted | machine or reviewers |
| inference | words that say more than any number measured | reviewers |
| answer | a question of the brief not answered as asked | machine or reviewers |

Of 68 defects, the machine stops 42, two are recorded under a declared threshold, and the model
reviewers stop the other 24. **Among these 68, no defect is stopped by nobody, and none is unmeasured.** That is a statement
about this corpus, not about every mistake there is: the system's own adversarial probes still
record open scenarios, among them a person's ruling on one question that can excuse an unverified
number it says nothing about.
The one mistake the machine is known to miss -- a caveat dropped from the figure it belongs to,
on a page that repeats the same words elsewhere -- was shown to three vendors' reviewers, and every
launch stopped it ([`machine/GAPS.md`](machine/GAPS.md)).

The zoo also says what each vendor lets through when it reviews alone. Some defects are stopped
by one vendor every time and by another almost never; the zoo names them.

## How the reviewers compare: the bench

[`bench/`](bench/) measures the model reviewers one defect at a time. A demo dataset is driven to
a finished stage, one defect is planted into the stage's output, the machine gates are run again
to prove they are silent on it, and the stage's reviewer is launched once, for real, with the same
prompt and evidence as in a live run. Each launch is scored **blocked** (the reviewer refused the
stage and named the defect), **warned** (it named it and let it through) or **missed**, with what
the vendor charged beside it. A clean control -- the same review over the untouched stage --
measures false alarms, on the orders demo only: the messy demo's reference release has real defects
of its own that the reviewers shown it block, and [`bench/METHOD.md`](bench/METHOD.md) says which.

[`bench/METHOD.md`](bench/METHOD.md) has the method, [`bench/CASES.md`](bench/CASES.md) every
planted defect, [`bench/RESULTS.md`](bench/RESULTS.md) the tables, and `bench/results/` every
launch as it was recorded.

## What the reader receives

[`samples/`](samples/) holds two finished examples. Each one is a report, a
document for the client, and a way to see that the files were not changed after they were handed over -- for the shop, which ran before receipts existed, a checksum in the run's own record rather than a receipt.

- [Online shop](samples/ecommerce-messy/CASE.md) -- a quarterly order export,
  44,531 orders. Six orders have two versions with the same update time and a
  different status. The rule "keep the latest" cannot choose. Taking the other
  version drops net revenue from 3,023,296.61 to 3,022,518.62 euros.
- [Asset manager](samples/asset-manager/CASE.md) -- four years of prices and
  the positions of fifteen funds, 106 figures in the report. The price vendor
  flags stale prices: the flag sits on 40 positions, the prices themselves
  show 42.

The index of both examples is [`samples/README.md`](samples/README.md).
The short check of an export whose recount code already exists is in
[`samples/verify.md`](samples/verify.md). A full review of a new export, the
profiles that use a model, is in [`samples/llm.md`](samples/llm.md).

## Checking a receipt yourself

A receipt shows one thing: the files you hold are the files that were handed
over. It does not show that the checks were right: the recount in the document shows the arithmetic, and whether the mandate was read correctly is a person's ruling, recorded with a name.

```bash
sha256sum samples/asset-manager/report.md
```

On Windows, `Get-FileHash samples/asset-manager/report.md -Algorithm SHA256`.
The command prints a digest of the file — a short string of its contents. It
must match the line in the receipt next to the report. If the file was changed
after it was handed over, the strings differ. For the shop example the digest
is written on the case page.

## What Iterum does not claim

- **That a model reviewer is reliable because it is a model.** Each vendor is measured, and the
  bench publishes its misses.
- **That the mandate was read correctly.** Definitions are a person's rulings, recorded with a
  name; the document prints every one of them.
- **That a sealed record is true.** The receipt and the history chain prove nothing was changed
  after it was written, not that it was right when it was written.
- **That the export is complete**, unless it was reconciled with a total from outside it -- and
  the document says which.

There is no sampling: every row of the export is read, every published number recomputed.

## License

The text and the data in this repository are under [CC BY 4.0](LICENSE): quote them, recount
them, publish them further, and name Iterum as the source. The checking system is not in this
repository, and the license does not reach it.
