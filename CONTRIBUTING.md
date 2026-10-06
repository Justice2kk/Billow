# Contributing to the public developer surface

This repository is contract/documentation work, not a place to mirror private Billow implementation files.

Before opening a change:

1. update `compatibility/registry.json` first when a compatibility claim changes;
2. attach a verification identifier to supported/limited/experimental/Billow-native claims;
3. do not strengthen a status because a feature merely resembles HTML/CSS/JavaScript;
4. keep Billow-native behavior visibly separate from standards compatibility;
5. do not copy private repository paths, service snapshots, secrets or implementation-only hierarchy into public docs;
6. run `python tools/validate_public.py --write` when the registry changes, then `python tools/validate_public.py --check`.

Documentation should answer a developer question or define a contract. Avoid duplicate overview files, generic contributor boilerplate and unverified roadmap promises.
