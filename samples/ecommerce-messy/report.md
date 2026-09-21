# Release report: orders placed inside the quarter, one row per order

Period: 2026-01-01..2026-03-31, inclusive on both ends, by the export's own order month.

## Net revenue over the reported quarter

<!-- claim:CLM-NET-REVENUE:value --> 3023296.61 EUR.

Basis and caveats:
- net of refunds
- delivered orders only
- one row per order after deduplication
- orders with a negative refund are excluded as an export fault
- shipping fees are excluded from revenue
- the period is inclusive on both ends

## Orders in the reported quarter

<!-- claim:CLM-ORDERS:value --> 44531.

Basis and caveats:
- one row per order after deduplication
- orders with a negative refund are excluded as an export fault
- cancelled and pending orders are orders, not sales, and stay out of the revenue but in the population
- the period is inclusive on both ends

## Completion rate, direct channel

<!-- claim:CLM-COMPLETION-DIRECT:value --> 0.724397; the sampling interval runs from <!-- claim:CLM-COMPLETION-DIRECT:ci_low --> 0.718779 to <!-- claim:CLM-COMPLETION-DIRECT:ci_high --> 0.729946, over n = 24597 orders, a 0.95 interval by the wilson method.

The interval is a sampling interval at the stated level; it says nothing about a channel whose mix moves between periods.

Basis and caveats:
- the denominator is all orders in this channel in the period, whatever their status
- the interval is the sampling interval only; it says nothing about a channel whose mix changes between periods
- one row per order after deduplication
- orders with a negative refund are excluded as an export fault
- the channel is the sales channel recorded on the order; the breakdown says where the order was placed, not where the customer came from

## Completion rate, partner channel

<!-- claim:CLM-COMPLETION-PARTNER:value --> 0.604746; the sampling interval runs from <!-- claim:CLM-COMPLETION-PARTNER:ci_low --> 0.597939 to <!-- claim:CLM-COMPLETION-PARTNER:ci_high --> 0.611512, over n = 19934 orders, a 0.95 interval by the wilson method.

The interval is a sampling interval at the stated level; it says nothing about a channel whose mix moves between periods.

Basis and caveats:
- the denominator is all orders in this channel in the period, whatever their status
- the interval is the sampling interval only; it says nothing about a channel whose mix changes between periods
- one row per order after deduplication
- orders with a negative refund are excluded as an export fault
- the channel is the sales channel recorded on the order; the breakdown says where the order was placed, not where the customer came from

## Average order value, direct channel

<!-- claim:CLM-AOV-DIRECT:value --> 110.64 EUR; the sampling interval runs from <!-- claim:CLM-AOV-DIRECT:ci_low --> 109.88 to <!-- claim:CLM-AOV-DIRECT:ci_high --> 111.39, over n = 17818 orders, a 0.95 interval by the student method.

The interval is a sampling interval at the stated level; it says nothing about a channel whose mix moves between periods.

Basis and caveats:
- the denominator is the delivered orders in this channel in the period; cancelled and pending orders are not in it
- delivered orders only
- net of refunds
- the interval is the sampling interval only; it says nothing about a channel whose mix changes between periods
- one row per order after deduplication
- orders with a negative refund are excluded as an export fault
- the channel is the sales channel recorded on the order; the breakdown says where the order was placed, not where the customer came from

## Average order value, partner channel

<!-- claim:CLM-AOV-PARTNER:value --> 87.27 EUR; the sampling interval runs from <!-- claim:CLM-AOV-PARTNER:ci_low --> 86.50 to <!-- claim:CLM-AOV-PARTNER:ci_high --> 88.03, over n = 12055 orders, a 0.95 interval by the student method.

The interval is a sampling interval at the stated level; it says nothing about a channel whose mix moves between periods.

Basis and caveats:
- the denominator is the delivered orders in this channel in the period; cancelled and pending orders are not in it
- delivered orders only
- net of refunds
- the interval is the sampling interval only; it says nothing about a channel whose mix changes between periods
- one row per order after deduplication
- orders with a negative refund are excluded as an export fault
- the channel is the sales channel recorded on the order; the breakdown says where the order was placed, not where the customer came from

## Why no shipping total appears here

The shipping column is written in several notations and some cells cannot be read at all; the sum the registry holds treats each unreadable cell as zero, so it understates itself by an amount this export cannot bound. It is kept out of the figures of record and is available as a lower bound only, in the metric registry.

Every figure above is rendered from the claim register; the register and the metric registry are the only sources of numbers on this page.
