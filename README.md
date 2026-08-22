# GoToWebinar (gotowebinar)

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
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

GoToWebinar is GoTo's (formerly LogMeIn) webinar and virtual event platform. The GoToWebinar REST API lets developers create and manage webinars, organizers, registrants, attendees, sessions, panelists, co-organizers, polls, surveys, and recordings, and subscribe to real-time webhook events for registrant and webinar lifecycle activity.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/gotowebinar/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/gotowebinar/main/apis.yml)

## Scope

- **Type:** Index
- **Position:** Consumer
- **Access:** 3rd-Party

## Tags

- Attendees
- Collaboration
- Communications
- Events
- Meetings
- Registrants
- Sessions
- Surveys
- Video Conferencing
- Virtual Events
- Webhooks
- Webinars

## Timestamps

- **Created:** 2026-05-23
- **Modified:** 2026-05-23

## APIs

### GoToWebinar REST API

The GoToWebinar V2 REST API exposes webinars, organizers, registrants, attendees, sessions, co-organizers, panelists, polls, questions, and surveys for the GoToWebinar virtual event platform, with OAuth 2.0 authentication via the GoTo authentication service.

- **Human URL:** [https://developer.goto.com/GoToWebinarV2](https://developer.goto.com/GoToWebinarV2)
- **Base URL:** `https://api.getgo.com/G2W/rest/v2`

#### Tags

- Attendees
- Co-Organizers
- Organizers
- Panelists
- Polls
- Questions
- Recordings
- Registrants
- Sessions
- Surveys
- Webinars

#### Properties

- [OpenAPI](openapi/gotowebinar-rest-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/gotowebinar-rest.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/gotowebinar-rest.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Documentation](https://developer.goto.com/GoToWebinarV2)
- [API Reference](https://developer.goto.com/GoToWebinarV2)
- [Getting Started](https://developer.goto.com/guides/Get%20Started/00_Quickstart_GettingStarted/)
- [Authentication](https://developer.goto.com/guides/Authentication/New_Token_Retrieval_Migration_Guide/)
- [Spectral Rules](rules/gotowebinar-rules.yml)

### GoToWebinar Webhooks API

The GoToWebinar Webhooks API lets developers create and manage webhook subscriptions and receive real-time HTTP callbacks for registrant.added, registrant.joined, webinar.created, and webinar.changed events, secured via the X-Webhook-Signature header.

- **Human URL:** [https://developer.goto.com/guides/GoToWebinar/07_HOW_WebHooksOverview/](https://developer.goto.com/guides/GoToWebinar/07_HOW_WebHooksOverview/)
- **Base URL:** `https://api.getgo.com/G2W/rest/v2`

#### Tags

- Callbacks
- Events
- Real-Time
- Subscriptions
- Webhooks

#### Properties

- [OpenAPI](openapi/gotowebinar-webhooks-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/gotowebinar-webhooks.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/gotowebinar-webhooks.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [AsyncAPI](asyncapi/gotowebinar-webhooks-asyncapi.yml) — [AsyncAPI Specification](https://www.asyncapi.com/docs/reference/specification/latest)
- [Documentation](https://developer.goto.com/guides/GoToWebinar/07_HOW_WebHooksOverview/)
- [API Reference](https://developer.goto.com/guides/GoToWebinar/08_HOW_webhooks/)

## Common Properties

- [Portal](https://developer.goto.com/)
- [Developer Portal](https://developer.goto.com/)
- [Documentation](https://developer.goto.com/)
- [Getting Started](https://developer.goto.com/guides/Get%20Started/00_Quickstart_GettingStarted/)
- [Authentication](https://developer.goto.com/guides/Authentication/New_Token_Retrieval_Migration_Guide/)
- [Changelog](https://developer.goto.com/changelog/)
- [Status Page](https://status.goto.com/)
- [Support](https://developer.goto.com/support)
- [Sign Up](https://developer.goto.com/)
- [Pricing](https://www.goto.com/pricing/webinar)
- [Marketplace](https://www.goto.com/integrations)
- [Partners](https://www.goto.com/partners)
- [JSON-LD](json-ld/gotowebinar-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [Vocabulary](vocabulary/gotowebinar-vocabulary.yml)
- [Plans](plans/gotowebinar-plans-pricing.yml)
- [Rate Limits](rate-limits/gotowebinar-rate-limits.yml)
- [Fin Ops](finops/gotowebinar-finops.yml)
- [Features](undefined)
- [Use Cases](undefined)
- [Integrations](undefined)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
