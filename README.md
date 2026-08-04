# Liveblocks (liveblocks)

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

Liveblocks is a real-time collaboration platform that provides ready-made building blocks for multiplayer experiences, including presence, broadcast events, shared storage (LiveObject/LiveList/LiveMap), comments and threads, notifications, and Yjs-based collaborative documents. It exposes a public authorization endpoint, a server-side private REST API, and SDKs for React, JavaScript, Node.js, Python, Redux, Zustand, and Yjs.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/liveblocks/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/liveblocks/refs/heads/main/apis.yml)

## Scope

- **Type:** Index

## Tags

- Real-Time
- Collaboration
- Multiplayer
- Presence
- CRDT
- Yjs
- Comments
- Threads
- Notifications
- WebSockets

## Timestamps

- **Created:** 2026-05-23
- **Modified:** 2026-05-23

## APIs

### Liveblocks REST API

Server-side REST API for managing rooms, room access, storage, active users, broadcast events, comments and threads, notifications, Yjs documents, and version history. Authenticated with a secret key via Bearer authorization.

- **Human URL:** [https://liveblocks.io/docs/api-reference/rest-api-endpoints](https://liveblocks.io/docs/api-reference/rest-api-endpoints)
- **Base URL:** `https://api.liveblocks.io/v2`

#### Tags

- REST
- Rooms
- Storage
- Comments
- Threads
- Notifications
- Yjs
- Webhooks

#### Properties

- [Documentation](https://liveblocks.io/docs/api-reference/rest-api-endpoints)
- [Authentication](https://liveblocks.io/docs/authentication)
- [Webhooks](https://liveblocks.io/docs/platform/webhooks)
- [Postman Collection](collections/liveblocks.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/liveblocks.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Liveblocks Authorization API

Public-facing authorization endpoint used by client SDKs to exchange a server-issued token for a Liveblocks session. Supports access token and ID token authorization patterns.

- **Human URL:** [https://liveblocks.io/docs/authentication](https://liveblocks.io/docs/authentication)
- **Base URL:** `https://api.liveblocks.io/v2`

#### Tags

- Auth
- Tokens
- Sessions

#### Properties

- [Documentation](https://liveblocks.io/docs/authentication)
- [Postman Collection](collections/liveblocks.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/liveblocks.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Liveblocks Realtime Client API

WebSocket-based client API exposed through Liveblocks client SDKs for React, JavaScript, Redux, Zustand, Vue (community), and Yjs. Provides presence, broadcast events, Live storage data structures, and threads.

- **Human URL:** [https://liveblocks.io/docs](https://liveblocks.io/docs)
- **Base URL:** `https://api.liveblocks.io/v7`

#### Tags

- WebSocket
- Client SDK
- Presence
- Storage
- Yjs

#### Properties

- [Documentation](https://liveblocks.io/docs)
- [SDK](https://www.npmjs.com/package/@liveblocks/client)
- [SDK](https://www.npmjs.com/package/@liveblocks/react)
- [SDK](https://www.npmjs.com/package/@liveblocks/node)
- [SDK](https://www.npmjs.com/package/@liveblocks/yjs)
- [Postman Collection](collections/liveblocks.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/liveblocks.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Website](https://liveblocks.io)
- [Portal](https://liveblocks.io/docs)
- [Documentation](https://liveblocks.io/docs)
- [Sign Up](https://liveblocks.io/signup)
- [Login](https://liveblocks.io/dashboard)
- [Pricing](https://liveblocks.io/pricing)
- [Blog](https://liveblocks.io/blog)
- [Git Hub](https://github.com/liveblocks/liveblocks)
- [Examples](https://liveblocks.io/examples)
- [Changelog](https://liveblocks.io/changelog)
- [Status Page](https://status.liveblocks.io)
- [Terms of Service](https://liveblocks.io/terms)
- [Privacy Policy](https://liveblocks.io/privacy)
- [Support](https://liveblocks.io/support)
- [Community](https://liveblocks.io/discord)
- [L L Ms Txt](https://liveblocks.io/llms.txt)

## Maintainers

**FN:** Kin Lane
**Email:** kinlane@gmail.com
