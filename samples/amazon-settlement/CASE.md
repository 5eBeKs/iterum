# Amazon sales against Amazon settlements, one month to the cent

[Русская версия](CASE.ru.md)

A seller on amazon.de shipped €73,646 of goods in March. The two March settlements paid €45,133 into
the bank. The seller asks what every Amazon seller asks: where did the other €28,513 go, and did
Amazon pay everything it owes?

## What was compared

| File | What it is | Rows |
|---|---|---:|
| [`all_orders_2026-03.txt`](all_orders_2026-03.txt) | Seller Central → Reports → Fulfillment → All Orders, March 2026 | 2,212 order lines |
| [`settlements_2026-03.txt`](settlements_2026-03.txt) | Seller Central → Payments → All Statements → Flat File V2, the settlements of 1–15 and 15–29 March | 6,021 transaction rows, 2 summary rows |
| [`catalogue.csv`](catalogue.csv) | The seller's own list of SKUs, their category and FBA fee | 10 products |

All three files are synthetic: a seller of home goods and phone accessories, fulfilled by Amazon, prices
including German VAT. The orders report and the settlement report follow the columns documented for
them, tab-separated as Seller Central writes them. The settlements were generated from the orders and
then given, on purpose, the kinds of disagreement a real seller's files have. The reconciliation code reads the files and nothing else. It was written by the same person
who planted the disagreements, so this case shows the method and what a client receives; it is not
a blind test.

## Rules agreed before counting

- **Key:** the order number and the SKU. The orders report has no key of its own for a row, and one
  order line can be split over several rows, so lines are summed by order and SKU first.
- **What should be paid:** every shipped line bought before 27 March. The second settlement closed on
  29 March, and two days is the shipping allowance agreed with the seller; later lines settle in April.
- **What must match:** the principal and the item price; the promotion and the report's discount; the
  commission and the rate card, 15% for home goods and 7% for electronics accessories on the price after
  promotions, never below €0.30; one FBA fee per unit at the catalogue's fee; a refund no larger than
  what was charged.

## Result

**1,869 of 1,873 settled lines match on every amount. Ten records do not:**

| What went wrong | Order | SKU | In the report | In the settlement | Difference |
|---|---|---|---:|---:|---:|
| Shipped, never paid | 302-2325519-1784447 | PW-BNK-10 | 34.90 | — | −34.90 |
| Shipped, never paid | 304-8652830-2994801 | KB-OAK-01 | 39.90 | — | −39.90 |
| Shipped, never paid | 304-8652830-2994801 | KB-OAK-02 | 24.90 | — | −24.90 |
| Paid less than the price | 302-8208660-2594574 | CB-USB-01 | 14.90 | 9.90 | −5.00 |
| Commission at 15%, rate card 7% | 305-1590219-6565686 | CB-USB-01 | 1.04 | 2.24 | −1.20 |
| Commission at 15%, rate card 7% | 302-1241663-9626194 | PW-BNK-10 | 2.44 | 5.24 | −2.80 |
| FBA fee charged twice | 305-9605719-8374807 | TM-CER-06 | 5.86 | 5.86 + 5.86 | −5.86 |
| Refund of two units, one was sold | 302-4861010-5346516 | LN-APR-01 | 29.90 | 59.80 | −29.90 |
| Cancelled, but charged | 304-8965748-2541815 | LN-TWL-02 | cancelled | 19.90 | +19.90 |
| Charge with no order in the report | 305-3570548-3024662 | PW-CHG-65 | — | 44.90 | +44.90 |

The first eight cost the seller €144.46, and each is a case to open with Seller Support with the order
number in hand. The last two brought money in that the orders report cannot account for: a customer
charged for a cancelled order, and a sale the report does not list.

**Refunds.** 58 refunds of March orders, and 38 refunds of February orders that the March report does
not carry, as it should be.

**Both settlements add up.** Each one's rows sum to the total its summary line prints: €20,482.04
deposited on 18 March and €24,650.90 on 1 April.

## From March sales to the bank

| | EUR |
|---|---:|
| Ordered in March, item prices | 78,206.90 |
| Cancelled | −3,368.30 |
| Not shipped by 31 March | −1,192.40 |
| **Shipped in March** | **73,646.20** |
| Shipped after 27 March, settles in April | −7,529.40 |
| Shipped, never paid | −99.70 |
| Paid less than the price | −5.00 |
| Cancelled, but charged | +19.90 |
| Charge with no order in the report | +44.90 |
| **Sales in the settlements** | **66,076.90** |
| Promotions | −341.19 |
| Commissions (of which €4.00 above the rate card) | −7,825.64 |
| FBA fees (of which €5.86 charged twice) | −7,554.77 |
| Refunds to customers: March orders | −2,091.62 |
| Refunds to customers: February orders | −1,234.20 |
| Commission returned on refunds | +417.74 |
| Refund administration fee | −83.71 |
| Storage fee | −61.37 |
| Subscription fee | −39.00 |
| Reimbursed for lost and damaged stock | +84.80 |
| Reserve: held on 29 March, less released on 15 March | −2,215.00 |
| **Deposited: 18 March and 1 April** | **45,132.94** |

Every line is a sum of rows of one of the files.

## What the seller learns

- **Amazon's fees take 23.3% of what it sells.** Commissions are 11.8% of sales and FBA fees 11.4%. A
  price has to carry both before it carries anything else.
- **€9,744 of March is money on its way, not money lost.** €7,529 of sales settles in April, and €2,215
  sits in Amazon's reserve until the next settlement releases it.
- **€144.46 is money Amazon owes the seller.** Three shipped lines never paid, one line paid €5 short,
  commission charged at the wrong rate on two lines, one FBA fee charged twice, and a refund of two units
  on an order of one.
- **Two records need a person.** A customer was charged for a cancelled order and should get the money
  back. A sale was paid with no order in the report: either the report was pulled before it arrived, or
  it is not this seller's.

## What was planted, and what was found

Checked against the planted list: all seven kinds of planted
disagreement are in the protocol, with the right orders, SKUs and amounts.

## What the client receives

- The protocol: every disagreement with both values, grouped by what went wrong, and the table from
  sales to the bank in which every line is recounted from the files.
- A claim list for Seller Support, one line per order.
- For a monthly client, the same check on every month's settlements.

---

*Files in this folder, for readers on GitHub.* The three files are the ones reconciled, byte for byte:
`all_orders_2026-03.txt` SHA-256 `4963f06c898cd1f89c1a52d394cd2f8177f2dfc1b9edac10ff567178b3570d78`,
`settlements_2026-03.txt` `e7e63379e6d2fe2fc149045348634468981a00fd5c22f66b66a0a447ad11e617`, `catalogue.csv`
`aef37136a32a4e7361e5eca988e8488ef20266231e324e60c2c6b8a2862c1336`. The column layouts were checked on
26 September 2026; the fees, the rate card and the reserve are illustrative, not Amazon's published rates.
