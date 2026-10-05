# Application APIs

Billow applications use Billow-native modules rather than direct Roblox engine access. These are capability-backed facades: an API being present does not automatically grant permission.

| Module | Purpose |
|---|---|
| `@billow/app` | identity, activation, lifecycle/events |
| `@billow/windows` | owned window/surface operations |
| `@billow/files` | opaque file-handle operations |
| `@billow/storage` | application-scoped persistent state |
| `@billow/ipc` | capability-mediated local service messaging |
| `@billow/notifications` | notifications |
| `@billow/clipboard` | permission-scoped clipboard operations |
| `@billow/logging` | application logging |

A file/window/IPC handle is an opaque Billow reference issued inside an authorized context. It cannot be usefully forged by guessing an ID and is not a raw Roblox object.

TypeScript is the default application authoring direction, with JavaScript and Luau alternatives. TS/JS end-to-end production integration is still marked **experimental** until the current standards cutover is certified.

Public code should depend on these module contracts, not private kernel/service hierarchy.
