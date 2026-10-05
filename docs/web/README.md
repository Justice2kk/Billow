# Billow web platform

Billow web development uses familiar concepts where they fit honestly:

- [HTML](HTML.md) for document structure/semantics;
- [CSS](CSS.md) for a bounded cascade/layout/style model;
- JavaScript/TypeScript page behavior through a capability-mediated page API;
- `billow://` for logical routing and origin identity.

The Browser does not expose a normal browser DOM backed by arbitrary engine objects. Page code receives controlled element/document operations, origin-scoped storage, bounded same-origin requests and navigation. APIs resembling `getElementById`, class manipulation, event listeners, storage, `fetch` and `location` exist as Billow facades, but production JS/TS page integration remains **experimental** during the standards cutover.

Deliberate boundaries include no `innerHTML`-style raw-markup sink, no arbitrary cross-origin/external HTTP for untrusted pages, no iframe-like arbitrary browsing context, and no raw Roblox Instances/services/remotes.

Use the [compatibility index](../compatibility/FEATURES.md) to search by familiar terms.
