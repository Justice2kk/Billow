# HTML profile

Billow accepts a bounded HTML profile and turns it into an inert document model for controlled rendering. It is closer to HTML syntax/semantics than legacy JML authoring while rejecting browser features Billow cannot or should not reproduce.

## Document behavior

- bounded UTF-8 source, node count and depth;
- `<!doctype html>` required; no silent quirks-mode emulation;
- HTML-style case folding, character references, comments and common void elements;
- supported optional paragraph/list-item closing behavior;
- unsupported recovery cases produce explicit diagnostics.

The current profile includes common structural/semantic elements, headings/paragraphs, phrasing elements, lists, links, images, buttons and a bounded form profile. Exact entries are in the [compatibility index](../compatibility/FEATURES.md).

Important restrictions: links use approved navigation references; images require `src` and bounded UTF-8 `alt`; forms are currently Billow service-bound with `data-billow-service` and `data-billow-action` plus POST; current input types are text/search; tables/SVG/MathML/template/select are not current profile features; iframe-style embedding is intentionally outside the public security model.

`data-billow-service` and `data-billow-action` are **Billow extensions**. Ordinary HTML form knowledge transfers conceptually, but authority is resolved by Billow rather than an arbitrary Internet endpoint.
