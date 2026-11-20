![QRL article banner](assets/banner-article.png)

# Buy QRL With a Bank Card

**Short answer.** A card purchase goes through a third party: either the card route built into the wallet, which delivers coins to an address you control, or an exchange that takes card payments. Both cost more than a bank transfer, both require identity checks, and both can fail for reasons that have nothing to do with QRL.

## How a card purchase works

You are not buying from the network. A card payment is handled by a payment processor and an on-ramp provider, who take the card, run their own checks, buy the asset on their side and send it to an address you name. The wallet's card route is exactly that: a third-party flow presented inside the application.

That is worth understanding because it determines who to ask when something goes wrong. A declined card, a blocked account or a delayed delivery is a question for the provider, not for the project, and not for anyone in a support channel offering to help.

The address you name matters. Coins delivered to an address you control are yours; coins delivered to an exchange balance are held by the exchange. Both are legitimate, and they are different arrangements.

## Why it costs more

Three costs stack on a card purchase. The processor charges for taking a card, the provider charges a spread on the conversion, and the card network charges the merchant, which is passed on.

A bank transfer avoids most of that, which is why venues price card purchases higher and often cap them. The convenience is real: a card works immediately, and a transfer can take a day.

There is no fee table here, because fees vary by provider, country and amount, and a number printed on this page would be wrong somewhere. Read the quote on the provider's screen before confirming; it is the only figure that applies to your transaction.

## Why payments fail

Card payments fail for ordinary reasons, and almost none of them are about the asset. A bank may decline a crypto merchant category. A provider may refuse a card issued in a country it does not serve. A verification step may need a document you have not uploaded. A daily limit may be lower than the amount you tried.

Some fail for reasons that look like the network's fault but are not: a purchase completes on the provider's side and the delivery is delayed, or the provider's system is busy. The coins are not lost in those cases; the transaction is pending with a company, which is a different kind of problem from a pending QRL transaction.

Genuine network problems show up differently. If a QRL transaction is confirmed on the chain and your balance has not changed, the wallet needs to sync rather than the payment needing to be repeated.

## What to do when one fails

Read the error rather than retrying immediately. A decline usually names a reason, and repeating the same attempt tends to produce the same result and another hold on your card.

Check the provider's own status and limits page, then contact its support with the reference number. Keep the reference: it is what identifies the payment, and it is the one thing the provider can act on.

Do not send the same purchase again through a second provider until you know the first did not complete. Two completed purchases are two purchases, and the coins arrive twice.

If the payment succeeded and the coins have not appeared, check the delivery address on the provider's confirmation against your wallet, and check whether the wallet is synced to the chain. https://github.com/qrl-wallet/wallet-setup-and-repair/blob/main/understanding-qrl-transaction-fees.md explains why a delivered transaction still needs a synced wallet to show up.

## KYC and what it means

Card routes require identity verification. That is the provider's obligation, not the project's choice, and it applies because fiat payment systems are regulated.

The practical consequences are a delay on the first purchase, a document upload, and a record of the transaction held by a company rather than by you. For a self-custody asset that is a real difference: the coins become yours when they arrive at your address, and the purchase record stays with the provider.

Buying on an exchange goes further, because the exchange holds the balance as well as the record until you withdraw.

## Moving the coins off the exchange

If the coins land on an exchange, withdraw them to an address you control when you are ready to hold rather than trade. That means creating a wallet, backing up the phrase before it holds anything, and testing with a small withdrawal first.

https://github.com/qrl-wallet/wallet-setup-and-repair/blob/main/create-your-first-qrl-address.md covers the sequence, and https://github.com/qrl-wallet/token-facts-and-prices/blob/main/how-to-buy-qrl-coin.md covers the checks that the withdrawal is going to the right network: ticker QRL, mainnet, and an address beginning with Q.

For a first purchase, the test withdrawal is worth more than the fee it costs. It proves the address you saved is the address you meant, while the amount at risk is small.

## What this route does not promise

It does not promise availability. A provider can stop serving a country, refuse a card type, or change its limits without notice, and none of that is something the project controls.

It does not promise a price either. The quote you see includes the provider's spread, and it is the price you pay for that purchase, not the market price on a chart. https://github.com/qrl-wallet/token-facts-and-prices/blob/main/qrl-price-and-market-cap.md explains the difference between the two, and https://github.com/qrl-wallet/token-facts-and-prices/blob/main/avoid-qrl-price-prediction-scams.md covers the pages that turn a purchase into a promise of profit.

## FAQ

### Can I buy QRL with a card without an account?

You can buy without a QRL account, because addresses need none. The provider will still require its own account and identity verification, because that is how card payments work.

### Why is a card purchase more expensive than a transfer?

Because three parties take a cut: the card processor, the provider's spread and the card network. A bank transfer removes most of that cost at the price of speed.

### The payment failed. Is my money gone?

Usually not. A declined payment is not a charge, and a completed payment that has not delivered is a pending item with the provider. Keep the reference number and contact them.

### Do the coins arrive in my wallet automatically?

Only if you gave your own address. If you bought on an exchange, the coins sit in your exchange balance until you withdraw them.

<!-- answers: Q215 -->
