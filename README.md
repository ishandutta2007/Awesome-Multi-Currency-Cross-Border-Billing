# Awesome-Multi-Currency-Cross-Border-Billing

# Awesome Multi-Currency & Cross-Border Billing

> A curated list of top Multi-Currency and Cross-Border Billing platforms — both SaaS/Hosted commercial solutions and open-source alternatives for invoicing, accepting payments, and settling funds across currencies and borders.
> 🌟 Star this repo if you find it useful! 🌟

---

## 📋 Table of Contents

- [SaaS / Hosted Platforms](#-saas--hosted-platforms)
  - [Stripe Multi-Currency](#stripe-multi-currency)
  - [Adyen Global Payouts](#adyen-global-payouts)
  - [Wise Business](#wise-business)
  - [PayPal Multi-Currency](#paypal-multi-currency)
  - [Airwallex](#airwallex)
  - [Revolut Business](#revolut-business)
- [Open-Source Software](#-open-source-software)
  - [Lago](#lago)
  - [Kill Bill](#kill-bill)
  - [Invoice Ninja](#invoice-ninja)
  - [InvoiceShelf](#invoiceshelf)
  - [Hyperswitch](#hyperswitch)
  - [Akaunting](#akaunting)
  - [Bitcart](#bitcart)

---

## 🟦 SaaS / Hosted Platforms

Commercial, cloud-hosted Multi-Currency and Cross-Border Billing platforms. These are not open-source but are included as reference points for feature comparison.

### Stripe Multi-Currency
**Type:** Global payment processing with presentment and settlement currencies
Stripe supports multi-currency payments with the ability to present prices in the customer's local currency and settle funds in your preferred currency. It handles automatic currency conversion, localized payment methods, and tax calculation across 135+ currencies. Stripe Connect extends this to marketplace payouts across borders.

### Adyen Global Payouts
**Type:** Cross-border payout and settlement platform
Adyen Global Payouts enables sending funds to third parties (sellers, contractors, suppliers) across borders and currencies, with settlement in local currencies and compliance handling. It is positioned for marketplaces and platforms needing to pay out globally at scale.

### Wise Business
**Type:** Multi-currency accounts and international transfers
Wise Business provides multi-currency business accounts with local account details in multiple countries, mid-market exchange rates, and international transfers. It is positioned for businesses needing to hold, send, and receive money in multiple currencies without hidden markup on exchange rates.

### PayPal Multi-Currency
**Type:** Global payments with multi-currency receiving
PayPal allows receiving payments in multiple currencies and holding balances in different currencies, with conversion at PayPal's rates. It is widely used for cross-border commerce due to its consumer recognition and broad market coverage.

### Airwallex
**Type:** Global business accounts and cross-border payments
Airwallex provides multi-currency business accounts, international payments, and virtual cards, with local payment collection in multiple markets. It is positioned for businesses expanding globally needing unified treasury and payment operations.

### Revolut Business
**Type:** Multi-currency business accounts with exchange and payments
Revolut Business provides multi-currency accounts, international transfers, and payment collection, with competitive exchange rates and virtual cards. It is positioned for SMBs and startups operating across borders.

---

## 🟩 Open-Source Software

Self-hosted, community-driven Multi-Currency and Cross-Border Billing tools. The open-source ecosystem spans **usage-based billing engines**, **subscription billing platforms**, **invoicing applications**, **payment orchestrators**, and **multi-currency accounting**.

### Lago
**Stack:** Ruby / PostgreSQL / Redis / ClickHouse | **License:** AGPL-3.0
Lago is the most widely adopted open-source billing platform, handling usage-based, subscription, prepaid, and hybrid pricing on a single engine. For multi-currency billing, Lago supports **customer-level currency configuration**, with plans priced in multiple currencies and invoices generated in the customer's chosen currency. It handles currency conversion for reporting while invoicing in the original currency, and supports payment collection across Stripe, Adyen, and GoCardless for cross-border settlement. **Trade-off:** AGPL licensing and the operational overhead of running the full stack (PostgreSQL, Redis, ClickHouse).
**Best for:** SaaS companies with usage-based or hybrid pricing needing multi-currency invoicing and a global customer base, accepting AGPL licensing.

### Kill Bill
**Stack:** Java / MySQL/MariaDB/PostgreSQL | **License:** Apache-2.0
Kill Bill is the most mature open-source subscription billing platform, in production since 2010, with native multi-currency support: price lists can be defined per currency, and the system handles currency conversion for reporting. It provides subscriptions, usage billing, invoicing, and payments with a REST API and the Kaui admin UI. Payment plugins exist for Stripe, Braintree, Adyen, and others, enabling cross-border collection. **Trade-off:** It is a billing engine, not a payment gateway—you integrate a processor for actual money movement.
**Best for:** Teams with a platform function wanting permissively licensed (Apache-2.0) multi-currency subscription billing with deep catalog control.

### Invoice Ninja
**Stack:** PHP / Laravel / MySQL | **License:** Elastic-2.0 (source-available)
Invoice Ninja is the most widely deployed open-source invoicing platform, with **multi-currency invoicing** supporting over 50 currencies, per-client currency settings, and exchange rate management. It handles recurring invoices, client portals, expense tracking, and payment gateway integrations across Stripe, PayPal, and others. **Important licensing caveat:** It uses the Elastic License 2.0, which is source-available but not OSI-approved, limiting commercial reuse. E-invoicing support covers ZUGFeRD, XRechnung, Facturae, and generic EN16931, useful for EU cross-border compliance.
**Best for:** Businesses wanting the most feature-complete open-source invoicing platform with multi-currency support and EU e-invoicing, accepting the source-available licensing.

### InvoiceShelf
**Stack:** PHP / Laravel / Vue.js / PostgreSQL | **License:** AGPL-3.0
InvoiceShelf is the actively maintained fork of the abandoned Crater project, providing invoicing, estimates, expense tracking, payment management, **multi-currency support**, customer portal, and Docker deployment. It is positioned as a comprehensive open-source invoicing and expense management platform for small to medium businesses. It offers a genuinely open-source (AGPL-3.0) alternative to Invoice Ninja, though it does not include built-in EU e-invoicing formats.
**Best for:** Businesses wanting a genuinely open-source (AGPL-3.0) multi-currency invoicing platform with active development, accepting the absence of built-in EU e-invoicing.

### Hyperswitch
**Stack:** Rust | **License:** Apache-2.0
Hyperswitch is the leading open-source payment orchestrator, connecting multiple payment processors through a single API with **multi-currency support** and intelligent routing across providers. It enables cross-border payment optimization by routing transactions to the processor with the best authorization rates or lowest cost for each currency, with revenue recovery and cost observability. It supports 200+ connectors covering 150+ payment methods, with self-hosted or SaaS deployment and PCI compliance.
**Best for:** Businesses operating across borders wanting to orchestrate multiple payment providers per currency through a single integration, with control over routing logic and cost optimization.

### Akaunting
**Stack:** PHP / Laravel / MySQL | **License:** GPL-3.0 (core)
Akaunting is a free, open-source online accounting software for small businesses, with **multi-currency support** allowing invoices and transactions in different currencies, exchange rate management, and multi-company support. It provides double-entry bookkeeping, invoice and bill management, and financial reporting. Self-hosted for complete data privacy.
**Best for:** Small businesses and accountants managing cross-border clients needing a free, self-hosted accounting solution with multi-currency invoicing.

### Bitcart
**Stack:** Python | **License:** Open Source
Bitcart is a free and open-source self-hosted payment processor for **BTC, LTC, BCH, XMR, ETH, TRX, USDT, and more**, enabling cross-border cryptocurrency payments without traditional banking intermediaries. It provides a platform for merchants with an admin panel, store integration, and Docker packaging. Crypto payments inherently bypass currency conversion and cross-border settlement friction, making Bitcart useful for merchants accepting international payments in digital assets.
**Best for:** Merchants wanting to accept multi-crypto payments across borders without banking intermediaries, accepting the volatility and compliance considerations of crypto payments.

---

## 📊 Comparison at a Glance

| Software | License | Stack | Multi-Currency Invoicing | Cross-Border Collection | Self-Hosted | Best For |
|----------|---------|-------|--------------------------|-------------------------|-------------|----------|
| **Stripe** | Proprietary | Cloud | ✅ | ✅ 135+ currencies | ❌ | Global payment processing |
| **Adyen** | Proprietary | Cloud | ✅ | ✅ Global payouts | ❌ | Marketplace cross-border payouts |
| **Wise Business** | Proprietary | Cloud | (Transfers) | ✅ Mid-market rates | ❌ | Multi-currency treasury |
| **Lago** | AGPL-3.0 | Ruby/Postgres | ✅ Customer currency | ✅ Via gateways | ✅ | Usage billing + multi-currency |
| **Kill Bill** | Apache-2.0 | Java/DB | ✅ Per-currency price lists | ✅ Via plugins | ✅ | Permissive OSS multi-currency |
| **Invoice Ninja** | Elastic-2.0 | PHP/Laravel | ✅ 50+ currencies | ✅ Via gateways | ✅ | Feature-rich multi-currency invoicing |
| **InvoiceShelf** | AGPL-3.0 | Laravel/Vue | ✅ | ✅ Via gateways | ✅ | Genuine OSS multi-currency invoicing |
| **Hyperswitch** | Apache-2.0 | Rust | (Orchestration) | ✅ Per-currency routing | ✅ | Multi-provider cross-border optimization |
| **Akaunting** | GPL-3.0 | PHP/Laravel | ✅ | (Check) | ✅ | SMB multi-currency accounting |
| **Bitcart** | Open Source | Python | ❌ (Crypto) | ✅ Crypto cross-border | ✅ | Crypto payments |

---

## 🤝 Contributing

Contributions are welcome! If you know of an open-source Multi-Currency or Cross-Border Billing tool that should be listed here, please open a pull request with:

- Project name and URL
- Brief description (1–2 sentences)
- Stack and license
- Why it stands out

Please ensure the project is actively maintained (releases within the last 12 months) and genuinely open-source (or clearly note if it is source-available but not OSI-approved, as with Invoice Ninja).

**Note on the open-source ecosystem:** Multi-currency billing in open source splits between **billing engines with multi-currency support** (Lago for usage-based pricing with customer-level currency, Kill Bill for per-currency price lists under a permissive Apache-2.0 license) and **invoicing applications** (Invoice Ninja for the broadest multi-currency feature set including EU e-invoicing, InvoiceShelf for a genuinely AGPL-licensed alternative, Akaunting for SMB accounting). **Hyperswitch** addresses a different layer—orchestrating multiple payment providers per currency to optimize authorization rates and costs across borders . **Lago** is the strongest open-source choice for SaaS companies with usage-based pricing and a global customer base , while **Kill Bill** remains the most permissive option for teams wanting to own their billing infrastructure . For straightforward multi-currency invoicing, **Invoice Ninja** is the most feature-complete option despite its source-available license, with **InvoiceShelf** as the genuinely open-source alternative.

---

## 📄 License

This list is released under CC0 1.0 Universal (Public Domain). The software projects listed retain their respective licenses.

---

⭐ **If this list helped you discover a useful tool, please star the repo!** ⭐
