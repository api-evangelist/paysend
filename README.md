# Paysend (paysend)

Paysend is a London-headquartered global fintech, founded in 2017, building a cross-border digital payments network that moves money to bank accounts, cards, and wallets across 170+ countries in 40+ currencies for more than 11 million consumers and a growing base of enterprise clients. Alongside its consumer money-transfer app, Paysend operates Paysend Enterprise, whose developer surface is a single Payout API: one integration disburses funds worldwide to cards and accounts, with FX rate lookups, bank and card tokenization utilities, partner statements, and balance queries.

The API is a partner-provisioned enterprise integration (United Kingdom home market) rather than a fully public self-serve product. Authentication is API key plus HMAC digital signature (`X-OPP-Signature`), requests are idempotent via a request id and date, and payout status is delivered through configurable webhook notifications. Paysend documents this surface openly on a Docusaurus developer portal with a sandbox mock service, but does not publish a downloadable OpenAPI/Swagger definition or a public base URL.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/paysend/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/paysend/refs/heads/main/apis.yml)

## Tags

- Payments
- United Kingdom
- Cross-Border
- Money Transfer
- Payouts
- Payment Processing
- FX
- Remittance
- Fintech

## Timestamps

- **Created:** 2026-07-24
- **Modified:** 2026-07-24

## APIs

### Paysend Enterprise Payout API

Paysend Enterprise's single Payout API disburses funds worldwide to cards and bank accounts through the Paysend payments network. A multi-task `POST /processing` endpoint carries operations including `pay.toCard`, `pay.toAccount`, `fx.rateGet` / `fx.rateGet.p2a`, `bank.get` / `bank.search`, `card.createToken` / `card.infoGet`, `partner.statementGet`, `getBalance`, and `task.statusGet`, with a companion `GET /processing/status/` for status retrieval. A sandbox mock service is provided.

- **Human URL:** [https://developer.paysend.com/product-overview/](https://developer.paysend.com/product-overview/)
- **Auth:** API key + HMAC digital signature (`X-OPP-Signature`, SHA-256/512); idempotency via `header.request.id` + `header.request.date`.

#### Tags

- Payouts
- Cross-Border
- FX
- Payments

#### Properties

- [Documentation](https://developer.paysend.com/product-overview/)
- [API Reference](https://developer.paysend.com/endpoints/get-processing-status/)
- [Authentication](https://developer.paysend.com/authentication-and-idempotency/)
- [Webhooks](https://developer.paysend.com/webhook-notification-service/)

## Common Properties

- [Website](https://paysend.com/)
- [Developer Portal](https://developer.paysend.com/)
- [Documentation](https://developer.paysend.com/product-overview/)
- [API Reference](https://developer.paysend.com/endpoints/get-processing-status/)
- [Authentication](https://developer.paysend.com/authentication-and-idempotency/)
- [GitHub Organization](https://github.com/paysend)
- [Blog](https://paysend.com/blog)
- [Privacy Policy](https://cloud.paysend.com/web/docs/Global_Privacy_Policy_Paysend.pdf)
- [Product](https://paysend.com/enterprise)

## Review

No downloadable OpenAPI/Swagger definition is exposed and no public base URL is documented — the Payout API is partner-provisioned. See [review.yml](review.yml) for the full reviewer findings.

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
