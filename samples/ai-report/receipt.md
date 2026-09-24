# Квитанция о печати релиза

- Датасет: fcc7b27658a04314a7fec9bb988d8f67
- Запечатано: 2026-09-23T18:30:29.156170+00:00
- Квитанция: `fcc7b27658a0-20260923183029-4fcfdd2c3afb`
- Итоговый отпечаток: `4fcfdd2c3afb4f40bc48581a69b82e8f6e458192b11e7c75b186427a9c70cfad`
- Контрольная плоскость (агрегат): `5824e4456f11b1b73580ef4cfe2439a496dc6d72aac9d8ed12d89d3783bbf048`

Журнал прогона: запись 13, голова `5babec983eec8e019f0f34100df8ea629f48da8361332e514a382253a9ed3fc2`.

Квитанция подтверждает одно: файлы, перечисленные ниже, — ровно те, что были запечатаны в момент печати. Изменённый после печати файл даёт другой отпечаток.

Квитанция не подтверждает, что проверки были верны. За проверки отвечает аудитор.

Отпечаток — SHA-256 байтов файла, в том виде, в каком его считает `Get-FileHash -Algorithm SHA256` или `shasum -a 256`.

Если к квитанции приложен файл подписи `.sig`, его проверяют открытым ключом оператора, без программ этой системы: `ssh-keygen -Y verify -f allowed_signers -I <подписант> -n max-v2-seal -s <квитанция>.md.sig < <квитанция>.md`. Подпись говорит, кто выдал квитанцию, и не говорит, что проверки были верны.

| роль | файл | байт | sha256 |
|---|---|---|---|
| выгрузка | `raw_data/orders_export.csv` | 7967899 | `4655ea261d1446cdb828cbf2106dae16d141b625cdbf5ac543c048f57004881f` |
| отчёт | `release/report.md` | 8654 | `e8df0c588839818aa655ae550b42efc2c82fe6cfff2b6604e323bb6f7ad8d9d4` |
| документ | `deliverable/verification_report.json` | 74406 | `d5705b2135f2210028d7133c76cfbea8ffbda9bccacc8f8e94d8b1f950a31a79` |
| документ | `deliverable/verification_report.md` | 50397 | `95bdf3f42fdef7ae799ce5058a917a97166a38b36fcfbd68db381ede3edd7b29` |

# Release seal receipt

- Dataset: fcc7b27658a04314a7fec9bb988d8f67
- Sealed at: 2026-09-23T18:30:29.156170+00:00
- Receipt: `fcc7b27658a0-20260923183029-4fcfdd2c3afb`
- Total digest: `4fcfdd2c3afb4f40bc48581a69b82e8f6e458192b11e7c75b186427a9c70cfad`
- Control plane (aggregate): `5824e4456f11b1b73580ef4cfe2439a496dc6d72aac9d8ed12d89d3783bbf048`

Run journal: record 13, head `5babec983eec8e019f0f34100df8ea629f48da8361332e514a382253a9ed3fc2`.

This receipt shows one thing: the files listed below are exactly the files sealed at the moment of the seal. A file changed after the seal has a different digest.

It does not show that the checks were right. The checks are the auditor's responsibility.

A digest is the SHA-256 of the file's bytes, as `Get-FileHash -Algorithm SHA256` or `shasum -a 256` computes it.

If a signature file `.sig` comes with this receipt, it is checked against the operator's public key with nothing of this system installed: `ssh-keygen -Y verify -f allowed_signers -I <signer> -n max-v2-seal -s <receipt>.md.sig < <receipt>.md`. A signature says who issued the receipt, not that the checks were right.

| role | file | bytes | sha256 |
|---|---|---|---|
| export | `raw_data/orders_export.csv` | 7967899 | `4655ea261d1446cdb828cbf2106dae16d141b625cdbf5ac543c048f57004881f` |
| report | `release/report.md` | 8654 | `e8df0c588839818aa655ae550b42efc2c82fe6cfff2b6604e323bb6f7ad8d9d4` |
| document | `deliverable/verification_report.json` | 74406 | `d5705b2135f2210028d7133c76cfbea8ffbda9bccacc8f8e94d8b1f950a31a79` |
| document | `deliverable/verification_report.md` | 50397 | `95bdf3f42fdef7ae799ce5058a917a97166a38b36fcfbd68db381ede3edd7b29` |
