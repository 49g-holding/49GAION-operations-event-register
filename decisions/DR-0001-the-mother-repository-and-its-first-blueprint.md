# DR-0001 · The mother repository of the Operations Event Register, and its first mother blueprint

- **Date:** 2026-10-17
- **Decided by:** the governing seat (GOV) of 49GAION
- **Sources:** `49GAION/DR-0027` (the Operations Event Register; Organisation Memory); `49GAION/DR-0024` (a mother repository for a Library part); `49GAION/DR-0019` (the Library register) and `DR-0021` (mother and instance)

## Decision

1. **This repository.** `github.com/49g-holding/49GAION-operations-event-register`, public, is the mother repository of the Library part 49GAION Operations Event Register. It holds the mother blueprint only, laid out and checked as a writing repository. The part's instances will hold an organisation's data in their own private repositories and stores, so the mother lives here (`49GAION/DR-0024`).
2. **The first mother blueprint.** `blueprint/OER-BLUEPRINT.md` `v0.1.0`, the part's first blueprint, written for any organisation on the 49GAION AIOC template. No instance runs yet.
3. **Acts, not activity.** Every rule of the blueprint keeps the boundary of `49GAION/DR-0027`, item 4: every act of an AI Cell is recorded; of a human position, only its formal acts; no figure about one human position.
4. **The fixed test.** TEST-OER v1, 60 cases, every one `NOT_RUN`. The Library's TEST-OPERATIONS-EVENT-REGISTER v1 is kept as cases 1 to 16 (`tests/TEST-OER.md`).
5. **The Library pin.** Once merged, this text is pinned in `49GAION-protocol` `library/README.md` by repository, path, version, commit and SHA-256.

*Powered by 49GAION*
