# Fifteen funds on one date: €13.55 billion, and over a third of it at last prices

An asset manager sends four years of prices and the positions of fifteen funds, and asks what the
platform holds on 26 June 2026. The report answers in 106 figures: **€13.55 billion** in 2,133
positions and 669 securities, three quarters of it in equities. And one figure the headline does
not show: **37.2%** of gross value sits in instruments suspended (14.4%) or delisted (22.8%) on
that date, carried at their last price. That was the owner's reading, chosen before any figure was
computed, and it is the first thing a reader of the total needs to know.

## What the check found along the way

The report was written from the export and checked against it.

The export has 761,005 price rows. On the reporting date, 26 June 2026, the
funds hold 2,133 positions in 669 securities. The report prints 106 figures.
Each one is recomputed from these files.

42 positions in 14 securities are valued at a price that is exactly the previous
trading day's close. The quote most likely did not move. That is 2.27% of gross
portfolio value.

The price vendor has its own "stale price" flag. The flag sits on 40 positions.
Of the 42 positions whose price did not actually move, the flag misses five.
On three positions the flag is set and the price did move. The client's own
data dictionary says the flag is not a complete list. The document prints both
counts: 40 by the vendor flag and 42 by the prices themselves.

One more thing. Next to the figures there was a sentence about a yield
threshold, with a number in it. That number is not in the export: the threshold
was set in advance, it is not a measurement. The check stopped and asked how
to write it. The ruling was to name the threshold in words, without a bare
figure. A finished release text was refused once and sent back to be rewritten,
before the client document existed.

The export is synthetic. There is no live fund behind it.

What the client receives: the report, a document saying what was checked and
what was found, and a receipt with a checksum of every file.

```powershell
Get-FileHash report.md -Algorithm SHA256
```

The command prints a digest of the file. Change the file by one character and
the digest changes. For this copy of the report it is:

`851814fbc2dae1c88e6bd3490f4de5f5765e8d302739ae83cfb4f2207a7869c9`

The same string stands in the receipt next to the report. Detail is in
[README.md](README.md).
