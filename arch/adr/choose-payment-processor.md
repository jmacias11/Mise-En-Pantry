# Choose Payment Processor

## Status

Initial ADR

## Context

We need to utilize a third party payment processor to manage charging users for their subscriptions. We don't want to deal with user financial data so they will store all regulated data.

## Decision

Processor,Transaction Fee,Fixed Fee,Monthly Cost,Best For
Stripe,2.9%,$0.30,$0,Developers & Custom SaaS
PayPal,2.99% – 3.49%,$0.49,$0,High-trust B2C checkouts
Braintree,2.9%,$0.30,$0,Mobile-first hybrid apps
Square,3.3%,$0.30,$0,Simple setups / omni-channel
Adyen,Interchange++,~$0.13,Custom,Global Enterprise scale
Helcim,Interchange + 0.5%,$0.25,$0,High-volume margin saving


Since there is no reason to have an exclusive payment processor, we can utilize both Stripe and Paypal to provide the user with different options. We could also include google pay and apple pay when using a mobile device. However, the first to be implemented will be stripe since they just allow credit cards.

## Consequences

Need to make various accounts for the services we are using and figure out how to embed them in app.