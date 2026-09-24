# Q1 2026 Sales Report

Source: `orders_export.csv` (Shopify), orders created 1 Jan – 31 Mar 2026, shop local time. All amounts in EUR, **including VAT, excluding shipping**. Script: `analysis.py`.

## Key numbers

| | Jan | Feb | Mar | **Q1** |
|---|---:|---:|---:|---:|
| Orders | 3,217 | 2,615 | 2,832 | **8,664** |
| Gross sales | 578,510.00 | 496,406.00 | 527,161.00 | 1,602,077.00 |
| – Discounts | 15,368.05 | 12,932.70 | 15,377.20 | 43,677.95 |
| – Refunds | 34,003.77 | 24,483.08 | 24,515.22 | 83,002.07 |
| **Net sales** | **529,138.18** | **458,990.22** | **487,268.58** | **1,475,396.98** |
| Average order value | 175.05 | 184.88 | 180.71 | **179.87** |

- **Net sales** = gross sales (list price × quantity) − discounts − refunds. Net sales excluding VAT for Q1: **€1,230,049.35** (each order's own VAT share removed; VAT rates 16–19% by country).
- **Average order value** = order value after discounts, before refunds, excluding shipping (€1,558,399.05 / 8,664).

## Refunds
- Refunded product value: **€83,002.07 = 5.33%** of order value (after discounts).
- **803 of 8,664 orders (9.27%)** had a full or partial refund (364 full, 439 partial).
- Customers were also refunded €1,815.05 of shipping, so the refunded total in the export is €84,817.12.
- By month (refund value as % of order value): Jan 6.04%, Feb 5.06%, Mar 4.79%.

## Discounts
- **€43,677.95** in total = 2.73% of gross sales. 1,910 orders (22.0%) used a code.
- By code: VIP20 13,271.60 · WELCOME10 10,519.70 · WINTER15 7,919.25 · SPRING20 6,437.40 · TENOFF 5,530.00.

## Top 10 products by sales
Sales = price × quantity after discounts, before refunds (Q1 total: €1,558,399.05).

| # | Product | Units | Sales (€) | Share |
|---|---|---:|---:|---:|
| 1 | Fjord Rain Jacket | 1,385 | 254,356.47 | 16.3% |
| 2 | Polar Down Jacket | 1,048 | 243,146.58 | 15.6% |
| 3 | Trail Hiking Trousers | 1,118 | 107,314.28 | 6.9% |
| 4 | Ridge Fleece Midlayer | 1,272 | 104,474.86 | 6.7% |
| 5 | Merino Base Layer Top | 1,486 | 99,507.22 | 6.4% |
| 6 | Solo Trekking Tent | 281 | 90,240.93 | 5.8% |
| 7 | Summit Daypack | 744 | 85,738.08 | 5.5% |
| 8 | Down Sleeping Bag | 326 | 84,666.39 | 5.4% |
| 9 | Storm Shell Trousers | 547 | 74,433.62 | 4.8% |
| 10 | Hiking Socks Pair | 3,659 | 67,465.31 | 4.3% |

The top 10 make up 77.7% of sales. The two jackets alone are 31.9%.

## Repeat customers
- 5,957 customers (identified by email) placed orders in Q1; **1,392 (23.4%) ordered more than once**, 551 of them three or more times.
- Repeat customers account for 45.3% of orders.
- Limits: this covers Q1 only (earlier purchases are not in the export), and 318 orders without an email (mostly pop-up store cash sales) cannot be linked to a customer.

## Sales by channel (net sales)

| Channel | Orders | Net sales (€) | Share |
|---|---:|---:|---:|
| Online store | 7,850 | 1,325,008.08 | 89.8% |
| POS (Pop-up Store Hamburg) | 531 | 99,157.00 | 6.7% |
| Draft orders – phone orders | 196 | 36,860.20 | 2.5% |
| Draft orders – wholesale | 87 | 14,371.70 | 1.0% |
| **Total** | **8,664** | **1,475,396.98** | 100% |

## How the data was cleaned (please read before presenting)
The raw file has 9,659 orders, but 9,159 were created in Q1 and only **8,664 are counted**:
- **1,068 orders were listed twice** in the export (identical rows at the end of the file). Removed. Left in, sales would be overstated by roughly 11%.
- **Excluded from Q1:** 84 internal orders (test/QA orders paid with a dummy gateway, and staff orders; €15,472 of order value), 260 cancelled orders (voided, or cancelled and fully refunded, all unfulfilled; €48,264.50), and 151 unpaid orders (payment only authorized or pending; €27,097.65).
- **Orders outside Q1** (29–31 Dec and 1–3 Apr, about 500) are excluded.
- **Refund timing:** the export has no refund date, so each refund is counted in the month the order was placed, not the month it was paid out.
- Refunds on fully refunded orders include shipping. Only the product share reduces net sales.
- Excluding cancelled orders makes the refund rate relate to orders that were actually fulfilled. Counting them would raise the refund rate.
