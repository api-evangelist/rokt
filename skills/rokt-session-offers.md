---
name: rokt-session-offers
description: Request Rokt offers for a transaction session and report the resulting engagement events.
api: openapi/rokt-session-api-openapi.yml
operations:
  - selectOffers
  - recordEvents
generated: 2026-10-21
method: generated
---
# Rokt Session API: request offers, then report events

Server: `https://api.rokt.com`. Auth: HTTP Basic, `base64(rpub:rsec)`, using the public and secret API keys your Rokt account team provides. Keep them server-side.

1. `selectOffers` (`POST /v2/sessions/offers`): send the session and customer attributes and get back the offers to show.
2. Show the offers in your own UI.
3. `recordEvents` (`POST /v2/sessions/events`): report impressions, engagements and conversions against the session you got in step 1.

Rules: neither operation documents an `Idempotency-Key`, so don't blindly retry `recordEvents` after a timeout, because events may be counted twice. Check the error responses in the spec before you retry.
