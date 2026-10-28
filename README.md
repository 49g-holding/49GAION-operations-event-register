# 49GAION Operations Event Register · the mother blueprint

The mother repository of the Library part **49GAION Operations Event Register**. In an `[ORG]AION`, the part is the AIOC `[ORG]AIOC-OER`. This repository is public. It holds the mother blueprint only, for any organisation, with no organisation's data (`49GAION/DR-0024`, `DR-0027`; Naming Standard R9, addition 4).

> **Reading (49GAION DR-0041).** The complete definition of 49GAION, approved by its governing seat on 25 October 2026, is `49GAION-FRAMEWORK.md` in `github.com/49g-holding/49GAION`. Where this repository differs from it, the definition governs, and this text is read with it. Every rule here that names `[ORG]AIOC-OCO` or the human hub reads as the Top Management Group, the hub of the operation, human and AI. The panel is the organisation's own code interface, and the AI chat workspace is its back office. The readings are in [`decisions/DR-0003`](decisions/DR-0003-the-readings-of-dr-0041.md). Nothing here is removed.

> **Reading (49GAION DR-0048, DR-0049; `decisions/DR-0004`).** Only AIOCs and HOAC positions: every human place here is a position, and who holds it, and how, is the organisation's own mechanism, outside the system. The acting filler, deputies of human seats and `appoint-acting-filler` are withdrawn.

## What the part does

The Operations Event Register is the record of an organisation's live operation. It gives every formal act and crossing of the organisation's units and positions, on every surface the organisation connects, one number in one append-only, hash-chained register, by reference to where the content lives.

From that register it gives:
- every unit an inbox and an outbox;
- each unit and process its feedback: what it had and what it lacked;
- evidence on demand.

It also feeds Source Lifecycle with:
- the correspondence a position asks to keep;
- the projection of the work by role-type and process;
- gap signals.

It decides nothing, carries nothing, and says nothing about a person: acts, not activity (Protocol §22).

The one-page summary is at the top of the blueprint.

## What is here

| Path | What it is |
|---|---|
| [`blueprint/OER-BLUEPRINT.md`](blueprint/OER-BLUEPRINT.md) | the mother blueprint, `v0.1.1`, on the 49GAION AIOC template |
| [`tests/TEST-OER.md`](tests/TEST-OER.md) | the fixed test, TEST-OER v1: 60 cases, every one `NOT_RUN`, with the Library's TEST-OPERATIONS-EVENT-REGISTER v1 kept as cases 1 to 16 |
| [`cards/`](cards/) | the unit cards of its Pods and Cells, and the bot identity cards, generated from blueprint §17 |
| [`decisions/`](decisions/) | the decision records of this repository |
| [`upstream/PROPOSALS.md`](upstream/PROPOSALS.md) | drafts of proposals to 49GAION, not yet proposed |
| [`tools/make_cards.py`](tools/make_cards.py) | generates and checks the cards (case 41) |

## Mother and instance

- **The Library pins this text** by repository, path, version, commit and SHA-256 (`49GAION-protocol`, `library/README.md`). A new version reaches the Library only by a pull request that moves the pin.
- **Each organisation makes its own instance** from it: its writing repository `<org>aioc-oer`, private, with the `<organisation>`, `<org>` and `<filled>` values set (blueprint §0, §2.1). The organisation's values, and its register, never come back here.
- **With Source Lifecycle** it forms the Library product **49GAION Organisation Memory** (Standard §3.1, item 14): what the organisation knows, and what it did.

## Checks

**The Protocol pin.** The checks are the one set of checks of the Library repositories, the action `library-checks` of `49GAION-protocol`, run at the commit in `PROTOCOL-PIN`, which also gives the schemas and the `no-org-names` scanner they read, never at `main`, so a change in the Protocol changes nothing here until this repository moves the pin by pull request.

On every pull request and on main (`.github/workflows/checks.yml`):

```
python3 tools/make_cards.py <49GAION-protocol>/spec/schemas      # 0 errors; the committed cards are the generated cards
bash <49GAION-protocol>/.github/scripts/no-org-names.sh          # no organisation name, host or prefixed code
```

The checks also find no Persian or Arabic-script character in any tracked file.

## Owner and licence

- **Owner and licence.** The copyright holder, and the licences of the texts (CC BY 4.0, credit "Powered by 49GAION") and of the code (Apache-2.0), are in [`LICENSE.md`](LICENSE.md).

*Powered by 49GAION*
