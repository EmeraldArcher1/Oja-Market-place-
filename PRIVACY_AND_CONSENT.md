# OJA Marketplace Privacy & Consent Settings

**Status:** privacy implementation specification; not a claim that a production consent dashboard or automated deletion workflow is live. Last reviewed: 19 October 2026.

## Purpose
OJA is a Nigerian marketplace pilot. Its public README states that sample stalls are examples and that payments, delivery, CAC/NAFDAC verification and some other integrations are not connected. Privacy disclosures must match the live code and must not imply those services are operational.

## Privacy settings users should be able to manage
- **Essential service and security — always active:** sign-in/session security, abuse prevention, enquiry handling, saving marketplace preferences needed for the service, and recording the user's consent choice.
- **Functional preferences — optional where not necessary:** language, voice navigation and interface preferences.
- **Analytics — off until disclosed and consented where required:** optional product measurement and diagnostics.
- **Marketing and advertising — off by default:** advertising pixels, remarketing, cross-site tracking and promotional profiling.
- **Privacy requests:** a clear route for account holders and visitors to request access, correction, export or deletion, subject to identity checks and lawful retention requirements.
- **Change choices later:** users can withdraw optional consent without losing essential marketplace access.

## Data categories to verify
Potential categories, only where the feature is enabled: account and contact details; business/stall information and documents submitted for review; buyer enquiries and trader replies; saved items and language preferences; moderation, abuse and support records; technical logs; consent choices. A phone number should not be disclosed to buyers unless the trader chooses to publish it. Do not collect NIN, BVN, CAC or NAFDAC information beyond the documented purpose, and do not describe user-submitted numbers as independently verified.

## Vendor and data-processing register
The provided vendor list is a reference taxonomy, not a confirmed list of OJA integrations. Do not state that OJA uses Google Analytics, Hotjar, TikTok, advertising pixels, maps providers, cloud services or other named vendors until verified. Audit code imports, network requests, deployment settings, server logs, databases and any connected provider contracts. Document purpose, data shared, retention, processing location, and transfer safeguards.

## Required implementation
1. Audit all collection points, authentication, enquiries, account data, cookies/local storage, analytics and server-side logs.
2. Add a privacy centre reachable from the header, footer and account/settings area on mobile and desktop.
3. Provide category-level toggles with optional categories off by default, consent version/timestamp and withdrawal handling.
4. Ensure optional trackers and SDKs do not load before consent where consent is required.
5. Create an account/privacy request workflow and a deletion/retention schedule. Do not promise deletion until connected data stores and backups are covered.
6. Test accessibility, keyboard use, mobile layouts, persistence, consent withdrawal and clean-checkout builds.
7. Review applicable Nigerian data-protection requirements and relevant launch-market laws before production use.

## Current limitations
The current repository describes OJA as a pilot and says it is not a live marketplace. This document does not itself add a working settings screen, prove that no optional trackers are active, or implement data export/deletion. The actual privacy notice and controls must be aligned with verified production behaviour.
