# A quarter of a Shopify shop, step by step: from the export to a report the owner can stand behind

[Русская версия](CASE.ru.md)

The owner sends the orders export from the Shopify admin (Orders → Export) and asks how the quarter
went. This page follows that export through every step to the report, with the figures of each step,
and shows what the owner gets at the end:

- [**the report**](sample-deliverable.pdf), two pages: the figures, charts by month and channel, the top
  products; then the check and the open questions;
- [**the document**](client-document.pdf), six pages: every figure beside its recount and the definitions
  it rests on, the sealed file as the owner receives it;
- [**the workbook**](shopify-quarter.xlsx): the path from rows to sales, the 36 figures with their
  formulas, the checks by stage, the five questions and what each answer changes, the 38 rules.

The example is a Shopify export; the same report is made from any orders or sales export with dates,
amounts and statuses.

## Step 1. The export arrives

21,687 rows, one per line item, 9,659 orders of an EU outdoor shop in Q1 2026. It is synthetic, in the
real Shopify format, and messy the way a real one is: the owner downloaded the quarter in two parts
that overlapped for eleven days, so 1,068 orders are in it twice. Shopify's admin logs what it exported,
and all five of its totals agree with the file: rows, orders, first and last order date, sum. Nothing
was lost between the admin and the file.

## Step 2. The shape, before any method

Before anyone decides how to count, the export is described column by column and nothing else: 77
columns; an email missing on 700 rows; six payment methods, one of them Shopify's test gateway; eight
tags, among them `test`, `staff` and `wholesale`; three shipping prices. The notes column, 653 rows of
free text, is set aside unread by anything that computes. The method is chosen after this and before
any figure exists, so a figure cannot choose its own method.

## Step 3. The definitions, answered before counting

38 definitions, each one a choice the export cannot make. The ones that move this report's figures:

| Question | Answer |
|---|---|
| Which orders are sales? | Paid, partially refunded or refunded; not cancelled, not a test or staff order |
| Does revenue include VAT? | Yes, as the shop prints its prices |
| Is shipping revenue? | No |
| What is a refund? | The goods refunded; shipping refunds are not |
| Which date puts an order in a month? | Its creation, in the shop's time zone |
| Who is a returning customer? | Two or more orders inside the quarter, one address being one customer |
| What is an average order? | Net sales after refunds over orders |

For this demonstration the owner's delegate answered them, and the document records who did.

## Step 4. From rows to sales

| Step | Count |
|---|---:|
| Rows in the export | 21,687 |
| Orders | 9,659 |
| Created in the quarter | 9,159 |
| Cancelled | −260 |
| Test and staff orders | −84 |
| Not paid: pending or only authorised | −151 |
| **Sales in the quarter** | **8,664** |
| Their line items, for the product figures | 17,298 |
| Those with an email, for the customer figures | 8,346 |

## Step 5. The figures

On a fixed menu: net sales by month, orders and the average order, refunds and the refund rate, the
discount share, the top ten products, the repeat-customer rate, sales by channel. Including VAT,
excluding shipping, after discounts and refunds:

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

Top products: Fjord Rain Jacket (€254,356.47), Polar Down Jacket (€243,146.58), Trail Hiking Trousers
(€107,314.28) and seven more.

## Step 6. Every figure checked, in 926 checks

An AI pipeline drafts the analysis; nothing in it is taken on its word. **678 checks by code** hold the
contracts, the cleaning and every figure to the export: the cleaned tables against the raw rows, every
figure recomputed from them, every number on the page bound to its recomputation. **248 checks by
reviewers** read what code cannot: the definitions against the mandate, the figures' meanings and
caveats, the report as the owner will read it. In the end every one of the report's 36 figures was
recounted by separate code: **36 of 36 match.** The checks by stage are in the workbook.

## Step 7. What only the owner can answer

The final review returned five questions. Until they are answered, the figures stand on the rules of
step 3, and the report says so.

| Question | What the answer changes |
|---|---|
| Do the 87 wholesale orders with payment terms (€14,371.70) count as shop sales? | Whether net sales, the average order and the customer base show wholesale apart |
| Is a returning customer one who came back inside the quarter, or also since late December? | The rate: 23.37% inside the quarter, 23.94% with the three December days as history |
| Does the export always write an email one way? | Two spellings of one address count as two customers |
| **Does a partial refund ever include shipping?** | Refunds of €83,507.42 and net sales rest on it; the export cannot show it. An AI assistant in [the neighbouring case](../ai-report/CASE.md) decided it silently and added €505 to net sales |
| May the report call March provisional? | Refunds on late-March orders are still arriving |

## Step 8. The next month

The code that produced these figures is frozen after the review. It runs next month's export with no
model, every figure is checked the same way, and the questions answered this time are not asked again.

## What the client receives

The three documents at the top, and a receipt: fingerprints of the export, the report and the document
at the moment of the check. If anyone later changes a single figure in the document, its fingerprint
no longer matches; anyone can compare it with a standard command, without us.

---

*Files in this folder, for readers on GitHub.* `report.sealed.md` and `client_document.md` are the sealed
files byte for byte: their SHA-256 equal the ones in `receipt.md`, where the report is listed as
`release/report.md`; `client-document.pdf` is the document rendered without a change. The document was
written before two later fixes: it says "not yet sealed", and it is in Russian with the final review's
questions in English. `report-readable.md` is the report with the check's anchors taken out;
`sample-deliverable.pdf`, the covers, the gallery images and `shopify-quarter.xlsx` were laid out after the
seal from the sealed run and compute nothing. None of them is in the receipt.
