# How the reviewer bench works

[Русская версия](METHOD.ru.md)

## The question it answers

A machine gate recomputes every number and refuses a wrong one. What it cannot refuse is a right
number under a wrong word: a population called "all orders" over a delivered-only figure, a refund
rate called "low" at 47%, a 0.95 interval read as a 95% probability, a difference between two
channels explained by a cause nothing measured. Those are the defects a reviewer is there to
notice, and the bench plants them one at a time and shows each to each vendor's reviewer under the
same prompt, the same contract and the same evidence.

## Method

1. A demo dataset is driven to a finished stage with a scripted stand-in for the model workers. No
   model runs yet; every machine gate does.
2. That base is copied once per case, and the case's defect is planted into the stage's own output:
   the claim register, an answer to a question of the brief, the report page, the dashboard.
3. The stage's machine gates run again over the planted output. **A defect the machine gates catch
   never reaches a reviewer**: it belongs to the machine corpus, and the zoo credits it to the
   machine rather than to a model. Calibration proves, at a named revision, that every case the
   bench shows a reviewer is one the machine is silent on.
4. The reviewer is launched **once**, through the same launcher a live run uses -- same prompt, same
   evidence, same permission boundary -- and without the retry ladder a live run has. One launch,
   one result, one cost line as the vendor's own client reported it.
5. The result is scored against the case's signals: patterns over the reviewer's blocking issues,
   warnings and failed checks. **blocked** -- the reviewer refused the stage and named the defect;
   **warned** -- it named the defect and let the stage through; **missed** -- nothing it said names
   the defect. A refusal for an unrelated reason is not a catch.

## Three reviewers

| Stage | Reviewer | What it is shown |
|---|---|---|
| `claims` | the claims-stage auditor | the claim register, the answers to the brief, the metrics |
| `release` | the release-stage auditor | the report page and the dashboard |
| `final` | the final red team | the whole finished run, after its stage auditor passed the defect |

The `final` stage is the second line of defence. The defect is planted where its own stage plants
it, the machine gates run, and the stand-in plays every reviewer between that stage and the end, so
the red team meets exactly what a defect the auditor missed looks like.

## Two datasets

| Dataset | What it is | Cases |
|---|---|---|
| `orders` | 200 tidy synthetic orders, five published figures, four questions | 17 (10 claims, 7 release) |
| `messy` | 45 917 synthetic export rows resolved to 44 531 orders -- revisions, four date notations, a quarantined free-text column -- with estimates and their 0.95 intervals and two registered tests | 14 (8 claims, 6 release) |

Both are synthetic. Every case is listed in [`CASES.md`](CASES.md), with the class of defect it
belongs to.

## What is counted

Per launch: the verdict, the outcome, how many blocking issues and warnings the reviewer raised,
their texts, the cost the vendor reported and the wall time. A **clean control** runs the same
reviewer over the untouched stage: the blocking issues it raises there are **false blockers**, and
its warnings **false warnings**. **Other blockers** are blocking issues on a planted case that name
nothing of the defect -- a reviewer that refuses a stage for the planted defect and for three things
that are not wrong costs a live run three retries, and the catch alone would hide it.

**Only orders has a clean control.** The untouched messy stage is not clean: its reference release
carries defects no machine gate names -- one population line over the whole page ending in
"delivered only" above rates computed over every order, estimate cards without their `n`, average
order values without their caveats or currency -- and both vendors shown it, Claude and GLM, block
them there, launch after launch. A reviewer that blocks a real defect is right, so messy's clean blocks are not
counted as false alarms, and the same defects are most of messy's other blockers. Which of them are
false is not sorted until the reference is fixed; the tables print what was raised and call it that.

Every launch is kept as it was recorded, in [`results/`](results/), one file per launch: the case,
the vendor, the verdict, what the reviewer said and what it cost.

## What this is not

- **Not a benchmark of the writing.** The data, the code, the metrics and the report are the demo's
  own and identical for every vendor; only the reviewer changes.
- **Not a benchmark of the machine gates.** The machine corpus measures those; the zoo joins the two.
- **Not a leaderboard of models.** A profile is a vendor's command-line client at one effort level
  under one prompt, and the cost beside a row is what that arrangement charged on that day. Some
  clients report no price at all; the tables say "not reported" rather than zero.
