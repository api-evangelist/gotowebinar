# GoToWebinar (gotowebinar)

API Evangelist profile for **GoToWebinar**, the webinar and virtual event platform from [GoTo](https://www.goto.com/) (formerly Citrix / LogMeIn). GoToWebinar sits alongside GoToMeeting, GoToTraining, and GoToConnect inside the [GoTo Developer Center](https://developer.goto.com/) and exposes a REST V2 API plus a real-time webhook stream for registrant and webinar lifecycle events.

- Provider: <https://www.goto.com/webinar>
- Developer center: <https://developer.goto.com/>
- API reference: <https://developer.goto.com/GoToWebinarV2>
- Base URL: `https://api.getgo.com/G2W/rest/v2`
- OAuth: `https://authentication.logmeininc.com/oauth/authorize` and `/oauth/token`
- Status: <https://status.goto.com/>
- Changelog: <https://developer.goto.com/changelog/>

## APIs

| API | Base URL | OpenAPI |
| --- | --- | --- |
| GoToWebinar REST API | `https://api.getgo.com/G2W/rest/v2` | [openapi/gotowebinar-rest-openapi.yml](openapi/gotowebinar-rest-openapi.yml) |
| GoToWebinar Webhooks Management API | `https://api.getgo.com/G2W/rest/v2` | [openapi/gotowebinar-webhooks-openapi.yml](openapi/gotowebinar-webhooks-openapi.yml) |

The webhook event stream itself is documented as an AsyncAPI 2.6 spec at [asyncapi/gotowebinar-webhooks-asyncapi.yml](asyncapi/gotowebinar-webhooks-asyncapi.yml). All four documented event types are covered: `registrant.added`, `registrant.joined`, `webinar.created`, `webinar.changed`. Receivers validate authenticity using the `X-Webhook-Signature` HTTP header.

## Resource Coverage

The REST surface is scoped under `/organizers/{organizerKey}/...` and covers:

- **Webinars** - create, read, update, list (by time range), cancel (with `deleteAll` for recurring series)
- **Registrants** - create, read, list, delete
- **Attendees** - list all (per webinar), list per session, get single attendee
- **Sessions** - list past sessions
- **Co-Organizers** - list, add
- **Panelists** - list, add
- **Polls / Questions / Surveys** - per-session readout
- **Recordings** - list organizer recording assets

Plus a top-level webhook surface (`/webhooks`, `/webhooks/secretkey`, `/userSubscriptions`) for managing webhook definitions and per-user subscriptions.

## Artifacts In This Repo

| Artifact | Path |
| --- | --- |
| Network index | [apis.yml](apis.yml) |
| OpenAPI (REST) | [openapi/gotowebinar-rest-openapi.yml](openapi/gotowebinar-rest-openapi.yml) |
| OpenAPI (Webhooks mgmt) | [openapi/gotowebinar-webhooks-openapi.yml](openapi/gotowebinar-webhooks-openapi.yml) |
| AsyncAPI (Webhook events) | [asyncapi/gotowebinar-webhooks-asyncapi.yml](asyncapi/gotowebinar-webhooks-asyncapi.yml) |
| JSON Schemas | [json-schema/](json-schema/) - webinar, registrant, attendee, session, webhook |
| JSON Structures | [json-structure/](json-structure/) - webinar, registrant |
| JSON-LD context | [json-ld/gotowebinar-context.jsonld](json-ld/gotowebinar-context.jsonld) |
| Spectral rules | [rules/gotowebinar-rules.yml](rules/gotowebinar-rules.yml) |
| Naftiko capabilities | [capabilities/](capabilities/) - 8 capability files (webinars, registrants, attendees, sessions, co-organizers, panelists, polls/surveys, recordings, webhooks) |
| Examples | [examples/](examples/) - request/response and webhook payload samples |
| Vocabulary | [vocabulary/gotowebinar-vocabulary.yml](vocabulary/gotowebinar-vocabulary.yml) |
| Plans & pricing | [plans/gotowebinar-plans-pricing.yml](plans/gotowebinar-plans-pricing.yml) |
| Rate limits | [rate-limits/gotowebinar-rate-limits.yml](rate-limits/gotowebinar-rate-limits.yml) |
| FinOps profile | [finops/gotowebinar-finops.yml](finops/gotowebinar-finops.yml) |

## Pricing Snapshot (2026-05-23)

GoToWebinar publishes four seat-based plans tiered by attendees per event. Pricing reflects annual-billed monthly-equivalent rates.

| Plan | Monthly | Annual (mo) | Attendees |
| --- | --- | --- | --- |
| Lite | $59 | $49 | 250 |
| Standard | $129 | $99 | 500 |
| Pro | $249 | $199 | 1,000 |
| Enterprise | $499 | $399 | 3,000 |

API access is bundled with the seat license; there is no separately metered API surcharge.

## Notable Gaps

- GoTo does not publish a numeric default rate-limit value for the GoToWebinar V2 API; developers consult the internal Rate Limits reference and email `developer-support@goto.com` for increases.
- The GoTo authentication migration deadline is 2025-09-30 - legacy `api.getgo.com/oauth/v2/*` endpoints are deprecated in favor of `authentication.logmeininc.com/oauth/*`.
- There is no public GitHub organization for GoTo SDKs - the `LogMeIn` org is empty and `goto-developer` resources live entirely under `developer.goto.com`.
- Postman collections and OpenAPI downloads are linked from `developer.goto.com/GoToWebinarV2` but are not exposed at a stable raw URL.

## Maintainer

- Kin Lane - <kin@apievangelist.com>
