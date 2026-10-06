# Terminology

| Term | Meaning |
|---|---|
| **BillowOS** | Hosted application/web environment implemented inside Roblox. |
| **host** | Roblox and the underlying device/runtime. Public Billow code does not own this layer. |
| **capability** | Authority to perform a bounded operation on an allowed resource/service. Declaring an API does not self-grant authority. |
| **handle** | Opaque reference to an already-authorized object such as a file or window; not a raw Roblox Instance. |
| **application** | Installed Billow package/registration; it can exist without running. |
| **application instance** | One logical activation of an application. |
| **process** | Billow logical execution/security/accounting container, not a native OS process. |
| **page program** | Sandboxed behavior associated with a Billow web document. |
| **origin** | Web security identity used by Billow page/network/storage policy. |
| **deployment** | Immutable published web output selected by a route pointer. |
| **Billow-native** | Feature designed specifically for Billow rather than claimed standards equivalence. |
| **legacy authoring format** | JML/JSS/`.bts` vocabulary retained for migration/history; new direction is HTML/CSS/`.ts`. |
