# Whova (whova)

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

Whova is an award-winning all-in-one event management platform built around a mobile event app that carries the agenda, speaker profiles, attendee networking, live polls, and session Q&A, plus registration, ticketing, name badges, surveys, abstract/speaker management, and exhibitor/sponsor tools.

## API Access: Gated / No Open Developer API

**Whova does not publish an open, self-serve developer API.** There is no developer portal, no documented REST reference, no OpenAPI definition, and no SDKs. Searches for `api.whova.com`, `developer.whova.com`, and `whova.com/developer` turn up nothing, and third-party aggregator pages (apitracker.io, apiorb.com) that claim to list a "Whova API / SDKs" contain only auto-generated boilerplate with no real endpoints, authentication, or reference material.

The **only** genuine programmatic surface Whova offers organizers is a partner **CRM integration through Zapier**, reached in the organizer dashboard under **Attendees > Integrations > CRM Integration**. That connector exposes:

- **Triggers:** Get Attendees (attendee-list change), Get Orders (order-list change), Get Registrants (registration form submission)
- **Action:** Create or Update Attendee (name, email, title, company, location, ticket type, attendance mode)

Whova also ships prebuilt connectors to Eventbrite, Cvent, Constant Contact, RegFox, OpenReview, ConfTool, SharePoint/OneDrive, MailChimp, Wild Apricot, and Google Drive. None of these expose a Whova-hosted REST base URL, auth scheme, or WebSocket.

Because there is no public API reference, the four APIs listed below are **honestly modeled** logical views of Whova's integration and platform surface (see each API's `endpointsModeled`). They are **not** sourced from a Whova API reference, and no base URL, auth scheme, or endpoint paths are published by Whova.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/whova/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/whova/refs/heads/main/apis.yml)

## Tags

- Events
- Event Management
- Event App
- Registration
- Conferences
- Attendees
- Exhibitors
- Gated API
- Modeled

## Timestamps

- **Created:** 2026-07-05
- **Modified:** 2026-07-05

## APIs (Modeled)

### Whova Attendees API (Modeled)

Modeled view of Whova's attendee integration surface: a Get Attendees trigger and a Create or Update Attendee action, exposed only through the Zapier CRM integration. No public REST endpoints or auth scheme are documented by Whova.

- **Reference:** [Zapier — Whova Integrations](https://zapier.com/apps/whova/integrations)

### Whova Registration and Orders API (Modeled)

Modeled view of Whova's registration/order surface: Get Orders and Get Registrants triggers via Zapier, plus prebuilt ticketing connectors (Eventbrite, Cvent, RegFox). No public REST endpoints are documented.

- **Reference:** [Zapier — Whova Integrations](https://zapier.com/apps/whova/integrations)



## Common Properties

- [LinkedIn](https://www.linkedin.com/company/whova)
- [Website](https://whova.com/)
- [Documentation (Help Center)](https://whova.zendesk.com/hc/en-us)
- [Integrations (Zapier)](https://zapier.com/apps/whova/integrations)
- [Plans](plans/whova-plans-pricing.yml)
- [Blog](https://whova.com/blog/)

## Pricing

Whova does not publish list pricing. Cost is **quote-based / contact-sales**, determined per event by size, format (in-person, virtual, hybrid), duration, and selected modules. Whova offers a **free ticketing plan for free events**. There is no separate published API plan; the Zapier CRM integration carries no documented standalone API fee. See [plans/whova-plans-pricing.yml](plans/whova-plans-pricing.yml).

## WebSocket Review

**Does Whova expose a documented public WebSocket API?** No. See [review.yml](review.yml). Whova publishes no WebSocket (or SSE) endpoint — indeed no open developer API at all — so no AsyncAPI document was authored.

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
