# Rokt

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Rokt is an eCommerce technology platform that uses AI and machine learning to serve personalized non-endemic offers and ads during transaction moments. The platform powers billions of ecommerce transactions annually for brands including Live Nation, PayPal, Uber, and HelloFresh.

## APIs

- **Query API** — Reporting and analytics for account and campaign performance data
- **Event API** — Conversion and attribution event ingestion
- **Cart API** — Ecommerce placement integration during checkout and confirmation moments
- **Custom Audience Import API** — Audience segment management for targeted offer delivery
- **Data Deletion API** — Privacy and data governance compliance
- **Nurture Unsubscribe API** — Opt-out management for nurture campaigns
- **Partnerships API** — Third-party integrations (mParticle and others)

## Authentication

All Rokt APIs use OAuth 2.0 Client Credentials. Obtain App ID and App Secret from One Platform (my.rokt.com) and exchange them for a Bearer token at `https://api.rokt.com/auth/oauth2/token`. Tokens expire after one hour.

## Resources

- [Developer Documentation](https://docs.rokt.com)
- [API Reference](https://docs.rokt.com/developers/api-reference/overview/)
- [OpenAPI Specifications](https://docs.rokt.com/openapi/)
- [Integration Guides](https://docs.rokt.com/developers/integration-guides/overview/)
- [GitHub Organization](https://github.com/ROKT)
- [Blog](https://www.rokt.com/blog/)
