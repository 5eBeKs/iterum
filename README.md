# Iterum

*Every number in an analytical report, computed again.*

[Русская версия](README.ru.md)

Iterum checks an analytical report against the data it was written from. Every figure the
report prints is recomputed from the raw export by code that never saw how the report's author
computed it, and compared with what is printed. The words beside the figures -- what a number
counts, over which rows, with which caveats, what it is said to prove -- are read by independent
model reviewers. What was found is sealed: the reader receives a document saying what was checked
and what was found, and a receipt with the digest of every file, which anyone can check without
Iterum.

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
reviewers stop the other 24. **No defect in the zoo is stopped by nobody, and none is unmeasured.**
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
measures false alarms.

[`bench/METHOD.md`](bench/METHOD.md) has the method, [`bench/CASES.md`](bench/CASES.md) every
planted defect, [`bench/RESULTS.md`](bench/RESULTS.md) the tables, and `bench/results/` every
launch as it was recorded.

## What the reader receives

[`samples/`](samples/) holds what a finished run hands over, from a run over a synthetic demo
dataset with real model stages:

- **the client document** -- what was checked and what was found, in the reader's words: every
  number with its status, what the independent review said, which definitions were decided and by
  whom, what was not checked, and whether the export was reconciled with anything outside it;
- **the receipt** -- the SHA-256 of every file the client was given, one total over them, and the
  head of the run's hash-chained history, written outside the dataset at the moment of the seal.

## Checking a receipt yourself

A receipt proves that the files you hold are the files that were sealed. It does not prove the
checks were right; that is what the rest of this repository is for.

```bash
sha256sum report.md
```

On Windows, `Get-FileHash report.md -Algorithm SHA256`. The digest it prints is the one the receipt
lists beside that file, or the file is not the one that was sealed.

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
