---
name: rokt-partnership-onboarding
description: Register a managed merchant through the Rokt Partnerships API, poll the async operation, and set up payouts.
api: openapi/rokt-partnerships-api-openapi.yml
operations:
  - registerPartnership
  - getOperation
  - getPartnershipStatus
  - putPartnershipStatus
  - postPayoutSetup
  - getPayoutSetupStatus
  - listManagedAccounts
generated: 2026-10-21
method: generated
---
# Rokt Partnerships API: onboard a managed merchant

Server: `https://accounts.rokt.com` (0.1.0-preview). Auth: Bearer JWT, exchanged from the platform `client_id` and `client_secret` that Rokt issues during onboarding. These credentials aren't self-serve.

1. `registerPartnership`: create or match the merchant account. The call is idempotent on `external_account_id`.
2. `getOperation`: poll the returned operation ID until it finishes.
3. `getPartnershipStatus` to check the account. Use `putPartnershipStatus` to pause or resume it.
4. `postPayoutSetup` starts Stripe Connect payout setup. Then poll `getPayoutSetupStatus`.
5. `listManagedAccounts` lists every merchant you manage.

Rules: write operations (`putPartnershipStatus`, `postPayoutSetup`, and the layout, page, controls and data-deletion calls) take an `Idempotency-Key` header. On a 5xx, retry with the same key. A key conflict returns the spec's IdempotencyConflict response.
