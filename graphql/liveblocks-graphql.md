# Liveblocks GraphQL Schema

Conceptual GraphQL schema for the [Liveblocks](https://liveblocks.io) collaborative presence and real-time sync platform.

**Source reference:** https://liveblocks.io/docs/api-reference/rest-api-endpoints

---

## Overview

Liveblocks provides infrastructure for building multiplayer collaborative experiences. Its REST API exposes endpoints for managing rooms, presence, shared storage (LiveObject / LiveList / LiveMap), Yjs documents, comments, threads, notifications, broadcast events, and webhooks. This schema maps those REST resources to a typed GraphQL surface.

---

## Schema file

[liveblocks-schema.graphql](./liveblocks-schema.graphql)

---

## Type inventory

### Room management

| Type | Description |
|---|---|
| `Room` | Primary container for a collaborative session |
| `RoomDetails` | Extended computed fields for a room |
| `RoomType` | Enum — `REGULAR` or `CUSTOM` |
| `RoomStatus` | Enum — `OPEN` or `CLOSED` |
| `RoomMetadata` | Arbitrary key-value metadata on a room |
| `RoomAccess` | Enum — `PUBLIC`, `PRIVATE`, or `UNLISTED` |
| `RoomPermissions` | Default, group, and user-level ACL for a room |
| `RoomConnection` | Cursor-paginated list of rooms |

### Users and presence

| Type | Description |
|---|---|
| `User` | A Liveblocks user identity |
| `UserDetails` | Extended profile fields for a user |
| `UserPresence` | Real-time presence data for a connected user |
| `UserInfo` | Static fields from an auth token or user-info endpoint |
| `Presence` | Full presence entry for a connected user |
| `PresenceDetails` | Detailed presence payload including cursor |
| `Cursor` | A user's cursor position within a document |
| `CursorDetails` | x/y coordinates and arbitrary cursor data |

### Sessions and connections

| Type | Description |
|---|---|
| `Session` | A Liveblocks session issued after authorization |
| `SessionDetails` | Metadata for a session token |
| `SessionStatus` | Enum — `ACTIVE`, `EXPIRED`, or `REVOKED` |
| `Connection` | A single WebSocket connection to a room |
| `ConnectionDetails` | Full details of a WebSocket connection |
| `ConnectionCount` | Aggregate connection count for a room |
| `ConnectionStatus` | Enum — `CONNECTED`, `DISCONNECTED`, or `RECONNECTING` |

### Documents and Yjs

| Type | Description |
|---|---|
| `Document` | A collaborative document stored in a room |
| `DocumentDetails` | Extended metadata about a document |
| `DocumentVersion` | A point-in-time snapshot of a document |
| `DocumentState` | Current content state of a document |
| `YDoc` | A Yjs-based shared document backed by Liveblocks |
| `YDocDetails` | Metadata for a Yjs document |
| `YjsUpdate` | A single incremental Yjs update payload |

### Storage

| Type | Description |
|---|---|
| `Storage` | Liveblocks shared storage for a room |
| `StorageDetails` | Metadata describing the storage layer |
| `StorageObject` | A single node in the Liveblocks storage tree |

### Comments and threads

| Type | Description |
|---|---|
| `Comment` | A comment posted within a thread |
| `CommentDetails` | Extended metadata for a comment |
| `CommentReaction` | An emoji reaction on a comment |
| `CommentAttachment` | A file or media attachment on a comment |
| `Thread` | A thread grouping one or more comments |
| `ThreadDetails` | Extended metadata for a thread |
| `ThreadStatus` | Enum — `OPEN` or `CLOSED` |
| `ThreadResolved` | Enum — `RESOLVED` or `UNRESOLVED` |
| `ThreadConnection` | Cursor-paginated list of threads |

### Notifications and mentions

| Type | Description |
|---|---|
| `Notification` | A notification sent to a user about collaborative activity |
| `NotificationDetails` | Full details for a notification |
| `NotificationKind` | Enum — `THREAD`, `COMMENT`, `MENTION`, `REACTION`, `TEXT_MENTION` |
| `Mention` | A @mention of a user inside a comment body |
| `MentionDetails` | Extended metadata for a mention |
| `NotificationConnection` | Cursor-paginated list of notifications |

### Collaboration aggregates

| Type | Description |
|---|---|
| `Collaboration` | Aggregate view of all collaborative activity in a room |
| `CollaborationDetails` | Summary statistics for collaboration in a room |

### Broadcast

| Type | Description |
|---|---|
| `Broadcast` | A broadcast event dispatched to all users in a room |
| `BroadcastMessage` | The payload of a broadcast event |

### Webhooks

| Type | Description |
|---|---|
| `Webhook` | A configured webhook endpoint |
| `WebhookEvent` | A webhook delivery event record |
| `WebhookHeaders` | Custom HTTP headers attached to webhook requests |

### Authentication and keys

| Type | Description |
|---|---|
| `AuthToken` | A Liveblocks authentication token |
| `PublicApiKey` | A public API key for client-side SDK initialization |
| `SecretApiKey` | A secret API key for server-side REST API calls |

### Pagination

| Type | Description |
|---|---|
| `PageInfo` | Cursor-based pagination metadata |

### Root types

| Type | Description |
|---|---|
| `Query` | Read operations — rooms, users, threads, notifications, storage, Yjs docs |
| `Mutation` | Write operations — create/delete rooms, broadcast, threads, comments, reactions |
| `Subscription` | Real-time subscriptions — presence, comments, storage, broadcasts, notifications |

---

## Key relationships

- A **Room** contains **Storage**, **Threads**, and a **YDoc**.
- A **Thread** contains one or more **Comments**.
- A **Comment** can have **CommentReactions** and **CommentAttachments**.
- A **Comment** body may include **Mentions**.
- Connected users expose **UserPresence**, which includes a **Cursor**.
- A **Webhook** fires **WebhookEvents** when platform events occur.
- **Notifications** are generated for mentions, reactions, and thread activity.

---

## Authentication

The Liveblocks REST API uses secret keys supplied as `Bearer` tokens in the `Authorization` header. Client SDKs exchange a server-issued token (via the authorization endpoint) for a **Session**. The schema represents both patterns via `AuthToken`, `PublicApiKey`, and `SecretApiKey`.

---

## References

- REST API reference: https://liveblocks.io/docs/api-reference/rest-api-endpoints
- Authentication guide: https://liveblocks.io/docs/authentication
- Webhooks guide: https://liveblocks.io/docs/platform/webhooks
- Platform overview: https://liveblocks.io/docs
