# Квитанция о печати релиза

- Датасет: 37b9ef362a704c17a85cd8d2829b54fd
- Запечатано: 2026-09-20T13:37:46.274088+00:00
- Квитанция: `37b9ef362a70-20260920133746-26eaeedc6017`
- Итоговый отпечаток: `26eaeedc6017d3ef3018e24d21a14530bfb1d329ee573884ed4d2a2b8cc0b322`
- Контрольная плоскость (агрегат): `2e99c7a2f5a98e908f6de76469b4077079fa0c4eefcd4a9ab3d70a1305c42f0e`

Журнал прогона: запись 93, голова `63b3ab40686df465146f46b0a582acf9ef3128c9b54fce5ec82ad82e41cf6920`.

Квитанция подтверждает одно: файлы, перечисленные ниже, — ровно те, что были запечатаны в момент печати. Изменённый после печати файл даёт другой отпечаток.

Квитанция не подтверждает, что проверки были верны. За проверки отвечает аудитор.

Отпечаток — SHA-256 байтов файла, в том виде, в каком его считает `Get-FileHash -Algorithm SHA256` или `shasum -a 256`.

Если к квитанции приложен файл подписи `.sig`, его проверяют открытым ключом оператора, без программ этой системы: `ssh-keygen -Y verify -f allowed_signers -I <подписант> -n max-v2-seal -s <квитанция>.md.sig < <квитанция>.md`. Подпись говорит, кто выдал квитанцию, и не говорит, что проверки были верны.

| роль | файл | байт | sha256 |
|---|---|---|---|
| выгрузка | `raw_data/02_fx_rates.csv` | 2211700 | `97b6a7e98fcfd7ca165b5f556da86c326636f0997a9f43d882c592d89b4ce3c9` |
| выгрузка | `raw_data/03_issuers.csv` | 244878 | `c09a5e7ff336130b5e370780d8dce0976956f455e1eb8c64ba56be24c6234813` |
| выгрузка | `raw_data/04_instrument_master.csv` | 3698149 | `0e134299f29c30dc8b8ddde82d87f916d3ef2ed85025051758f57557281f9459` |
| выгрузка | `raw_data/07_funds.csv` | 2196 | `1bf20d5f03bc187c1bfdf35866193577bb3510ce61f805a6d34c7d8b5d0e7a3e` |
| выгрузка | `raw_data/11_prices_eod.csv` | 90509425 | `53af9f3aea32b0d8adebf5672d196f91ea3da11a5f7aff8af18ffa9e288d03d3` |
| выгрузка | `raw_data/16_positions_eod.csv` | 83808266 | `a5e7c350d0405fbb35ce0a8644f81ab274f209c182e726a88db01f9d02468eb9` |
| отчёт | `release/release_number_manifest.json` | 13283 | `d9c1ed755c02ead20977c5b25335247f5b28278549eac60213055b3041a5b2b9` |
| отчёт | `release/report.md` | 14451 | `851814fbc2dae1c88e6bd3490f4de5f5765e8d302739ae83cfb4f2207a7869c9` |
| документ | `deliverable/client_document.html` | 49478 | `dc115e8c7e3b448583b6b20e81a6e2359a16910d1e2e71b7d7576b53ce34e725` |
| документ | `deliverable/client_document.json` | 105817 | `9879a0944dfee301744fb0dc9aca349c2270521061fbec163a3d76d4cc78c9ca` |
| документ | `deliverable/client_document.md` | 33101 | `87971a2bb7cc5f4826e3839c31a2ec74e8fc981c814034d3d6974cfd89b4338d` |

# Release seal receipt

- Dataset: 37b9ef362a704c17a85cd8d2829b54fd
- Sealed at: 2026-09-20T13:37:46.274088+00:00
- Receipt: `37b9ef362a70-20260920133746-26eaeedc6017`
- Total digest: `26eaeedc6017d3ef3018e24d21a14530bfb1d329ee573884ed4d2a2b8cc0b322`
- Control plane (aggregate): `2e99c7a2f5a98e908f6de76469b4077079fa0c4eefcd4a9ab3d70a1305c42f0e`

Run journal: record 93, head `63b3ab40686df465146f46b0a582acf9ef3128c9b54fce5ec82ad82e41cf6920`.

This receipt shows one thing: the files listed below are exactly the files sealed at the moment of the seal. A file changed after the seal has a different digest.

It does not show that the checks were right. The checks are the auditor's responsibility.

A digest is the SHA-256 of the file's bytes, as `Get-FileHash -Algorithm SHA256` or `shasum -a 256` computes it.

If a signature file `.sig` comes with this receipt, it is checked against the operator's public key with nothing of this system installed: `ssh-keygen -Y verify -f allowed_signers -I <signer> -n max-v2-seal -s <receipt>.md.sig < <receipt>.md`. A signature says who issued the receipt, not that the checks were right.

| role | file | bytes | sha256 |
|---|---|---|---|
| export | `raw_data/02_fx_rates.csv` | 2211700 | `97b6a7e98fcfd7ca165b5f556da86c326636f0997a9f43d882c592d89b4ce3c9` |
| export | `raw_data/03_issuers.csv` | 244878 | `c09a5e7ff336130b5e370780d8dce0976956f455e1eb8c64ba56be24c6234813` |
| export | `raw_data/04_instrument_master.csv` | 3698149 | `0e134299f29c30dc8b8ddde82d87f916d3ef2ed85025051758f57557281f9459` |
| export | `raw_data/07_funds.csv` | 2196 | `1bf20d5f03bc187c1bfdf35866193577bb3510ce61f805a6d34c7d8b5d0e7a3e` |
| export | `raw_data/11_prices_eod.csv` | 90509425 | `53af9f3aea32b0d8adebf5672d196f91ea3da11a5f7aff8af18ffa9e288d03d3` |
| export | `raw_data/16_positions_eod.csv` | 83808266 | `a5e7c350d0405fbb35ce0a8644f81ab274f209c182e726a88db01f9d02468eb9` |
| report | `release/release_number_manifest.json` | 13283 | `d9c1ed755c02ead20977c5b25335247f5b28278549eac60213055b3041a5b2b9` |
| report | `release/report.md` | 14451 | `851814fbc2dae1c88e6bd3490f4de5f5765e8d302739ae83cfb4f2207a7869c9` |
| document | `deliverable/client_document.html` | 49478 | `dc115e8c7e3b448583b6b20e81a6e2359a16910d1e2e71b7d7576b53ce34e725` |
| document | `deliverable/client_document.json` | 105817 | `9879a0944dfee301744fb0dc9aca349c2270521061fbec163a3d76d4cc78c9ca` |
| document | `deliverable/client_document.md` | 33101 | `87971a2bb7cc5f4826e3839c31a2ec74e8fc981c814034d3d6974cfd89b4338d` |
