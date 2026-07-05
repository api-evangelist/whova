# Whova (whova)

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

### Whova Agenda and Sessions API (Modeled)

Modeled view of Whova's agenda/session surface. Whova imports sessions, speakers, and abstracts from spreadsheets and partner systems (OpenReview, ConfTool) but exposes no documented public API for agenda data.

- **Reference:** [OpenReview Integration](https://whova.com/blog/openreview-integration/)

### Whova Exhibitors and Sponsors API (Modeled)

Modeled view of Whova's exhibitor/sponsor surface (booths, sponsored sessions, lead retrieval via QR/stamp scanning, virtual booths). No documented public API for exhibitor or lead data.

- **Reference:** [Whova App Exhibitor Guide](https://whova.com/pages/whova-app-exhibitor-guide/)

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
