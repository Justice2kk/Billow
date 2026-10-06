# Public file model

Public application APIs work with Billow-managed file/resource concepts and **opaque handles**, not arbitrary Roblox filesystem/Instance access.

A handle represents already-authorized access to an object. Read/stat/write/close remain capability checked, and a caller cannot gain authority by fabricating a path or identifier.

Internal persistence/storage implementation is intentionally not part of this public repository. Program against the documented file API rather than storage internals.
