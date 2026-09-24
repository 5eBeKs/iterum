# Q1 2026 Sales Report

Source: `orders_export.csv` (Shopify), orders created 1 Jan – 31 Mar 2026, shop local time. All amounts in EUR, **including VAT, excluding shipping**. Script: `analysis.py`.

## Key numbers

| | Jan | Feb | Mar | **Q1** |
|---|---:|---:|---:|---:|
| Orders | <!-- UNVERIFIED_CLAIM:QUARTER_ONLY -->3,217 | <!-- UNVERIFIED_CLAIM:QUARTER_ONLY -->2,615 | <!-- UNVERIFIED_CLAIM:QUARTER_ONLY -->2,832 | **<!-- claim:CLM-ORDERS:value -->8,664** |
| Gross sales | <!-- UNVERIFIED_CLAIM:QUARTER_ONLY -->578,510.00 | <!-- UNVERIFIED_CLAIM:QUARTER_ONLY -->496,406.00 | <!-- UNVERIFIED_CLAIM:QUARTER_ONLY -->527,161.00 | <!-- claim:CLM-GROSS-SALES:value -->1,602,077.00 |
| – Discounts | <!-- UNVERIFIED_CLAIM:QUARTER_ONLY -->15,368.05 | <!-- UNVERIFIED_CLAIM:QUARTER_ONLY -->12,932.70 | <!-- UNVERIFIED_CLAIM:QUARTER_ONLY -->15,377.20 | <!-- claim:CLM-DISCOUNTS:value -->43,677.95 |
| – Refunds | <!-- UNVERIFIED_CLAIM:QUARTER_ONLY -->34,003.77 | <!-- UNVERIFIED_CLAIM:QUARTER_ONLY -->24,483.08 | <!-- UNVERIFIED_CLAIM:QUARTER_ONLY -->24,515.22 | <!-- claim:CLM-REFUNDS:value -->83,002.07 |
| **Net sales** | **<!-- claim:CLM-NET-SALES-JAN:value -->529,138.18** | **<!-- claim:CLM-NET-SALES-FEB:value -->458,990.22** | **<!-- claim:CLM-NET-SALES-MAR:value -->487,268.58** | **<!-- claim:CLM-NET-SALES:value -->1,475,396.98** |
| Average order value | <!-- UNVERIFIED_CLAIM:DIFFERENT_DEFINITION -->175.05 | <!-- UNVERIFIED_CLAIM:DIFFERENT_DEFINITION -->184.88 | <!-- UNVERIFIED_CLAIM:DIFFERENT_DEFINITION -->180.71 | **<!-- UNVERIFIED_CLAIM:DIFFERENT_DEFINITION -->179.87** |

- **Net sales** = gross sales (list price × quantity) − discounts − refunds. Net sales excluding VAT for Q1: **€<!-- UNVERIFIED_CLAIM:DIFFERENT_DEFINITION -->1,230,049.35** (each order's own VAT share removed; VAT rates 16–19% by country).
- **Average order value** = order value after discounts, before refunds, excluding shipping (€<!-- claim:CLM-PRODUCT-SALES-TOTAL:value -->1,558,399.05 / <!-- claim:CLM-ORDERS:again2 -->8,664).

## Refunds
- Refunded product value: **€<!-- claim:CLM-REFUNDS:again2 -->83,002.07 = <!-- UNVERIFIED_CLAIM:DIFFERENT_DEFINITION -->5.33%** of order value (after discounts).
- **<!-- claim:CLM-REFUNDED-ORDERS:value -->803 of <!-- claim:CLM-ORDERS:again3 -->8,664 orders (<!-- claim:CLM-REFUND-RATE:value -->9.27%)** had a full or partial refund (<!-- UNVERIFIED_CLAIM:NOT_COMPUTED -->364 full, <!-- UNVERIFIED_CLAIM:NOT_COMPUTED -->439 partial).
- Customers were also refunded €<!-- UNVERIFIED_CLAIM:NOT_COMPUTED -->1,815.05 of shipping, so the refunded total in the export is €<!-- UNVERIFIED_CLAIM:DIFFERENT_DEFINITION -->84,817.12.
- By month (refund value as % of order value): Jan <!-- UNVERIFIED_CLAIM:DIFFERENT_DEFINITION -->6.04%, Feb <!-- UNVERIFIED_CLAIM:DIFFERENT_DEFINITION -->5.06%, Mar <!-- UNVERIFIED_CLAIM:DIFFERENT_DEFINITION -->4.79%.

## Discounts
- **€<!-- claim:CLM-DISCOUNTS:again2 -->43,677.95** in total = <!-- claim:CLM-DISCOUNT-SHARE:value -->2.73% of gross sales. <!-- UNVERIFIED_CLAIM:NOT_COMPUTED -->1,910 orders (<!-- UNVERIFIED_CLAIM:NOT_COMPUTED -->22.0%) used a code.
- By code: VIP20 <!-- UNVERIFIED_CLAIM:NOT_COMPUTED -->13,271.60 · WELCOME10 <!-- UNVERIFIED_CLAIM:NOT_COMPUTED -->10,519.70 · WINTER15 <!-- UNVERIFIED_CLAIM:NOT_COMPUTED -->7,919.25 · SPRING20 <!-- UNVERIFIED_CLAIM:NOT_COMPUTED -->6,437.40 · TENOFF <!-- UNVERIFIED_CLAIM:NOT_COMPUTED -->5,530.00.

## Top 10 products by sales
Sales = price × quantity after discounts, before refunds (Q1 total: €<!-- claim:CLM-PRODUCT-SALES-TOTAL:again2 -->1,558,399.05).

| # | Product | Units | Sales (€) | Share |
|---|---|---:|---:|---:|
| 1 | Fjord Rain Jacket | <!-- UNVERIFIED_CLAIM:NOT_COMPUTED -->1,385 | <!-- claim:CLM-PRODUCT-JKT-RAIN:value -->254,356.47 | <!-- UNVERIFIED_CLAIM:NOT_COMPUTED -->16.3% |
| 2 | Polar Down Jacket | <!-- UNVERIFIED_CLAIM:NOT_COMPUTED -->1,048 | <!-- claim:CLM-PRODUCT-JKT-DOWN:value -->243,146.58 | <!-- UNVERIFIED_CLAIM:NOT_COMPUTED -->15.6% |
| 3 | Trail Hiking Trousers | <!-- UNVERIFIED_CLAIM:NOT_COMPUTED -->1,118 | <!-- claim:CLM-PRODUCT-PNT-HIKE:value -->107,314.28 | <!-- UNVERIFIED_CLAIM:NOT_COMPUTED -->6.9% |
| 4 | Ridge Fleece Midlayer | <!-- UNVERIFIED_CLAIM:NOT_COMPUTED -->1,272 | <!-- claim:CLM-PRODUCT-FLC-MID:value -->104,474.86 | <!-- UNVERIFIED_CLAIM:NOT_COMPUTED -->6.7% |
| 5 | Merino Base Layer Top | <!-- UNVERIFIED_CLAIM:NOT_COMPUTED -->1,486 | <!-- claim:CLM-PRODUCT-BSL-TOP:value -->99,507.22 | <!-- UNVERIFIED_CLAIM:NOT_COMPUTED -->6.4% |
| 6 | Solo Trekking Tent | <!-- UNVERIFIED_CLAIM:NOT_COMPUTED -->281 | <!-- claim:CLM-PRODUCT-TNT-SOLO:value -->90,240.93 | <!-- UNVERIFIED_CLAIM:NOT_COMPUTED -->5.8% |
| 7 | Summit Daypack | <!-- UNVERIFIED_CLAIM:NOT_COMPUTED -->744 | <!-- claim:CLM-PRODUCT-BAG-DAY:value -->85,738.08 | <!-- UNVERIFIED_CLAIM:NOT_COMPUTED -->5.5% |
| 8 | Down Sleeping Bag | <!-- UNVERIFIED_CLAIM:NOT_COMPUTED -->326 | <!-- claim:CLM-PRODUCT-SLP-DOWN:value -->84,666.39 | <!-- UNVERIFIED_CLAIM:NOT_COMPUTED -->5.4% |
| 9 | Storm Shell Trousers | <!-- UNVERIFIED_CLAIM:NOT_COMPUTED -->547 | <!-- claim:CLM-PRODUCT-PNT-SHELL:value -->74,433.62 | <!-- UNVERIFIED_CLAIM:NOT_COMPUTED -->4.8% |
| 10 | Hiking Socks Pair | <!-- UNVERIFIED_CLAIM:NOT_COMPUTED -->3,659 | <!-- claim:CLM-PRODUCT-SCK-HIKE:value -->67,465.31 | <!-- UNVERIFIED_CLAIM:NOT_COMPUTED -->4.3% |

The top 10 make up <!-- UNVERIFIED_CLAIM:NOT_COMPUTED -->77.7% of sales. The two jackets alone are <!-- UNVERIFIED_CLAIM:NOT_COMPUTED -->31.9%.

## Repeat customers
- <!-- claim:CLM-CUSTOMERS:value -->5,957 customers (identified by email) placed orders in Q1; **<!-- claim:CLM-REPEAT-CUSTOMERS:value -->1,392 (<!-- claim:CLM-REPEAT-CUSTOMER-RATE:value -->23.4%) ordered more than once**, <!-- UNVERIFIED_CLAIM:NOT_COMPUTED -->551 of them three or more times.
- Repeat customers account for <!-- UNVERIFIED_CLAIM:NOT_COMPUTED -->45.3% of orders.
- Limits: this covers Q1 only (earlier purchases are not in the export), and <!-- UNVERIFIED_CLAIM:NOT_COMPUTED -->318 orders without an email (mostly pop-up store cash sales) cannot be linked to a customer.

## Sales by channel (net sales)

| Channel | Orders | Net sales (€) | Share |
|---|---:|---:|---:|
| Online store | <!-- UNVERIFIED_CLAIM:NOT_COMPUTED -->7,850 | <!-- claim:CLM-NET-SALES-WEB:value -->1,325,008.08 | <!-- UNVERIFIED_CLAIM:NOT_COMPUTED -->89.8% |
| POS (Pop-up Store Hamburg) | <!-- UNVERIFIED_CLAIM:NOT_COMPUTED -->531 | <!-- claim:CLM-NET-SALES-POS:value -->99,157.00 | <!-- UNVERIFIED_CLAIM:NOT_COMPUTED -->6.7% |
| Draft orders – phone orders | <!-- UNVERIFIED_CLAIM:NOT_COMPUTED -->196 | <!-- UNVERIFIED_CLAIM:NOT_COMPUTED -->36,860.20 | <!-- UNVERIFIED_CLAIM:NOT_COMPUTED -->2.5% |
| Draft orders – wholesale | <!-- UNVERIFIED_CLAIM:NOT_COMPUTED -->87 | <!-- UNVERIFIED_CLAIM:NOT_COMPUTED -->14,371.70 | <!-- UNVERIFIED_CLAIM:NOT_COMPUTED -->1.0% |
| **Total** | **<!-- claim:CLM-ORDERS:again4 -->8,664** | **<!-- claim:CLM-NET-SALES:again2 -->1,475,396.98** | 100% |

## How the data was cleaned (please read before presenting)
The raw file has <!-- UNVERIFIED_CLAIM:CLEANING_NOT_PUBLISHED -->9,659 orders, but <!-- UNVERIFIED_CLAIM:CLEANING_NOT_PUBLISHED -->9,159 were created in Q1 and only **<!-- claim:CLM-ORDERS:again5 -->8,664 are counted**:
- **<!-- UNVERIFIED_CLAIM:CLEANING_NOT_PUBLISHED -->1,068 orders were listed twice** in the export (identical rows at the end of the file). Removed. Left in, sales would be overstated by roughly <!-- UNVERIFIED_CLAIM:NOT_COMPUTED -->11%.
- **Excluded from Q1:** <!-- UNVERIFIED_CLAIM:CLEANING_NOT_PUBLISHED -->84 internal orders (test/QA orders paid with a dummy gateway, and staff orders; €<!-- UNVERIFIED_CLAIM:CLEANING_NOT_PUBLISHED -->15,472 of order value), <!-- UNVERIFIED_CLAIM:CLEANING_NOT_PUBLISHED -->260 cancelled orders (voided, or cancelled and fully refunded, all unfulfilled; €<!-- UNVERIFIED_CLAIM:CLEANING_NOT_PUBLISHED -->48,264.50), and <!-- UNVERIFIED_CLAIM:CLEANING_NOT_PUBLISHED -->151 unpaid orders (payment only authorized or pending; €<!-- UNVERIFIED_CLAIM:CLEANING_NOT_PUBLISHED -->27,097.65).
- **Orders outside Q1** (29–31 Dec and 1–3 Apr, about <!-- UNVERIFIED_CLAIM:CLEANING_NOT_PUBLISHED -->500) are excluded.
- **Refund timing:** the export has no refund date, so each refund is counted in the month the order was placed, not the month it was paid out.
- Refunds on fully refunded orders include shipping. Only the product share reduces net sales.
- Excluding cancelled orders makes the refund rate relate to orders that were actually fulfilled. Counting them would raise the refund rate.
