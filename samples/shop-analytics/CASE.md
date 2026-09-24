# A quarter of a Shopify shop, analysed and checked

[Русская версия](CASE.ru.md)

The owner sends the orders export from the Shopify admin (Orders → Export). They get a sales report
for the quarter in which every figure is recounted by separate code. With the report come the
questions their data cannot answer, asked instead of guessed.

## The export and the menu

The export is synthetic but in the real Shopify format: 21,687 rows and 9,659 orders of an EU
outdoor shop in Q1 2026. It carries duplicates from two pasted downloads, cancelled, test and staff
orders, VAT-inclusive prices and discount codes.

The report's menu is fixed in advance:
- net sales by month;
- orders and the average order value;
- refunds and the refund rate;
- the discount share;
- the top ten products;
- the repeat-customer rate;
- sales by channel.

Claude Opus 5.5 does the work. Each stage (cleaning, metrics, analysis, the report) is written by
one context and reviewed by another that starts fresh, and a final review reads the whole run. It
took 85 minutes.

## The result

**Headline figures** (including VAT, excluding shipping, after discounts and refunds; paid orders
only; cancelled, test and staff orders left out):

| | |
|---|---:|
| Net sales, Q1 | €1,474,891.63 |
| January / February / March | €528,930.40 / €458,841.03 / €487,120.20 |
| Orders | 8,664 |
| Average order value | €170.23 |
| Orders with a refund | 9.27% |
| Returning customers | 23.4% |
| Discount share | 2.73% |
| Online store / point of sale / draft orders | €1,324,502.73 / €99,157.00 / €51,231.90 |

Top products: Fjord Rain Jacket (€254,356.47), Polar Down Jacket (€243,146.58), Trail Hiking
Trousers (€107,314.28) and seven more.

**The check.** All 36 figures of the report were recounted from the export by independent code:
**36 of 36 match**. The export itself was reconciled to the Shopify admin's own record of what it
exported: rows, orders, first and last date, total. All five agree, so nothing went missing from
the file.

## Five questions for the owner

This is what a report a model writes on its own does not give: the final review returned five
questions only the owner can answer. Until they are answered, the figures stand on the rules written
down before counting.

1. The 87 wholesale orders with payment terms (€14,371.70) count as shop sales now. Report them
   separately?
2. Returning customers are counted inside the quarter. The export also holds the last three days of
   December. Counting them as history moves the rate from 23.37% to 23.94%.
3. Does the export always write customer emails in lower case? Two spellings of one address would
   count as two customers.
4. **Does a partial refund ever include shipping?** The export cannot show it, and refunds and net
   sales depend on the answer. The AI assistant in [the neighbouring case](../ai-report/CASE.md)
   decided it silently and added €505 to net sales.
5. May the report say March is provisional, since refunds on late-March orders are still arriving?

## What the client receives

- A two-page report: figures, charts by month and by channel and the top products on the first page;
  the check and the open questions on the second.
- A document that puts every figure beside its recount and the definitions it rests on.
- A receipt: fingerprints of the export, the report and the document at the moment of the check. If
  anyone later changes a single figure in the document, its fingerprint no longer matches, which
  shows the document is the one that was checked. Anyone can compare it with a standard command,
  without us.

**Next month.** The code that produced these figures is frozen after review. It runs next month's
export with no model, and every figure is checked the same way. That is faster and cheaper than the
first time.

---

*Files in this folder, for readers on GitHub:* `sample-deliverable.pdf` (the two-page report),
`report.md` (the run's machine report), `client_document.md` (the check document; written just
before the seal, so it still says "not yet sealed", and in Russian with the questions in English —
both to be fixed), `receipt.md` (the receipt), `cover.png` (the gig cover). The owner's definitions
were answered by a delegate for this demonstration, and the document records that.
