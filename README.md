# OKX maker taker fees: what spot and futures cost, how the VIP ladder actually works, and why some accounts see 0.35%

OKX charges **0.08% maker and 0.10% taker on spot**, and **0.02% maker / 0.05% taker on perpetual futures** at the regular tier. That is what most people pay, and it is the number to build a trade around. It is also not universal: the same exchange's US fee page lists **0.20% maker and 0.35% taker** on spot for regular users, and the pair you trade can put you in a different fee group with different rates.

Below are the tier tables, the arithmetic behind a single fill, where the 0.35% figure comes from, and the account mechanics that decide whether you get a rebate or a bill.

> **Quick version**
> - Regular tier, global: spot **0.08% / 0.10%**, perpetuals **0.02% / 0.05%**.
> - Post a limit order that rests in the book and you pay the maker rate. A limit order that fills on arrival pays taker.
> - The next rung down, VIP 1, needs **$100,000 in assets or $10,000,000 of 30-day volume**. Below that, the maker/taker choice is your only real lever.
> - 👉 [Create an OKX account and check the tier your balance puts you in](https://okx.com/join/CASH20)

## What the regular tier costs on spot and futures

| Market | Maker | Taker |
| --- | --- | --- |
| Spot (standard pairs) | 0.080% | 0.100% |
| USDT perpetual futures | 0.020% | 0.050% |
| US spot (OKX US entity) | 0.200% | 0.350% |

The global figures were independently checked against OKX's fee page in October and November 2026 by two fee-tracking sites, which landed on identical numbers. The US row comes from OKX's own en-us fee page, which also publishes a different VIP ladder from the global one.

Three things follow from that table.

First, futures taker is two and a half times the maker rate. Spot taker is only a quarter above maker. If you are going to bother posting limit orders, the saving is far larger on perpetuals.

Second, a limit order is not automatically a maker order. If you place a limit buy above the best ask, it crosses the book and fills immediately, and OKX charges you the taker rate. The maker rate only applies to orders that sit in the book waiting.

Third, every fill is charged. A futures position that is opened and closed pays the fee twice, on the position value each time, not once on the margin you posted.

## The full fee ladder for futures (Regular through VIP 9)

OKX splits futures pairs into two groups. Group 1 is the top 10: BTC-USDT, ETH-USDT, SOL-USDT, DOGE-USDT, BTC-USD, XRP-USDT, ETH-USD, PEPE-USDT, PUMP-USDT, SUI-USDT. Group 2 is every other futures pair.

**Qualification**

| Tier | Assets (USD) | Or 30-day volume (USD) | 24h withdrawal limit (USD) |
| --- | --- | --- | --- |
| Regular | < 100,000 | < 10,000,000 | 10,000,000 |
| VIP 1 | ≥ 100,000 | ≥ 10,000,000 | 20,000,000 |
| VIP 2 | ≥ 250,000 | ≥ 50,000,000 | 24,000,000 |
| VIP 3 | ≥ 500,000 | ≥ 100,000,000 | 32,000,000 |
| VIP 4 | ≥ 2,000,000 | ≥ 200,000,000 | 40,000,000 |
| VIP 5 | ≥ 5,000,000 | ≥ 600,000,000 | 48,000,000 |
| VIP 6 | ≥ 10,000,000 | ≥ 1,000,000,000 | 60,000,000 |
| VIP 7 | — | ≥ 1,500,000,000 | 72,000,000 |
| VIP 8 | — | ≥ 2,000,000,000 | 80,000,000 |
| VIP 9 | — | ≥ 20,000,000,000 | 80,000,000 |

You qualify on either column, whichever gets you higher. VIP 7 and above have no asset threshold at all; volume is the only route in.

**Fees**

| Tier | Group 1 maker | Group 1 taker | Group 2 maker | Group 2 taker |
| --- | --- | --- | --- | --- |
| Regular | 0.0200% | 0.0500% | 0.0200% | 0.0500% |
| VIP 1 | 0.0180% | 0.0400% | 0.0180% | 0.0400% |
| VIP 2 | 0.0130% | 0.0350% | 0.0130% | 0.0350% |
| VIP 3 | 0.0100% | 0.0280% | 0.0100% | 0.0280% |
| VIP 4 | 0.0080% | 0.0270% | 0.0080% | 0.0270% |
| VIP 5 | 0.0050% | 0.0260% | 0.0050% | 0.0260% |
| VIP 6 | 0.0000% | 0.0250% | 0.0000% | 0.0250% |
| VIP 7 | -0.0020% | 0.0200% | -0.0050% | 0.0250% |
| VIP 8 | -0.0050% | 0.0200% | -0.0100% | 0.0250% |
| VIP 9 | -0.0050% | 0.0150% | -0.0100% | 0.0200% |

This table comes from OKX's own "Updates to Global Fee Framework" notice, published 3 November 2025 and effective 25 November 2025, which also expanded the ladder from eight tiers to nine and lowered the entry requirements.

Two details in it are easy to miss. VIP 1 through VIP 6 charge identical rates on both pair groups, so there is nothing to optimise by pair choice until VIP 7. And negative maker fees, where OKX pays you a rebate instead of charging you, start only at VIP 7 and apply only to resting orders.

Tiers are not something you buy. 👉 [Open an OKX account and the fee page shows which tier your assets and volume qualify for](https://okx.com/join/CASH20).

## Spot fees depend on which pair group you're trading

Spot is split into three groups plus two special categories:

- **Group 1, top 10 pairs:** ADA-USDT, BTC-USDT, DOGE-USDT, ETH-USDT, PENGU-USDT, PEPE-USDT, PUMP-USDT, SOL-USDT, SUI-USDT, XRP-USDT.
- **Group 2, mid-tier active pairs:** a long list that includes BTC-USD, ETH-BTC, ETH-USD, SOL-USD, OKB-USDT and USDT-EUR.
- **Group 3:** every other spot pair.
- **Zero-fee pairs:** DAI-USDT, PYUSD-USDT, USDC-USDT, USDG-USDT, USDT-USD.
- **Special-rule pair:** USDT-TRY, offered only under the Bahamas and Seychelles entities.

The 0.08% / 0.10% headline applies to standard pairs. Treat the exact maker and taker rate for a specific spot group as something to confirm inside your account's fee page before you size a position, because it is set per entity and per group, and the 0.20% / 0.35% US schedule shows how far apart two entities can be.

OKX says pair groups and fee rates may be reviewed roughly every three months, and that it reserves the right to change effective dates without further notice.

## How a maker fee and a taker fee are actually calculated

A maker order enters the order book and does not fill immediately. OKX's own illustration: with the lowest BTC ask at 1,000 USDT, a buy order at 999 USDT will not match, so it sits in the book until someone takes it. When it fills, you pay the maker fee and the counterparty pays the taker fee.

**Spot formula:** fee rate × amount of crypto bought when the order was filled.

The official worked example uses USDT at 10 USD with a trader on 0.04% maker and 0.1% taker. Buying 1 USDT at market makes them the taker: 0.1% × 1 = **0.001 USDT**, leaving 0.999 USDT. Selling 1 USDT at a limit price for 10 USD makes them the maker: 0.04% × 10 = **0.004 USD**, leaving 9.996 USD.

Note what the fee is charged on in the spot case: the amount of coin received, not the dollar value of the order. At the regular tier that distinction is small, but it matters if you are reconciling fills in a non-USD pair.

At regular-tier rates, a spot order costs:

| Order size | Maker (0.08%) | Taker (0.10%) |
| --- | --- | --- |
| 100 USDT | 0.08 USDT | 0.10 USDT |
| 1,000 USDT | 0.80 USDT | 1.00 USDT |
| 10,000 USDT | 8.00 USDT | 10.00 USDT |

**Futures formula:** fee rate × position value, charged at open and again at close. Leverage does not change it. OKX's example: 1 BTC of BTCUSDT perpetual at 20,000 USDT costs **10 USDT as taker** (0.05%) or **4 USDT as maker** (0.02%), whatever leverage you used to get there.

On a 10,000 USDT futures position, that is 5 USDT as taker against 2 USDT as maker, a 3 USDT difference per side. On spot at 10,000 USDT, the gap is 2 USDT. Neither is dramatic on one trade. Across a hundred round trips a month it is the difference between 1,000 USDT and 400 USDT in fees.

## Why your rate doesn't match what you read online

OKX operates through different legal entities in different markets, and each one publishes its own schedule. The disclaimer on the fee page says it plainly: fees may vary depending on your region, and users should check the fee page inside their own account for the rate that applies to them.

**United States.** The en-us fee page lists regular users at **0.2000% maker / 0.3500% taker** on spot, with a 10,000,000 USD 24-hour withdrawal limit. If your account shows 0.35% on a market buy, that is not an error and no referral code will fix it. You are on the US schedule, where the VIP ladder also differs: spot VIP 1 there starts at 0.1000% maker / 0.2000% taker, and spot maker only turns negative at VIP 7.

**European Union.** EU clients trade through OKX Europe Limited, which holds a MiCA licence in Malta. Euro deposits run over SEPA and SEPA Instant, spot taker is 0.10%, and retail clients have perpetual leverage capped at 10x.

**Everyone else.** The 0.08% / 0.10% and 0.02% / 0.05% figures in the tables above, with the VIP ladder from the global framework notice.

A second variable sits inside every account regardless of entity: which pair group the instrument belongs to. BTC-USDT spot and a thin Group 3 altcoin pair do not necessarily cost the same, and the special-rule and lira pairs are priced apart from the standard ones.

👉 [Check the fee schedule attached to your own OKX account before you place the order](https://okx.com/join/CASH20)

## Climbing the ladder, and what VIP 7 really requires

The fees fall in a straight line from VIP 1 to VIP 6. Taker on Group 1 goes 0.0500% → 0.0400% → 0.0350% → 0.0280% → 0.0270% → 0.0260% → 0.0250%. Maker goes 0.0200% down to 0.0000%, so at VIP 6 a resting order costs nothing and only takers pay.

Then the structure changes shape. From VIP 7 up, maker turns negative: -0.0020% on Group 1 and -0.0050% on Group 2 at VIP 7, deepening to -0.0050% and -0.0100% at VIP 8 and VIP 9. OKX pays you a rebate when your resting order fills. Takers still pay at every tier, including VIP 9.

The price of entry is where most people should stop reading. VIP 7 needs **1,500,000,000 USD of 30-day volume**. VIP 9 needs **20,000,000,000 USD**. Those are market-maker and institutional numbers. A retail account doing 1,000,000 USDT a month in futures volume is three orders of magnitude short of VIP 7 and still short of the 10,000,000 USD needed for VIP 1 through volume alone.

Which leaves the asset route for anyone with a real balance: 100,000 USD held on the platform gets you VIP 1 and takes Group 1 futures taker from 0.0500% to 0.0400%. On 5,000,000 USDT of monthly volume that is 500 USDT saved per month. Whether it is worth moving 100,000 USD onto an exchange to capture depends on what else you would do with the capital, and that is a portfolio question, not a fee question.

## Six rules that change your real bill

1. **Zero-fee pairs don't count toward volume.** Spot pairs with 0% maker and 0% taker are excluded from your 30-day spot trading volume and from market-maker tier assessment. Trading USDC-USDT all month will not move you toward VIP 1, however much size you do.
2. **Sub-accounts share the main tier, but not instantly.** Your main account's tier is set by the combined 30-day volume and daily asset snapshot of the main account and all sub-accounts. A newly created sub-account picks up that tier from 16:00 UTC.
3. **Your asset figure is the higher of two numbers.** OKX snapshots all crypto and fiat balances daily at 16:00 UTC, converts to BTC and then USD, and uses whichever is greater between your 30-day average asset amount and that day's snapshot. A withdrawal that halves your balance today does not halve your qualifying assets today.
4. **Tiers refresh late in the day.** OKX updates fee tiers between 20:00 and 22:00 UTC. A trade big enough to push you over a threshold in the morning still settles at yesterday's rate for the rest of the day.
5. **Liquidation is billed at your taker rate.** A forced liquidation is charged on top of the loss, at whatever taker fee applies to your tier. Budget for it if you run tight margin.
6. **Four charges that aren't the trading fee.** Delivery futures settlement costs 0.01% for all users. Spread trading gives each leg a 50% fee discount. Convert shows no trading fee, but OKX sets the quoted rate, so compare it against the spot price before swapping size. Funding on perpetuals settles every eight hours and moves between longs and shorts; it is not OKX revenue, but on a multi-day hold it can exceed what you paid to open.

## FAQ

**Is OKX's maker fee ever negative?**
Yes, from VIP 7 upward, and only for maker orders. Group 1 pays -0.0020% at VIP 7, Group 2 pays -0.0050%, rising to -0.0050% and -0.0100% at VIP 8 and VIP 9. Taker fees stay positive at every tier.

**Why is my OKX fee 0.35%?**
Because your account sits under the US entity, where spot regular users pay 0.2000% maker and 0.3500% taker. The global 0.08% / 0.10% schedule does not apply to that account.

**Do zero-fee pairs count toward my 30-day volume?**
No. Spot pairs with both maker and taker at 0% are excluded from 30-day spot volume and from market-maker tier assessment.

**Does OKX charge for deposits?**
Crypto deposits are free on OKX's side; you pay the sending network's fee. Fiat depends on the method and the entity, and EU users can fund with euros over SEPA or SEPA Instant, where bank charges may still apply.

**Are futures fees charged twice?**
Yes. Each fill is charged on position value, so opening and closing the same position costs the rate twice. A 10,000 USDT position costs 5 USDT to open and 5 USDT to close at regular-tier taker.

## Which rate applies to you

Three cases cover almost everyone.

**Under 100,000 USD in assets and under 10,000,000 USD of 30-day volume:** you are on the regular tier and will stay there. The levers that work are posting limit orders instead of crossing the book, trading standard pair groups rather than special-rule pairs, and using the spot market instead of Convert for size. That alone moves spot from 0.10% to 0.08% and futures from 0.05% to 0.02%.

**Able to hold 100,000 USD or more on the platform:** check both the asset and volume columns, because either one qualifies you, and confirm which entity your account is under before assuming the global thresholds apply. VIP 1 saves 0.0100% on Group 1 futures taker, which is worth calculating against the cost of keeping that balance on an exchange.

**Trading top-10 futures pairs at 1,500,000,000 USD a month or more:** only then does the rebate conversation start, and it is worth reading the Group 1 versus Group 2 maker numbers before routing order flow.

One last check before your next order: open the fee page inside your account, not the public marketing page, and confirm the entity, the pair group and the tier shown for today. The three together determine the rate you actually pay.

👉 [Open your OKX account and confirm your tier before the next fill](https://okx.com/join/CASH20)
