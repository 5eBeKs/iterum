# Asset manager: what the client received

[Русская версия](README.ru.md)

Short page for a proposal: [CASE.md](CASE.md).

Three files from one finished check. They were not edited after the check ended.
There were no folder paths of another machine in them.

| File | What is in it |
|---|---|
| [report.md](report.md) | The report from the export: which figures it prints |
| [client_document.md](client_document.md) | The client document: every figure in the report next to an independent recount, whether they match, what else was found, which rules were fixed before any counting |
| [receipt.md](receipt.md) | The receipt: a checksum of every file the client was given. It shows the files were not changed after they were handed over |

## Where the data came from

A synthetic asset-manager export. There is no live fund behind it. Six tables:
761,005 price rows over four years, and the positions of fifteen funds. The
reporting date is 26 June 2026. On that date: 2,133 positions in 669 securities.
39 of them are quoted as a yield, not a price: a value cannot be computed from
this export, and they are reported by quantity, without a sum.

The report prints 106 figures. Each one is recomputed from the export,
separately from however the report's author computed it.

One model (GLM) wrote the report, another vendor's model (Grok) reviewed it.
The figures themselves are recounted by ordinary code, with no model in that
step. 16 model launches. The receipt was
issued on 20 September 2026. The last review of the whole report passed with
17 notes, none of which stopped the hand-over.

## What was found

**Stale prices are counted from the prices themselves, not from the vendor
flag.** 42 positions in 14 securities are valued at a price that matches the
previous trading day's close. That is 2.2719% of gross value. The vendor's
"stale price" flag sits on 40 positions: it misses five of those 42, and three
flagged positions actually have a different price. The client's data dictionary
says the flag is incomplete. The document prints both numbers.

**One question was put to a person.** Next to the figures there was a sentence
about a yield threshold, with a number in it. The export does not measure that
number: the threshold was set in advance as a working condition, not as a
result. The check stopped, offered three ways to write it, and showed what
each would do. The ruling was to name the threshold in words. The ruling is in
the document with the name of the person who made it.

**A finished release text was refused once** and sent back to be rewritten.
The client document did not exist yet.

## How to check the receipt

On Windows:

```powershell
Get-FileHash report.md -Algorithm SHA256
```

The command computes a digest of the file — a short string of its contents.
If the file is changed after it was handed over, the string changes. For this
copy of the report the digest is:

`851814fbc2dae1c88e6bd3490f4de5f5765e8d302739ae83cfb4f2207a7869c9`

The same string stands in the receipt on the report's row. The export is listed
in the receipt too; it is not here: it is the client's data, and it is not
published.

The receipt shows one thing: the files you hold are the files that were handed
over. It does not show that the checks were right: the recount in the document shows the arithmetic, and whether the mandate was read correctly is a person's ruling, recorded with a name.

The client document carries the line that the check is not sealed yet. The
document is written one step before the receipt. The receipt beside it is the
record that the work was finished after that document.
