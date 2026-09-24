# A quarter of a Shopify shop, analysed and checked

[Русская версия](CASE.ru.md)

What a shop owner receives from the full analysis: the Shopify orders export in, a sales report
out, every figure of the report recomputed from the export by separate code, and the questions the
data could not answer, written to the owner instead of guessed.

**The export** is the same synthetic Shopify file as in [the AI-report case](../ai-report/CASE.md):
21,687 rows, 9,659 orders of an EU outdoor shop in Q1 2026, with the mess a real export carries.
**The menu** is fixed in advance:
- net sales by month;
- orders and the average order value;
- refunds and the refund rate;
- the discount share;
- the top ten products;
- the repeat-customer rate;
- sales by channel.

**The run** is one profile, claude-build on Claude Opus 5.5. Each stage (cleaning, metrics,
analysis, the report) is written by one context and reviewed by another that starts fresh, and a
final review reads the whole run. It took 85 minutes.

## What came out

- [**A two-page sample of what the owner receives**](sample-deliverable.pdf): the report as the owner reads it, with the checks and the open questions on the second page.
- [The report](report.md): 36 figures. Net sales are €1,474,891.63 over 8,664 orders, including
  VAT, excluding shipping, net of refunds, after discount codes. Each figure carries what it counts.
- [The document for the reader](client_document.md): all 36 figures recomputed from the export,
  **36 of 36 match**. The export itself is reconciled to the Shopify admin's own record of what it
  exported: rows, orders, first and last date, total. Every definition the figures rest on is listed
  beside who answered it.
- [The receipt](receipt.md): the SHA-256 of the export, the report and the document at the seal.

## The five questions

The part a report written by a model on its own does not give you: the final review returned five
questions only the owner can answer. The figures stand on the rules written before counting until
the owner answers.

1. The 87 wholesale orders with payment terms count as shop sales now (€14,371.70). Should they be
   reported separately?
2. The repeat-customer rate counts repeats inside the quarter. The export also holds three days of
   late December. Counting them as history moves the rate from 23.37% to 23.94%.
3. Does the export always write customer emails in lower case? Two spellings of one address would
   count as two customers.
4. **Does a partial refund in this shop ever include shipping?** The export cannot show it, and
   refunds and net sales rely on the answer.
5. May the report say that March is provisional, because refunds on late-March orders are still
   coming in?

Question 4 is the assumption that [the AI report](../ai-report/CASE.md) made silently, and that put
€505 into its net sales. Here it is asked.

## Notes on the files

- The document was written by the step before the seal and is sealed with the run: its digest is in
  the receipt. Its line "the check is not sealed yet" describes the moment it was written. It will
  say so plainly in the next version.
- The document is in Russian with the questions in English, because the run's documents were set to
  Russian and the final review wrote in English. A client's document comes in one language, the
  client's.
- The owner's definitions were answered by a delegate for this demonstration, and the document
  records that for every one.
