# Drafts of proposals to 49GAION

**`[ORG]AIOC-OER` mother blueprint v0.1.0 · 17 October 2026.** These are drafts only. Nothing here is proposed to 49GAION without the word of its governing seat, and then only by pull request, merged by that seat. Each draft is generalised: no organisation's name or data.

## 1. A negative test for person fields at every adapter

- **Current text.** Protocol §5, the ports and the input check: an input is checked against the receiver's card, its acceptance test and its provenance.
- **Proposed text.** Add: "An adapter to an outside work surface removes every field that identifies a natural person before any write. An input that cannot be cleared is refused, and nothing of it is kept. Each adapter carries a negative test that proves it."
- **Reason and evidence.** Most work surfaces carry the actor's name, address or handle in their event payloads (blueprint §12, item 1; Annex D).
- **Parts and tests affected.** Protocol §5; every part with an outside port; TEST-OPERATIONS-EVENT-REGISTER case 4.

## 2. Capture modes and snapshot hashes

- **Current text.** Protocol §14, item 1: records live in one home as immutable events.
- **Proposed text.** Add: "A record of an outside object states how it was captured (gated, pushed, fetched or reconciled). The hash of a mutable object is a snapshot hash, with its `as_of` time."
- **Reason and evidence.** Some surfaces send only a signal; the content is fetched and may change later (blueprint §12, item 2).
- **Parts and tests affected.** Protocol §14; TEST-OPERATIONS-EVENT-REGISTER case 3.

## 3. "Per position" for human positions, in every part

- **Current text.** Standard §1.1, item 10 lets the AI side measure per position, while DR-0023 keeps records of the work by role-type and process, never about a person, and Delivery and Implementation shows no measure for a single position (§3.1, item 5). `49GAION/DR-0027`, item 4 settles the reading for this part only.
- **Proposed text.** A reading note for every part: "For a human position, a measure per position means only the live state of its own open items, shown to that position; never a count, rate or history of its acts."
- **Reason and evidence.** The labour-law and data-protection review of this part (`49GAION/DR-0027`, Review); a position with one occupant identifies that person.
- **Parts and tests affected.** Standard §1.1, item 10; §4.1, items 13 and 15; Protocol §4.6, item 7.

*Powered by 49GAION*
