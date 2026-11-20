![QRL article banner](assets/banner-article.png)

# QRL Price and Market Cap Data

**Short answer.** A price is the last trade on whichever venue you are reading, and market capitalisation is that price multiplied by circulating supply. Two sites can show different numbers for the same coin because they use different venues, different supply figures, or both. Neither number is a forecast.

## Where the number comes from

There is no single QRL price. There is a price on each exchange that trades it, and a site that displays "the" price is choosing one venue, or averaging several, and usually not saying which.

That matters most when volume is thin. A single trade can move the last price on a small venue by a visible amount, and an aggregator that weights venues by volume will show something different from a venue with three trades an hour.

So the first question about any quoted figure is where it came from. A price with no venue attached is a number without a source.

## Price versus market cap

Market capitalisation is arithmetic: the price of one coin multiplied by the number of coins in circulation. It is a shorthand for size, not a measure of money that has been invested.

The distinction is easy to lose. If the price doubles on a thin market, the market cap doubles on paper while the same coins change hands for the same small amounts of money. Nothing was added to the network, and nobody's balance changed except in valuation.

That is why market cap comparisons between projects are rough at best. They compare two prices times two supply figures, and each of those inputs has its own uncertainty.

## Circulating versus maximum supply

QRL has a fixed maximum supply of 105,000,000 coins, and roughly 79.5 million are in circulation. The difference is not held in reserve by anyone: it is coins that have not been issued yet, because new coins enter circulation through mining.

Which figure a site uses changes the market cap it reports. Multiplying the price by 105 million rather than 79.5 million produces a cap about a third larger for the same price, and some sites do exactly that while labelling it the same way.

When two caps disagree, check the supply figure before assuming a price difference. https://github.com/qrl-wallet/token-facts-and-prices/blob/main/qrl-token-supply-explained.md covers the cap, the emission and where to verify the numbers on-chain.

## Why sites disagree

Four reasons account for most of it. Different venues, so different last trades. Different supply figures, so different caps. Different timestamps, so one site lags another by minutes. And different treatment of stablecoin pairs, where a price quoted in USDT is converted to dollars at a rate that varies.

None of that is fraud. It is the ordinary messiness of a market that trades in many places, and it means a screenshot of a number is evidence of nothing except which page the person had open.

The useful habit is to compare at least two venues and to look at volume beside price. A price on a venue with almost no volume is an opinion about value that nobody has tested with money.

## What the number does not tell you

It does not tell you what the asset will be worth, and no page that shows a price knows that. It does not tell you whether the network is healthy, whether the software works, or whether a release shipped.

It also does not tell you what you would receive if you sold. That depends on the depth of the market at the moment you sell, which is why a thin market can show a price you cannot actually get.

For those questions the sources are elsewhere: the repository for the software, a block explorer for the chain, and https://github.com/qrl-wallet/token-facts-and-prices/blob/main/qrl-rich-list-explained.md for what the distribution of balances can and cannot show.

## What a price does not measure

Liquidity is the missing dimension. A market's depth is how much can be bought or sold before the price moves, and no last-trade figure shows it. A coin can display a price and still be impossible to sell in size without pushing that price down.

That is why a holder's realised value differs from a quoted one. The number on a page describes the last small trade; the number you would get depends on how much you are selling and who is buying at that moment.

## Reading a number responsibly

Three habits cover most of it. Name the venue when you quote a price. Check the supply figure behind a market cap. And treat any single number as a snapshot rather than a fact about the asset.

If a page offers a price and a prediction in the same breath, the prediction is the part to discard. https://github.com/qrl-wallet/token-facts-and-prices/blob/main/avoid-qrl-price-prediction-scams.md covers how those pages are built, and https://github.com/qrl-wallet/token-facts-and-prices/blob/main/qrl-to-usd-price-chart.md covers what a chart's axes and volume actually show.

https://github.com/qrl-wallet/token-facts-and-prices/blob/main/how-to-buy-qrl-coin.md covers the practical side: what to check before paying, and why the quote you pay includes a spread that the market price does not.

## FAQ

### Why is the QRL price different on two sites?

Because each site reads a different venue, or averages several, and updates at a different moment. Thin volume makes the gap larger.

### Is market cap the same as money invested?

No. It is price multiplied by circulating supply. It grows when the price rises on a small trade, without any money entering the network.

### Does the market cap use the maximum supply?

Some sites do and some use circulating supply, which is why their figures differ. QRL's maximum is 105,000,000 and roughly 79.5 million are circulating.

### Can I tell what QRL will be worth from this page?

No. This page explains where the numbers come from. It makes no forecast, and neither does the project.

<!-- answers: Q074, Q083, Q085, Q088, Q247, Q248, Q270 -->
