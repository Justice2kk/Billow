# System overview

BillowOS is a hosted, server-authoritative platform above Roblox. Public applications and page programs interact with Billow services through validated, capability-mediated interfaces.

```text
Roblox host runtime
        │
        ▼
Billow trusted authority/services
  ├─ identity + capabilities
  ├─ application/package services
  ├─ virtual files + resources
  └─ web routes/deployments
        │ validated contracts
        ▼
Sandboxed Billow workloads
  ├─ applications
  └─ page programs
        │ controlled render/input descriptions
        ▼
Client presentation
  ├─ desktop/windows
  └─ Browser renderer
```

## Boundaries that matter

**Browser is a client of the web platform.** Addressing, origin, deployment, resources and publication are platform concepts the Browser consumes.

**Markup/styles become controlled representations.** HTML/CSS do not become arbitrary Roblox UI execution.

**Code is capability-mediated.** Public code uses Billow APIs and opaque handles. Raw Roblox Instances/services/remotes are outside the public sandbox contract.

**Published state is immutable.** Editing source and serving a public deployment are separate stages; a failed publication must not mutate the previous approved deployment.

**Familiarity is not equivalence.** The [compatibility registry](../compatibility/FEATURES.md) is authoritative about the supported subset.
