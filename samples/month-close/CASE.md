# Closing March across every channel: what was sold, what arrived, where the rest is

[Русская версия](CASE.ru.md)

A shop sells through its own Shopify store, where customers pay by card, PayPal, Klarna, bank transfer
or cash at the till; on amazon.de; and by invoice to a US wholesale customer through Stripe, in dollars.
At the end of March the owner asks the question every month-end comes down to: **how much did I
actually receive this month, and where is the rest of my money?**

## The answer

**Received from customers in March: €422,108.80 into the euro account and $32,753.08 into the dollar
account.** Sold in March: €561,258.10 across six euro channels, and $45,570.75 of invoices due in dollars.

| From what was sold to what reached the bank | EUR | USD |
|---|---:|---:|
| **Sold in March** | **561,258.10** | **45,570.75** |
| Refunds to customers | −30,175.80 | −600.00 |
| Fees | −17,274.48 | −1,210.83 |
| Paid out in March, booked in April | −42,234.27 | — |
| Not yet paid out on 31 March | −33,655.93 | — |
| Held by the providers | −7,938.33 | −7,126.84 |
| Missing: paid out, never booked by the bank | −9,341.59 | — |
| Not yet paid by the customer | — | −3,880.00 |
| Brought from February (PayPal) | +1,840.22 | — |
| Differences, promotions and other items | −369.12 | — |
| **Received in the bank in March** | **422,108.80** | **32,753.08** |

**€93,170.12 of the shop's money had not reached its account on 31 March.** Most of it is only late.
€42,234 was paid out on the last days of March and is booked in April. €33,656 had not been paid out
yet: Shopify Payments' payouts of 1 and 2 April, Amazon's settlement deposited on 1 April, Klarna's
captures of 30–31 March, Amazon's last shipments and the till's last two days. €7,938 is held by the
providers: Klarna's reserve, Amazon's reserve, the PayPal balance. And €9,341.59 is lost on the way:
Shopify's file says the payout of 18 March was paid, and the bank never booked it.

**Refunds still to go out.** The shop recorded refunds on 119 March orders paid by card, PayPal or
Klarna that no provider paid in March: €12,307.90. They leave in April, or were made another way, such as
a gift card or cash at the till. The orders export carries no refund date, so the close lists them rather
than guesses, and April's files settle each one.

**€33,132 that came into the account is not revenue**, and a close that counted it would overstate March
by exactly that: €10,000 moved from the savings account, €18,132 converted from the dollar account and a
€5,000 shareholder loan.

## What to do this week

From the 28 records that did not agree, the largest first:

1. **Ask Shopify for the trace of the payout of 18 March**, €9,341.59.
2. **Remind the US customer of invoice NO-US-2026-007**, $3,880.00, due 30 March.
3. **Ask Klarna why €2,000 was held back**, and until when, and claim the fee charged at 3.49% instead of
   2.99% for one week: €146.50.
4. **Refund two customers who paid twice**, by card and through PayPal: #9490, €745.00, and #9031, €47.95.
5. **Find order #8041**: paid by PayPal in the shop, €582.00, with no payment in PayPal.
6. **Ask Shopify support about two card orders marked paid with no charge**: #8935, €337.85, and #10394, €38.95.
7. **Ask the bank who sent €310.00 on 26 March** with no reference.
8. **Answer the chargeback on #7795**, €154.00 and a €15.00 fee, or record it on the order, which still reads paid.
9. **Open cases with Amazon Seller Support**: three lines shipped and never paid, one paid €5 short, a
   commission above the rate card, an FBA fee charged twice, a refund larger than the sale. And refund the
   Amazon customer charged for a cancelled order, and find the order behind the charge the report does not list.
10. **Find who refunded**: €45.00 in PayPal on order #9232, where the shop records no refund, and €4.95 by
    card on #9090 beyond what the order records. Ask Shopify what the adjustment of €23.40 on 12 March was for.
11. **Count the till for the week of 9 March**: the deposit is €40.00 short. And invoice the €15.00 a
    customer's bank took from a transfer.
12. **Collect or correct the two card charges short of their order**: #9838, €12.50, and #8345, €4.95.

The card channel's records are those of [the payouts case](../payouts-reconciliation/CASE.md), from the
same file, and the payout that never reached the bank is this close's own.

## Why this is not a spreadsheet afternoon

Eleven files, and no two write the same thing the same way:

| File | Rows | What makes it hard |
|---|---:|---|
| Shopify orders export | 21,687 | one row per line item, two overlapping downloads, 2,882 orders paid in March |
| Shopify Payments transactions | 1,599 | charges, refunds, a chargeback, payouts by day |
| [PayPal activity](paypal_activity_2026-03.csv) | 753 | dates day/month/year, the order number without its `#` |
| [Klarna settlements](klarna_settlements_2026-03.csv) | 1,660 | a sale is three rows, keyed by a UUID; the shop's number is a reference |
| [Amazon All Orders](amazon_all_orders_2026-03.txt) and [settlements](amazon_settlements_2026-03.txt) | 1,034 + 2,805 | tab-separated, one row per amount type, fees negative, a reserve carried between settlements |
| [Amazon catalogue](amazon_catalogue.csv) | 8 | the rate card by category |
| [Stripe balance](stripe_balance_2026-03.csv) and [invoice register](invoice_register_2026-03.csv) | 9 + 7 | dollars, a refund, an unpaid invoice |
| [Bank, euro account](bank_eur_2026-03.csv) | 143 | semicolons, decimal commas, dd.mm.yyyy, one line per payout and none per order |
| [Bank, dollar account](bank_usd_2026-03.csv) | 3 | two payouts and one conversion |

One order shows it. **#7490**, €195.30, paid by Klarna: in the shop it is `#7490`; in Klarna's file it is
a SALE of 195.30 and two FEE rows, 5.84 and 0.35, under an order id `5ccf8997-…` and the reference
`#7490`; in the bank it is part of one credit of €19,496.48 on 10 March, reference `KL202603096057`,
which carries every Klarna order of that week. The close joins each order to its provider and each
provider's payout to its bank line, and only then can it say what is missing.

## Rules written down before counting

- The month's sales: Shopify orders paid 1–31 March in the shop's time; Amazon lines shipped from orders
  placed in March; wholesale invoices due in March. Orders on Shopify's test gateway are not sales.
- Money is received when the bank books it. A payout the provider sent by 31 March and the bank booked in
  April is on its way; one the provider sent in April had not been paid out at the close.
- Cut-offs: Klarna settles weekly, so its captures of 30–31 March settle on 6 April; the till's takings of
  30–31 March are deposited in April; Amazon lines of orders placed from 27 March settle in April. Amazon's
  dates are read in UTC, as its reports write them.
- Fees are held to the contracts: PayPal 2.49% + €0.35, Klarna 2.99% + €0.35, Stripe 2.9% + $0.30,
  Amazon's rate card. Shopify Payments' fees are taken as its file states them.
- A credit that is not a customer's money is listed and kept out of what was received.

## What the client receives

- [**The close document**](month-close-document.pdf) (8 pages): the answer, where the money is, each
  channel's bridge closed to the cent, all 28 records that did not agree with what to do about each,
  every credit to the account by what it was, the rules, and the same money in five formats.
- [**The workbook**](month-close.xlsx): the bridge by channel, the exceptions with filters, every bank
  credit labelled, the payments out, the files' fingerprints.
- **The exceptions as data**, [CSV](exceptions.csv) and [JSON](exceptions.json), to filter or to load
  into the shop's own tools.
- For a monthly client, the same close every month, with last month's items in transit checked off when
  they arrive.

## What this case is, and is not

The shop, its orders, the providers' files and the bank statements are synthetic, generated in the
documented formats, and the disagreements were planted on purpose. The code that reconciles reads only the
files, but it was written by the same person who planted the disagreements, so this case shows the
method and what a client receives; it is not a blind test. Every planted disagreement is in the
exceptions. The fees, rates and reserves are illustrative.

---

*Files in this folder, for readers on GitHub.* The source files are the ones reconciled, byte for byte,
except the Shopify orders export (not in this repository, as in the neighbouring cases) and the Shopify
Payments transactions, which are [the payouts case's](../payouts-reconciliation/payout_transactions_2026-03.csv).
The close document lists every file's SHA-256.
