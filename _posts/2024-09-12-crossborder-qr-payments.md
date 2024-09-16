---
layout: post
title: Cross-border QR Payments
date: 2024-9-12 00:00:00+0800
description: Cross-border QR payments. How hard is it?
tags: qr cross-border payments
categories: QR Payments
thumbnail: /assets/img/2024-09-12-crossborder-qr-payments/screenshot.jpg
---

![](/assets/img/2024-09-12-crossborder-qr-payments/screenshot.jpg){: width="100%" }

An article on [aisa.nikei.com](https://asia.nikkei.com/Business/Retail/Japan-ASEAN-to-launch-joint-QR-code-payment-services-in-FY2025) about an initiative of the Japanese government to agree on cross-border acceptance of QR codes prompted me to think about the challenges of QR payment interoperability.

First, I wonder what the real motivation of the South-East Asian countries is. Even QR payment interoperability within one country has been an elusive goal in some countries. So, why not start there before venturing to other countries?

I think this may have to do with the rise of international acceptance for e-wallet payments, for instance, based on Alipay+. I haven't tried it myself, but apparently my GCash e-wallet, which is run on Alipay systems, is now accepted in countries such as Japan and even Germany.

It could be that governments are concerned that QR payment and e-wallets go the same way as cross-border credit and debit card acceptance in the past.

Domestic payment systems have a hard time competing with international payment networks when it comes to cross-border acceptance. After all, there is no way that a merchant, say in Germany, would install payment terminals that accept the various domestic payment card brands from around the world.

The only strategy to avoid too much reliance on foreign payment networks has been to make sure that domestic transactions are processed domestically.

In this sense, governments may perceive somebody like Alipay to be on the brink of becoming the Visa/MasterCard equivalent of the cross-border e-wallet world. A cross-border QR payment standard could help avoid that problem in the future.

Secondly, QR code interoperability is a much harder problem to solve than it appears at first. The easiest part of interoperability in QR payments is the QR code specification, in the same way the specification of the data on a magnetic stripe was exceedingly simple.

The magic of QR code payments happens at the backend, because a QR payment is effectively a real-time backend-mediated conversation between the e-wallet application on the merchant's phone (or payment terminal) and the application on the customer phone.

After the QR code has been scanned, each side, merchant and customer, talk exclusively to their respective backends.

The confidence that payment is happening correctly is entirely dependent on the trust of either side in the application on their own device. There is no need for the merchant to inspect the customer's phone, or to install costly infrastructure to verify the customer's identity, that is there is no PIN or signature to check.

As long as customer and merchant connect to the same e-wallet provider, this was, if not easy, fairly straight forward: once the backend is satisfied that at least the initiating side has been properly authenticated by the e-wallet application, the funds will be pulled or pushed from the paying account to the payee account, and both sides are informed of the success or failure and their new balance. That's it.

The transaction amount is immediately deducted from the payer account and credited to the payee account. There is no risk that the payer spends the money somewhere else before the funds are settled, and it is unlikely that the merchant pulls more money than what was authorized by the payer.

As soon as two or more e-wallet providers are involved, which will be the case for cross-border payments, things will become complex. Many things have to come together for a payment to succeed:

1. Since two independent e-wallets are involved, there needs to be a robust and fast connection between the backend systems, with data specifications and communication protocols. All of this across borders and language barriers.

1. There has to be a settlement agency that can move money from one e-wallet provider to the other.
   The two e-wallets also need to have a way to inform each other of the availability of sufficient funds for the transactions.

1. The customer needs to have a stable data connection on their phone, which can be tricky in a mobile roaming situation.

1. Each e-wallet provider needs to have confidence in the security of the other's e-wallet application.

1. Each e-wallet provider will have to trust that after a payment authorization, the funds will eventually be settled at the right amount.

1. Since transaction authorization and money transfer will usually not happen at the same time, there will be substantial overhead for reconciling authorization amounts with settled amounts, including the correct application of foreign currency exchange rates.

1. The paying side's e-wallet provider would likely have to build a system in which transaction amounts are deducted from the customer's account in real-time.The amount would then have to be put into a settlement account from which the money transfers to the payee e-wallet providers will have to be funded.

The list above likely only scratches the surface of what is required to build a cross-border QR code payment system.
