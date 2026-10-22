---
name: rokt-reporting-query
description: Find accessible Rokt accounts and pull advertiser campaign or partner transaction reports through the Query API.
api: openapi/rokt-query-api-openapi.yml
operations:
  - get_user_accounts_v1_query_accounts__get
  - get_account_v1_query_accounts__account_id__get
  - get_help_v1_query_accounts__account_id__campaigns_help_get
  - get_advertiser_report_v1_query_accounts__account_id__campaigns__post
  - get_help_v1_query_accounts__account_id__transactions_help_get
  - get_partner_report_v1_query_accounts__account_id__transactions_post
generated: 2026-10-21
method: generated
---
# Rokt Query API: reporting

Server: `https://api.rokt.com`. Auth: Bearer (a user's Rokt JWT or encoded OAuth2 token).

1. `get_user_accounts_v1_query_accounts__get`: list the accounts this token can see. Then confirm one with `get_account_v1_query_accounts__account_id__get`.
2. Advertisers: call `get_help_v1_query_accounts__account_id__campaigns_help_get` to find the available dimensions and metrics, then `get_advertiser_report_v1_query_accounts__account_id__campaigns__post` with a reporting request.
3. Partners: call `get_help_v1_query_accounts__account_id__transactions_help_get`, then `get_partner_report_v1_query_accounts__account_id__transactions_post`.

The report calls use POST, but they are read-only queries and safe to retry.
