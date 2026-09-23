# Квитанция о печати релиза

- Датасет: d9265497ef0042cfaed4423c46e39f37
- Запечатано: 2026-09-23T08:20:50.355781+00:00
- Квитанция: `d9265497ef00-20260923082050-f650b018f378`
- Итоговый отпечаток: `f650b018f37889dab1de11793099d7f16a6b01d1eda1317edba944271597304d`
- Контрольная плоскость (агрегат): `8d0567a308799fb881afe2261d90bcebd82cbd97f3b06ddb7c5c8b1f5f33fa50`

Журнал прогона: запись 12, голова `54d3f1f43de6590d5f68b54a7004d0cc2570e902ca294bd3c5bcf394714ba491`.

Квитанция подтверждает одно: файлы, перечисленные ниже, — ровно те, что были запечатаны в момент печати. Изменённый после печати файл даёт другой отпечаток.

Квитанция не подтверждает, что проверки были верны. За проверки отвечает аудитор.

Отпечаток — SHA-256 байтов файла, в том виде, в каком его считает `Get-FileHash -Algorithm SHA256` или `shasum -a 256`.

Если к квитанции приложен файл подписи `.sig`, его проверяют открытым ключом оператора, без программ этой системы: `ssh-keygen -Y verify -f allowed_signers -I <подписант> -n max-v2-seal -s <квитанция>.md.sig < <квитанция>.md`. Подпись говорит, кто выдал квитанцию, и не говорит, что проверки были верны.

| роль | файл | байт | sha256 |
|---|---|---|---|
| выгрузка | `raw_data/SMEA_holdings.csv` | 60265 | `1522469665017d604661a567440380356a687a045f2b0842f4ba8e6e05599819` |
| отчёт | `release/annotated_factsheet.md` | 16536 | `bd7077b87f16b8fbe13f722184949678b9db44877afbaf3e16b4518102815e94` |
| документ | `deliverable/verification_report.json` | 45024 | `eaadf224fb8d48b18f29a24b8109dce84bc72d29c995dc39ed98ecb08e96a27f` |
| документ | `deliverable/verification_report.md` | 29492 | `385ab7aed78017eb0ecf7c79dca4da8ff4710628caf6487ad0c51e879daa945a` |

# Release seal receipt

- Dataset: d9265497ef0042cfaed4423c46e39f37
- Sealed at: 2026-09-23T08:20:50.355781+00:00
- Receipt: `d9265497ef00-20260923082050-f650b018f378`
- Total digest: `f650b018f37889dab1de11793099d7f16a6b01d1eda1317edba944271597304d`
- Control plane (aggregate): `8d0567a308799fb881afe2261d90bcebd82cbd97f3b06ddb7c5c8b1f5f33fa50`

Run journal: record 12, head `54d3f1f43de6590d5f68b54a7004d0cc2570e902ca294bd3c5bcf394714ba491`.

This receipt shows one thing: the files listed below are exactly the files sealed at the moment of the seal. A file changed after the seal has a different digest.

It does not show that the checks were right. The checks are the auditor's responsibility.

A digest is the SHA-256 of the file's bytes, as `Get-FileHash -Algorithm SHA256` or `shasum -a 256` computes it.

If a signature file `.sig` comes with this receipt, it is checked against the operator's public key with nothing of this system installed: `ssh-keygen -Y verify -f allowed_signers -I <signer> -n max-v2-seal -s <receipt>.md.sig < <receipt>.md`. A signature says who issued the receipt, not that the checks were right.

| role | file | bytes | sha256 |
|---|---|---|---|
| export | `raw_data/SMEA_holdings.csv` | 60265 | `1522469665017d604661a567440380356a687a045f2b0842f4ba8e6e05599819` |
| report | `release/annotated_factsheet.md` | 16536 | `bd7077b87f16b8fbe13f722184949678b9db44877afbaf3e16b4518102815e94` |
| document | `deliverable/verification_report.json` | 45024 | `eaadf224fb8d48b18f29a24b8109dce84bc72d29c995dc39ed98ecb08e96a27f` |
| document | `deliverable/verification_report.md` | 29492 | `385ab7aed78017eb0ecf7c79dca4da8ff4710628caf6487ad0c51e879daa945a` |
