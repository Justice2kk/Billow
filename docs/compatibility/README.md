# Compatibility model

`compatibility/registry.json` is the authoritative public compatibility registry. [FEATURES.md](FEATURES.md) is generated from it.

Statuses intentionally distinguish `supported`, `supported_with_limits`, `experimental`, `unsupported`, `intentionally_unsupported`, `billow_extension`, `deprecated` and `planned`.

Supported/limited/experimental/Billow-extension entries require a verification identifier. Some map to conformance tests; others map to implementation contracts where a dedicated public test does not yet exist. This prevents generated documentation from silently claiming support with no evidence owner.

External resources are centralized in the registry. They teach transferable concepts; Billow docs still define the supported subset and differences.
