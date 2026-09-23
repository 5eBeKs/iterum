# What is in this folder

[Русская версия](README.ru.md)

Three finished examples. Each one is an export (the export itself is not in this
repository), a report written from that export, and a document in which every
figure in the report is recomputed from the same files. The short case page is
for someone looking for the first time.
The short check of an export kind that is already covered is in
[The verify check](verify.md).
A full review of a new export is in
[Profiles that use a model](llm.md).
The shop and the asset manager are a full review; the fund factsheet is a verify check.

| Example | What the data was | What turned up |
|---|---|---|
| [Online shop](ecommerce-messy/CASE.md) | A quarterly order export, 44,531 orders, duplicates, mixed date formats, a shipping column written several ways | Six orders have two versions with the same update time. The rule "keep the latest" cannot choose. Taking the other version drops net revenue from 3,023,296.61 to 3,022,518.62 euros |
| [Asset manager](asset-manager/CASE.md) | Four years of prices and the positions of fifteen funds on one date, 106 figures in the report | The price vendor flags stale prices. The flag sits on 40 positions; the prices themselves show 42 |
| [Fund factsheet, real and public](etf-smea/CASE.md) | An iShares ETF's September factsheet and the fund's own holdings file, checked with no model | The top 10 weights do not reproduce from the issuer's own holdings on either date the factsheet names |

And a one-page [reconciliation protocol](reconciliation/PROTOCOL.md): two synthetic exports, a store's orders and a payment processor's payments, every discrepancy with both values, and how one file's total becomes the other's.

The checking program is not in this repository. What is here is what the client
receives, and the measurements: which mistakes the checks stop, which they miss,
and what that cost.
