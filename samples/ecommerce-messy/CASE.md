# Six orders where "latest version" cannot be chosen

A client needs an online-shop report for the first quarter of 2026 checked
against the order export it was written from.

The file has 45,917 rows. Some orders appear more than once: each time the
status changed, a new row with the same order number was appended. After keeping
one row per order, there are 44,531 orders.

The agreed rule: if an order appears more than once, the version with the later
update time goes into the figures. Revenue is delivered orders only, after
refunds, excluding shipping.

Six orders (M006912, M008447, M015636, M016369, M035357, M037901) have two rows
with **the same** update time and a different status. One row is still pending
or already cancelled; the other is delivered. Time cannot pick a "latest"
version. What remains is which of the two rows sits lower in the file.

The report computed revenue from the row that sits lower. A recount from the
export matches that choice. By the final review's own count, taking the earlier row moves 10 of 12 published values beyond tolerance. Net revenue falls from **3,023,296.61** to **3,022,518.62** euros.
The arithmetic matches the row that was kept. What does not hold is the reason the rule was accepted: the owner's ruling says every new version of an order is written with a later update time, and for these six it is not. No machine check and no stage review noticed. The final review of the whole run did, and a person has to confirm the tie-break.

The export is synthetic. There is no live shop behind it. The file is built the
way clients send files: several date formats, shipping written with spaces,
commas or a EUR suffix, and a comment column of free text that was kept out of
the calculation.

The six ties were not planted. The program that generated this file writes each
re-exported order one to five hours later, but never past 23:00, and copies the
minutes and seconds. An order last updated at 23 o'clock gets a copy with the
same time to the second. The program's own comment says the timestamp moves
forward, and the owner's ruling repeats it. We made the file ourselves and did
not know; the final review found it.

What the client receives: the report, a document saying what was checked and
what was found, and a checksum of the files so it is possible to see that the
document was not changed after it was handed over.

```powershell
Get-FileHash report.md -Algorithm SHA256
```

The command prints a digest of the file — a short string of its contents. Change
the file by one character and the string changes. For this copy of the report
the digest is:

`2c73dbc26af176932724618ad7d036706778ed5a06244109f25aa203f7e01b03`

The rest of the files are in [README.md](README.md).
