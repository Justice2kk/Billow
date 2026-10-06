# Getting started

## Mental model

BillowOS is not a replacement for the device operating system and it does not pretend to provide real TCP sockets, native processes or direct Roblox engine access to public programs. It is an application platform running **inside Roblox** with a controlled OS-like model: applications, windows, files, packages, capabilities and a logical `billow://` web platform.

## If you know web development

Start with ordinary HTML and CSS concepts:

```text
HTML concept  → Billow HTML profile → controlled document model
CSS concept   → Billow CSS profile  → controlled layout/style model
page behavior → JS/TS page runtime  → capability-mediated APIs
URL concept   → billow://            → Billow route/deployment resolution
```

Billow is a deterministic subset. Current HTML supports common structural/text/link/image/form elements but not every browser tree-construction case. CSS supports a useful flex/layout/typography subset but not arbitrary browser CSS. Check the [compatibility index](../compatibility/FEATURES.md) before assuming a browser feature exists.

## Application languages

- TypeScript (`.ts`) — default direction, currently **experimental while production cutover finishes**;
- JavaScript (`.js`) — standards source under the same integration gate;
- Luau (`.lua` / `.luau`) — supported within Billow application authority boundaries.

Billow-native APIs such as `@billow/app`, `@billow/files`, `@billow/storage` and `@billow/ipc` expose bounded operations backed by capabilities, not raw Roblox services.

The [basic web example](../../examples/web/basic/README.md) is deliberately a source/conformance example. It does not invent a new site packaging manifest while that production contract is still being cut over.
