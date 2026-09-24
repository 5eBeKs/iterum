# Reconciliation of the report's figures with the export

Every number of the report `client/report.md` submitted for checking was recomputed from the export, independently of the calculation the report rests on. This document computes nothing: every value in it was written by the checks of the run, and it is sealed together with them.

The contracts of the check were fixed at 2026-09-23 18:30 UTC.

## Summary

Submitted for checking: 113. Matches: 27. Does not match: 8. Not confirmed: 0. Cannot be verified: 78.

## The report's numbers

| Where | In the report | What it means | From the export | Tolerance | Status |
|---|---|---|---|---|---|
|  | 3,217 | Orders counted in January 2026 |  |  | cannot be verified |
|  | 2,615 | Orders counted in February 2026 |  |  | cannot be verified |
|  | 2,832 | Orders counted in March 2026 |  |  | cannot be verified |
|  | 578,510.00 | Gross sales of January 2026, EUR |  |  | cannot be verified |
|  | 496,406.00 | Gross sales of February 2026, EUR |  |  | cannot be verified |
|  | 527,161.00 | Gross sales of March 2026, EUR |  |  | cannot be verified |
| line 10 | 1,602,077.00 | Gross sales in Q1 2026 (list price times quantity, before discount codes and refunds), EUR including VAT, excluding shipping; sale orders created in Q1 2026 (shop time): paid, partially refunded or refunded, not cancelled, not a test or staff order | 1602077.00 | ±0.01 EUR | matches |
| line 9 | 8,664 | Orders in Q1 2026: sale orders created in Q1 2026 (shop time): paid, partially refunded or refunded, not cancelled, not a test or staff order | 8664 | exact | matches |
|  | 15,368.05 | Discounts of January 2026, EUR |  |  | cannot be verified |
|  | 12,932.70 | Discounts of February 2026, EUR |  |  | cannot be verified |
|  | 15,377.20 | Discounts of March 2026, EUR |  |  | cannot be verified |
| line 11 | 43,677.95 | Discount codes in Q1 2026, EUR including VAT; sale orders created in Q1 2026 (shop time): paid, partially refunded or refunded, not cancelled, not a test or staff order | 43677.95 | ±0.01 EUR | matches |
|  | 34,003.77 | Refunds of January 2026 orders, EUR |  |  | cannot be verified |
|  | 24,483.08 | Refunds of February 2026 orders, EUR |  |  | cannot be verified |
|  | 24,515.22 | Refunds of March 2026 orders, EUR |  |  | cannot be verified |
| line 12 | 83,002.07 | Refunds of goods on Q1 2026 orders (shipping refunds excluded), EUR including VAT; sale orders created in Q1 2026 (shop time): paid, partially refunded or refunded, not cancelled, not a test or staff order | 83507.42 | ±0.01 EUR | does not match: 83,002.07 in the report, 83507.42 from the export |
| line 13 | 529,138.18 | Net sales of the orders created in January 2026 (gross sales minus discounts minus refunds of goods), EUR including VAT, excluding shipping | 528930.40 | ±0.01 EUR | does not match: 529,138.18 in the report, 528930.40 from the export |
| line 13 | 458,990.22 | Net sales of the orders created in February 2026 (gross sales minus discounts minus refunds of goods), EUR including VAT, excluding shipping | 458841.03 | ±0.01 EUR | does not match: 458,990.22 in the report, 458841.03 from the export |
| line 13 | 487,268.58 | Net sales of the orders created in March 2026 (gross sales minus discounts minus refunds of goods), EUR including VAT, excluding shipping | 487120.20 | ±0.01 EUR | does not match: 487,268.58 in the report, 487120.20 from the export |
| line 13 | 1,475,396.98 | Net sales in Q1 2026 (gross sales minus discounts minus refunds of goods), EUR including VAT, excluding shipping; sale orders created in Q1 2026 (shop time): paid, partially refunded or refunded, not cancelled, not a test or staff order | 1474891.63 | ±0.01 EUR | does not match: 1,475,396.98 in the report, 1474891.63 from the export |
|  | 175.05 | Average order value of January 2026, EUR |  |  | cannot be verified |
|  | 184.88 | Average order value of February 2026, EUR |  |  | cannot be verified |
|  | 180.71 | Average order value of March 2026, EUR |  |  | cannot be verified |
|  | 179.87 | Average order value in Q1 2026, EUR |  |  | cannot be verified |
|  | 1,230,049.35 | Net sales excluding VAT in Q1 2026, EUR |  |  | cannot be verified |
| line 17 | 1,558,399.05 | Order value in Q1 2026 after discount codes and before refunds, EUR including VAT, excluding shipping; sale orders created in Q1 2026 (shop time): paid, partially refunded or refunded, not cancelled, not a test or staff order | 1558399.05 | ±0.01 EUR | matches |
| line 17 | 8,664 | Orders in Q1 2026, the divisor of the average order value | 8664 | exact | matches |
| line 20 | 83,002.07 | Refunded product value in Q1 2026, EUR | 83507.42 | ±0.01 EUR | does not match: 83,002.07 in the report, 83507.42 from the export |
|  | 5.33% | Refunds as a share of order value, Q1 2026 |  |  | cannot be verified |
| line 21 | 803 | Orders of Q1 2026 with a full or partial refund (Financial Status refunded or partially_refunded) | 803 | exact | matches |
| line 21 | 8,664 | Orders in Q1 2026, the base of the refund rate | 8664 | exact | matches |
| line 21 | 9.27% | Share of Q1 2026 orders with a full or partial refund, in percent | 9.27% | ±0.000001 proportion | matches |
|  | 364 | Orders fully refunded |  |  | cannot be verified |
|  | 439 | Orders partially refunded |  |  | cannot be verified |
|  | 1,815.05 | Shipping refunded to customers, EUR |  |  | cannot be verified |
|  | 84,817.12 | Refunded total in the export, shipping included, EUR |  |  | cannot be verified |
|  | 6.04% | Refunds as a share of order value, January 2026 |  |  | cannot be verified |
|  | 5.06% | Refunds as a share of order value, February 2026 |  |  | cannot be verified |
|  | 4.79% | Refunds as a share of order value, March 2026 |  |  | cannot be verified |
| line 26 | 43,677.95 | Discounts in Q1 2026, EUR | 43677.95 | ±0.01 EUR | matches |
| line 26 | 2.73% | Discount codes as a share of gross sales in Q1 2026, in percent | 2.73% | ±0.000001 proportion | matches |
|  | 1,910 | Orders that used a discount code |  |  | cannot be verified |
|  | 22.0% | Share of orders that used a discount code |  |  | cannot be verified |
|  | 13,271.60 | Discounts given under the code VIP20, EUR |  |  | cannot be verified |
|  | 10,519.70 | Discounts given under the code WELCOME10, EUR |  |  | cannot be verified |
|  | 7,919.25 | Discounts given under the code WINTER15, EUR |  |  | cannot be verified |
|  | 6,437.40 | Discounts given under the code SPRING20, EUR |  |  | cannot be verified |
|  | 5,530.00 | Discounts given under the code TENOFF, EUR |  |  | cannot be verified |
| line 30 | 1,558,399.05 | Sales of all products in Q1 2026, after discounts, before refunds, EUR | 1558399.05 | ±0.01 EUR | matches |
|  | 1,385 | Units of Fjord Rain Jacket sold in Q1 2026 |  |  | cannot be verified |
| line 34 | 254,356.47 | Sales of Fjord Rain Jacket (SKU NLO-JKT-RAIN) in Q1 2026: quantity times price minus line discount, before refunds, EUR including VAT | 254356.47 | ±0.01 EUR | matches |
|  | 16.3% | Share of Fjord Rain Jacket in all product sales |  |  | cannot be verified |
|  | 1,048 | Units of Polar Down Jacket sold in Q1 2026 |  |  | cannot be verified |
| line 35 | 243,146.58 | Sales of Polar Down Jacket (SKU NLO-JKT-DOWN) in Q1 2026: quantity times price minus line discount, before refunds, EUR including VAT | 243146.58 | ±0.01 EUR | matches |
|  | 15.6% | Share of Polar Down Jacket in all product sales |  |  | cannot be verified |
|  | 1,118 | Units of Trail Hiking Trousers sold in Q1 2026 |  |  | cannot be verified |
| line 36 | 107,314.28 | Sales of Trail Hiking Trousers (SKU NLO-PNT-HIKE) in Q1 2026: quantity times price minus line discount, before refunds, EUR including VAT | 107314.28 | ±0.01 EUR | matches |
|  | 6.9% | Share of Trail Hiking Trousers in all product sales |  |  | cannot be verified |
|  | 1,272 | Units of Ridge Fleece Midlayer sold in Q1 2026 |  |  | cannot be verified |
| line 37 | 104,474.86 | Sales of Ridge Fleece Midlayer (SKU NLO-FLC-MID) in Q1 2026: quantity times price minus line discount, before refunds, EUR including VAT | 104474.86 | ±0.01 EUR | matches |
|  | 6.7% | Share of Ridge Fleece Midlayer in all product sales |  |  | cannot be verified |
|  | 1,486 | Units of Merino Base Layer Top sold in Q1 2026 |  |  | cannot be verified |
| line 38 | 99,507.22 | Sales of Merino Base Layer Top (SKU NLO-BSL-TOP) in Q1 2026: quantity times price minus line discount, before refunds, EUR including VAT | 99507.22 | ±0.01 EUR | matches |
|  | 6.4% | Share of Merino Base Layer Top in all product sales |  |  | cannot be verified |
|  | 281 | Units of Solo Trekking Tent sold in Q1 2026 |  |  | cannot be verified |
| line 39 | 90,240.93 | Sales of Solo Trekking Tent (SKU NLO-TNT-SOLO) in Q1 2026: quantity times price minus line discount, before refunds, EUR including VAT | 90240.93 | ±0.01 EUR | matches |
|  | 5.8% | Share of Solo Trekking Tent in all product sales |  |  | cannot be verified |
|  | 744 | Units of Summit Daypack sold in Q1 2026 |  |  | cannot be verified |
| line 40 | 85,738.08 | Sales of Summit Daypack (SKU NLO-BAG-DAY) in Q1 2026: quantity times price minus line discount, before refunds, EUR including VAT | 85738.08 | ±0.01 EUR | matches |
|  | 5.5% | Share of Summit Daypack in all product sales |  |  | cannot be verified |
|  | 326 | Units of Down Sleeping Bag sold in Q1 2026 |  |  | cannot be verified |
| line 41 | 84,666.39 | Sales of Down Sleeping Bag (SKU NLO-SLP-DOWN) in Q1 2026: quantity times price minus line discount, before refunds, EUR including VAT | 84666.39 | ±0.01 EUR | matches |
|  | 5.4% | Share of Down Sleeping Bag in all product sales |  |  | cannot be verified |
|  | 547 | Units of Storm Shell Trousers sold in Q1 2026 |  |  | cannot be verified |
| line 42 | 74,433.62 | Sales of Storm Shell Trousers (SKU NLO-PNT-SHELL) in Q1 2026: quantity times price minus line discount, before refunds, EUR including VAT | 74433.62 | ±0.01 EUR | matches |
|  | 4.8% | Share of Storm Shell Trousers in all product sales |  |  | cannot be verified |
|  | 3,659 | Units of Hiking Socks Pair sold in Q1 2026 |  |  | cannot be verified |
| line 43 | 67,465.31 | Sales of Hiking Socks Pair (SKU NLO-SCK-HIKE) in Q1 2026: quantity times price minus line discount, before refunds, EUR including VAT | 67465.31 | ±0.01 EUR | matches |
|  | 4.3% | Share of Hiking Socks Pair in all product sales |  |  | cannot be verified |
|  | 77.7% | Share of the top 10 products in all product sales |  |  | cannot be verified |
|  | 31.9% | Share of the two jackets in all product sales |  |  | cannot be verified |
| line 48 | 5,957 | Customers (by email address) with a sale order in Q1 2026 | 5957 | exact | matches |
| line 48 | 1,392 | Customers (by email address) with two or more sale orders in Q1 2026 | 1392 | exact | matches |
| line 48 | 23.4% | Share of customers with two or more sale orders in Q1 2026, in percent | 23.4% | ±0.000001 proportion | matches |
|  | 551 | Customers with three or more orders |  |  | cannot be verified |
|  | 45.3% | Share of orders placed by repeat customers |  |  | cannot be verified |
|  | 318 | Orders without an email address |  |  | cannot be verified |
|  | 7,850 | Orders through the online store |  |  | cannot be verified |
| line 56 | 1,325,008.08 | Net sales of the online store (Source web) in Q1 2026, EUR including VAT, excluding shipping | 1324502.73 | ±0.01 EUR | does not match: 1,325,008.08 in the report, 1324502.73 from the export |
|  | 89.8% | Online store's share of net sales |  |  | cannot be verified |
|  | 531 | Orders at the point of sale |  |  | cannot be verified |
| line 57 | 99,157.00 | Net sales at the point of sale (Source pos, the Hamburg pop-up store) in Q1 2026, EUR including VAT | 99157.00 | ±0.01 EUR | matches |
|  | 6.7% | Point of sale's share of net sales |  |  | cannot be verified |
|  | 196 | Draft orders: phone orders, number of orders |  |  | cannot be verified |
|  | 36,860.20 | Net sales of draft orders: phone orders, EUR |  |  | cannot be verified |
|  | 2.5% | Share of draft orders: phone orders in net sales |  |  | cannot be verified |
|  | 87 | Draft orders: wholesale orders, number of orders |  |  | cannot be verified |
|  | 14,371.70 | Net sales of draft orders: wholesale orders, EUR |  |  | cannot be verified |
|  | 1.0% | Share of draft orders: wholesale orders in net sales |  |  | cannot be verified |
| line 60 | 8,664 | Orders in Q1 2026, total of the channel table | 8664 | exact | matches |
| line 60 | 1,475,396.98 | Net sales in Q1 2026, total of the channel table, EUR | 1474891.63 | ±0.01 EUR | does not match: 1,475,396.98 in the report, 1474891.63 from the export |
|  | 9,659 | Orders in the raw file |  |  | cannot be verified |
|  | 9,159 | Orders created in Q1 2026, before exclusions |  |  | cannot be verified |
| line 63 | 8,664 | Orders counted in Q1 2026 | 8664 | exact | matches |
|  | 1,068 | Orders listed twice in the export |  |  | cannot be verified |
|  | 11% | How much sales would be overstated with the duplicates left in |  |  | cannot be verified |
|  | 84 | Internal (test and staff) orders excluded |  |  | cannot be verified |
|  | 15,472 | Order value of the internal orders excluded, EUR |  |  | cannot be verified |
|  | 260 | Cancelled orders excluded |  |  | cannot be verified |
|  | 48,264.50 | Order value of the cancelled orders excluded, EUR |  |  | cannot be verified |
|  | 151 | Unpaid orders excluded |  |  | cannot be verified |
|  | 27,097.65 | Order value of the unpaid orders excluded, EUR |  |  | cannot be verified |
|  | 500 | Orders created outside Q1 2026 |  |  | cannot be verified |

### What the statuses mean

- **matches**: the number in the report equals the recomputation from the export, to the digits it is printed in.
- **does not match**: the number in the report differs from the recomputation from the export.
- **not confirmed**: the pack's calculation and the independent recomputation from the raw rows disagree with each other; the fault is in the calculation, not in the report, and the number can be called neither right nor wrong.
- **cannot be verified**: the number cannot be recomputed from this export; the reason is given below.

## Cannot be verified

- 3,217 (Orders counted in January 2026): The checked code computes the number of sale orders for the whole quarter only, not for one month. `QUARTER_ONLY`
- 2,615 (Orders counted in February 2026): The checked code computes the number of sale orders for the whole quarter only, not for one month. `QUARTER_ONLY`
- 2,832 (Orders counted in March 2026): The checked code computes the number of sale orders for the whole quarter only, not for one month. `QUARTER_ONLY`
- 578,510.00 (Gross sales of January 2026, EUR): The checked code computes gross sales for the whole quarter only, not for one month. `QUARTER_ONLY`
- 496,406.00 (Gross sales of February 2026, EUR): The checked code computes gross sales for the whole quarter only, not for one month. `QUARTER_ONLY`
- 527,161.00 (Gross sales of March 2026, EUR): The checked code computes gross sales for the whole quarter only, not for one month. `QUARTER_ONLY`
- 15,368.05 (Discounts of January 2026, EUR): The checked code computes discounts for the whole quarter only, not for one month. `QUARTER_ONLY`
- 12,932.70 (Discounts of February 2026, EUR): The checked code computes discounts for the whole quarter only, not for one month. `QUARTER_ONLY`
- 15,377.20 (Discounts of March 2026, EUR): The checked code computes discounts for the whole quarter only, not for one month. `QUARTER_ONLY`
- 34,003.77 (Refunds of January 2026 orders, EUR): The checked code computes refunds for the whole quarter only, not for one month. `QUARTER_ONLY`
- 24,483.08 (Refunds of February 2026 orders, EUR): The checked code computes refunds for the whole quarter only, not for one month. `QUARTER_ONLY`
- 24,515.22 (Refunds of March 2026 orders, EUR): The checked code computes refunds for the whole quarter only, not for one month. `QUARTER_ONLY`
- 175.05 (Average order value of January 2026, EUR): A different definition from the one the checked code computes: one month's order value after discounts and before refunds, over that month's orders; the checked code's average order value is net sales after refunds over orders, and for the whole quarter only. `DIFFERENT_DEFINITION`
- 184.88 (Average order value of February 2026, EUR): A different definition from the one the checked code computes: one month's order value after discounts and before refunds, over that month's orders; the checked code's average order value is net sales after refunds over orders, and for the whole quarter only. `DIFFERENT_DEFINITION`
- 180.71 (Average order value of March 2026, EUR): A different definition from the one the checked code computes: one month's order value after discounts and before refunds, over that month's orders; the checked code's average order value is net sales after refunds over orders, and for the whole quarter only. `DIFFERENT_DEFINITION`
- 179.87 (Average order value in Q1 2026, EUR): A different definition from the one the checked code computes: order value after discounts and before refunds (1,558,399.05) over orders; the checked code's average order value is net sales after refunds over orders. `DIFFERENT_DEFINITION`
- 1,230,049.35 (Net sales excluding VAT in Q1 2026, EUR): A different definition from the one the checked code computes: net sales with each order's VAT share taken out; the checked code computes sales including VAT, and the owner's ruling is that partial refunds carry no VAT split, so a figure without VAT cannot be recomputed exactly. `DIFFERENT_DEFINITION`
- 5.33% (Refunds as a share of order value, Q1 2026): A different definition from the one the checked code computes: refunds as a share of order value; the checked code's refund rate is the share of orders with a refund. `DIFFERENT_DEFINITION`
- 364 (Orders fully refunded): The checked code does not compute this figure: it counts orders with a full or a partial refund together, and does not split them. `NOT_COMPUTED`
- 439 (Orders partially refunded): The checked code does not compute this figure: it counts orders with a full or a partial refund together, and does not split them. `NOT_COMPUTED`
- 1,815.05 (Shipping refunded to customers, EUR): The checked code does not compute this figure: it computes refunds of goods only, and no figure for shipping refunded. `NOT_COMPUTED`
- 84,817.12 (Refunded total in the export, shipping included, EUR): A different definition from the one the checked code computes: the export's whole refunded amount, shipping included; the checked code computes refunds of goods only. `DIFFERENT_DEFINITION`
- 6.04% (Refunds as a share of order value, January 2026): A different definition from the one the checked code computes: one month's refunds as a share of its order value; the checked code's refund rate is the share of orders with a refund, and for the whole quarter only. `DIFFERENT_DEFINITION`
- 5.06% (Refunds as a share of order value, February 2026): A different definition from the one the checked code computes: one month's refunds as a share of its order value; the checked code's refund rate is the share of orders with a refund, and for the whole quarter only. `DIFFERENT_DEFINITION`
- 4.79% (Refunds as a share of order value, March 2026): A different definition from the one the checked code computes: one month's refunds as a share of its order value; the checked code's refund rate is the share of orders with a refund, and for the whole quarter only. `DIFFERENT_DEFINITION`
- 1,910 (Orders that used a discount code): The checked code does not compute this figure: it computes the discount amount, not the number of orders that used a code. `NOT_COMPUTED`
- 22.0% (Share of orders that used a discount code): The checked code does not compute this figure: it computes the discount amount, not the share of orders that used a code. `NOT_COMPUTED`
- 13,271.60 (Discounts given under the code VIP20, EUR): The checked code does not compute this figure: it computes discounts for all codes together, not per code. `NOT_COMPUTED`
- 10,519.70 (Discounts given under the code WELCOME10, EUR): The checked code does not compute this figure: it computes discounts for all codes together, not per code. `NOT_COMPUTED`
- 7,919.25 (Discounts given under the code WINTER15, EUR): The checked code does not compute this figure: it computes discounts for all codes together, not per code. `NOT_COMPUTED`
- 6,437.40 (Discounts given under the code SPRING20, EUR): The checked code does not compute this figure: it computes discounts for all codes together, not per code. `NOT_COMPUTED`
- 5,530.00 (Discounts given under the code TENOFF, EUR): The checked code does not compute this figure: it computes discounts for all codes together, not per code. `NOT_COMPUTED`
- 1,385 (Units of Fjord Rain Jacket sold in Q1 2026): The checked code does not compute this figure: it computes each product's sales in euros, not the units sold. `NOT_COMPUTED`
- 16.3% (Share of Fjord Rain Jacket in all product sales): The checked code does not compute this figure: it computes each product's sales and the total, not the share of one in the other. `NOT_COMPUTED`
- 1,048 (Units of Polar Down Jacket sold in Q1 2026): The checked code does not compute this figure: it computes each product's sales in euros, not the units sold. `NOT_COMPUTED`
- 15.6% (Share of Polar Down Jacket in all product sales): The checked code does not compute this figure: it computes each product's sales and the total, not the share of one in the other. `NOT_COMPUTED`
- 1,118 (Units of Trail Hiking Trousers sold in Q1 2026): The checked code does not compute this figure: it computes each product's sales in euros, not the units sold. `NOT_COMPUTED`
- 6.9% (Share of Trail Hiking Trousers in all product sales): The checked code does not compute this figure: it computes each product's sales and the total, not the share of one in the other. `NOT_COMPUTED`
- 1,272 (Units of Ridge Fleece Midlayer sold in Q1 2026): The checked code does not compute this figure: it computes each product's sales in euros, not the units sold. `NOT_COMPUTED`
- 6.7% (Share of Ridge Fleece Midlayer in all product sales): The checked code does not compute this figure: it computes each product's sales and the total, not the share of one in the other. `NOT_COMPUTED`
- 1,486 (Units of Merino Base Layer Top sold in Q1 2026): The checked code does not compute this figure: it computes each product's sales in euros, not the units sold. `NOT_COMPUTED`
- 6.4% (Share of Merino Base Layer Top in all product sales): The checked code does not compute this figure: it computes each product's sales and the total, not the share of one in the other. `NOT_COMPUTED`
- 281 (Units of Solo Trekking Tent sold in Q1 2026): The checked code does not compute this figure: it computes each product's sales in euros, not the units sold. `NOT_COMPUTED`
- 5.8% (Share of Solo Trekking Tent in all product sales): The checked code does not compute this figure: it computes each product's sales and the total, not the share of one in the other. `NOT_COMPUTED`
- 744 (Units of Summit Daypack sold in Q1 2026): The checked code does not compute this figure: it computes each product's sales in euros, not the units sold. `NOT_COMPUTED`
- 5.5% (Share of Summit Daypack in all product sales): The checked code does not compute this figure: it computes each product's sales and the total, not the share of one in the other. `NOT_COMPUTED`
- 326 (Units of Down Sleeping Bag sold in Q1 2026): The checked code does not compute this figure: it computes each product's sales in euros, not the units sold. `NOT_COMPUTED`
- 5.4% (Share of Down Sleeping Bag in all product sales): The checked code does not compute this figure: it computes each product's sales and the total, not the share of one in the other. `NOT_COMPUTED`
- 547 (Units of Storm Shell Trousers sold in Q1 2026): The checked code does not compute this figure: it computes each product's sales in euros, not the units sold. `NOT_COMPUTED`
- 4.8% (Share of Storm Shell Trousers in all product sales): The checked code does not compute this figure: it computes each product's sales and the total, not the share of one in the other. `NOT_COMPUTED`
- 3,659 (Units of Hiking Socks Pair sold in Q1 2026): The checked code does not compute this figure: it computes each product's sales in euros, not the units sold. `NOT_COMPUTED`
- 4.3% (Share of Hiking Socks Pair in all product sales): The checked code does not compute this figure: it computes each product's sales and the total, not the share of one in the other. `NOT_COMPUTED`
- 77.7% (Share of the top 10 products in all product sales): The checked code does not compute this figure: it computes each product's sales and the total, not the share of the ten largest. `NOT_COMPUTED`
- 31.9% (Share of the two jackets in all product sales): The checked code does not compute this figure: it computes each product's sales and the total, not the share of the two jackets. `NOT_COMPUTED`
- 551 (Customers with three or more orders): The checked code does not compute this figure: it counts customers with two or more orders, not three or more. `NOT_COMPUTED`
- 45.3% (Share of orders placed by repeat customers): The checked code does not compute this figure: it computes the share of customers who ordered again, not the share of orders they placed. `NOT_COMPUTED`
- 318 (Orders without an email address): The checked code does not compute this figure: it leaves orders without an email out of the customer count and publishes no count of them. `NOT_COMPUTED`
- 7,850 (Orders through the online store): The checked code does not compute this figure: it computes net sales per sales channel, not the number of orders. `NOT_COMPUTED`
- 89.8% (Online store's share of net sales): The checked code does not compute this figure: it computes net sales per sales channel, not a channel's share of them. `NOT_COMPUTED`
- 531 (Orders at the point of sale): The checked code does not compute this figure: it computes net sales per sales channel, not the number of orders. `NOT_COMPUTED`
- 6.7% (Point of sale's share of net sales): The checked code does not compute this figure: it computes net sales per sales channel, not a channel's share of them. `NOT_COMPUTED`
- 196 (Draft orders: phone orders, number of orders): The checked code does not compute this figure: it computes net sales per sales channel, not the number of orders. `NOT_COMPUTED`
- 36,860.20 (Net sales of draft orders: phone orders, EUR): The checked code does not compute this figure: it computes net sales of all draft orders together (Source shopify_draft_order), not split into phone and wholesale orders. `NOT_COMPUTED`
- 2.5% (Share of draft orders: phone orders in net sales): The checked code does not compute this figure: it computes net sales per sales channel, not a channel's share of them. `NOT_COMPUTED`
- 87 (Draft orders: wholesale orders, number of orders): The checked code does not compute this figure: it computes net sales per sales channel, not the number of orders. `NOT_COMPUTED`
- 14,371.70 (Net sales of draft orders: wholesale orders, EUR): The checked code does not compute this figure: it computes net sales of all draft orders together (Source shopify_draft_order), not split into phone and wholesale orders. `NOT_COMPUTED`
- 1.0% (Share of draft orders: wholesale orders in net sales): The checked code does not compute this figure: it computes net sales per sales channel, not a channel's share of them. `NOT_COMPUTED`
- 9,659 (Orders in the raw file): The checked code removes these orders from the count but publishes no figure for them: the number of distinct orders in the raw file. `CLEANING_NOT_PUBLISHED`
- 9,159 (Orders created in Q1 2026, before exclusions): The checked code removes these orders from the count but publishes no figure for them: the number of orders created in the quarter before test, staff, cancelled and unpaid orders are taken out. `CLEANING_NOT_PUBLISHED`
- 1,068 (Orders listed twice in the export): The checked code removes these orders from the count but publishes no figure for them: the number of orders the two overlapping exports list twice. `CLEANING_NOT_PUBLISHED`
- 11% (How much sales would be overstated with the duplicates left in): The checked code does not compute this figure: it removes the duplicates and does not compute what they would have added. `NOT_COMPUTED`
- 84 (Internal (test and staff) orders excluded): The checked code removes these orders from the count but publishes no figure for them: the number of test and staff orders. `CLEANING_NOT_PUBLISHED`
- 15,472 (Order value of the internal orders excluded, EUR): The checked code removes these orders from the count but publishes no figure for them: the order value of test and staff orders. `CLEANING_NOT_PUBLISHED`
- 260 (Cancelled orders excluded): The checked code removes these orders from the count but publishes no figure for them: the number of cancelled orders. `CLEANING_NOT_PUBLISHED`
- 48,264.50 (Order value of the cancelled orders excluded, EUR): The checked code removes these orders from the count but publishes no figure for them: the order value of cancelled orders. `CLEANING_NOT_PUBLISHED`
- 151 (Unpaid orders excluded): The checked code removes these orders from the count but publishes no figure for them: the number of unpaid (authorized or pending) orders. `CLEANING_NOT_PUBLISHED`
- 27,097.65 (Order value of the unpaid orders excluded, EUR): The checked code removes these orders from the count but publishes no figure for them: the order value of unpaid orders. `CLEANING_NOT_PUBLISHED`
- 500 (Orders created outside Q1 2026): The checked code removes these orders from the count but publishes no figure for them: the number of orders created before or after the quarter. `CLEANING_NOT_PUBLISHED`

## Not submitted for checking

Every number of the report was submitted for checking.

## Assumptions

Readings of what the figures mean, settled before the contracts were fixed. The numbers follow these choices rather than the data, so each is a place a reader may disagree.

| Reading | Decision | Recorded as |
|---|---|---|
| `sale_status_basis` — Какой статус заказа считается продажей в отчётном периоде? | `paid_any_status` | Ilya, 2026-09-23 (reasoned by Claude (claude-opus-5-5, architect subagent) under Ilya delegation for test runs) -- the export has no delivery status; a captured payment is a sale and a refund after it is a return |
| `cancelled_order_policy` — Как считать отменённые заказы? | `excluded_from_population` | Ilya, 2026-09-23 (reasoned by Claude (claude-opus-5-5, architect subagent) under Ilya delegation for test runs) -- a cancelled order is voided or refunded at once; neither a sale nor a return |
| `test_order_policy` — Как распознаются и куда деваются тестовые и внутренние заказы? | `excluded_by_flag` | Ilya, 2026-09-23 (reasoned by Claude (claude-opus-5-5, architect subagent) under Ilya delegation for test runs) -- Tags test and staff mark the shop's internal orders; the vocabulary is closed at gate0 |
| `order_grain` — Что такое одна строка популяции: заказ или строка заказа? | `one_row_per_order` | Ilya, 2026-09-23 (reasoned by Claude (claude-opus-5-5, architect subagent) under Ilya delegation for test runs) -- orders are the export's first rows; only the product ranking is line-level |
| `marketplace_seller_scope` — Чьи продажи входят в отчёт: собственные, продавцов площадки или обе группы? | NOT_APPLICABLE | Ilya, 2026-09-23 (reasoned by Claude (claude-opus-5-5, architect subagent) under Ilya delegation for test runs) -- one first-party store; no third-party sellers |
| `refund_rate_basis` — На какой базе считается ставка возвратов? | `order_rows` | Ilya, 2026-09-23 (reasoned by Claude (claude-opus-5-5, architect subagent) under Ilya delegation for test runs) -- refunded sale orders over sale orders; the amount is published beside it |
| `partial_refund_policy` — Как считается частичный возврат? | `counts_as_refunded_order` | Ilya, 2026-09-23 (reasoned by Claude (claude-opus-5-5, architect subagent) under Ilya delegation for test runs) -- any refund makes an order refunded in the rate; the money figure takes the amount |
| `refund_period_attribution` — К какому периоду относится возврат: к периоду заказа или к периоду возврата? | `order_period` | Ilya, 2026-09-23 (reasoned by Claude (claude-opus-5-5, architect subagent) under Ilya delegation for test runs) -- Refunded Amount carries no date; a refund sits in its order's month as of the export date |
| `refund_amount_scope` — Что входит в сумму возврата: только товар, или и доставка, и комиссии? | `goods_only` | Ilya, 2026-09-23 (reasoned by Claude (claude-opus-5-5, architect subagent) under Ilya delegation for test runs) -- net sales exclude shipping, so only returned goods are taken off them |
| `order_event_date_basis` — Какая дата определяет принадлежность заказа периоду? | `order_date` | Ilya, 2026-09-23 (reasoned by Claude (claude-opus-5-5, architect subagent) under Ilya delegation for test runs) -- Created at is on every order; Paid at is blank for unpaid ones |
| `period_boundary_rule` — Границы периода включительные с обеих сторон или конец исключён? | `inclusive_both_ends` | Ilya, 2026-09-23 (reasoned by Claude (claude-opus-5-5, architect subagent) under Ilya delegation for test runs) -- 2026-01-01 to 2026-03-31, both days inside |
| `event_timezone_basis` — В каком часовом поясе читается дата события? | `export_local_date` | Ilya, 2026-09-23 (reasoned by Claude (claude-opus-5-5, architect subagent) under Ilya delegation for test runs) -- Created at is shop time with its offset, as Shopify's own reports assign days |
| `late_revision_rule` — Как читается строка заказа, у которой несколько версий в выгрузке? | `no_revisions_expected` | Ilya, 2026-09-23 (reasoned by Claude (claude-opus-5-5, architect subagent) under Ilya delegation for test runs) -- both exports were pulled the same morning; gate0 holds the overlap's copies equal |
| `revenue_recognition` — Что такое выручка в заголовке: до или после возвратов? | `net_of_refunds` | Ilya, 2026-09-23 (reasoned by Claude (claude-opus-5-5, architect subagent) under Ilya delegation for test runs) -- the menu asks for net sales; gross is published beside it as gross |
| `vat_basis` — Суммы в выручке с НДС или без? | `vat_inclusive` | Ilya, 2026-09-23 (reasoned by Claude (claude-opus-5-5, architect subagent) under Ilya delegation for test runs) -- prices include VAT and partial refunds carry no VAT split, so ex-VAT cannot be recomputed exactly |
| `discount_basis` — Сумма заказа берётся до или после скидок и промокодов? | `after_discounts` | Ilya, 2026-09-23 (reasoned by Claude (claude-opus-5-5, architect subagent) under Ilya delegation for test runs) -- Subtotal is after discount codes; gross and discounts are published beside it |
| `shipping_fee_treatment` — Плата за доставку входит в выручку? | `excluded_from_revenue` | Ilya, 2026-09-23 (reasoned by Claude (claude-opus-5-5, architect subagent) under Ilya delegation for test runs) -- Subtotal carries no shipping; net sales are goods only |
| `reporting_currency_basis` — В какой валюте и по какому курсу суммируются заказы в разных валютах? | `single_currency_export` | Ilya, 2026-09-23 (reasoned by Claude (claude-opus-5-5, architect subagent) under Ilya delegation for test runs) -- EUR on every order, held at gate0 |
| `rounding_rule` — Где округляются суммы: по строке или в итоге? | `round_totals_only` | Ilya, 2026-09-23 (reasoned by Claude (claude-opus-5-5, architect subagent) under Ilya delegation for test runs) -- amounts are cents already; figures are summed exactly and rounded once |
| `customer_identity_basis` — Что такое один клиент? | `normalised_email` | Ilya, 2026-09-23 (reasoned by Claude (claude-opus-5-5, architect subagent) under Ilya delegation for test runs) -- no customer id in the export; Email, lower-case as exported, seen as a pseudonym |
| `guest_checkout_policy` — Как считать заказы без аккаунта (гостевые)? | `matched_by_email` | Ilya, 2026-09-23 (reasoned by Claude (claude-opus-5-5, architect subagent) under Ilya delegation for test runs) -- the export does not mark account checkouts; orders are grouped by email, no-email orders left out |
| `new_customer_definition` — Кто такой новый клиент периода? | NOT_APPLICABLE | Ilya, 2026-09-23 (reasoned by Claude (claude-opus-5-5, architect subagent) under Ilya delegation for test runs) -- no new-customer figure is on the menu; the repeat rate names its history depth instead |
| `paying_customer_definition` — Кто такой платящий клиент в знаменателе ставок? | `at_least_one_sale_in_population` | Ilya, 2026-09-23 (reasoned by Claude (claude-opus-5-5, architect subagent) under Ilya delegation for test runs) -- the repeat rate's denominator is customers with a sale order in the quarter |
| `line_item_unit` — Что такое количество в строке: штуки, упаковки или вес? | `units_as_exported` | Ilya, 2026-09-23 (reasoned by Claude (claude-opus-5-5, architect subagent) under Ilya delegation for test runs) -- every product is sold by the piece |
| `bundle_policy` — Как считается набор (бандл) из нескольких товаров? | NOT_APPLICABLE | Ilya, 2026-09-23 (reasoned by Claude (claude-opus-5-5, architect subagent) under Ilya delegation for test runs) -- the catalogue has no bundles |
| `negative_quantity_policy` — Что означает отрицательное количество или отрицательная сумма в строке? | `negative_rows_are_defects` | Ilya, 2026-09-23 (reasoned by Claude (claude-opus-5-5, architect subagent) under Ilya delegation for test runs) -- Shopify records refunds in Refunded Amount, never as negative lines |
| `zero_amount_row_policy` — Как считать строки с нулевой суммой? | `kept_in_counts` | Ilya, 2026-09-23 (reasoned by Claude (claude-opus-5-5, architect subagent) under Ilya delegation for test runs) -- the February free gift is a real line at 0.00 and stays in the product table |
| `channel_basis` — Что такое канал заказа? | `sales_channel_column` | Ilya, 2026-09-23 (reasoned by Claude (claude-opus-5-5, architect subagent) under Ilya delegation for test runs) -- Source is where the order was placed, not where the customer came from |
| `promo_attribution_rule` — Как заказ относится к промокампании? | `not_attributed` | Ilya, 2026-09-23 (reasoned by Claude (claude-opus-5-5, architect subagent) under Ilya delegation for test runs) -- no campaign figure is on the menu; the discount share is money, not attribution |
| `unknown_channel_policy` — Куда идут заказы с пустым или неизвестным каналом? | NOT_APPLICABLE | Ilya, 2026-09-23 (reasoned by Claude (claude-opus-5-5, architect subagent) under Ilya delegation for test runs) -- Source is never blank and gate0 holds it to three values |
| `duplicate_order_rule` — Что делать с повторяющимся идентификатором заказа? | `rows_are_line_items` | Ilya, 2026-09-23 (reasoned by Claude (claude-opus-5-5, architect subagent) under Ilya delegation for test runs) -- a repeated Name is the next line; a repeated Name and SKU is the overlap's copy |
| `truncated_period_policy` — Как поступать, если выгрузка не покрывает весь отчётный период? | `stop_on_gap` | Ilya, 2026-09-23 (reasoned by Claude (claude-opus-5-5, architect subagent) under Ilya delegation for test runs) -- the order system's log states the range and counts, held at gate0 |
| `missing_amount_policy` — Как считать строки с пустой суммой? | `missing_amount_is_defect` | Ilya, 2026-09-23 (reasoned by Claude (claude-opus-5-5, architect subagent) under Ilya delegation for test runs) -- no order-level amount may be blank on a first row, held at gate0 |
| `free_text_policy` — Что делать с колонками свободного текста (комментарии, адреса, заметки)? | `quarantined_before_agents` | Ilya, 2026-09-23 (reasoned by Claude (claude-opus-5-5, architect subagent) under Ilya delegation for test runs) -- Notes carries a sentence addressed to an AI |
| `product_sales_basis` | `after_discounts_before_refunds` | Ilya, 2026-09-23 (reasoned by Claude (claude-opus-5-5, architect subagent) under Ilya delegation for test runs) -- Refunded Amount does not say which line came back |
| `discount_share_basis` | `discounts_over_gross_sales` | Ilya, 2026-09-23 (reasoned by Claude (claude-opus-5-5, architect subagent) under Ilya delegation for test runs) -- discount codes over sales before discounts |
| `repeat_customer_basis` | `repeat_within_period` | Ilya, 2026-09-23 (reasoned by Claude (claude-opus-5-5, architect subagent) under Ilya delegation for test runs) -- the export holds no history before 2025-12-29 |
| `aov_basis` | `net_sales_per_order` | Ilya, 2026-09-23 (reasoned by Claude (claude-opus-5-5, architect subagent) under Ilya delegation for test runs) -- net sales over sale orders, never a mean of means |

Domain pack `ecommerce`, topics: `order_population`, `refunds_and_returns`, `period_and_time`, `money`, `customers`, `catalog_and_units`, `channels_and_attribution`, `export_quality`.

Traps of those topics declared not applicable:

- `EC-FX-RATE-DATE`: Ilya, 2026-09-23 (reasoned by Claude (claude-opus-5-5, architect subagent) under Ilya delegation for test runs) -- one currency, nothing is converted
- `EC-GMV-IS-NOT-REVENUE`: Ilya, 2026-09-23 (reasoned by Claude (claude-opus-5-5, architect subagent) under Ilya delegation for test runs) -- one first-party store, no marketplace turnover
- `EC-UNITS-MIXED`: Ilya, 2026-09-23 (reasoned by Claude (claude-opus-5-5, architect subagent) under Ilya delegation for test runs) -- every product is sold by the piece; there is no unit column
- `EC-BUNDLE-DOUBLE-COUNT`: Ilya, 2026-09-23 (reasoned by Claude (claude-opus-5-5, architect subagent) under Ilya delegation for test runs) -- the catalogue has no bundles
- `EC-PROMO-ATTRIBUTION`: Ilya, 2026-09-23 (reasoned by Claude (claude-opus-5-5, architect subagent) under Ilya delegation for test runs) -- no campaign figure is published

## Is the export complete

The report's numbers are checked against the export. The export itself is checked against totals from other documents: a month or a region missing from it shows in a total, and never in a recomputation.

| Total | Stated | In the export | Status | Where the total comes from |
|---|---|---|---|---|
| last Created at | 2026-04-03 | 2026-04-03 | matches | the Shopify admin's record of the two exports it wrote (the client's own system: proves the export is all that system holds, not all that happened) |
| rows | 21687 | 21687 | matches | the Shopify admin's record of the two exports it wrote (the client's own system: proves the export is all that system holds, not all that happened) |
| distinct Name | 9659 | 9659 | matches | the Shopify admin's record of the two exports it wrote (the client's own system: proves the export is all that system holds, not all that happened) |
| first Created at | 2025-12-29 | 2025-12-29 | matches | the Shopify admin's record of the two exports it wrote (the client's own system: proves the export is all that system holds, not all that happened) |
| sum of Total | 1770193.90 | 1770193.90 | matches | the Shopify admin's record of the two exports it wrote (the client's own system: proves the export is all that system holds, not all that happened) |

## What was not checked

No check recorded a figure it left without recomputation.

## What stayed on the machine

Three facts read from the run's own records, not written by hand.

- The pipeline under the lock has no step that starts a model: 11 steps, every one a command; pipeline digest `934a0bf65b7b98fa7c55fc902677a5399f1db962bda75d0e177f27dafa240a5b`.
- The driver was started with `--offline`: at 2026-09-23 18:29 UTC it checked the run's environment for 20 model-access variables -- removed 3 from the run's environment: `ANTHROPIC_BASE_URL`, `OPENROUTER_API_KEY`, `ZAI_API_KEY` -- and journaled it.
- No model launch is recorded: the cost file is absent, the launches folder is absent.

## What was proved about the plan

Before the plan was frozen, every check in it was tried: a copy of the data was broken exactly the way that check exists to notice, and the gate was watched for firing. Gate 0 does not mint the lock over a plan without that proof.

Checks tried: 127; fired: 108; accepted untried, by name: 19.

### What was not proved, and why

| gate | rule | scope | verdict | why |
|---|---|---|---|---|
| `gate0_machine` | `row_count` | raw | no breaker | no breaker is written for this rule |
| `gate0_machine` | `control_totals_match` | raw_orders | caught by another rule | left one row it counts out of orders_export.csv, which the total orders-total-sum describes — stopped by enum_values, no_nulls, source_data |
| `gate0_machine` | `resolved_decisions_are_declared` | audit/human_decisions.yaml | no breaker | breaking it means removing a ruling's declaration from the spec, and which line that is cannot be read off the check |
| `gate0_machine` | `domain_definitions_answered` |  | no breaker | no breaker is written for this rule |
| `gate0_machine` | `semantic_traps_are_checked` | audit/audit_spec.yaml | no breaker | breaking it means deleting the check that enforces a trap, which changes the plan this tool is proving |
| `gate0_machine` | `plan_written_over_profile` |  | no breaker | on an audit that registers no hypothesis the rule has nothing to refuse, so breaking it means inventing one -- a change to what the audit asks rather than to a value; examples/mutations does exactly that, as method_registered_after_the_look |
| `gate0_machine` | `step_models_match_spec` | audit/audit_spec.yaml | could not break | pipeline.json has no agent step declaring a model |
| `gate0_machine` | `plan_proven` |  | no breaker | the rule reads the proof this tool writes, so breaking it means writing a false proof, which is what the rule exists to refuse and not a mistake in the data |
| `gate0_machine` | `claim_map_resolves` |  | no breaker | no breaker is written for this rule |
| `gate_clean_machine` | `flag_identity` | is_cancelled | no breaker | no breaker is written for this rule |
| `gate_clean_machine` | `flag_identity` | is_test | no breaker | no breaker is written for this rule |
| `gate_clean_machine` | `flag_identity` | is_sale | no breaker | no breaker is written for this rule |
| `gate_clean_machine` | `flag_identity` | is_refunded | no breaker | no breaker is written for this rule |
| `gate_clean_machine` | `pii_minimised` | clean_orders | no breaker | no breaker is written for this rule |
| `gate_clean_machine` | `pii_minimised` | clean_customers | no breaker | no breaker is written for this rule |
| `gate_metrics_machine` | `recompute_group` | line_net | caught by another rule | changed the recorded value of product_sales_total in calculated_metrics.json — stopped by component_sum, recompute_metric |
| `gate_claims_machine` | `claims_are_single_assertions` |  | no breaker | breaking it means writing a claim that is a folder of figures, which is a judgement about wording rather than an edit to a value |
| `gate_release_document` | `wording_matches_claims` | claims | no breaker | no breaker is written for this rule |
| `gate_release_document` | `free_text_quarantined` | claims | no breaker | no breaker is written for this rule |

## Where this check came from

- Shape pack `shopify-orders` version 1, stage cleaning: its code was reviewed in run 2026-09-23 15:39 UTC of dataset `shopify-orders-claude-build` under profile `claude-build`; the stage's code was fixed at 2026-09-23 17:05 UTC, digest `a7186263e5587df698536c5b35eaef5717d42eb31debe9ef5f343f60ee8c4dd8`.
- Shape pack `shopify-orders` version 1, stage metrics: its code was reviewed in run 2026-09-23 15:39 UTC of dataset `shopify-orders-claude-build` under profile `claude-build`; the stage's code was fixed at 2026-09-23 17:05 UTC, digest `fa198cb58f8846858e242e695cfbdd499351f02317dc68d751acf0ca55b207e9`.
- Profile `verify`, revision `b8c78dba5429e2faf28993230e977f164d8c6316`. Raw protection: `no_agent_runs`.
- Digest of the fixed contracts: `5824e4456f11b1b73580ef4cfe2439a496dc6d72aac9d8ed12d89d3783bbf048`.
- Python 3.12.10, SQLite 3.49.1.

### Source files

| File | SHA-256 |
|---|---|
| `client/report.md` | `af04d8493da5c7224bebb8b3f53698320103db82bada3bdfca013dcc07fbc58b` |
| `raw_data/orders_export.csv` | `4655ea261d1446cdb828cbf2106dae16d141b625cdbf5ac543c048f57004881f` |

### The files as they were sent

| File | SHA-256 | Became |
|---|---|---|
| `orders_export.csv` | `4655ea261d1446cdb828cbf2106dae16d141b625cdbf5ac543c048f57004881f` | `raw_data/orders_export.csv` |
| `report.md` | `af04d8493da5c7224bebb8b3f53698320103db82bada3bdfca013dcc07fbc58b` | `client/report.md` |
