# Квитанция о печати релиза

- Датасет: 7c95896f3527458b85fab37981437224
- Запечатано: 2026-09-23T17:04:55.129622+00:00
- Квитанция: `7c95896f3527-20260923170455-290db5a3095f`
- Итоговый отпечаток: `290db5a3095f3954f82ec662cc131dd9f55b30e6be9633973b63a9cdd9eb2b40`
- Контрольная плоскость (агрегат): `1b9e81a4621d511bce60d590b01dbc37a985753009f70238d00f6eb803e750c5`

Журнал прогона: запись 94, голова `123b6ee7ba728918b92500ecfcb44dbfaa909619f98f4e3559102768e68c1be5`.

Квитанция подтверждает одно: файлы, перечисленные ниже, — ровно те, что были запечатаны в момент печати. Изменённый после печати файл даёт другой отпечаток.

Квитанция не подтверждает, что проверки были верны. За проверки отвечает аудитор.

Отпечаток — SHA-256 байтов файла, в том виде, в каком его считает `Get-FileHash -Algorithm SHA256` или `shasum -a 256`.

Если к квитанции приложен файл подписи `.sig`, его проверяют открытым ключом оператора, без программ этой системы: `ssh-keygen -Y verify -f allowed_signers -I <подписант> -n max-v2-seal -s <квитанция>.md.sig < <квитанция>.md`. Подпись говорит, кто выдал квитанцию, и не говорит, что проверки были верны.

| роль | файл | байт | sha256 |
|---|---|---|---|
| выгрузка | `raw_data/orders_export.csv` | 7967899 | `4655ea261d1446cdb828cbf2106dae16d141b625cdbf5ac543c048f57004881f` |
| отчёт | `release/dashboard_data.json` | 21600 | `0fef3ffa410352959eb0cfaa07f9caa298682d9eda695f33478cb6597f9d70e1` |
| отчёт | `release/release_number_manifest.json` | 4310 | `6a8b6d535f079e7a2e04d878f8c712aa2cc6a709ed0f2ccee7ba5874a444cfa1` |
| отчёт | `release/report.md` | 9123 | `4e86280e0b5b7732f8a9f9a4f1ccc2c7e0edbe3e48b4c7f4366ce106c1263b04` |
| документ | `deliverable/client_document.html` | 34777 | `93573dce4e1722ee98ac484fb5a533dba589b0a1e12a20e1b7e731e95623d6a0` |
| документ | `deliverable/client_document.json` | 67553 | `a980319d0437154eb0792b1764cc5f3107a77fb3e376497fd9ef413f13b5a3af` |
| документ | `deliverable/client_document.md` | 25204 | `96023c03a01504479e181fafe749d05b76eae98105f69ba263d9545fbfe69343` |

# Release seal receipt

- Dataset: 7c95896f3527458b85fab37981437224
- Sealed at: 2026-09-23T17:04:55.129622+00:00
- Receipt: `7c95896f3527-20260923170455-290db5a3095f`
- Total digest: `290db5a3095f3954f82ec662cc131dd9f55b30e6be9633973b63a9cdd9eb2b40`
- Control plane (aggregate): `1b9e81a4621d511bce60d590b01dbc37a985753009f70238d00f6eb803e750c5`

Run journal: record 94, head `123b6ee7ba728918b92500ecfcb44dbfaa909619f98f4e3559102768e68c1be5`.

This receipt shows one thing: the files listed below are exactly the files sealed at the moment of the seal. A file changed after the seal has a different digest.

It does not show that the checks were right. The checks are the auditor's responsibility.

A digest is the SHA-256 of the file's bytes, as `Get-FileHash -Algorithm SHA256` or `shasum -a 256` computes it.

If a signature file `.sig` comes with this receipt, it is checked against the operator's public key with nothing of this system installed: `ssh-keygen -Y verify -f allowed_signers -I <signer> -n max-v2-seal -s <receipt>.md.sig < <receipt>.md`. A signature says who issued the receipt, not that the checks were right.

| role | file | bytes | sha256 |
|---|---|---|---|
| export | `raw_data/orders_export.csv` | 7967899 | `4655ea261d1446cdb828cbf2106dae16d141b625cdbf5ac543c048f57004881f` |
| report | `release/dashboard_data.json` | 21600 | `0fef3ffa410352959eb0cfaa07f9caa298682d9eda695f33478cb6597f9d70e1` |
| report | `release/release_number_manifest.json` | 4310 | `6a8b6d535f079e7a2e04d878f8c712aa2cc6a709ed0f2ccee7ba5874a444cfa1` |
| report | `release/report.md` | 9123 | `4e86280e0b5b7732f8a9f9a4f1ccc2c7e0edbe3e48b4c7f4366ce106c1263b04` |
| document | `deliverable/client_document.html` | 34777 | `93573dce4e1722ee98ac484fb5a533dba589b0a1e12a20e1b7e731e95623d6a0` |
| document | `deliverable/client_document.json` | 67553 | `a980319d0437154eb0792b1764cc5f3107a77fb3e376497fd9ef413f13b5a3af` |
| document | `deliverable/client_document.md` | 25204 | `96023c03a01504479e181fafe749d05b76eae98105f69ba263d9545fbfe69343` |
