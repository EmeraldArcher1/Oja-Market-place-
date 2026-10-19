# OJA Privacy Centre — implementation plan

**Status:** Draft product requirements for review. Not a final legal notice and not proof that these controls are implemented. Audit the deployed app, database, analytics and integrations before publication.

## Privacy settings

- **Essential:** authentication, account security, stall management, enquiries and order-related functions.
- **Functional:** language preference, accessibility and saved marketplace preferences.
- **Analytics:** optional usage measurement; off until consent where required.
- **Marketing:** advertising pixels, retargeting and promotional profiling; optional and off by default.
- **Voice messages and media:** explain when audio/photos are uploaded, who can access them, and how long they are retained.
- **Merchant verification:** explain what business/CAC evidence is requested, what is checked, who can review it and what is publicly displayed. Never publish identity documents.
- **Orders and payments:** collect/share only the data needed to fulfil an order, prevent fraud, settle funds and resolve disputes. Do not imply payments are active until a provider is integrated and tested.
- **Rights requests:** offer access, correction, deletion, export and complaint routes, subject to lawful retention duties.
- **Consent history:** keep the chosen purposes, policy version and timestamp where required; permit withdrawal.

## Data inventory — verify implementation

| Purpose | Possible data | Safeguards |
|---|---|---|
| Buyer/merchant accounts | contact details, account role, preferences | role-based access; secure authentication |
| Stall and product listings | business details, listings, photos, market/LGA | distinguish public business data from private account data |
| Merchant verification | submitted CAC/business evidence and review result | private storage; limited reviewer access; no public document URLs |
| Enquiries and voice messages | message text/audio, attachments, timestamps | access limited to conversation participants and authorised support |
| Orders and delivery | order details, delivery address/contact, status | share only with parties needed to fulfil the order |
| Payments/refunds | provider references, amounts, settlement/dispute status | only after integration; no raw card data |
| Security/diagnostics | logs, IP/device events | minimise and define retention |
| Analytics/marketing | only tools actually installed and enabled | identify real vendors; consent where required |

The inDrive screenshot is a reference for organising categories, not a vendor inventory for OJA. Do not claim OJA uses AppsFlyer, TikTok, Google Ads, Hotjar, PostHog or other listed providers unless confirmed in the actual build/configuration.

## Acceptance criteria

1. Put Privacy Settings in account/menu and a privacy link on signup, merchant registration and order flows.
2. Explain Essential, Functional, Analytics and Marketing in plain language, with granular controls.
3. Keep optional categories off until consent where required; make Reject optional as easy as Accept optional.
4. Ensure the app's actual SDKs/tags obey consent, rather than only saving a preference in the interface.
5. Protect merchant documents and private messages using server-side access control and private storage.
6. Let users request account/data access, correction or deletion; define lawful exceptions and operational handling.
7. Provide clear notice of public stall information versus private account/verification information.
8. Do not advertise verified merchants, live payments, refunds or delivery integrations until operational and tested.

## Release blockers

Confirm data controller/privacy contact, legal bases, actual third-party processors, retention/deletion policy, security rules, consent implementation and current deployed domain. Review against Nigerian data-protection requirements and applicable markets with qualified counsel before public release.
