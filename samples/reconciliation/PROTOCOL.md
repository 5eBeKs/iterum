# Reconciliation protocol: store orders vs payment processor

*Sample on synthetic data. Every figure below is computed from the two files beside this page, [`orders.csv`](orders.csv) and [`payments.csv`](payments.csv), and can be recounted from them.*

## What was compared

| File | What it is | Rows | SHA-256 |
|---|---|---:|---|
| `orders.csv` | the store's order export, 1 August to 1 September 2026 | 1200 | `c3fa381ce3964a3f…` |
| `payments.csv` | the payment processor's export, same dates | 1035 | `9925cd2c384bf169…` |

## Rules agreed before counting

- **Key:** `order_id` in both files.
- **Which orders should have a payment:** status `paid` or `refunded` (1034 orders). `cancelled` orders (166) should have none.
- **What must match:** the order `total` and the payment `amount`, same currency.
- **Tolerance:** a difference of 0.01 or less counts as matched and is listed in the totals below.
- **An order paid twice:** every payment row is listed.

## Result

**1022 of 1034 orders reconcile** (3 of them a cent apart, inside the tolerance). **15 records do not**, grouped by what went wrong:

| What went wrong | Order | Payment | Store | Processor | Difference |
|---|---|---|---:|---:|---:|
| Order paid, no payment | SO-10717 |  | 195.61 | — | -195.61 |
| Order paid, no payment | SO-10927 |  | 284.00 | — | -284.00 |
| Order paid, no payment | SO-10988 |  | 200.00 | — | -200.00 |
| Order paid, no payment | SO-11061 |  | 291.82 | — | -291.82 |
| Amount differs | SO-10104 | PY-700668 | 345.66 | 333.16 | -12.50 |
| Amount differs | SO-10588 | PY-700954 | 182.86 | 162.86 | -20.00 |
| Amount differs | SO-10690 | PY-700914 | 79.73 | 76.38 | -3.35 |
| Amount differs | SO-10920 | PY-700210 | 409.66 | 397.16 | -12.50 |
| Amount differs | SO-10974 | PY-700329 | 223.40 | 222.50 | -0.90 |
| Charged more than once | SO-10157 | PY-700205, PY-701036 | 254.90 | 254.90 + 254.90 | +254.90 |
| Charged more than once | SO-10344 | PY-700263, PY-701035 | 474.97 | 474.97 + 474.97 | +474.97 |
| Currency differs | SO-10086 | PY-700847 | 321.01 EUR | 321.01 USD | not comparable |
| Payment, no order | SO-19000 | PY-701037 | — | 186.08 | +186.08 |
| Payment, no order | SO-19001 | PY-701038 | — | 31.27 | +31.27 |
| Payment, no order | SO-19002 | PY-701039 | — | 161.82 | +161.82 |

## How the store's total becomes the processor's total (EUR)

| | EUR |
|---|---:|
| Store: paid and refunded orders | 249,511.39 |
| Order paid, no payment | -971.43 |
| Amount differs | -49.25 |
| Charged more than once | +729.87 |
| Payment, no order | +379.17 |
| Currency differs (left out of the EUR total) | -321.01 |
| Within tolerance (±0.01 each) | +0.03 |
| **Processor: EUR payments** | **249,278.77** |

## What this does not check

- Whether refunds were paid back to the customer: refunds are not in either file.
- The processor's fees: they are in `payments.csv` but were not part of what must match.
- Whether the store's totals are right: the check is that the two files agree, not that either is correct.

The full SHA-256 of each file: `orders.csv` c3fa381ce3964a3f5b8a33f161da3571a6a6c7eb4dcd283ecfdb3d25d9513895, `payments.csv` 9925cd2c384bf169412b3b55db8ce3e23c811b4f82dbc7ec62222c7e976826f3.
