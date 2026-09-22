# The verify check

[Русская версия](verify.ru.md)

This order is only a repeat check. The recount code for your kind of tables
has already been written and reviewed. I run that code on a new export and a
new report. A language model does not read the files in this order.

A full review of a new export, where a model writes the text and the code, is
on [Profiles that use a model](llm.md). Both examples in this folder are that
kind of review, not the short check.


**Not for sale yet.** No verify check has reached a document on any kind so far. Kinds 1 and 2
have reviewed code and no finished verify run; the iShares kind stopped one step short of the
document. Each kind goes on sale after its first finished run.

## When you can buy this check

Every item below. If one of them fails, this is not the order: I say so on
the first day and do not start counting.

1. **The export is one of the two kinds below.** A different set of columns, a different kind of row, or a
   different name on a required column is not this order.
2. **Your written answers are the rules this code already computes.** A
   different answer to the same question is different code. That is the page
   about profiles that use a model.
3. **Every figure you want checked is printed as text.** A number that exists
   only as a picture, a scan without a text layer, or a chart with no caption
   cannot be recomputed.
4. **The report date and the export's as-of date are the same.** If they are
   not, the gap is explained in writing before the start.
5. **The list of figures is agreed before any counting.** The list does not
   grow inside the same order after that.

An orders export from a shop is not one of the two kinds. Verify is not
sold for it.

### Kind 1 and kind 2. An asset manager's positions on one date

Six tables: positions, a security master with version dates, prices, exchange
rates, issuers, funds. One position row is one security of one fund on one
date.

Both kinds count like this:

- the position quantity is the traded quantity;
- the security version is the one valid on the reporting date;
- the exchange rate is the mid rate on the valuation date;
- a security quoted as a yield stays out of the value and is reported as a
  quantity;
- the price currency is the currency on the price row;
- long and short positions both enter gross exposure;
- the issuer's country is the country of risk;
- the headline is net of short positions and covers securities only, not cash;
- a halted security is valued at its last price, and the document says so;
- a closed fund stays in the report, and the document says so;
- a stale price and a model price stay in the valuation, and the document
  says so;
- the price source is the one selected in the price file.

The two kinds differ by one rule. You name it before the start.

- Kind 1: a bond at the clean price, without accrued interest.
- Kind 2: a bond at the dirty price, with accrued interest.

### Coming later, not for sale yet

An iShares UCITS fund holding file. A verify check on it cannot be bought
until one run has reached a document.

## What to send

The clock starts when the conditions above hold and the files and answers are
in. Not from the first chat message.

1. **The export,** Excel or CSV. The first row of the table is the column
   names. If there are several sheets, say which sheet is which table.
2. **The report,** PDF, Word, or text, with the figures printed as text.
3. **Which figures to check.** Every figure on the pages you name, or a short
   list.
4. **Written answers.** After I open the files I send a short list of
   questions. You answer them. A call is not required. An answer the recorded
   rules do not already contain means verify cannot be bought.
5. **A column description,** if you have not sent one before: the name, the
   unit, what a blank cell means. On the first day that shows whether the
   file is one of the two kinds.

## What you get back

A short document, and checksums of the files you received. The document is in
the language of the report, Russian or English.

Each checked figure has one status:

| Status | What it means |
|---|---|
| совпадает | the export produces the same figure, within the stated tolerance |
| не совпадает | the export produces a different figure; the document prints both and the difference |
| не проверить | the files you sent do not contain what is needed to recompute it; the document says what is missing |
| не подтверждено | two recounts disagreed; the figure is not called right or wrong |

Beside that: the rules fixed before any counting, and who named them.

A checksum is a short string of the file's contents. On Windows:

```powershell
Get-FileHash file-name -Algorithm SHA256
```

If the string matches the one in the document, the file was not changed after
it was handed over. The checksum does not say the figures are right. That is
what the statuses above are for.

The document answers one question: does the report reproduce from the file
you sent, under the rules already recorded. It does not say the file
contained everything, and it does not say which decision to take from it.
This order does not include a written review like the
[shop example](ecommerce-messy/CASE.md) or the
[asset-manager example](asset-manager/CASE.md).

## How many days

| What happened | Time |
|---|---|
| The export is one of the kinds above, the answers match the recorded rules, the figures are text | 1–2 days |
| On the first day a file will not open, the figures are only pictures, the columns differ, or an answer differs | I do not start the check |

## What the order does not include

A dashboard, Power BI, fixing a marketplace cabinet, installing a pixel or
counters. A new kind of table, a renamed required column, or a new counting
rule is a [full review](llm.md). I name the price and the time for that after
seeing the files, and before starting.
