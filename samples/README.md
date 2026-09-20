# What a finished audit hands over

[Русская версия](README.ru.md)

Three files from one real run, exactly as it recorded them. Nothing is touched up; the only thing
taken out would have been the folder paths of the machine it ran on, and there were none in them.

| file | what it is |
|---|---|
| [`report.md`](report.md) | the **report** the system wrote from the export: what was checked |
| [`client_document.md`](client_document.md) | the **client document**: what was checked, what was found, and what it rests on |
| [`receipt.md`](receipt.md) | the **receipt** of the seal: the SHA-256 of every file the client was given |

## The run

A synthetic export from an asset manager: six tables, 761,005 price rows over four years, the
positions of fifteen funds. One reporting date, 2026-06-26, with 2,133 positions in 669 securities,
39 of them quoted as yields and therefore unvalued. 106 published figures, every one recomputed from
the export.

Two vendors' models did the work: **GLM writes, Grok reviews** -- four worker stages and six reviews.
16 launches, $5.25 by the vendors' own counters, sealed on 2026-09-20. The final red team passed with
17 warnings and no blocking issues.

## What stopped the work in this run

- **One question for a person.** A caveat about the yield threshold carried a number bound to no
  published claim: the threshold is a parameter of the mandate, not a measured figure. The stage
  stopped, offered three options with the consequence of each, and the owner ruled that the threshold
  is named in words. The ruling is in the client document with the name beside it.
- **One review refused the release** and sent it back to be written again, before the document existed.
- **Carried-forward prices** are disclosed from the data rather than from the vendor's flag: 42
  positions in 14 securities are valued at a price repeating the previous quoted day's close, 2.2719%
  of gross exposure. The vendor's flag marks 40 positions, misses five carried prices, and three of
  the prices it marks actually moved. The client's own data dictionary says the flag is not complete,
  and the document prints both readings.

## Checking the receipt

```bash
sha256sum report.md
```

On Windows, `Get-FileHash report.md -Algorithm SHA256`. The digest must be the one the receipt lists
beside `release/report.md`. The export is listed in the receipt too but is not here: it is the client's
data, not evidence about the audit.

One honest caveat about the document itself: it is written one step before the seal, so it carries the
line that the audit is not sealed yet. The seal followed immediately, and the receipt beside it is the
proof of that.
