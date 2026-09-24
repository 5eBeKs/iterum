# Nordlicht Outdoor — Q1 2026 Sales Report

Source: Shopify orders export (`orders_export.csv`), orders created 1 Jan – 31 Mar 2026. All amounts are in EUR.
**Net sales** are product sales after discounts and refunds, **excluding VAT and shipping** (the same definition Shopify uses).

## Key numbers

| | January | February | March | **Q1 2026** |
|---|---:|---:|---:|---:|
| Orders | 3,250 | 2,638 | 2,950 | **8,838** |
| Gross sales | €487,518.60 | €417,103.45 | €457,953.58 | **€1,362,575.64** |
| Discounts | −€13,216.58 | −€11,197.47 | −€14,643.66 | **−€39,057.72** |
| Refunds (returns) | −€28,508.33 | −€20,529.62 | −€20,514.23 | **−€69,552.19** |
| **Net sales** | **€445,793.69** | **€385,376.36** | **€422,795.68** | **€1,253,965.73** |
| Average order value¹ | €145.94 | €153.87 | €150.27 | **€149.75** |
| Refund rate² | 6.01% | 5.04% | 4.63% | **5.25%** |

¹ (Gross sales − discounts) ÷ orders, excl. VAT and shipping. Including VAT and shipping, customers paid €182.81 per order on average.
² Money refunded ÷ order value, both including VAT.

## Refunds
- **€84,817.12** paid back to customers (incl. VAT and refunded shipping). Without VAT and shipping this is €69,552.19.
- **Refund rate: 5.25%** of order value. It went down each month: 6.01% in January, 5.04% in February, 4.63% in March.
- 803 orders (9.09%) had a refund: 364 in full and 439 in part.

## Discounts
- **€39,057.72** in discounts excl. VAT (€46,876.80 incl. VAT). That is **2.87% of gross sales**, spread over 1,970 orders (22.3%).
- By code (excl. VAT): VIP20 €11,225.57 · WELCOME10 €8,939.14 · WINTER15 €6,600.10 · SPRING20 €5,889.70 · TENOFF €4,631.73 · STAFF50 €1,771.48

## Top 10 products (sales after discounts, excl. VAT)

| # | Product | Units | Sales | Share |
|---|---|---:|---:|---:|
| 1 | Fjord Rain Jacket | 1,412 | €215,881.46 | 16.3% |
| 2 | Polar Down Jacket | 1,066 | €205,930.75 | 15.6% |
| 3 | Trail Hiking Trousers | 1,154 | €92,166.41 | 7.0% |
| 4 | Ridge Fleece Midlayer | 1,294 | €88,450.21 | 6.7% |
| 5 | Merino Base Layer Top | 1,515 | €84,554.27 | 6.4% |
| 6 | Solo Trekking Tent | 289 | €77,315.46 | 5.8% |
| 7 | Summit Daypack | 756 | €72,486.79 | 5.5% |
| 8 | Down Sleeping Bag | 329 | €71,266.38 | 5.4% |
| 9 | Storm Shell Trousers | 561 | €63,621.98 | 4.8% |
| 10 | Hiking Socks Pair | 3,735 | €57,337.31 | 4.3% |

The top 10 products made up 77.7% of product sales. These figures are before refunds, because the export does not show which product each refund was for.

## Returning customers
- There were **6,036 customers** in Q1, counted by email address. **1,419 of them (23.51%) ordered 2 or more times** during the quarter.
- Those returning customers placed **45.66% of all orders** from identifiable customers.
- 318 orders with no email address (mostly in-store sales) and staff accounts are not counted here.

## Sales by channel (net sales)

| Channel | Orders | Net sales | Share |
|---|---:|---:|---:|
| Online store | 7,940 | €1,116,146.12 | 89.0% |
| POS: Pop-up Store Hamburg | 531 | €83,324.93 | 6.6% |
| Phone orders (draft orders) | 236 | €36,968.14 | 2.9% |
| Wholesale (draft orders, Net 30) | 108 | €15,755.06 | 1.3% |
| Staff purchases | 23 | €1,771.48 | 0.1% |
| **Total** | **8,838** | **€1,253,965.73** | **100%** |

All refunds in Q1 were on online store orders (5.85% refund rate there).

## How the data was cleaned
- **2,509 duplicate rows were removed.** The export contained a second copy of 1,068 orders; counting them twice would inflate sales.
- **Removed:** 500 orders dated outside Q1 (29–31 Dec 2025 and 1–3 Apr 2026), 61 test orders (tag "test" / "bogus" payment), and 260 cancelled orders (€49,004.45 incl. VAT).
- The export only has the order date, not the refund date. Refunds are therefore counted in the month of the original order, which is why the monthly figures can differ slightly from Shopify Analytics.
- 151 orders (€27,509.35 incl. VAT) were still unpaid (authorized/pending, including Net 30 wholesale invoices). They are included in sales.
- The returning-customer rate only looks at orders within Q1. Customers whose earlier orders were before 2026 are not recognised as returning, so the real rate is probably higher.

*Reproducible with `analyze_q1.py` (Python/pandas) in this folder.*
