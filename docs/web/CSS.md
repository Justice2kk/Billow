# CSS profile

Billow CSS implements a deterministic subset of familiar CSS parsing, cascade, selectors, layout, typography and responsive behavior. Ordinary CSS tutorials are useful for concepts such as flexbox, margin, specificity and media queries; Billow documentation defines which parts transfer.

The current profile includes common size/position properties, flex layout, margin/padding/gap, typography, colors/backgrounds, opacity/overflow, borders, object fitting and interaction/geometry properties. The [compatibility index](../compatibility/FEATURES.md) lists every property.

Current length units include `px`, `%`, `vw` and `vh` where a property accepts them. Selectors include type, ID, class and universal selectors; descendant/child combinators; and `:hover`, `:focus`, `:disabled`, `:checked`, `:first-child`, `:last-child`. Responsive blocks support bounded `min-width`/`max-width` queries in pixels.

The current profile rejects attribute selectors, pseudo-elements, CSS custom properties and nested rules. A recognized property does not imply every browser value/edge case: the public promise is the documented renderer-faithful subset.
