# Liveblocks (liveblocks)

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
