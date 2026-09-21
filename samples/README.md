# What is in this folder

[Русская версия](README.ru.md)

Two finished examples. Each one is an export (the export itself is not in this
repository), a report written from that export, and a document in which every
figure in the report is recomputed from the same files. The short case page is
for someone looking for the first time.

| Example | What the data was | What turned up |
|---|---|---|
| [Online shop](ecommerce-messy/CASE.md) | A quarterly order export, 44,531 orders, duplicates, mixed date formats, a shipping column written several ways | Six orders have two versions with the same update time. The rule "keep the latest" cannot choose. Taking the other version drops net revenue from 3,023,296.61 to 3,022,518.62 euros |
| [Asset manager](asset-manager/CASE.md) | Four years of prices and the positions of fifteen funds on one date, 106 figures in the report | The price vendor flags stale prices. The flag sits on 40 positions; the prices themselves show 42 |

The checking program is not in this repository. What is here is what the client
receives, and the measurements: which mistakes the checks stop, which they miss,
and what that cost.
