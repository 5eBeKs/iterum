# A full review: profiles that use a model

[Русская версия](llm.ru.md)

This order is for a new kind of export. A model writes the review and the
recount code, and a separate pass reads the result. The figures themselves
are recomputed by ordinary code.

The short check, once recount code for this kind of table already exists and
your answers match it, is on [The verify check](verify.md). A model does not
read the files there.

## When to buy this review

One item is enough.

- The tables are not one of the kinds sold on the verify page. An orders export from a shop system other than Shopify is this case: verify is not sold for it.
- The columns, the kind of row, or the name of a required column differ from
  a ready kind.
- You need a rule the ready code does not compute. For an asset manager's
  positions that is, for example, a different bond price, a different
  headline, or a different exchange rate.
- You want a written review, not only a status on each figure. Both examples
  in this folder are that kind of review.

The next period of the same kind, with the same columns and the same answers,
is not this order. After this order that is a verify check, 1–2 days.

## Who does the work

One profile, claude-build: Claude Opus 5.5 writes each stage, and separate
Claude contexts review it, each starting fresh. The recount in the document is
what speaks for the figures, not the fact that a model reviewed them.

On the same messy shop export, four Opus 5.5 runs published the same figures
to the last digit as the older Opus 5 runs, at a quarter to a fifth of their
cost.

Finished examples, made on profiles since retired; the checks are the same:

- [Online shop](ecommerce-messy/CASE.md). GLM wrote, Claude reviewed.
- [Asset manager](asset-manager/CASE.md). GLM wrote, Grok reviewed.

## What to send

Five things. The clock starts when all five are in. Not from the first chat
message.

1. **The export.** Excel or CSV. The first row of the table is the column
   names. One row is the same kind of thing all the way down: one order, one
   position, one ledger line. If there are several sheets, say which sheet
   belongs to which figure.
2. **A description of the columns.** The name, the unit, what a blank cell
   means. Without it the questions about the rules cannot be assembled, and
   I do not start.
3. **The report.** PDF, Word, or text, with the figures printed as text. I
   cannot recompute a number that exists only as a picture, a scan without a
   text layer, or a chart with no caption. If that is the case, I say so on
   the first day and do not start.
4. **Which figures to check.** Every figure on the pages you name, or a short
   list. Up to 20 figures takes the time in the table below. A longer list:
   I name the time from the files before starting.
5. **Written answers.** What counts as a sale or a value, what to do when the
   same row is repeated, which date to use, what is inside the total, which
   exchange rate. I send the questions after I have opened the files. You
   answer them. A call is not required.

In this order a model reads the files you send: the layout of the tables and
the values. Of the model vendors, only Anthropic sees them. The document you receive names the model of each stage. If that
is not acceptable, send a file of the same shape with the values replaced,
and say so before the start. An anonymized copy is enough to write the code.
It is not enough to check your real report: that check needs the real
figures, and it is a verify order once the code is ready.

## What you get back

A report from the export, a document for you, and checksums of the files you
received.

In the document each figure of the agreed list either stands next to an independent recount or
is named as not recomputed, with the reason:
whether it matched, both figures and the difference when it did not, and what
was missing when it could not be recomputed. Beside that, the rules fixed
before any counting, and who named them. A different answer to the same
question would have produced different figures. If two recounts disagreed,
the figure is not called right or wrong.

The document may end by refusing to call the report in agreement with the
export. That is a result of the order, not a missed delivery.

A checksum is a short string of the file's contents. On Windows:

```powershell
Get-FileHash file-name -Algorithm SHA256
```

If the string matches, the file was not changed after it was handed over. The
checksum does not say the figures are right.

A separate receipt listing the checksums comes with the
[asset-manager example](asset-manager/receipt.md). The
[shop example](ecommerce-messy/AUDIT_REPORT.md) has no receipt: that work
finished earlier, and its own end record does the same job. I do not write a
receipt after the fact.

The document answers whether the report reproduces from the file you sent,
under the rules you named. It does not say the file contained everything, and
it does not say which decision to take from it.

The recount code for this kind of export stays. The next period with the same
columns and the same answers is a verify check, with no model.

## How many days

| The order | Time |
|---|---|
| One new kind of tables, one report, up to 20 figures | 5 days |
| More than 20 figures, or several tables of a new kind | I name the time from the files before starting; usually 5–7 days |
| The same kind and the same answers next period | that is a [verify check](verify.md), 1–2 days |

If a file will not open, or the figures in the report are only pictures, that
is visible on the first day. I do not start counting in that case.

## What the order does not include

A dashboard, Power BI, fixing a marketplace cabinet, installing a pixel or
counters.
