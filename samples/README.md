# What is in this folder

[Русская версия](README.ru.md)

Seven finished examples, grouped by the three things you can order. Each case page reads on its
own; the files beside it are for anyone who wants to recount.

## A sales or business report, written from your export

You send the export and a question. You get the report, every figure in it recounted from the
export by separate code, and the questions only you can answer.

| Example | What the data was | What the owner learned |
|---|---|---|
| [A quarter of a Shopify shop](shop-analytics/CASE.md) | A Shopify orders export, 9,659 orders, analysed on a fixed menu | €1,474,891.63 of net sales, repeat customers at 23.4%, and five questions for the owner, one of them the assumption an AI assistant made silently. 36 of 36 figures recounted and matched |
| [An online shop's quarter](ecommerce-messy/CASE.md) | A quarterly order export, 44,531 orders, duplicates, mixed date formats, a shipping column written several ways | The partner channel brings 45% of orders, delivers 60.5% of them against 72.4% direct, at €87 an order against €111. Along the way, six orders whose "latest version" the file cannot choose |
| [Fifteen funds on one date](asset-manager/CASE.md) | Four years of prices and the positions of fifteen funds, 106 figures | €13.55 billion, and 37.2% of gross value in instruments suspended or delisted, carried at their last price. Along the way, a vendor's stale-price flag that misses five positions |

## A check of a report you already have

You send the report, from an analyst or an AI, and the export it was written from. Every figure is
recounted: it matches, it does not with both values, or it cannot be checked and why.

| Example | What the data was | What turned up |
|---|---|---|
| [An AI's sales report](ai-report/CASE.md) | A Shopify orders export given to two AI assistants with Python; one report checked with no model | One silent assumption in the assistant's code put 8 of 35 checkable figures off, €505 into net sales. The other assistant's headline is €221 thousand away through definitions nobody asked about |
| [Fund factsheet, real and public](etf-smea/CASE.md) | An iShares ETF's September factsheet and the fund's own holdings file, checked with no model | The top 10 weights do not reproduce from the issuer's own holdings on either date the factsheet names |

## A reconciliation of two files that should agree

You send the two files. You get every difference with both values and its kind, and a table that
turns one file's total into the other's.

| Example | What the data was | What turned up |
|---|---|---|
| [Shopify sales against Shopify Payments payouts](payouts-reconciliation/CASE.md) | A month of Shopify orders and the Shopify Payments transactions export | Where €285,611 between March sales and the payout went, to the cent: other payment methods, refunds, fees. Eight orders for a person, among them a double charge and a dispute the shop's books do not show |
| [Store orders against processor payments](reconciliation/PROTOCOL.md) | Two synthetic exports, a store's orders and a payment processor's payments | 15 records that do not reconcile, grouped by what went wrong, and how one file's total becomes the other's |

The report cases are a full review, done with [a model and every check](llm.md); the checks of a
report are done [with no model](verify.md) where the export is of a kind already covered.

The checking program is not in this repository. What is here is what the client receives, and the
measurements: which mistakes the checks stop, which they miss, and what that cost.
