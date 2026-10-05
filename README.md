# BillowOS developer platform

BillowOS is a hosted, capability-secured application and web environment implemented inside Roblox. Roblox remains the real host runtime; Billow provides its own application, file, package, window and `billow://` abstractions above it.

This repository is the **public developer surface**, not the private BillowOS implementation repository. It exists so a developer can understand what they can build, which familiar web/programming concepts transfer, where Billow deliberately differs, and which capabilities are stable enough to rely on.

## Current public direction

- **Applications:** TypeScript is the default authoring direction; JavaScript and Luau are supported alternatives.
- **Web:** HTML and CSS are the canonical markup/style direction. JavaScript/TypeScript page behavior is being integrated through Billow's capability-mediated page runtime.
- **Legacy authoring:** JML, JSS and `.bts` are migration/history vocabulary, not the recommended format for new work.
- **Security boundary:** public code does not receive arbitrary Roblox Instances/services, DataStore access, raw remotes, arbitrary Luau execution, or unrestricted external networking.

The standards-language cutover is still being integrated end to end. Documentation therefore distinguishes **supported**, **limited**, **experimental**, **unsupported**, **intentionally unsupported**, and **Billow-native** features instead of claiming browser compatibility that has not been proven.

## Start here

1. [Getting started](docs/getting-started/OVERVIEW.md)
2. [Platform terminology](docs/getting-started/TERMINOLOGY.md)
3. [Web platform](docs/web/README.md)
4. [Application APIs](docs/applications/README.md)
5. [Compatibility index](docs/compatibility/FEATURES.md)
6. [System overview](docs/architecture/SYSTEM_OVERVIEW.md)

If you already know HTML/CSS/web development, the compatibility index is the fastest route from a familiar term such as **flexbox**, **margin**, **DOM**, **event listener**, **image**, or **fetch** to the Billow equivalent and its current support level.

## Public/private boundary

This repository documents public contracts, examples, compatibility information and Billow-native developer APIs. It intentionally does not publish private kernel/runtime/security/persistence implementation source merely because those systems are described conceptually.

Public compatibility claims are validated from `compatibility/registry.json`. Generated compatibility pages and public-boundary checks run in CI:

```text
python tools/validate_public.py --check
```

## License status

Formal license terms for this public developer surface have not yet been published. Repository visibility should not be interpreted as an open-source license for the private BillowOS implementation.
