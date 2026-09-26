# Online shop: what the client received

**Status: one question is open.** The final review asked the owner of the data to confirm which of
two same-time versions of an order counts, and nobody has confirmed it. The seal certifies the
figures under the rule recorded before counting. The run's own record lists nothing open, because
the review wrote this as a warning rather than a question. A ruling would mean a new run and a new
record, not an edit of this one.

[Русская версия](README.ru.md)

Short page for a proposal: [CASE.md](CASE.md).

Three files from one finished check. They were not edited after the check ended.

| File | What is in it |
|---|---|
| [report.md](report.md) | The report from the export: which figures it prints |
| [client_document.md](client_document.md) | The client document: every figure in the report next to an independent recount, whether they match, what else was found, which rules were fixed before any counting |
| [AUDIT_REPORT.md](AUDIT_REPORT.md) | A technical record of the end of the work: which steps passed, how long they took, checksums of the report |

The later asset-manager example has a separate receipt — a list of checksums
written outside the working folder at the moment the work is treated as
finished. This check ended on 16 September 2026, before that receipt existed.
`AUDIT_REPORT.md` stands in for it. A receipt of the later kind was not written
after the fact.

## Where the data came from

A synthetic shop export. There is no live client behind it. The file is built
the way clients send files:

- a byte-order mark at the start of the file, which can hide column names from
  a naive program;
- dates written as `2026-03-01`, as `01.03.2026`, and as `03/01/2026`;
- one order occupying several rows, one per status change;
- shipping written with a thousands space, a decimal comma, or a EUR suffix,
  and some cells blank or unreadable;
- a comment column of free text; that column was removed from the calculation
  before any automated check read the file.

Reporting period: 1 January to 31 March 2026, both ends included. 45,917 rows
in the file; 45,000 orders after keeping one row per order, 44,531 of them in the quarter once 10 with a negative refund are left out as an export fault. Six figures in the report, printed as fourteen numbers: four of the six are estimates and carry an interval. Each one is recomputed from the export, separately from however the
report's author computed it.

One model (GLM) wrote the report, another vendor's model (Claude) reviewed it.
The figures themselves are recounted by ordinary code, with no model in that
step. 18 model launches. Work ended
16 September 2026.

## What was found

**Six orders with the same update time and a different status.**
Ids: M006912, M008447, M015636, M016369, M035357, M037901. Each has two rows.
The update time is the same. On one row the order is cancelled or still waiting;
on the other it is delivered.

The rule was: take the version with the later time. Equal times leave the rule
with nothing to choose. The row that sits lower in the file wins. The report
is computed on that order, and a recount matches it.

By the final review's own count, taking the earlier row moves 10 published values beyond tolerance. Net revenue
(delivered orders, minus refunds, excluding shipping) falls from 3,023,296.61
to 3,022,518.62 euros. A person has to confirm that "lower row in the file" is what they meant when the times matched. Only the final review of the whole run noticed this; no machine check and no stage review did.

The six ties were not planted. The program that generated this file writes each
re-exported order one to five hours later, but never past 23:00, and copies the
minutes and seconds. An order last updated at 23 o'clock gets a copy with the
same time to the second. The program's own comment says the timestamp moves
forward, and the owner's ruling repeats it. We made the file ourselves and did
not know; the final review found it.

**Shipping is left off the report.** The column is written several ways, and
some cells cannot be read. Treating each unreadable cell as zero understates
the sum by an amount this file cannot bound. So the report does not print it.

## How to see that the file is the same one

On Windows:

```powershell
Get-FileHash report.md -Algorithm SHA256
```

The command computes a digest of the file. That is a short string of the whole
contents: change the file and the string changes. For this copy of the report
the digest is:

`2c73dbc26af176932724618ad7d036706778ed5a06244109f25aa203f7e01b03`

The same digest is recorded in `AUDIT_REPORT.md` for the report file. The
export is not here: it is synthetic, and a live job does not publish it.

The client document carries the line that the check is not sealed yet. The
document is written one step before the work is treated as finished. The record
of that finish is in `AUDIT_REPORT.md` beside it.
