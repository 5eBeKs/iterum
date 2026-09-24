# Shopify sales against Shopify Payments payouts, one month to the cent

[Русская версия](CASE.ru.md)

A Shopify shop sold €529,976 of orders in March. Its Shopify Payments account paid out €244,365
for March. The owner asks the question every shop owner asks sooner or later: where did the
other €285,611 go, and is any of it money that should have arrived and did not?

## What was compared

| File | What it is | Rows |
|---|---|---:|
| Orders export | Shopify admin → Orders → Export, Q1 2026, the same EU outdoor shop as in [the neighbouring cases](../shop-analytics/CASE.md) | 21,687 rows, 9,659 orders |
| [`payout_transactions_2026-03.csv`](payout_transactions_2026-03.csv) | Shopify admin → Finance → Payouts → Export transactions, March 2026 | 1,599 transactions |

Both files are synthetic, in the real Shopify layouts. The payouts file was generated from the
orders export and then given, on purpose, the kinds of disagreement a real shop's files have.
The reconciliation read the two files and nothing else; the list of what had been planted was
opened only afterwards, to check the result.

## Rules agreed before counting

- **Which orders should have a card payment:** paid in March (by `Paid at`, shop time), status paid,
  partially refunded or refunded, payment method Shopify Payments. That is 1,444 orders.
- **Key:** the order number, `Name` in the orders export and `Order` in the transactions.
- **What must match:** the order total and the charge, to the cent; each refund recorded on the order
  and the refund transaction.
- **Test orders** (Shopify's test gateway, 18 orders) are left out of sales.

## Result

**1,439 of 1,444 card orders match their charge to the cent. Seven records do not:**

| What went wrong | Order | In Shopify | In the payouts | Difference |
|---|---|---:|---:|---:|
| Order paid, no charge | #8935 | 337.85 | — | −337.85 |
| Order paid, no charge | #10394 | 38.95 | — | −38.95 |
| Charged less than the order | #7596 | 42.95 | 30.45 | −12.50 |
| Charged less than the order | #8345 | 52.95 | 48.00 | −4.95 |
| Charged twice, second charge refunded | #7560 | 266.00 | 266.00 + 266.00 | +266.00, then −266.00 |
| Charge with no order in the export | #10662 | — | 129.00 | +129.00 |
| Charge with no order in the export | #10666 | — | 129.00 | +129.00 |

**Refunds.** 77 refunds of March orders match to the cent. One does not: on #9090 Shopify records
€99.00 refunded and the card refund was €103.95. The order had free shipping, so the €4.95 is not
a shipping fee, and neither file says what it was; it is a question for the owner. 73 refunds in
the file belong to orders paid in February, as they should.

**Also in the file:** a chargeback on #7795 (−€154.00 and a €15.00 fee) while the order still reads
*paid* in Shopify, and an adjustment of −€23.40 on 12 March with no order.

## From March sales to the payout

| | EUR |
|---|---:|
| Orders paid in March, all payment methods | 529,975.80 |
| Paid through PayPal | −128,380.60 |
| Paid through Klarna | −99,928.80 |
| Paid manually (bank transfer, invoice) | −18,150.35 |
| Paid in cash at the till | −15,710.00 |
| **Card orders (Shopify Payments)** | **267,806.05** |
| Orders paid, no charge | −376.80 |
| Charged less than the order | −17.45 |
| Charged twice | +266.00 |
| Charges with no order | +258.00 |
| **Charges in the payouts file** | **267,935.80** |
| Refunds: March orders, as recorded in Shopify | −9,934.50 |
| Refund larger than Shopify records (#9090) | −103.95 |
| Refunds: February orders | −8,464.41 |
| Refund of the second charge (#7560) | −266.00 |
| Chargeback | −154.00 |
| Adjustment | −23.40 |
| Card fees | −4,624.84 |
| **Net for March transactions** | **244,364.70** |
| of which paid out by 31 March | 228,421.57 |
| of which in transit, paid out in the first days of April | 15,943.13 |

Every line is a sum of rows of one of the two files.

## What the owner learns

- **Half of March never passes through this account.** €262,170 of €529,976 was paid by PayPal,
  Klarna, transfer and cash. Their money reaches the bank by other routes, each with its own file.
- **Cards cost 1.73% of what they charged.** American Express carried 6.1% of card sales and 10.8% of
  the fees: 3.0% on each Amex payment against 1.6% on Visa and Mastercard.
- **Eight orders need a person.** Two orders say paid with no money behind them (€376.80). Two were
  charged less than their total. Two charges have no order in the export. One customer was charged
  twice: the second charge was refunded, and its fee was not. One refund was €4.95 larger than
  the order says.
- **One dispute is not in the shop's books.** Order #7795 still reads paid, while the card network
  took back €154.00 and €15.00 more.

## Still open, and why

78 March orders carry a refund in Shopify (€7,501.54) with no refund transaction in March. Most of
them were almost certainly refunded in April. The orders export has no refund date, so this file
cannot tell an April refund from a refund made outside Shopify Payments, such as a gift card or a
cash refund at the till. The April transactions file closes the question for each order. Until
then they are listed, not guessed.

## What was planted, and what was found

Checked against the planted list after the protocol was written. Eight kinds of disagreement were
planted, and seven are in the protocol with the right orders and amounts. The eighth, a refund made
outside Shopify Payments, is among the 78 open refunds. From these two files alone it cannot be
told apart from an April refund.

## What the client receives

- The protocol: every disagreement with both values, grouped by what went wrong, and the table
  from sales to the payout in which every line is recounted from the files.
- A list of what needs a decision or another file, like the April refunds above.
- For a monthly client, the same check on every month's pair of files.

---

*Files in this folder, for readers on GitHub.* `payout_transactions_2026-03.csv` is the payouts file,
byte for byte (SHA-256 `36d1113a3df13b412067c5662c80a93f72ffd7ae80c284ead5ed230909023e3f`). The
orders export is not in this repository, for the same reason as in the neighbouring cases (SHA-256
`4655ea261d1446cdb828cbf2106dae16d141b625cdbf5ac543c048f57004881f`). The payouts file follows the
columns help.shopify.com lists for the transactions export, checked on 24 September 2026. Its
fees are illustrative, not Shopify's published rates.
