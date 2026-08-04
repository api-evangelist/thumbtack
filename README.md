# Thumbtack (thumbtack)

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

Thumbtack is a local services marketplace connecting homeowners with local service professionals (cleaning, home improvement, events, wellness, and more). There is no self-serve public API - Thumbtack operates an approval-gated Partner Platform (developers.thumbtack.com) with two documented API surfaces - a Demand API for marketplace integrations (pro search, categories, autocomplete, requests) and a Pro API for supply-side integrations (leads, messages, pro profiles, reviews) - plus low-code embeddable widgets. Access requires Thumbtack to approve a partner and issue OAuth 2.0 credentials; there is no public signup or API key self-service.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/thumbtack/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/thumbtack/refs/heads/main/apis.yml)

## Access Model

Thumbtack is primarily a consumer/pro marketplace app, not an API-first company. Both the Docs and API Reference sections of [developers.thumbtack.com](https://developers.thumbtack.com/) are gated behind a "Request Access" call to action - Thumbtack reviews and approves partners before issuing OAuth 2.0 credentials in production. There is no public signup form, no self-serve API key, and no published per-call pricing for API usage itself. See [review.yml](review.yml) for the full findings on transports and confirmed endpoints.

## Tags

- Local Services
- Marketplace
- Home Services
- Leads
- Partner API

## Timestamps

- **Created:** 2026-07-03
- **Modified:** 2026-07-03

## APIs

### Thumbtack Demand API

Marketplace-side ("Demand Partner") integration surface for helping customers find pros, explore service categories, and submit project requests - pro search by zip code/category, filtered pro matching, autocomplete, homecare checklists, category recommendations, and on-demand order management. v1/v2 routes use HTTP Basic auth; v4 routes use OAuth 2.0. Approval required; access is granted by Thumbtack after a partner application, not self-serve.

- **Human URL:** [https://developers.thumbtack.com/docs/overview](https://developers.thumbtack.com/docs/overview)
- **Base URL:** `https://api.thumbtack.com`

#### Tags

- Marketplace
- Pros
- Categories
- Requests

#### Properties

- [Documentation](https://developers.thumbtack.com/docs/overview)
- [API Reference](https://developers.thumbtack.com/api-reference)
- [API Reference](https://api.thumbtack.com/docs/demand_api.html)
- [OpenAPI](openapi/thumbtack-demand-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### Thumbtack Pro API

Supply-side ("Supply Partner") integration surface launched 2021 (first partner GoSite) letting business-workflow platforms manage a pro's Thumbtack leads and messages alongside their other customer communications - two-way lead messaging, business profile and targeting-preference management, review notifications, business phone numbers for call attribution, and job status signals. Thumbtack calls partner-implemented webhook-style endpoints (lead, message, lead update, review) and partners call Thumbtack's OAuth 2.0-protected endpoints with a bearer token obtained via the partner-connect authorization code flow. Approval required.

- **Human URL:** [https://developers.thumbtack.com/docs/overview](https://developers.thumbtack.com/docs/overview)
- **Base URL:** `https://pro-api.thumbtack.com`

#### Tags

- Leads
- Messages
- Pro Profiles
- Reviews

#### Properties

- [Documentation](https://developers.thumbtack.com/docs/overview)
- [Documentation](https://developers.thumbtack.com/guides/2Hqdq7prrqyDfW2HvoPRXb)
- [API Reference](https://pro-api.thumbtack.com/docs/)
- [OpenAPI](openapi/thumbtack-pro-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

## Pricing (Marketplace, not API)

Thumbtack has no published API price list. The marketplace itself is free for consumers; pros pay per matched lead / customer opportunity at a dynamic price (roughly $8-$150+ depending on trade and market) set weekly by category, job size, and competition - see [plans/thumbtack-plans-pricing.yml](plans/thumbtack-plans-pricing.yml). Partner Platform integration terms are negotiated directly with Thumbtack.

## Common Properties

- [LinkedIn](https://www.linkedin.com/company/thumbtack-inc.)
- [Website](https://www.thumbtack.com)
- [Documentation](https://developers.thumbtack.com/)
- [Plans](plans/thumbtack-plans-pricing.yml)
- [Rate Limits](rate-limits/thumbtack-rate-limits.yml)
- [Fin Ops](finops/thumbtack-finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
