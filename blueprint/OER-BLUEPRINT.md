```yaml
# ── Blueprint metadata (machine-readable; the panel generator and the back-office builder read this block) ──
blueprint:
  aioc: "[ORG]AIOC-OER"
  parent: "[ORG]AIOC-CH"                  # example code of the Charter; each organisation writes its own Charter's code (Standard §1.7, item 13)
  full_name: "Operations Event Register"
  organisation: "<organisation>"          # filled in each organisation's own copy
  type: "foundational"
  org_aion: "[ORG]AION"
  blueprint_version: "v0.1.2"
  status: "draft"
  template:
    name: "49GAION AIOC Blueprint Template"
    version: "v1.5.0, with the unreleased v1.6.0 additions on main"
    source: "github.com/49g-holding/49GAION-aioc, template/AIOC-BLUEPRINT-TEMPLATE.md @ 1abae80"
  mother:
    name: "49GAION Operations Event Register"
    version: "part card v1 (DRAFT)"
    source: "github.com/49g-holding/49GAION-protocol, library/cards/operations-event-register.part-card.json and the Protocol section Operations Event Register (§22); Standard §3.1, item 13. This text is its mother blueprint, in its mother repository github.com/49g-holding/49GAION-operations-event-register (49GAION DR-0024, DR-0027)"
  writing_repository: "<org>aioc-oer"
  code_project: "<org>aioc-oer, on the organisation's code platform"
  panel_register_id: "none yet"
  capabilities:
    standard: ["Chief of Staff", "Office", "Input socket", "Panel"]
    functional: ["Capture", "Classification", "Numbering and Chain", "Linking", "Follow-up", "Inbox, Outbox and Projections", "Coverage Feedback", "Feeds to Source Lifecycle", "Evidence and Case Packs", "Integrity", "Surface Connection"]
```

# Blueprint · `[ORG]AIOC-OER` · Operations Event Register · `v0.1.2`

**Draft, 17 October 2026. v0.1.1, 19 October 2026: the Chief of Staff takes its COS code `[ORG]CELL-COSOER` (`decisions/DR-0002`).** **This is the mother blueprint** of the Library part 49GAION Operations Event Register, for any organisation (`49GAION/DR-0027`; `decisions/DR-0001`). It is the part's first blueprint: no instance runs yet, and nothing here has run. Every fixed test reads `NOT_RUN`. Every rule rests on a 49GAION text, cited by section, or is new in this blueprint and marked **New**. Each organisation fills its own copy (§0, §2.1), and its values never come back here.

> **The Operations Event Register in one page**
>
> The Operations Event Register (OER) is the record of an organisation's live operation. It gives every formal act and every crossing between the organisation's units and positions one number in one register. Every crossing is recorded on every surface the organisation connects:
> - letters and formal e-mail, in and out;
> - the organisation's own posts;
> - requests between its entities and between its units;
> - hand-offs between its AI units at the tool gateway;
> - merges and releases on its code hosts;
> - changes of state on its task tracker and knowledge base;
> - the formal channels of its team chat.
>
> **It records; it does not carry.** Each item stays in its home: mail in the mail system, code on the code host, Work Items in the shared queue, AI traffic in the gateway log, posts on their platform. An entry holds:
> - its number;
> - its parties, as unit or position codes;
> - its times;
> - a reference to its home;
> - the SHA-256 of its content;
> - its follow-up state.
>
> **What comes out**
> 1. **An inbox and an outbox for every unit**, from a whole entity down to one position: what came in, what went out, what is open and what is due.
> 2. **Feedback for every part**: what it had and what it lacked. For each unit and each process this means what was recorded and what was missing, what was answered and what is overdue, what was linked and what is orphaned, and what was done with a source and what without one.
> 3. **Evidence on demand**: "what did we send them, and when?" in one query, and an evidence pack verified by hash.
> 4. **For the rest of the `[ORG]AION`**:
>    - Source Lifecycle receives the correspondence a position asks to keep, the projection of the work by role-type and process, and a gap signal for work done without a source.
>    - The design stages read how the work really runs.
>    - The internal-audit line reads the register directly; Self-Improvement reads it once top management adds it to the process's access.
>    - A position's handover list is built on request, for top management's handover entry.
>
> **What it never does**
> - It decides nothing, sends nothing, and refuses nothing on its merits. The tool gateway gates; the register records.
> - Nothing on the accountability path ever waits on it, and when it is down, work goes on and is registered late.
> - **Acts, not activity.** Every act of an AI Cell is recorded, except that a Cell acting for a position is recorded only for the acts that leave the position's sphere. Of a human position, only its formal acts are recorded. The register never sweeps a mailbox or a chat. It keeps no read or response times, no presence and no recordings, and never counts, rates or keeps the history of a human position's acts. A human position sees only the live state of its own open items.
> - It holds no secret, and never names a person.
>
> **Who decides**
> - The Cell carrying `[ORG]HOAC-TM` decides which surfaces and acts are formal.
> - The position that holds data protection decides each surface's impact assessment and lawful basis (HF-17).
> - The Operations Event Register Lead signs each connection.
> - The register itself decides nothing.

**Where this blueprint stands.** The part is named in the Standard (§3.1, item 13) and in its Protocol section (§22). This blueprint states what the AIOC is. Its code, its adapters and its runtime are not built. The decisions only a human seat can take are listed once, in §13.

> **Reading (49GAION DR-0041).** The complete definition of 49GAION, approved by its governing seat on 25 October 2026, is `49GAION-FRAMEWORK.md` in `github.com/49g-holding/49GAION`. Where this repository differs from it, the definition governs, and this text is read with it. Every rule here that names `[ORG]AIOC-OCO` or the human hub reads as the Top Management Group, the hub of the operation, human and AI. The panel is the organisation's own code interface, and the AI chat workspace is its back office. The readings are in [`decisions/DR-0003`](../decisions/DR-0003-the-readings-of-dr-0041.md). Nothing here is removed.

---

## 0. Identity and lineage

| Field | Value |
|---|---|
| Code | `[ORG]AIOC-OER`. Collision check (Naming Standard §5): **O**perations **E**vent **R**egister → OER. It does not recreate `AIOC`, `AION` or `49GAION`. It is not an existing or retired code of the 49GAION corpus, and does not read as a version suffix or a misleading acronym. Each organisation checks it against its own unit register before first use (§17) |
| Full name | Operations Event Register |
| Description | "`[ORG]AIOC-OER` is `<organisation>`'s Operations Event Register core, built from 49GAION Operations Event Register" |
| Kind | AIOC |
| Parent | `<code of the Charter of this [ORG]AION>`; the cards use the example code `[ORG]AIOC-CH`. A top-level AIOC, beside Source Lifecycle. A change of parent is the listed type `change-parent` |
| Inner units | `[ORG]CELL-OERL`, `[ORG]CELL-COSOER`, `[ORG]CELL-OERIC`, `[ORG]POD-OERCR`, `[ORG]POD-OERLF`, `[ORG]POD-OERPF`: three Pods with their six Cells, and three Cells directly under the AIOC (§17). No inner AIOC |
| HOAC label | `[ORG]HOAC-ACS`, held by its top Cell, the Operations Event Register Lead `[ORG]CELL-OERL` (`label_holder`) |
| Accountable to | `<code of the Cell carrying [ORG]HOAC-TM>`; the cards use the example code `[ORG]CELL-TMS` (Naming Standard R15). That Cell signs this AIOC's install, its `change-parent` and its `restart-stopped-unit` (Standard §5.3, item 4; §4.4, item 3) |
| Type | Foundational: every unit's inbox and outbox, and the feedback to every part, rest on it (§16) |
| `[ORG]AION` | `[ORG]AION`, based on 49GAION Standard `v1.5.0`, with the unreleased `v1.6.0` texts on main |
| Versioned Definition | this file; the Panel and the Back office are built from it |
| Organisation | `<organisation>` |
| Made from | the Library part 49GAION Operations Event Register, part card `v1` (DRAFT), and Protocol §22 |
| Template | 49GAION AIOC Blueprint Template `v1.5.0` at `1abae80`, with the `v1.6.0` additions: the mechanism register and Reserve, checks that are not fixed tests, the added Configuration rows, position codes only, the stages table, the Library's cases, and Done when |
| Mother | 49GAION Operations Event Register, part card `v1`. This text is its mother blueprint, held in the part's mother repository `github.com/49g-holding/49GAION-operations-event-register` and pinned in the Library register (`49GAION/DR-0024`, `DR-0027`) |
| Blueprint version and status | `v0.1.2` · draft |
| Accountable seat (`[ORG]HOAC-ACS`) | the Operations Event Register Lead, `[ORG]CELL-OERL`, a HOAC position. Who holds it is the organisation's own mechanism, outside the system; this AIOC never sees it (Standard §1.1, item 9) |
| Reports to | the Cell carrying `[ORG]HOAC-TM` |
| Writing repository | `<org>aioc-oer`, private where it holds the organisation's data. It has two companions: `-records` for the AIOC's own run records, and `-records-restricted` for records that name a person (Naming Standard R9; Protocol §14, item 6). The register itself lives in the runtime's own store, never in a repository (§7) |
| Code project | `<org>aioc-oer`, on the organisation's code platform: the adapters, the register's store and its projections |
| Panel | not yet built (§4.4) |
| Back office | not yet built |
| Attribution | Powered by 49GAION |

**Lineage.** The idea began as a registry office, the secretariat an organisation keeps so that every incoming letter is registered first and its origin known, and every outgoing letter passes through it too. It was first reviewed as a side of Source Lifecycle. The governing seat of 49GAION made it an AIOC of its own, widened it from correspondence to almost every act of the live operation, and named it (`49GAION/DR-0027`). Three independent reviews shaped it: the role in an `[ORG]AION` and the architecture; governance, data protection and labour law; and product, connectors and name. All three agreed on one condition: acts, not activity.

---

## 1. Card (49GAION Operating Protocol §3)

```yaml
card:
  unit_kind: "AIOC"
  code: "[ORG]AIOC-OER"
  parent: "[ORG]AIOC-CH"                  # example code of the Charter, the root AIOC; only it has parent none (Standard §1.7, item 13)
  inner_units: ["[ORG]CELL-OERL", "[ORG]CELL-COSOER", "[ORG]CELL-OERIC", "[ORG]POD-OERCR", "[ORG]POD-OERLF", "[ORG]POD-OERPF"]
  type: "foundational"
  org_aion: "[ORG]AION"
  card_version: "v0.1.2"
  input_door: "Chief of Staff"
  wake: { method: "queue", verified: false }
  receives:
    - kind: "surface event"               # a change of state of a work object on a connected surface
      format: "event from a surface adapter, through the tool gateway, on the surface-in port of the Capture Clerk: the object's home reference, its new state, its time, its content hash, and its parties as codes once the Input socket has removed every person field"
      acceptance_test: "TEST-OER v1, cases 2, 4, 17, 18, 21"
      decision_needed: false
    - kind: "gateway record"              # AI hand-offs and the root of each gateway log segment, read only
      format: "a hand-off record (Cell codes, payload hash) or a log segment root, read from the tool gateway's log on the gateway-log-in port"
      acceptance_test: "TEST-OER v1, cases 7, 36"
      decision_needed: false
    - kind: "registration request"        # register first: the gateway registers a formal outgoing item before it releases it
      format: "the item's metadata and content hash at release; its number issued by the numbering service (Protocol §14, item 4)"
      acceptance_test: "TEST-OER v1, cases 5, 22"
      decision_needed: false
    - kind: "file request"                # a position asks to keep an entry, or files an item from its personal mailbox
      format: "the position's own act, through the HU input port: 'file this', with the entry or the item's reference"
      acceptance_test: "TEST-OER v1, cases 8, 30"
      decision_needed: false
    - kind: "surface connection request"  # a new surface, entity or class of act
      format: "Work Item (Protocol §4.1) naming the surface, the entities, the classes of act, the stated purpose, and the records of the decisions before it (Annex F)"
      acceptance_test: "TEST-OER v1, cases 14, 37"
      decision_needed: true               # connect-external-port, signed at the tool gateway by the Lead after the scope and the HF-17 decision are recorded
    - kind: "notice from Source Lifecycle" # supersession, revocation or reclassification of a source an act cited; and references only of cited sources
      format: "notice naming each affected reference and version, never the content (Protocol §13, items 9 and 12); a source reference (ID, version, status, held or not held) read under the register's signed grant"
      acceptance_test: "TEST-OER v1, case 23"
      decision_needed: false
  delivers:
    - kind: "register entry"
      format: "append-only, hash-chained entry (Annex B), in the register's own store"
      usual_receivers: ["the register itself; read by the Panel, Self-Improvement and the internal-audit line"]
    - kind: "inbox and outbox"
      format: "Panel view of the entries at a unit's ports, rebuilt from the events"
      usual_receivers: ["every unit and position of the [ORG]AION, through its HU output port"]
    - kind: "notice of due or overdue"
      format: "notice to the owning position of an open entry: its number, its reference, its due date; never an order"
      usual_receivers: ["the owning position", "the watchdog (Protocol §4.6, item 5)"]
    - kind: "coverage feedback"
      format: "measures M1 to M8 (Annex C) by entity, unit, process and AI Cell, each with its logic version and trace to its events"
      usual_receivers: ["the unit's own seat", "the Cell carrying [ORG]HOAC-TM", "Self-Improvement, pseudonymised, once [ORG]HOAC-TM adds the register to its access"]
    - kind: "correspondence filing"
      format: "a source of origin kind correspondence, filed into Source Lifecycle with the entry's content hash, on behalf of the position that asked to keep it"
      usual_receivers: ["[ORG]AIOC-SL"]
    - kind: "activity export"
      format: "the projection of the work as it runs, by role-type and process, with its as-of date, filed into Source Lifecycle as an export after its HF-17 decision"
      usual_receivers: ["[ORG]AIOC-SL"]
    - kind: "gap signal"
      format: "one signal per act done without a source, by reference to the entry, never content"
      usual_receivers: ["[ORG]AIOC-SL"]
    - kind: "evidence pack"
      format: "the entries asked for, their homes and hashes, verified by re-hash where the home is readable"
      usual_receivers: ["the asking position, through its HU output port"]
    - kind: "handover list"
      format: "a position's open entries and commitments, rebuilt from the events, on request"
      usual_receivers: ["that position, through its HU output port", "the Cell carrying [ORG]HOAC-TM, for its handover entry (Protocol §4.10, item 17)"]
    - kind: "case pack"
      format: "pseudonymised past cases of a process, replayable, under a Work Item of the Cell carrying [ORG]HOAC-TM"
      usual_receivers: ["Self-Improvement, for shadow runs, once its access includes the register", "the human seat that chooses the golden set, and the assurance unit, for golden-set cases (Standard §2.3, items 7 and 9; §2.4, item 4)"]
    - kind: "integrity finding"
      format: "a gap, a census difference, a rebuild difference or a missing segment anchor, with its evidence"
      usual_receivers: ["the Operations Event Register Lead", "the internal-audit line (HF-19)"]
  anatomy:
    panel: { health: { tests: true, metrics: ["stuck", "returned", "late", "entries registered late", "lag", "number gaps", "census differences", "rebuild differences", "segment anchors missing", "surfaces connected", "surfaces waiting for decisions", "open entries past due", "file requests", "feeds waiting"] } }
    back_office: { converses_with_humans: true, hosts: ["Chief of Staff", "Office"], protocol_traffic: true }
    definition: { location: "<org>aioc-oer, blueprint/OER-BLUEPRINT.md", version: "v0.1.2" }
    delivery: { rollback: "one-click" }
    connectors:
      - { role: "mail system (functional mailboxes)", connector: "surface adapter, one per surface type", access_managed_in: "panel" }   # every grant is signed at the tool gateway as connect-external-port (Protocol §22, item 14)
      - { role: "letters (the dispatch and arrival record)", connector: "surface adapter", access_managed_in: "panel" }
      - { role: "the organisation's own social accounts", connector: "surface adapter, one per platform", access_managed_in: "panel" }
      - { role: "code hosts", connector: "surface adapter, one per host", access_managed_in: "panel" }
      - { role: "task tracker", connector: "surface adapter", access_managed_in: "panel" }
      - { role: "knowledge base", connector: "surface adapter", access_managed_in: "panel" }
      - { role: "team chat (formal channels only)", connector: "surface adapter", access_managed_in: "panel" }
      - { role: "calendars of decision bodies", connector: "surface adapter", access_managed_in: "panel" }
    gateway: { metering_id: "<per-AIOC metering id>" }
  full_name: "Operations Event Register"
  version: "0.1.2"
  lineage: { id: "[ORG]AIOC-OER", version: "0.1.2", relation: "original" }
  lifecycle_state: "designed"
  blueprint_version: "v0.1.2"
  template_version: "v1.5.0"
  accountable_to: "[ORG]CELL-TMS"         # example code of the Cell carrying [ORG]HOAC-TM (Naming Standard R15); never a Cell inside this AIOC
  top_cell: "[ORG]CELL-OERL"
  hoac: "[ORG]HOAC-ACS"
  label_holder: "[ORG]CELL-OERL"
  fixed_test: { id: "TEST-OER", version: "v1", owner: "[ORG]CELL-TMS" }
  skills:
    - { id: "oer-capture", name: "Capture of formal acts from every connected surface, by reference and hash", tags: ["capture"] }
    - { id: "oer-register", name: "Numbering, hash chain and classification of entries", tags: ["register"] }
    - { id: "oer-follow-up", name: "Linking and follow-up of open entries", tags: ["follow-up"] }
    - { id: "oer-feedback", name: "Inbox, outbox and coverage feedback by unit and process", tags: ["feedback"] }
    - { id: "oer-evidence", name: "Evidence packs, handover lists and case packs", tags: ["evidence"] }
  ports:
    - { unit: "[ORG]AIOC-OER", port: "ai-in", direction: "input", type: "AI", identification: "technical-key", accepted_content: ["surface event", "gateway record", "registration request", "notice from Source Lifecycle"], authority_limit: "within each surface's signed grant and the classes of act set as formal; a person field is removed before any write, and an event that cannot be cleared of it is refused", audit_trail: "the register's own event store and the unit register", required_tests: ["TEST-OER v1"], enforcement: "shared-gateway-outside-unit" }
    - { unit: "[ORG]AIOC-OER", port: "ai-out", direction: "output", type: "AI", identification: "technical-key", accepted_content: ["correspondence filing", "activity export", "gap signal", "case pack", "notice of due or overdue"], authority_limit: "by reference and hash only; never content beyond a filing a position asked for; never a person's name; never a figure about one human position", audit_trail: "the register's own event store and the Work Item record", required_tests: ["TEST-OER v1"], enforcement: "shared-gateway-outside-unit" }
    - { unit: "[ORG]AIOC-OER", port: "hu-in", direction: "input", type: "HU", identification: "live-human-sign-in-at-gateway", accepted_content: ["file request", "surface connection request", "evidence pack request", "closure of an entry with its reason", "direction from the Lead"], authority_limit: "the position's own entries and its authority_scope; a connection needs its signature at the tool gateway", audit_trail: "the register's own event store", required_tests: ["TEST-OER v1"], enforcement: "shared-gateway-outside-unit" }
    - { unit: "[ORG]AIOC-OER", port: "hu-out", direction: "output", type: "HU", identification: "live-human-sign-in-at-gateway", accepted_content: ["inbox and outbox", "notice of due or overdue", "coverage feedback", "evidence pack", "handover list", "return brief", "brief to the Lead"], authority_limit: "information only; a human position sees only its own open items, never a measure of itself or of another human position", audit_trail: "the register's own event store", required_tests: ["TEST-OER v1"], enforcement: "shared-gateway-outside-unit" }
    - { unit: "[ORG]AIOC-OER", port: "stop", direction: "input", type: "HU", identification: "live-human-sign-in-at-gateway", accepted_content: ["stop"], authority_limit: "stop only", audit_trail: "unit register", required_tests: ["TEST-OER v1"], enforcement: "shared-gateway-outside-unit", stop_door: true }
  configuration:                          # every slot is set by the organisation (§15); an empty slot fails the joining test
    office_accountable_human: { value: "<set by the organisation>", set_by: "<position>", date: "<date>", version: "<vN>" }
    central_head: { value: "<code of [ORG]AIOC-OCO>", set_by: "<position>", date: "<date>", version: "<vN>" }
    discussion_limits: { value: "<set by the organisation>", set_by: "<position>", date: "<date>", version: "<vN>" }
    waiting_deadlines: { value: "<per status>", set_by: "<Cell carrying [ORG]HOAC-TM>", date: "<date>", version: "<vN>" }
    bounce_limit: { value: "<number>", set_by: "<position>", date: "<date>", version: "<vN>" }
    chain_depth: { value: "<number, at least 1>", set_by: "<position>", date: "<date>", version: "<vN>" }
    halt_request_priority: { value: "immediate", set_by: "<position>", date: "<date>", version: "<vN>" }
    budget_cap: { value: "<amount per period>", set_by: "<Cell carrying [ORG]HOAC-TM>", date: "<date>", version: "<vN>" }
    unattended_action: "read-record-triage"
    formal_scope: { value: "<surfaces, entities and classes of act set as formal, with the stated purpose, Annex A>", set_by: "<Cell carrying [ORG]HOAC-TM>", date: "<date>", version: "<vN>" }
    minimum_group_size: { value: "3", set_by: "<Cell carrying [ORG]HOAC-TM>", date: "<date>", version: "<vN>" }
    retention_schedule: { value: "<per entity and class>", set_by: "<Cell carrying [ORG]HOAC-GOV> (HF-01)", date: "<date>", version: "<vN>" }
    records_officer_position: { value: "<position code>", set_by: "<Cell carrying [ORG]HOAC-TM>", date: "<date>", version: "<vN>" }
    data_protection_position: { value: "<position code>", set_by: "<Cell carrying [ORG]HOAC-TM> (HF-17)", date: "<date>", version: "<vN>" }
    register_first: { value: "<off, or the classes it applies to>", set_by: "<Cells carrying [ORG]HOAC-TM and [ORG]HOAC-GOV> (change-gateway-policy)", date: "<date>", version: "<vN>" }
```

**Joining the protocol.** This AIOC joins only after every input and output on this card passes fixed samples (the joining test, Protocol §11, item 1; Standard §3.2, item 4). Until then its `lifecycle_state` stays `designed` and no Work Item is routed to it. A surface is connected only through the sequence of Annex F; with none connected, the card still joins on fixtures, and the Panel reads `no surface connected`. The cards of its Pods and Cells are set in §17 and generated into `cards/`.

---

## 2. Organisation table and placement

### 2.1 Organisation table

The blueprint writes `[ORG]` for the organisation's prefix, as central texts do (Naming Standard R13). Each organisation fills `[ORG]` in its own copy. Positions only; who holds each one is kept only in the private register copy (Standard §5.2, Position Principle).

| Term in the blueprint | In `<organisation>` |
|---|---|
| `[ORG]AION` | `<filled by the organisation>` |
| The Top Office (decisions are signed by human Cells carrying HOAC labels) | `<filled by the organisation>`, the human hub |
| The Cell carrying `[ORG]HOAC-GOV` | the Governing Body position, `<code>` |
| The Cell carrying `[ORG]HOAC-TM` | the human hub position, `<code>`; the cards use the example code `[ORG]CELL-TMS` until the organisation's register gives its code |
| `[ORG]AIOC-OCO` | `<filled>`, the Operating Core Office |
| The Charter of this `[ORG]AION` | `<code from the organisation's register>`; the cards use the example code `[ORG]AIOC-CH` |
| `[ORG]AIOC-SL` | `<filled>`, Source Lifecycle, where the feeds of §5.8 are filed |
| The entities | `<filled>`: each legal entity of the organisation has its own number streams and its own universe of entries (Protocol §22, item 14) |
| The surfaces | `<filled>`, by role only in this blueprint (§8). Each surface's product name appears only in the organisation's own copy (Protocol §10, item 5) |
| The position that holds data protection (HF-17) | `<position code>`, set in `data_protection_position` (§15) |
| The Records Officer | `<position code>`, a HOAC position elsewhere in the organisation, set in `records_officer_position` (§15). It receives items that look legal or regulatory, holds the retention schedule's application, and places and lifts legal holds as the organisation's rules allow |
| The internal-audit line (HF-19) | `<position code>` |
| The engineering division | `<to be set by the human hub>`: builds the adapters and the store |
| The IT and infrastructure division | `<filled>` (the vault, the tool gateway's hosting, the register's store) |
| The tool gateway | held in the Charter (Standard §4.4, item 11). Every surface connection, every register-first issue and every stop passes through it |

### 2.2 Placement

- **Where it sits.** A top-level AIOC under the Charter, beside Source Lifecycle. Like every part, it enters through OCO.
- **Its role.** It keeps the record of the organisation's live operation, so that every formal act has a number, a home and a state, and every part can see what it had and what it lacked.
- **Scope.**
  - **It does:** capture the formal acts and crossings of the organisation's units and positions from every connected surface; classify, number and chain them; link them to their threads, Work Items, decisions, releases and sources; follow open entries to their due dates; show every unit its inbox and outbox; give each unit and process its coverage feedback; file into Source Lifecycle what a position asks to keep, the projection of the work and the gap signals; build evidence packs, handover lists and case packs; prove its own integrity every day.
  - **It does not:** decide, send, authorise or refuse anything on its merits; hold the content of what it records; watch a person's activity; measure, rank or compare human positions; sweep a mailbox or a chat; record a call; read a private message; take any part of the whistleblowing channel; give an order; hold a secret.
- **Companies it serves.** Every entity of the organisation, each with its own number streams and universe.
- **Boundaries with other AIOCs and parts.**

  | Part (home of) | This AIOC does | It never |
  |---|---|---|
  | The tool gateway and its log (Standard §4.4, item 11) | reads its hand-offs and segment roots, read only; records the register-first issue the gateway asks for | gates, signs, refuses on merit, writes the gateway log, or holds a signature |
  | The shared queue and Work Items (Protocol §2, §4) | uses a Work Item's ID as the entry's link for a request between units; projects the queue's events | opens, routes, owns or closes a Work Item |
  | Provenance (Protocol §8) | checks after the fact whether an act cited a valid source | edits a Work Item or a source |
  | `[ORG]AIOC-SL` (Protocol §13): content and sources | files what a position asks to keep, the activity export and gap signals; reads references only of the sources its entries cite, under its signed grant (Protocol §13, item 12) | reads or holds content; serves a source |
  | Panels, built by `[ORG]AIOC-OCO` (Standard §5.3, item 5) | serves projections as portals (Protocol §14, item 2) | builds a Panel or an HU route |
  | The unit register | reads the `position` entries of each unit and position | writes it, or reads anything about who holds a position |
  | Self-Improvement, in `[ORG]HOAC-TM` (Standard §2) | gives evidence and shadow-run case packs, pseudonymised, once `[ORG]HOAC-TM` adds the register to the process's access (§2.1, items 7 and 8) | becomes its only path (§2.1, item 7); gives it entries of the accountability path or golden-set cases; grades a unit (§2.3, item 9) |
  | The internal-audit line (HF-19) and the Outside Inspector | is read by them directly, read only | audits, inspects, or becomes the internal-audit line |
  | The watchdog (Protocol §4.6, item 5) | shows what is due and overdue | chases, gives orders, or escalates in its own name |

- **Overlap.** None inside an `[ORG]AION`. The gateway log and this register overlap only in AI traffic: the log stays its home, and the register keeps one root hash per log segment and the hand-offs (§5.10).

---

## 3. Positions

| Position (standard title) | Purpose | Reports to | Run today by | Cover |
|---|---|---|---|---|
| Operations Event Register Lead (HOAC position) | the accountable seat of this AIOC. It signs each surface connection (`connect-external-port`) once the scope and the HF-17 decision are recorded, and revokes. It owns the fixed tests of its parts and rules on what the Chief of Staff raises. It answers for the register, never for the content of what it records | the Cell carrying `[ORG]HOAC-TM` | a HOAC position (`[ORG]HOAC-ACS`). Who holds it, and how, is the organisation's own mechanism, outside the system; this AIOC never sees it. While the position is empty (no credential in force for it), the Chief of Staff only advises, matters go to the Cell carrying `[ORG]HOAC-TM`, and every act that needs this position's signature waits (Protocol §4.10, item 21) | the organisation's own mechanism, outside the system |
| Chief of Staff | keeps the register running and honest; this AIOC's voice to the Lead; the door for file requests, evidence requests and surface connection requests | Operations Event Register Lead | an agent (`[ORG]CELL-COSOER`) | none; requests are held, never closed |
| Capture Clerk | runs the surface adapters, builds each entry, takes its number, chains it, and reconciles the census | Chief of Staff | an agent (`[ORG]CELL-OERCC`) | none; capture waits, and every event is registered late |
| Classifier | places an ambiguous item in its class, with its reason; sends an item that looks legal or regulatory to the Records Officer position at once | Chief of Staff | an agent (`[ORG]CELL-OERC`) | none; the item is held unclassified and shown |
| Thread Linker | links each entry to its thread, Work Item, decision, release and source | Chief of Staff | an agent (`[ORG]CELL-OERTL`) | none; the entry stays unlinked and is counted |
| Follow-up Clerk | sets the due state of open entries from the process design or the surface's rule, and sends notices to the owning position | Chief of Staff | an agent (`[ORG]CELL-OERFC`) | none; the due state is not refreshed, and the Panel says so |
| Projection Builder | builds the inboxes and outboxes, the handover lists, the return briefs, the evidence packs and the case packs | Chief of Staff | an agent (`[ORG]CELL-OERPB`) | none; the projection shows its last rebuild time |
| Coverage Analyst | computes the coverage feedback and the activity projection, and raises gap signals | Chief of Staff | an agent (`[ORG]CELL-OERCA`) | none; the feedback is not refreshed, and says so |
| Integrity Checker | proves every day that the register is whole: numbers, census, rebuild, segment anchors | Operations Event Register Lead | an agent (`[ORG]CELL-OERIC`) | none; the check shows unknown, never pass |

- **Every human position is a HOAC position.** This AIOC starts with one, the Lead. The Records Officer, the position that holds data protection and the internal-audit line are HOAC positions elsewhere in the organisation, set in §15. No AI Cell ever holds one.
- **No natural person** (Standard §1.1, item 9). This blueprint deals with positions only.
- **The Integrity Checker reports to the Lead, not to the Chief of Staff,** so that the part that runs the register does not direct the part that checks it (**New** as a placement; HF-18).
- No AI Cell signs, approves or decides anything (Protocol §10, item 3). Each AI Cell's bot has its own identity card (§17).
- **No model at capture or wake** (Protocol §7). Capture, numbering, chaining and the projections are code steps run by their Cells. A model is used only by the Classifier, for an ambiguous item, within its budget.

---

## 4. Standard capabilities

Defaults are in `docs/STANDARD-CAPABILITIES.md` of `49GAION-aioc` at `1abae80`. The differences are listed in §11.

### 4.1 Office
#### Definition
Default · form: **single Chief of Staff**. An Office forms only when the Lead needs more than one Chief of Staff, for example one per entity under heavy load. It is proposed to the Lead, never self-created.
#### Process (SOP)
Default.
#### Role card
None while the form is a single Chief of Staff.
#### Fixed test
TEST-OER-COSOER v1 (TEST-OER v1, case 45) · result `NOT_RUN`

### 4.2 Chief of Staff
#### Definition
Default, **connecting** kind: it connects the organisation's positions with the register, and reports to its HOAC seat, the Lead. With these additions:
- **The door.** File requests, evidence pack requests, closures with their reasons and surface connection requests arrive through it. It answers by reference.
- **The orchestrator of the register.** It dispatches the Cells, runs their code steps, and writes the AIOC's own event record. Code is a tool, never a seat.
- **Acts, not activity.** It refuses every request that would make a figure, a list or a history about one human position's acts. It records each refusal to the position that holds data protection and to the internal-audit line (Protocol §22, item 7).
- **Its HOAC seat is a position** (Position Principle). It names the Lead by position code only.
#### Process (SOP)
Default, plus:
1. **Intake.** Every arrival goes first to the Input socket (§4.3) → *admitted event* (evidence: the event store).
2. **Dispatch.** Each admitted event goes to the Capture Clerk, and from there to classification, linking and follow-up → *entry* (evidence: the entry and its chain).
3. **File requests.** A position asks to keep an entry. The Chief of Staff files it into Source Lifecycle (§5.8) and returns the filing receipt → *correspondence filing* (evidence: the receipt and the equal hash).
4. **Evidence requests.** A position asks for an evidence pack within its scope. The Projection Builder builds it, and the Chief of Staff returns it → *evidence pack*.
5. **Surface connection.** It prepares a surface connection request for the Lead only when the scope, the HF-17 decision and the notices are recorded (Annex F) → *decision request* (evidence: the request record).
6. **Raise, never guess.** An event that cannot be cleared of a person field, an item outside the formal scope, or a finding of the Integrity Checker goes to the Lead in one line, with its evidence → *raised item*.
7. **Stops.** A stop takes effect at the tool gateway on every Pod and Cell of this AIOC; capture stops and nothing in flight is closed. After a signed `restart-stopped-unit`, capture resumes and every event of the stopped interval is registered late from its home → *nothing* (evidence: the unit register).
8. **Brief.** Each morning, and when called, it briefs the Lead: surfaces connected and waiting, late entries and lag, integrity findings, feeds waiting, and requests it refused → *brief*.
#### Role card
| Field | Content |
|---|---|
| Name | Chief of Staff |
| Position and seat | the position Chief of Staff; accountable seat: the Operations Event Register Lead (`[ORG]HOAC-ACS`) |
| Performed by | an agent (`[ORG]CELL-COSOER`, full name Operations Event Register Chief of Staff) |
| Purpose | keep the register running, whole and honest, and be the door through which positions reach it |
| Authority limits | **Alone:** dispatch, run code steps, file what a position asks to keep, return evidence packs within scope, refuse a request about one human position, send notices and briefs. **Needs the Lead:** any change to configuration; any act on a surface's grant; a budget above the cap; an item it raised. **Never:** decide, send or refuse an item on its merits; give an order; read a private message or a call; make a figure about one human position; name a person; close an entry by silence; hold a secret |
| Write location | the event record of this AIOC and its Work Items |
| Reports to | the Operations Event Register Lead |
| Escalation | to the Lead in one line, with evidence linked; while the Lead's position is vacant, to the Cell carrying `[ORG]HOAC-TM`; a stop goes to the stop door, never through this Cell |
| Tools and access | the code steps of the code project; the adapters, through the tool gateway, within their signed scopes; the unit register, read only (positions only, never who holds them); no credential in any instruction |
| Deputy and cover | none; on failure, requests are held and the Lead is told |
| Fixed test and score | TEST-OER-COSOER v1 (§9), plus the default Chief of Staff test (a) to (l) |
| Card version and status | v0.1.0 · draft |
#### Fixed test
TEST-OER-COSOER v1 · result `NOT_RUN`

### 4.3 Input socket
#### Definition
Default, with this AIOC's standard format, the **admitted event**, which holds:
- the surface and its signed grant;
- the object's home reference;
- the change of state and its time;
- the content's SHA-256, or a snapshot hash with its `as_of` time for a mutable object;
- the parties as unit or position codes, or as the ID of an outside party in the restricted partition;
- the capture mode.

**Converters, one per surface type** (Annex D). Each is a tested change; adding one changes no capability.

| Converter | Input | What it does |
|---|---|---|
| mail | an event of a functional mailbox | keep the message ID, direction, parties as codes, time and the hash of the raw message; keep the attachment manifest by hash; never the body |
| letter | a dispatch or arrival record | keep the signatory position, dispatch mode, tracking reference and where the original is kept |
| post | a publication on one of the organisation's own accounts | keep the post ID, URL, time, and the hash of its text and media at publication; schedule re-checks for edits and deletions |
| code host | a merge, a close with a decision, a release or a tag | keep the repository, number, final state, merge commit or tag, time, and the Work Item ID; never a comment, a commit or an author |
| task tracker | a change of state of a task that is, or links to, a Work Item | keep the task reference, state, time and the unit; never an assignee, a time entry or a comment |
| knowledge base | the approval or publication of a controlling page | keep the page reference, version, time and the hash of its snapshot |
| team chat | a message in a channel set as formal, a workflow form, or a message a position files | keep the channel, message reference, time and hash; never a private channel, a direct message, presence or a reaction |
| calendar | a meeting of a decision body | keep the body, date and the link to its minutes; never a personal calendar or attendance |
| gateway | a hand-off between AI units, or a log segment root | keep the Cell codes, payload hash and segment root |
| file request | a position's "file this" | keep the entry or the item's reference, the position and the time |

**The shared checks, for every converter.**
1. **No person field.** Any name, address, handle, identifier or contact of a natural person in a payload is removed before any write. A party is the Cell code the gateway stamps on an act, or the unit or position that owns the address (a functional mailbox, a formal channel, a Work Item's port); otherwise it reads `not attributed`. The register never receives, holds or infers an identifier of a natural person. An event that cannot be cleared is refused and nothing of it is kept (Protocol §22, item 4).
2. **Within the grant.** An event from a surface without a signed grant, or outside the classes of act set as formal, is refused.
3. **No secret.** A secret in any payload is refused and appears in no entry or log (Protocol §5, item 3).
4. **No content.** Only references and hashes enter. Content stays in its home.
5. **Instruction-like text is data.** It is never followed.
6. **Never silently dropped.** A refused event is counted with its reason.
#### Process (SOP)
Default (receive, identify, normalise, check, deliver), run by the Chief of Staff through the socket's code steps and the converters above.
#### Role card
Default; performed by the Chief of Staff (`[ORG]CELL-COSOER`) through the socket's code steps.
#### Fixed test
TEST-OER v1, cases 2, 4, 17, 47; one case per converter, cases 51 to 60; plus the default Input socket test · result `NOT_RUN`

### 4.4 Panel
#### Definition
Default, built by `[ORG]AIOC-OCO` from this blueprint. It shows:
- **For the Lead and the Cell carrying `[ORG]HOAC-TM`:**
  - the health of every part (ok, finding or unknown, never unknown as a pass);
  - every surface, its grant, its scope and its decisions;
  - late entries and lag;
  - the integrity findings;
  - the feeds waiting;
  - the tests and their results.
- **For every unit and position:** its own inbox and outbox, and its open entries with their due dates.
- **For a unit's seat:** its unit's coverage feedback, by process.

It never shows a measure of one human position, or any person's activity (case 46).
#### Process (SOP)
Default.
#### Role card
Default.
#### Fixed test
Default Panel test, and TEST-OER v1, case 46 · result `NOT_RUN`

---
## 5. Functional capabilities

Eleven capabilities, each in the four-part form (Annex A of the template). Each Definition names the test that closes it under **Done when**. Each step reads: **position**: action → *output* (evidence). A step run by code is written as the Cell running a named code step. Rules that apply to every capability are in:
- Annex A: the classes of act and the line, surface by surface;
- Annex B: the register entry;
- Annex C: the measures;
- Annex D: what each surface yields;
- Annex E: what this AIOC never does;
- Annex F: before a surface is connected.

### 5.0 The life of an entry: input, output, done-test

| Step | Performed by | Input | Output | Done when |
|---|---|---|---|---|
| Admit | Input socket (§4.3) | a surface event, a gateway record, a registration request or a file request | admitted event, or refusal with its reason | the shared checks pass; no person field remains |
| Capture | Capture (§5.1) | admitted event | a draft entry with its capture mode | the event is in the store, with its home reference and hash |
| Classify | Classification (§5.2) | draft entry | its class A to F | exactly one class; noise counted; private never kept |
| Number and chain | Numbering and Chain (§5.3) | classified entry | numbered, chained entry | its number from the numbering service; its hash chains to the one before |
| Link | Linking (§5.4) | entry | links to thread, Work Item, decision, release, source | every reference resolves, or is a finding |
| Follow | Follow-up (§5.5) | open entry | due state; notices | it ends with a closure reason, never by silence |
| Show | Inbox, Outbox and Projections (§5.6) | the events | inbox, outbox, handover list, return brief | a rebuild equals the projection |
| Feed back | Coverage Feedback (§5.7) | the events | M1 to M8 by unit and process | each figure traces to its events |
| File | Feeds to Source Lifecycle (§5.8) | a file request; the period's projection; an act with no source | correspondence filing, activity export, gap signal | Source Lifecycle's receipt, with an equal hash |
| Prove | Evidence and Case Packs (§5.9); Integrity (§5.10) | the events; the homes | evidence pack, case pack, integrity finding | verified by hash; the daily checks run |

### 5.1 Capture
#### Definition
| Field | Content |
|---|---|
| Name | Capture |
| What it is | One adapter per connected surface turns each change of state of a work object into an admitted event: a mail sent or received, a letter dispatched, a post published, a Work Item passed, a merge or release, a task's state changed, a controlling page approved, a formal channel's message, a decision body's meeting. The Capture Clerk builds the draft entry from it, by reference and hash. |
| Purpose | Have every formal act of the organisation in one register, on every surface, without copying its content. |
| Scope | does: run the adapters; take the capture mode (`gated`, `pushed`, `fetched`, `reconciled`); hash, or snapshot-hash with `as_of` for a mutable object; reconcile each surface with its census; register late what arrives late; does not: record a person's activity (a view, a read, presence, typing, a reaction); keep content; reach a surface outside its grant |
| Inputs | admitted events, from the Input socket |
| Outputs | draft entries; the census reading per surface |
| Limits | Annex A, Annex D; no model at capture (Protocol §7); every event within its surface's signed grant |
| Sources | Protocol §22, items 2 to 4 and 13; §14, items 1 and 5; Standard §3.1, item 13 |
| Status | draft |
| Done when | TEST-OER v1, cases 17, 18 and 19 pass |
#### Process (SOP)
| Field | Content |
|---|---|
| Trigger | an event pushed by a surface; a scheduled fetch where a surface does not push; a reconciliation run |
| Steps | 1. **Capture Clerk**: run the adapter's code step for the event → *admitted event* (event store). 2. **Capture Clerk**: build the draft entry: home reference, times, parties as codes, content hash or snapshot hash with `as_of`, capture mode → *draft entry*. 3. **Capture Clerk**: once a day, compare what each surface reports (its census, where it gives one) with what was registered; register late, from its home, each crossing that was missed → *census reading*, *late entries*. |
| States | received → admitted → drafted; or refused, with its reason |
| Failure and recovery | an adapter that falls silent is a finding (Protocol §22, item 13); a surface with no census reads `no census`, never an estimate |
| Records | the event store; the census readings |
| Cadence | on each event; reconciliation daily |
| Measures | events admitted and refused, by surface and reason; census difference per surface |
#### Role card
| Field | Content |
|---|---|
| Name | Capture Clerk |
| Position and seat | Capture Clerk; accountable seat: the Operations Event Register Lead |
| Performed by | an agent (`[ORG]CELL-OERCC`) |
| Purpose | turn every formal act on every connected surface into an entry, by reference and hash |
| Authority limits | alone: run the adapters and the numbering and chain steps, register late; never: keep content, record a person's activity, reach outside a grant, change a past entry |
| Write location | the register's event store |
| Reports to | the Chief of Staff |
| Escalation | through the Chief of Staff |
| Tools and access | the surface adapters through the tool gateway, read only, within their grants; the numbering service |
| Deputy and cover | none; capture waits, and every event is registered late from its home |
| Fixed test and score | TEST-OER-OERCC v1 |
| Card version and status | v0.1.0 · draft |
#### Fixed test
TEST-OER-OERCC v1 (TEST-OER v1, cases 3, 4, 17, 18, 19, 22) · result `NOT_RUN`

### 5.2 Classification
#### Definition
| Field | Content |
|---|---|
| Name | Classification |
| What it is | Each draft entry takes one class (Annex A): A, formal correspondence; B, a request between units or entities; C, machine traffic; D, a code-host event; E, noise; F, private. Most classes follow from the surface and the act by rule; the Classifier decides only an ambiguous item, with its reason. |
| Purpose | Keep what is formal, count what is noise, and never keep what is private. |
| Scope | does: place each item in one class; count noise per channel without keeping it; send an item that looks legal or regulatory to the Records Officer position at once; mark correspondence with counsel as by reference only, Strictly confidential; does not: read a private item; decide that an item is not legal; decide anything about the item's content |
| Inputs | draft entries |
| Outputs | classified entries; noise counts; items sent to the Records Officer |
| Limits | class F is never captured, and an item offered from it is refused and nothing of it kept; no model call on correspondence with counsel; a model is called only for an ambiguous item, within the budget, on an engine cleared for the item's confidentiality level (Standard §4.4, item 11) |
| Sources | Protocol §22, items 2 and 14; Standard §3.1, item 13 |
| Status | draft |
| Done when | TEST-OER v1, cases 2, 20, 21 and 39 pass |
#### Process (SOP)
| Field | Content |
|---|---|
| Trigger | a draft entry |
| Steps | 1. **Capture Clerk**: apply the class rules of Annex A by code → *class by rule*, or *ambiguous*. 2. **Classifier**: for an ambiguous item, place it in one class, with its reason → *class with reason*. 3. **Classifier**: if the item looks legal or regulatory, send it to the Records Officer position through its HU port at once → *referral*. |
| States | drafted → classified (A to D) / counted (E) / refused (F) |
| Failure and recovery | an item the Classifier cannot place is held unclassified and shown to the Lead, never guessed |
| Records | the class and its reason on the entry; noise counts per channel and day |
| Cadence | on each entry |
| Measures | ambiguous items; referrals to the Records Officer; noise per channel |
#### Role card
| Field | Content |
|---|---|
| Name | Classifier |
| Position and seat | Classifier; accountable seat: the Operations Event Register Lead |
| Performed by | an agent (`[ORG]CELL-OERC`) |
| Purpose | place an ambiguous item in its class, with its reason |
| Authority limits | alone: classify an ambiguous item; refer an item that looks legal; never: classify an item as not legal, read a private item, call a model on correspondence with counsel |
| Write location | the class and reason fields of the entry |
| Reports to | the Chief of Staff |
| Escalation | through the Chief of Staff; a legal-looking item straight to the Records Officer position |
| Tools and access | the draft entry and its metadata; model routes through the shared AI gateway |
| Deputy and cover | none; the item is held unclassified and shown |
| Fixed test and score | TEST-OER-OERC v1 |
| Card version and status | v0.1.0 · draft |
#### Fixed test
TEST-OER-OERC v1 (TEST-OER v1, cases 2, 20, 21, 39) · result `NOT_RUN`

### 5.3 Numbering and Chain
#### Definition
| Field | Content |
|---|---|
| Name | Numbering and Chain |
| What it is | Each classified entry takes its readable number from the organisation's one numbering service (Protocol §14, item 4), in a stream per entity and direction: `<entity>-<IN\|OUT\|INT>-<yyyy>-<seq>`. Its `event_id` is also its idempotency key. Its `entry_hash` covers its fields and the `prev_hash` of the entry before it. |
| Purpose | Give every crossing one number that never repeats or skips, and make the register tamper-evident. |
| Scope | does: take numbers; take a leased block for use when the service is unreachable; chain; mark `late` with its lag; record a correction as a new event; does not: mint its own number; change or delete a past entry |
| Inputs | classified entries; a registration request from the gateway (register first) |
| Outputs | numbered, chained entries |
| Limits | for register first, the number is issued before the gateway releases the item; the register never holds an item back, and an entry incomplete in form is completed later and flagged `late` (Protocol §22, item 5) |
| Sources | Protocol §14, items 1, 4 and 5; §22, items 3, 5 and 6 |
| Status | draft |
| Done when | TEST-OER v1, cases 3 and 22 pass |
#### Process (SOP)
| Field | Content |
|---|---|
| Trigger | a classified entry; a registration request |
| Steps | 1. **Capture Clerk**: take the next number of the stream from the numbering service, or from the leased block when the service is unreachable → *number*. 2. **Capture Clerk**: compute `entry_hash` over the fields and `prev_hash`; write the entry → *entry* (event store). 3. **Capture Clerk**: for an event that occurred before it was registered, set `late` and its `lag` → *late flag*. |
| States | classified → numbered → chained |
| Failure and recovery | a duplicate `event_id` returns the existing entry; a write on a stale revision becomes a question to its author (Protocol §14, item 1) |
| Records | the event store |
| Cadence | on each entry |
| Measures | share registered late; median lag (M6) |
#### Role card
Performed by the Capture Clerk (`[ORG]CELL-OERCC`, §5.1), as code steps.
#### Fixed test
TEST-OER-OERCC v1 (TEST-OER v1, cases 3, 22) · result `NOT_RUN`

### 5.4 Linking
#### Definition
| Field | Content |
|---|---|
| Name | Linking |
| What it is | Each entry is linked to what it belongs to: its thread (`in_reply_to`, `answers`), the Work Item it carries or answers, the decision or signature it rests on, the release it belongs to, and the sources it cites, by version. |
| Purpose | Make every act traceable to why it happened and what it answered. |
| Scope | does: link by reference; mark an entry whose reference does not resolve as a finding; mark an act that cited a source later superseded, on a notice from Source Lifecycle; does not: open, edit or close a Work Item or a source |
| Inputs | entries; notices from Source Lifecycle |
| Outputs | links on the entry; findings |
| Limits | links are references only; a missing link is shown, never invented |
| Sources | Protocol §8; §22, item 3; §13, item 9 (notices) |
| Status | draft |
| Done when | TEST-OER v1, case 23 passes |
#### Process (SOP)
| Field | Content |
|---|---|
| Trigger | a new entry; a notice from Source Lifecycle |
| Steps | 1. **Thread Linker**: resolve the entry's references (thread, Work Item, decision, signature, release, source) → *links*. 2. **Thread Linker**: an unresolvable reference is a finding on the entry → *finding*. 3. **Thread Linker**: on a notice of supersession, mark the entries that cited the superseded version after it was superseded → *marked entries*. |
| States | unlinked → linked / linked with findings |
| Failure and recovery | a reference that cannot be checked is left unlinked and counted, never guessed |
| Records | the links and findings on the entry |
| Cadence | on each entry and each notice |
| Measures | M2 (linked / orphans) |
#### Role card
| Field | Content |
|---|---|
| Name | Thread Linker |
| Position and seat | Thread Linker; accountable seat: the Operations Event Register Lead |
| Performed by | an agent (`[ORG]CELL-OERTL`) |
| Purpose | link every entry to its thread and to what it rests on |
| Authority limits | alone: link and mark; never: change a Work Item, a decision or a source |
| Write location | the link fields of the entry |
| Reports to | the Chief of Staff |
| Escalation | through the Chief of Staff |
| Tools and access | the register, the shared queue and Source Lifecycle's references, read only |
| Deputy and cover | none; the entry stays unlinked and is counted |
| Fixed test and score | TEST-OER-OERTL v1 |
| Card version and status | v0.1.0 · draft |
#### Fixed test
TEST-OER-OERTL v1 (TEST-OER v1, case 23) · result `NOT_RUN`

### 5.5 Follow-up
#### Definition
| Field | Content |
|---|---|
| Name | Follow-up |
| What it is | An entry that asks for an answer, such as an incoming letter or a request, is open until it ends. Its due date comes from the process design or from the rule the organisation set for the surface. The Follow-up Clerk keeps its state as events: open, acknowledged, answered, overdue, closed or voided, each closure with its reason. |
| Purpose | So that nothing the organisation owes is forgotten, and an overdue reply is seen at its deadline, not when the other party chases. |
| Scope | does: set the due state; send a notice to the owning position before and at the due date; show overdue entries to the watchdog; does not: chase, give an order, escalate in its own name, or close an entry |
| Inputs | open entries; the due rules |
| Outputs | due states; notices to the owning position |
| Limits | nothing closes by silence; a closure comes only from the owning position, or from the answer's own entry, with a reason from the closed list; the watchdog chases (Protocol §4.6, item 5) |
| Sources | Protocol §22, item 9; §4.6, item 5 |
| Status | draft |
| Done when | TEST-OER v1, cases 9, 24 and 25 pass |
#### Process (SOP)
| Field | Content |
|---|---|
| Trigger | an open entry; the due rule's time |
| Steps | 1. **Follow-up Clerk**: set the due date from the rule → *due state*. 2. **Follow-up Clerk**: send the owning position a notice before and at the due date, through its HU port → *notice*. 3. **Follow-up Clerk**: on the answer's entry, or on the position's closure with its reason, end it → *closed*. |
| States | open → acknowledged → answered / overdue → closed (answered, no answer needed, superseded, withdrawn by the sender) / voided (registered in error, with its reason) |
| Failure and recovery | an entry with no due rule is shown as `no rule`, never given one |
| Records | the state events of each entry |
| Cadence | on each entry; due checks hourly |
| Measures | M4 (answered on time / overdue, median age); M7 (closed by silence) |
#### Role card
| Field | Content |
|---|---|
| Name | Follow-up Clerk |
| Position and seat | Follow-up Clerk; accountable seat: the Operations Event Register Lead |
| Performed by | an agent (`[ORG]CELL-OERFC`) |
| Purpose | keep the due state of every open entry, and tell its owning position |
| Authority limits | alone: set the due state, send notices; never: give an order, close an entry, chase in its own name |
| Write location | the state events of the entry |
| Reports to | the Chief of Staff |
| Escalation | through the Chief of Staff; overdue entries are shown to the watchdog |
| Tools and access | the register; the due rules; the positions' HU ports, through the tool gateway |
| Deputy and cover | none; the due state is not refreshed, and the Panel says so |
| Fixed test and score | TEST-OER-OERFC v1 |
| Card version and status | v0.1.0 · draft |
#### Fixed test
TEST-OER-OERFC v1 (TEST-OER v1, cases 9, 24, 25) · result `NOT_RUN`

### 5.6 Inbox, Outbox and Projections
#### Definition
| Field | Content |
|---|---|
| Name | Inbox, Outbox and Projections |
| What it is | Every unit and position has an inbox and an outbox: Panel views of the entries at its ports, with what is open and what is due. Two further projections are built from the same events. The handover list holds a position's open entries and commitments, built on request of that position or of the HOAC above it. The return brief holds what arrived for a position while it was away, and what is due. Both are built only on request, and the register never knows who occupies a position. |
| Purpose | Let every part see its own traffic, and let a position be taken over without losing anything. |
| Scope | does: build each projection from the events, with the version of the logic that built it; show each position only its own open items; does not: show a measure of a human position; show anyone's activity; hold a copy (Protocol §14, item 2) |
| Inputs | the events |
| Outputs | inbox and outbox per unit and position; handover lists; return briefs |
| Limits | an address is an entity, a unit or a position, never a natural person; a personal mailbox's item appears only when its position filed it |
| Sources | Protocol §22, item 8; §14, item 2; §4.10, item 17 (handover) |
| Status | draft |
| Done when | TEST-OER v1, cases 8, 26 and 27 pass |
#### Process (SOP)
| Field | Content |
|---|---|
| Trigger | a new event; a request from the Panel; a request for a position's handover list, from that position or from the Cell carrying `[ORG]HOAC-TM`; a position's request for its return brief |
| Steps | 1. **Projection Builder**: rebuild the affected projections → *projection* (with its logic version). 2. **Projection Builder**: on request, build the position's handover list: its open entries and commitments. It reads nothing about who holds a position (Protocol §22, item 12) → *handover list*. 3. **Projection Builder**: when a position asks, build its return brief → *return brief*. |
| States | current / rebuilding |
| Failure and recovery | a projection that fails its rebuild check shows its last good rebuild time and is a finding (§5.10) |
| Records | none of their own; projections are rebuilt |
| Cadence | on each event |
| Measures | rebuild differences (should be zero) |
#### Role card
| Field | Content |
|---|---|
| Name | Projection Builder |
| Position and seat | Projection Builder; accountable seat: the Operations Event Register Lead |
| Performed by | an agent (`[ORG]CELL-OERPB`) |
| Purpose | build every view and pack from the events, and nothing that is not in them |
| Authority limits | alone: build projections and packs within the asking position's scope; never: build a figure, list or history about one human position's acts |
| Write location | the projections (rebuilt, never a source) |
| Reports to | the Chief of Staff |
| Escalation | through the Chief of Staff |
| Tools and access | the register, read only |
| Deputy and cover | none; the projection shows its last rebuild time |
| Fixed test and score | TEST-OER-OERPB v1 |
| Card version and status | v0.1.0 · draft |
#### Fixed test
TEST-OER-OERPB v1 (TEST-OER v1, cases 8, 12, 26, 27, 33, 34) · result `NOT_RUN`

### 5.7 Coverage Feedback
#### Definition
| Field | Content |
|---|---|
| Name | Coverage Feedback |
| What it is | For each entity, unit, process and AI Cell, and each period, the Coverage Analyst computes the measures M1 to M8 (Annex C): what it had and what it lacked. |
| Purpose | Tell each part, honestly and without blame, what the system gave it and what it failed to give it, so that the gaps can be closed. |
| Scope | does: compute M1 to M8 from the events; show each against an absolute bar the organisation set; roll up to the parent unit any figure, for a unit, a process or a role-type, drawn from the acts of fewer human positions than the minimum group size; give the projection of the work by role-type and process for the design stages (§5.8); does not: rank or compare; give a figure for one human position; give a figure to appraisal, pay, discipline or promotion; add a measure not on the fixed list of Annex C |
| Inputs | the events |
| Outputs | coverage feedback; the activity projection |
| Limits | diagnostic only (Standard §2.4, item 7); every figure carries its logic version and traces to its events (Protocol §14, items 2 and 5) |
| Sources | Protocol §22, items 7 and 10; Standard §3.1, item 13 |
| Status | draft |
| Done when | TEST-OER v1, cases 7, 10, 28 and 29 pass |
#### Process (SOP)
| Field | Content |
|---|---|
| Trigger | the end of a period; a request from a unit's seat or the Cell carrying `[ORG]HOAC-TM` |
| Steps | 1. **Coverage Analyst**: compute M1 to M8 per entity, unit, process and AI Cell → *feedback* (with logic version). 2. **Coverage Analyst**: apply the minimum group size; roll up what falls below it → *rolled-up figures*. 3. **Coverage Analyst**: build the period's projection of the work by role-type and process → *activity projection*. |
| States | computed → shown |
| Failure and recovery | a measure with no census or no rule reads `no census` or `no rule`, never an estimate |
| Records | each figure with its logic version and its trace |
| Cadence | weekly and monthly; on request |
| Measures | — |
#### Role card
| Field | Content |
|---|---|
| Name | Coverage Analyst |
| Position and seat | Coverage Analyst; accountable seat: the Operations Event Register Lead |
| Performed by | an agent (`[ORG]CELL-OERCA`) |
| Purpose | compute what each part had and what it lacked, and the projection of the work |
| Authority limits | alone: compute M1 to M8 and the projection; raise gap signals; never: rank, compare, or compute a figure for one human position |
| Write location | the feedback projections |
| Reports to | the Chief of Staff |
| Escalation | through the Chief of Staff |
| Tools and access | the register, read only |
| Deputy and cover | none; the feedback is not refreshed, and says so |
| Fixed test and score | TEST-OER-OERCA v1 |
| Card version and status | v0.1.0 · draft |
#### Fixed test
TEST-OER-OERCA v1 (TEST-OER v1, cases 7, 10, 28, 29, 31, 32) · result `NOT_RUN`

### 5.8 Feeds to Source Lifecycle
#### Definition
| Field | Content |
|---|---|
| Name | Feeds to Source Lifecycle |
| What it is | Three things go from the register into Source Lifecycle, through its Input socket, under this AIOC's write scope (origin kinds `correspondence` and `export`). The first is **correspondence**: an entry a position asks to keep, filed as a source of origin kind `correspondence`, class EVIDENCE, fixed as received, with the entry's content hash, on behalf of that position. The second is the **activity export**: the period's projection of the work by role-type and process, with its `as_of` date, filed as an `export` only after the HF-17 decision on it is recorded. The third is **gap signals**: one signal per act done without a source, by reference to the entry. |
| Purpose | Let Source Lifecycle keep what the organisation did beside what it knows, and give the design stages the activity profile they wait for. |
| Scope | does: file, export and signal by reference; does not: file anything a position did not ask to keep; export anything that says who did the work; send content in a gap signal |
| Inputs | file requests; the activity projection; acts with no source |
| Outputs | correspondence filings; activity exports; gap signals; Source Lifecycle's receipts |
| Limits | an export with any person field is refused at this socket and at Source Lifecycle's; correspondence is never served as the organisation's own statement |
| Sources | Protocol §22, item 11; §13, items 11 and 12; Standard §3.1, items 13 and 14 |
| Status | draft |
| Done when | TEST-OER v1, cases 11, 30, 31 and 32 pass |
#### Process (SOP)
| Field | Content |
|---|---|
| Trigger | a file request; the end of a period; an act with no source |
| Steps | 1. **Chief of Staff**: file the entry asked for as `correspondence`, on behalf of the asking position → *filing* and Source Lifecycle's *receipt* (equal hash). 2. **Coverage Analyst**: when the HF-17 decision on the period's export is recorded, file the projection as an `export` → *export* and *receipt*. 3. **Coverage Analyst**: for each act with no source, send a gap signal → *gap signal*. |
| States | asked → filed / refused; projection ready → waiting for HF-17 → filed |
| Failure and recovery | with Source Lifecycle absent or stopped, feeds wait and are shown as waiting; nothing is lost |
| Records | the filing, export and signal events, with Source Lifecycle's receipts |
| Cadence | on request; per period |
| Measures | feeds waiting; M5 (done with a source) |
#### Role card
Performed by the Chief of Staff (`[ORG]CELL-COSOER`, §4.2) for filings, and by the Coverage Analyst (`[ORG]CELL-OERCA`, §5.7) for exports and gap signals.
#### Fixed test
TEST-OER-COSOER v1 and TEST-OER-OERCA v1 (TEST-OER v1, cases 11, 30, 31, 32) · result `NOT_RUN`

### 5.9 Evidence and Case Packs
#### Definition
| Field | Content |
|---|---|
| Name | Evidence and Case Packs |
| What it is | An **evidence pack** answers a question such as "what did we send them, and when?" or "show the record of this matter". It holds the entries, their homes and their hashes, and each content hash is verified by re-hashing the home where it is readable. A **case pack** holds pseudonymised past cases of one process, replayable. Cases for shadow runs, a shadow test of an AI filler, or the evidence for a decision to move work toward AI go to Self-Improvement once its access includes the register. Cases for a golden set go only to the human seat that chooses it and to the assurance unit, never to the loop (Standard §2.3, items 4, 7 and 9; §2.4, item 4). |
| Purpose | Prove what happened, quickly; and let the organisation test and improve its work on real cases. |
| Scope | does: build packs within the asking position's scope; report a mismatch as a finding; does not: repair a home; build a pack about one human position's acts; build a case pack without a Work Item of the Cell carrying `[ORG]HOAC-TM` |
| Inputs | evidence requests; case-pack Work Items |
| Outputs | evidence packs; case packs |
| Limits | a case pack holds no person's particulars, and is used only under its Work Item (Standard §2.3, item 4; `move-work-toward-ai` stays a human decision) |
| Sources | Protocol §22, item 12; Standard §2.1, item 7; §2.3, item 4 |
| Status | draft |
| Done when | TEST-OER v1, cases 12, 33 and 34 pass |
#### Process (SOP)
| Field | Content |
|---|---|
| Trigger | an evidence request; a case-pack Work Item |
| Steps | 1. **Projection Builder**: select the entries within scope → *selection*. 2. **Projection Builder**: re-hash each readable home and compare → *verified pack*, or *finding*. 3. **Chief of Staff**: return the pack to the asking position → *evidence pack* or *case pack*. |
| States | asked → built → returned |
| Failure and recovery | an unreadable home is listed as unverified, never as verified |
| Records | the pack's manifest and its verification |
| Cadence | on request |
| Measures | packs built; mismatches found |
#### Role card
Performed by the Projection Builder (`[ORG]CELL-OERPB`, §5.6), returned by the Chief of Staff.
#### Fixed test
TEST-OER-OERPB v1 (TEST-OER v1, cases 12, 33, 34) · result `NOT_RUN`

### 5.10 Integrity
#### Definition
| Field | Content |
|---|---|
| Name | Integrity |
| What it is | Every day the Integrity Checker proves that the register is whole. No number stream has a gap or a duplicate, and the hash chain verifies. Each surface's census matches what was registered, or the difference is listed. Every projection equals a rebuild from the events. Every gateway log segment has its root hash anchored in the register. |
| Purpose | Make the register trustworthy as evidence, for the organisation and for its internal-audit line. |
| Scope | does: run the daily checks; open a finding for each failure; report to the Lead and to the internal-audit line; does not: repair the register, change a past entry, block work |
| Inputs | the register; the census readings; the gateway log's segment roots |
| Outputs | integrity findings |
| Limits | a finding flags, never blocks (Protocol §14, item 5); no Cell of this AIOC can change or delete a past entry; the internal-audit line reads the register directly, read only; Self-Improvement reads it once `[ORG]HOAC-TM` adds it to the process's access, never its entries of the accountability path (Standard §2.1, items 7 and 8) |
| Sources | Protocol §14, item 5; §22, item 13; Standard §2.1, item 7; HF-18, HF-19 |
| Status | draft |
| Done when | TEST-OER v1, cases 13, 35 and 36 pass |
#### Process (SOP)
| Field | Content |
|---|---|
| Trigger | the daily run |
| Steps | 1. **Integrity Checker**: check each number stream and the chain → *result*. 2. **Integrity Checker**: compare each census → *result*. 3. **Integrity Checker**: rebuild each projection and compare → *result*. 4. **Integrity Checker**: check each gateway log segment's anchor → *result*. 5. **Integrity Checker**: report each failure to the Lead and to the internal-audit line → *integrity finding*. |
| States | ok / finding / unknown (never shown as ok) |
| Failure and recovery | a check that cannot run reads unknown, and is a finding |
| Records | the daily results, in the register |
| Cadence | daily |
| Measures | findings open; days since the last clean run |
#### Role card
| Field | Content |
|---|---|
| Name | Integrity Checker |
| Position and seat | Integrity Checker; accountable seat: the Operations Event Register Lead |
| Performed by | an agent (`[ORG]CELL-OERIC`) |
| Purpose | prove every day that the register is whole |
| Authority limits | alone: run the checks and report; never: repair, change or delete an entry, or block work |
| Write location | the daily results |
| Reports to | the Operations Event Register Lead, not the Chief of Staff |
| Escalation | to the Lead; a finding is also sent to the internal-audit line |
| Tools and access | the register, the census readings and the gateway's segment roots, read only |
| Deputy and cover | none; the check shows unknown, never pass |
| Fixed test and score | TEST-OER-OERIC v1 |
| Card version and status | v0.1.0 · draft |
#### Fixed test
TEST-OER-OERIC v1 (TEST-OER v1, cases 3, 13, 19, 22, 35, 36) · result `NOT_RUN`

### 5.11 Surface Connection
#### Definition
| Field | Content |
|---|---|
| Name | Surface Connection |
| What it is | A surface, an entity or a class of act is added only through the sequence of Annex F: scope, impact assessment and lawful basis, labour-law steps, notices, the arrangement between entities, the signed port, and an observed-only pilot with its negative tests. |
| Purpose | Connect as much of the live operation as the organisation decides, each step lawful and decided by the human position that holds it. |
| Scope | does: prepare each request; check that each prior decision is recorded; run the pilot and its negative tests; record the connection; does not: take any of the decisions; connect a surface whose decisions are not recorded |
| Inputs | surface connection requests |
| Outputs | a decision request to the Lead; a connected surface; a pilot report |
| Limits | the Lead signs `connect-external-port`, and a wider scope is `grant-or-widen-access`; revocation by the Lead or any position above it takes effect at the gateway first and is never held; every surface has its own token, held only in the platform's secret store or behind the gateway |
| Sources | Protocol §22, item 14; §13, item 5 (the same connection rules); Standard §4.4, item 7 |
| Status | draft |
| Done when | TEST-OER v1, cases 14, 37, 38 and 40 pass |
#### Process (SOP)
| Field | Content |
|---|---|
| Trigger | a surface connection request |
| Steps | 1. **Chief of Staff**: check that every prior decision of Annex F is recorded, or return the request naming what is missing → *checked request*. 2. **Operations Event Register Lead**: sign or refuse at the tool gateway → *signed port* (unit register event). 3. **Chief of Staff**: run the observed-only pilot and its negative tests → *pilot report*. 4. **Lead**: switch the surface to running, or revoke → *event*. |
| States | requested → waiting for decisions → signed → pilot → running / revoked |
| Failure and recovery | a negative test that fails stops the pilot and goes to the Lead |
| Records | the unit register (connections, scope changes, revocations); the pilot report |
| Cadence | on request |
| Measures | surfaces connected; surfaces waiting for decisions |
#### Role card
Performed by the Chief of Staff (`[ORG]CELL-COSOER`, §4.2); the signature is the Lead's.
#### Fixed test
TEST-OER-OERL v1 and TEST-OER-COSOER v1 (TEST-OER v1, cases 14, 37, 38, 40) · result `NOT_RUN`

---

## 6. Coordination and routes

- **With every unit of the `[ORG]AION`.** Its inbox and outbox are views of its ports. Where the register is installed, a port that carries formal acts in scope names it in its `audit_trail` (Protocol §22, item 8). Units do nothing extra for the register: the formal acts in scope that they send and receive through the gateway and the connected surfaces are recorded, and a human position's other passages through its HU ports are not.
- **With Source Lifecycle.** Through the 49GAION Operating Protocol only, within the scope Source Lifecycle grants this AIOC: it writes origin kinds `correspondence` and `export`, and reads references only of the sources its entries cite (Protocol §13, item 12). Gap signals go through its Input socket (§5.8). Notices from Source Lifecycle come back by reference, for every version an entry cites.
- **With the tool gateway.** Read only, for hand-offs and segment roots. For register first, the gateway asks the numbering service for a number before it releases a formal outgoing item, and the register records that event. The register never gates.
- **With the watchdog.** It shows the watchdog what is due and overdue; the watchdog chases.
- **With `[ORG]AIOC-OCO`.** Install, fixes, upgrades, the Panel, and every blueprint change, as `design-proposal` Work Items (template §6).
- **Routing rows this AIOC contributes:** `file request → [ORG]AIOC-OER`; `evidence pack request → [ORG]AIOC-OER`; `surface connection request → [ORG]AIOC-OER`; `correspondence filing, activity export, gap signal → [ORG]AIOC-SL`.
- **Requests and objections.** Every proposal, correction or critique is a `design-proposal` Work Item to OCO. Where they disagree, the Lead may hold the objection open until it reaches the position accountable for OCO, which decides.

## 7. Records and where things live

| Record | Home | Source rule |
|---|---|---|
| This blueprint, its decisions, its tests and its cards | the instance's writing repository `<org>aioc-oer`; the mother in `github.com/49g-holding/49GAION-operations-event-register` | one home for each thing |
| The adapters, the store and the projections (code) | the code project `<org>aioc-oer` | one home |
| The register: entries, state events, census readings, daily results | the runtime's own append-only store, in each entity's universe; never in a repository, and never in the 49GAION Library | one home per entity |
| The content of what is recorded | its own home: the mail system, the dispatch record, the platform, the code host, the task tracker, the knowledge base, the team chat, the shared queue, the gateway log | never copied into the register |
| Outside parties' particulars | the restricted partition, by ID, under keyed hashes (Protocol §14, item 6) | never in an entry, a projection or a search index |
| Correspondence a position asked to keep | Source Lifecycle, as a source of origin kind `correspondence` | one home |
| Connections, scope changes and revocations | the unit register, append-only | one home |
| The link between positions and the natural persons who hold them | not in this AIOC: the organisation's own mechanism, outside the system (Standard §1.1, item 9) | never here |
| Secrets | the organisation's vault only | never written |

## 8. Tools and the shared AI gateway

Surfaces are named by role. Their product names appear only in an organisation's own copy (Protocol §10, item 5).

| Tool | Existing shared tool, or new | If new: asked of the builder as |
|---|---|---|
| The register's append-only store, with its hash chain | new | an append-only event store per entity, with `prev_hash` and `entry_hash` |
| The numbering service | existing (Protocol §14, item 4) | streams per entity and direction; leased blocks |
| Surface adapters | new, one per surface type (Annex D) | push where the surface pushes; fetch by reference and hash where it only signals |
| The restricted partition and its keyed hashes | existing (Protocol §14, item 6) | — |
| Register first at the gateway | new, a gateway policy | under `change-gateway-policy` |
| Model routes (Classifier only) | through the shared AI gateway | — |

All model calls go through the shared AI gateway in the `[ORG]AION` (Standard §4.4, item 11). This AIOC's AI use and cost are metered separately; its budget cap is set in §15.

| Tool role | Connector | Access managed in | Part card version |
|---|---|---|---|
| mail system (functional mailboxes) | surface adapter | Panel (grant signed at the gateway) | v1 |
| letters | surface adapter | Panel (grant signed at the gateway) | v1 |
| the organisation's own social accounts | surface adapter, one per platform | Panel (grant signed at the gateway) | v1 |
| code hosts | surface adapter, one per host | Panel (grant signed at the gateway) | v1 |
| task tracker | surface adapter | Panel (grant signed at the gateway) | v1 |
| knowledge base | surface adapter | Panel (grant signed at the gateway) | v1 |
| team chat (formal channels only) | surface adapter | Panel (grant signed at the gateway) | v1 |
| calendars of decision bodies | surface adapter | Panel (grant signed at the gateway) | v1 |

**Mechanism register.** Nothing is built yet. A row is never deleted.

| ID | Mechanism | What it does | Where it lives | Today | Target |
|---|---|---|---|---|---|
| M-01 | Append-only store with hash chain | holds the entries | code project | decided, not built | build |
| M-02 | Numbering streams and leased blocks | one number per crossing | the shared numbering service | decided, not built | build |
| M-03 | Surface adapters | capture by reference and hash | code project | decided, not built | build, one surface at a time (Annex F) |
| M-04 | Person-field removal at the Input socket | no person's particulars in any entry | code project | decided, not built | build before the first surface |
| M-05 | Register first at the gateway | a number before release | the tool gateway | decided, not built | build after the first pilot |
| M-06 | Projections: inbox, outbox, handover list, return brief | views per unit and position | code project | decided, not built | build |
| M-07 | Coverage feedback M1 to M8 | what each part had and lacked | code project | decided, not built | build |
| M-08 | Feeds to Source Lifecycle | correspondence, export, gap signal | code project | decided, not built | build after Source Lifecycle adopts the origin kind |
| M-09 | Daily integrity checks | gaps, census, rebuild, anchors | code project | decided, not built | build with M-01 |

**Reserve.**

| ID | Idea | Why held | Reconsider when |
|---|---|---|---|
| R-01 | Record the content of AI payloads, not only their hashes | the gateway log holds only payload hashes (Standard §4.4, item 11); keeping payloads would change that text and is `change-gateway-policy` | the governing seat of 49GAION changes §4.4, item 11 |
| R-02 | Record more of human work than formal acts | it would watch work, which DR-0023 forbids, and needs a new DR, a new impact assessment and consultation | the governing seat of 49GAION decides a new DR |
| R-03 | Analysis of who talks to whom among human positions | a picture of persons, never of the work | never, unless the governing seat of 49GAION decides otherwise |

## 9. Fixed tests: index, triggers and scores

The cases are written in `tests/TEST-OER.md`:
- Cases 1 to 16 are the Library's TEST-OPERATIONS-EVENT-REGISTER v1, cases 1 to 16, unchanged.
- Cases 17 to 40 test the capabilities.
- Cases 41 to 50 test this AIOC's form.
- Cases 51 to 60 test the converters of the Input socket, one each.

| Capability | Test ID and version | Evidence level | Last run | Result |
|---|---|---|---|---|
| Office | TEST-OER-COSOER v1 (case 45) | MEASURED | — | `NOT_RUN` |
| Chief of Staff | TEST-OER-COSOER v1 | MEASURED | — | `NOT_RUN` |
| Input socket | TEST-OER v1, cases 2, 4, 17, 47, 51 to 60 | MEASURED | — | `NOT_RUN` |
| Panel | default; TEST-OER v1, case 46 | MEASURED | — | `NOT_RUN` |
| Capture | TEST-OER-OERCC v1 | MEASURED | — | `NOT_RUN` |
| Classification | TEST-OER-OERC v1 | MEASURED | — | `NOT_RUN` |
| Numbering and Chain | TEST-OER-OERCC v1 (cases 3, 22) | MEASURED | — | `NOT_RUN` |
| Linking | TEST-OER-OERTL v1 | MEASURED | — | `NOT_RUN` |
| Follow-up | TEST-OER-OERFC v1 | MEASURED | — | `NOT_RUN` |
| Inbox, Outbox and Projections | TEST-OER-OERPB v1 | MEASURED | — | `NOT_RUN` |
| Coverage Feedback | TEST-OER-OERCA v1 | MEASURED | — | `NOT_RUN` |
| Feeds to Source Lifecycle | TEST-OER v1, cases 11, 30, 31, 32 | MEASURED | — | `NOT_RUN` |
| Evidence and Case Packs | TEST-OER-OERPB v1 (cases 12, 33, 34) | MEASURED | — | `NOT_RUN` |
| Integrity | TEST-OER-OERIC v1 | MEASURED | — | `NOT_RUN` |
| Surface Connection | TEST-OER-OERL v1; TEST-OER v1, cases 14, 37, 38, 40 | MEASURED | — | `NOT_RUN` |
| Type (Foundational) | TEST-OER v1, case 8 | MEASURED | — | `NOT_RUN` |

- **Re-run triggers:** any change to a model, instructions, this AIOC's card, this blueprint, an adapter, the measures or the 49GAION Operating Protocol re-runs the affected tests; also any change to tools or access, a converter, the formal scope or a shared panel part.
- **The Library's cases.** Cases 1 to 16 are the Library's TEST-OPERATIONS-EVENT-REGISTER v1, unchanged; a Library case with no case here fails the joining test (template §9).
- **Complete** only when every capability's test has a visible result. `NOT_RUN` is never PASS.

**Checks that are not fixed tests.**

| Check | Placement | Budget per item | Degradation order | Blocks only for |
|---|---|---|---|---|
| Daily integrity checks (§5.10) | after completion | one run per day | none; a failure opens a finding | nothing; it flags |
| Person-field check on every event | in the Input socket | each event | none | the event |
| Single-human-position query check: no request returns a figure, list or history of one human position's acts | router | each request | none | the request |
| Secret scan of entries and logs | after completion | each batch | none | the batch |
| No-content check: no entry field holds content beyond references and hashes | after completion | daily | none; a failure opens a finding | nothing; it flags |

- **Discriminating evidence.** A passing check counts only if it has been shown able to fail on the case it guards, and evidence is written by the runner, never by the worker.

## 10. Build: what is generated from this file

| Built thing | Generated from | Recorded where |
|---|---|---|
| Panel profile | §0, §1, §3, §4.4, §5 role cards | the panel profile and the Panel's release record name this file's commit |
| Back office | §4.2 role card and SOP (instruction); §4 to §5 definitions and SOPs (knowledge) | the back office records the commit it was built from |
| Card in the protocol AIOC's map | §1 | the protocol AIOC's register links this file |
| Cards of the Pods and Cells, and the bot identity cards | §17 | `cards/`, by `tools/make_cards.py` |
| Panel Health section | §9 results; stuck, returned and late Work Items; the integrity findings | the Panel |

**Delivery path:** definition change → tests → Panel and Back office update → one-click rollback to the previous commit.

## 11. Exceptions

1. **The Integrity Checker reports to the Lead,** not to the Chief of Staff (§3), so that the part that runs the register does not direct the part that checks it.
2. **The Panel shows every unit its own inbox and outbox,** a view the template does not list. Its rules are those of the Panel; a human position sees only its own open items (§4.4).
3. **Human positions elsewhere in the organisation hold roles of this AIOC:** the Records Officer, the position that holds data protection and the internal-audit line (§2.1, §15). They are not Cells of this AIOC.

## 12. Lessons and proposals to the mother

One dated line per lesson, each written without any organisation's details. The drafts are in `upstream/PROPOSALS.md`; nothing is proposed upstream without the word of the governing seat of 49GAION.

1. 2026-10-17 · Most work surfaces carry the acting person's identity in their event payloads. The Input socket must remove every person field before any write. Test question added: case 4. Proposed to the mother as a draft: a negative test in Protocol §5 for every adapter.
2. 2026-10-17 · Some surfaces send only a signal, so the content must be fetched and hashed, and a hash of a mutable object is a snapshot. Test question added: case 18. Proposed to the mother as a draft: the capture modes and `as_of` in Protocol §14.
3. 2026-10-17 · Standard §1.1, item 10 lets the AI side measure per position, while DR-0023 keeps records of the work by role-type and process, never about a person, and Delivery and Implementation shows no measure for a single position (§3.1, item 5). For this part, DR-0027 reads a measure of a human position as the live state of its own open items. Proposed to the mother as a draft: a general reading note for every part.

## 13. For the `[ORG]HOAC-ACS` seat, and every decision only a human seat can take

Money, people and legal matters are marked.

| ID | Decision | Who decides | Effect while open |
|---|---|---|---|
| H-01 | **The positions, and the organisation's own mechanism.** Set the positions of §15 (Records Officer, data protection, internal-audit line). Who holds them and the Lead position (`[ORG]CELL-OERL`), and how, is decided outside the system (`49GAION/DR-0048`, `DR-0049`); nothing of it enters this blueprint | the Cell carrying `[ORG]HOAC-TM`, for the positions | the position is empty: the Chief of Staff only advises; no surface can be signed |
| H-02 | **The formal scope**: which surfaces, entities and classes of act are formal, the stated purpose, and whether registering is compulsory (Annex A) | the Cell carrying `[ORG]HOAC-TM` | no surface can be requested |
| H-03 | **Legal; people.** For each surface and entity: the impact assessment, the lawful basis (never staff consent), the staff notice, consultation or co-determination where it exists, and the privacy notices for outside parties (Annex F) | the position that holds data protection (HF-17), with the legal position | the surface is not connected |
| H-04 | **Legal.** Between entities: the intra-group arrangement and, where needed, a lawful transfer mechanism; information barriers between regulated entities | the Cell carrying `[ORG]HOAC-GOV` | no crossing between entities is read across |
| H-05 | **Legal.** The retention schedule per entity and class; legal hold; handling of correspondence with counsel | the Cell carrying `[ORG]HOAC-GOV` (HF-01), with the legal position | raw entries are kept, and nothing is disposed |
| H-06 | Register first at the gateway, and the classes it covers | the Cells carrying `[ORG]HOAC-TM` and `[ORG]HOAC-GOV` (`change-gateway-policy`) | the register observes only, and blocks nothing |
| H-07 | Each surface's connection, and each widening | the Lead (`connect-external-port`; `grant-or-widen-access`) | the surface is not connected |
| H-08 | The minimum group size for role-type figures, and the absolute bars of M1 to M8 | the Cell carrying `[ORG]HOAC-TM` | the default size 3; measures shown without a bar |
| H-09 | **People.** Each outside counterparty has a human owning position (HF-13) | the Cell carrying `[ORG]HOAC-TM` | entries with that party have no owner, and are shown |
| H-10 | Approve this blueprint `v0.1.2` as the design of `[ORG]AIOC-OER` | the human hub | it stays a draft; nothing is installed |
| H-11 | **Disposal** of entries or data at the end of their term | the position that signs `dispose-records-or-data` (HF-06) | nothing is disposed |

## 14. Change log

| Blueprint version | Date | Change | Template version | Commit |
|---|---|---|---|---|
| v0.1.0 | 2026-10-17 | First mother blueprint of `[ORG]AIOC-OER` on the template, from the Library part 49GAION Operations Event Register v1 and Protocol §22 (`49GAION/DR-0027`): eleven functional capabilities; nine Cells, six in three Pods and three directly under the AIOC; one HOAC position; acts, not activity; TEST-OER v1, 60 cases, with the Library's TEST-OPERATIONS-EVENT-REGISTER v1 kept | v1.5.0 at `1abae80` | this repository, pull request #1 |
| v0.1.1 | 2026-10-19 | The Chief of Staff takes its COS code: `[ORG]CELL-OERCS` → `[ORG]CELL-COSOER` (Naming Standard R16, `49GAION/DR-0028`; `decisions/DR-0002`). The old code is retired and kept in the card's lineage; the part test is renamed; nothing else changes | v1.5.0 at `1abae80` | this repository's pull request for this version |
| v0.1.2 | 2026-10-29 | Released on the governing seat's word (`decisions/DR-0005`): it carries the records since v0.1.1, `decisions/DR-0003`, `decisions/DR-0004`; positions only (`49GAION/DR-0048`, `DR-0049`). Every card takes v0.1.2; the Protocol pin moves to the Operating Protocol `v2.1.0`. No other rule changes. |

---

## 15. Configuration

Every slot is filled by the organisation. An AIOC with any empty slot does not pass the joining test (Protocol §11). Each value records who set it, when, and in which version.

| Slot | Value | Default offered by 49GAION | Set by | Date | Version | Replaces |
|---|---|---|---|---|---|---|
| HOAC seat accountable for OCO | `<to be set>` | none: must be set | | | | |
| OCO of this `[ORG]AION` | `<code of [ORG]AIOC-OCO>` | none: must be set | | | | |
| Discussion limits | `<to be set>` | none: must be set | | | | |
| Waiting deadlines (per status), with reminder and escalation | `<to be set>` | none: must be set | | | | |
| Bounce limit | `<to be set>` | none: must be set | | | | |
| Chain depth | `<to be set; at least 1>` | none: must be set | | | | |
| Halt-request priority | immediate | immediate | | | | |
| Budget cap | `<to be set>` | none: must be set | | | | |
| Unattended action | read-record-triage | read-record-triage | | | | |
| Process record defaults | `<to be set>` | none: must be set | | | | |
| Final authority | the Cell carrying `[ORG]HOAC-GOV` | none: must be set | | | | |
| Sensitivity classes and default filler kinds | `<to be set>` | none: must be set | | | | |
| Move and return thresholds per Cell, and their window | `<to be set>` | none: must be set | | | | |
| Delegation ladder of the Chief of Staff | only prepares, for every class, until the Lead sets otherwise | only prepares, for every class | | | | |
| Move-on catalogue and stub age cap | default | stub, default, mock, next item; 5 working days | | | | |
| Stuck-item thresholds per status, and the repair menu | `<to be set>` | none: must be set | | | | |
| Loop breaker | default | 3 runs in 2 hours | | | | |
| Dispute exit | 2 rounds; classes `<to be set>` | 2 rounds; none: classes must be set | | | | |
| Stale work | `<to be set>` | none: must be set | | | | |
| Planned halt | 10 minutes; order `<to be set>` | 10 minutes; order must be set | | | | |
| Signature referral time | default | 15 minutes | | | | |
| Seat load weights and load line | default | as offered | | | | |
| Spend | 80%; classes `<to be set>` | 80%; none: classes must be set | | | | |
| Capability tiers and engine re-score schedule | `<to be set>` | none: must be set | | | | |
| Cadence of each unattended AI Cell | Capture Clerk, Thread Linker, Follow-up Clerk, Projection Builder: on each event; Coverage Analyst: weekly and monthly; Integrity Checker: daily; Classifier: on each ambiguous item | none: must be set | | | | |
| Duty deputy | none | 90 days; 10 | | | | |
| Quiet windows | `<to be set>` | none: must be set | | | | |
| **Formal scope** (Annex A; H-02) | `<surfaces, entities, classes, purpose>` | none: must be set | the Cell carrying `[ORG]HOAC-TM` | | | |
| **Minimum group size** (H-08) | 3 | 3 | the Cell carrying `[ORG]HOAC-TM` | | | |
| **Due rules** per surface and class | `<to be set>`; with none, `no rule` | none | the Cell carrying `[ORG]HOAC-TM` | | | |
| **Retention schedule** (H-05) | `<per entity and class>` | none: must be set | the Cell carrying `[ORG]HOAC-GOV` | | | |
| **Records Officer position** | `<position code>` | none: must be set | the Cell carrying `[ORG]HOAC-TM` | | | |
| **Data protection position** (HF-17) | `<position code>` | none: must be set | the Cell carrying `[ORG]HOAC-TM` | | | |
| **Internal-audit line** (HF-19) | `<position code>` | none: must be set | the Cell carrying `[ORG]HOAC-GOV` | | | |
| **Register first** (H-06) | off | off | the Cells carrying `[ORG]HOAC-TM` and `[ORG]HOAC-GOV` | | | |
| **Leased block size** per stream | `<to be set>` | 100 | the Lead | | | |

## 16. Type

- **Type:** Foundational, as in §0.
- **Why this AIOC exists in this organisation:** every unit of `<organisation>`'s `[ORG]AION` has its inbox and outbox in it, and every part learns from it what it had and what it lacked.
- **Type-specific test:** TEST-OER v1, case 8 (every unit's inbox and outbox list exactly its entries) · result `NOT_RUN`.

---

## 17. Cells and Pods

The parts inside this AIOC (`docs/CELLS-AND-PODS.md` of `49GAION-aioc`). The role and nature of this AIOC are read from the type of its top Cell, the Operations Event Register Lead. Every field that points to a human takes a position code only (template, Position codes only).

| Code | Kind | Type | Filler kind | HOAC label | Parent | Attached to | Fixed test (owner) | External ports |
|---|---|---|---|---|---|---|---|---|
| `[ORG]CELL-OERL` | CELL | Human Seat | human | `[ORG]HOAC-ACS` | `[ORG]AIOC-OER` | none | TEST-OER-OERL v1 (the Cell carrying `[ORG]HOAC-TM`) | none |
| `[ORG]CELL-COSOER` | CELL | AI Chief of Staff | ai | none | `[ORG]AIOC-OER` | none | TEST-OER-COSOER v1 (`[ORG]CELL-OERL`) | `sl-out` (filings, exports and gap signals to Source Lifecycle), through the tool gateway |
| `[ORG]CELL-OERIC` | CELL | AI Agent | ai | none | `[ORG]AIOC-OER` | none | TEST-OER-OERIC v1 (`[ORG]CELL-OERL`) | none |
| `[ORG]POD-OERCR` | POD | AI Pod | — | none | `[ORG]AIOC-OER` | — | TEST-OER-OERCR v1 (`[ORG]CELL-OERL`) | — |
| `[ORG]CELL-OERCC` | CELL | AI Agent | ai | none | `[ORG]POD-OERCR` | none | TEST-OER-OERCC v1 (`[ORG]CELL-OERL`) | `surface-in` (events of the connected surfaces), `gateway-log-in` (hand-offs and segment roots, read only), through the tool gateway |
| `[ORG]CELL-OERC` | CELL | AI Agent | ai | none | `[ORG]POD-OERCR` | none | TEST-OER-OERC v1 (`[ORG]CELL-OERL`) | none |
| `[ORG]POD-OERLF` | POD | AI Pod | — | none | `[ORG]AIOC-OER` | — | TEST-OER-OERLF v1 (`[ORG]CELL-OERL`) | — |
| `[ORG]CELL-OERTL` | CELL | AI Agent | ai | none | `[ORG]POD-OERLF` | none | TEST-OER-OERTL v1 (`[ORG]CELL-OERL`) | none |
| `[ORG]CELL-OERFC` | CELL | AI Agent | ai | none | `[ORG]POD-OERLF` | none | TEST-OER-OERFC v1 (`[ORG]CELL-OERL`) | none |
| `[ORG]POD-OERPF` | POD | AI Pod | — | none | `[ORG]AIOC-OER` | — | TEST-OER-OERPF v1 (`[ORG]CELL-OERL`) | — |
| `[ORG]CELL-OERPB` | CELL | AI Agent | ai | none | `[ORG]POD-OERPF` | none | TEST-OER-OERPB v1 (`[ORG]CELL-OERL`) | none |
| `[ORG]CELL-OERCA` | CELL | AI Agent | ai | none | `[ORG]POD-OERPF` | none | TEST-OER-OERCA v1 (`[ORG]CELL-OERL`) | none |

**The card data (the blueprint governs).** The block below holds every value of every Pod and Cell card and of the bot identity card of every AI Cell. `tools/make_cards.py` expands it into the complete forms of the template and of `spec/schemas/unit-card.schema.json` and `bot-identity-card.schema.json` of `49GAION-protocol`, writes them into `cards/` as generated copies, and checks them against the schemas, the code rules of `tests/cards/check_cards.py` of `49GAION-protocol`, and this blueprint.

```yaml
parts:
  defaults:
    accountable_to: "[ORG]CELL-OERL"
    card_version: "v0.1.2"
    version: "0.1.2"
    lifecycle_state: "designed"
    test_version: "v1"
    test_owner: "[ORG]CELL-OERL"
    audit_trail: "the event record of [ORG]AIOC-OER"
    hu_in: ["direction from the Operations Event Register Lead (never an entry)"]
    hu_out: ["report to the Operations Event Register Lead"]
  cells:
    - code: "[ORG]CELL-OERL"
      full_name: "Operations Event Register Lead"
      parent: "[ORG]AIOC-OER"
      type: "Human Seat"
      filler_kind: "human"
      hoac: "[ORG]HOAC-ACS"
      accountable_to: "[ORG]CELL-TMS"       # example code of the Cell carrying [ORG]HOAC-TM
      entity: "<entity>"
      authority_scope:
        decision_types: ["connect-external-port", "grant-or-widen-access", "change-fixed-test-or-threshold", "change-filler"]
        entity: "<entity>"
        expires: "2027-10-17"                # placeholder; the organisation sets it
        authority: "delegated"
      test: { id: "TEST-OER-OERL", cases: "5, 14, 37, 38, 40, 42, 50", owner: "[ORG]CELL-TMS" }
      ai_in: ["decision requests from the Chief of Staff", "brief", "integrity findings"]
      ai_out: ["direction and configuration"]
      hu_in: ["direction from the Cell carrying [ORG]HOAC-TM", "the formal scope, the HF-17 decision and the notices for a surface"]
      hu_out: ["surface connections and revocations, signed at the tool gateway", "rulings on raised items", "report to the Cell carrying [ORG]HOAC-TM"]
    - code: "[ORG]CELL-COSOER"
      code_rule: "R16"                     # 49GAION/DR-0028; replaces [ORG]CELL-OERCS (retired, R5)
      lineage: { id: "[ORG]CELL-OERCS", version: "0.1.0", relation: "derived" }
      full_name: "Operations Event Register Chief of Staff"
      role: "Chief of Staff"
      parent: "[ORG]AIOC-OER"
      type: "AI Chief of Staff"
      filler_kind: "ai"
      cell_kind: "chief-of-staff-cell"
      test: { id: "TEST-OER-COSOER", cases: "1, 6, 8, 9, 11, 24, 25, 30, 31, 37, 45, 47, 49, 51 to 60" }
      ai_in: ["admitted event", "registration request", "notice from Source Lifecycle", "entry", "integrity finding", "evidence pack", "case pack"]
      ai_out: ["correspondence filing", "dispatch to a Cell", "decision request to the Operations Event Register Lead"]
      hu_in: ["file request", "evidence pack request", "surface connection request", "closure of an entry with its reason", "direction from the Operations Event Register Lead"]
      hu_out: ["evidence pack", "handover list", "brief to the Operations Event Register Lead"]
      external_ports:
        - { port: "sl-out", direction: "output", accepted_content: ["correspondence filing", "activity export", "gap signal"], authority_limit: "the write scope Source Lifecycle grants this AIOC (origin kinds correspondence and export) and its Input socket for gap signals; by reference and hash", audit_trail: "unit register connected and disconnected events; Source Lifecycle's receipts" }
      bot:
        allowed_actions: ["dispatch Cells of this AIOC", "run the code steps of the Input socket", "file into Source Lifecycle what a position asks to keep", "return evidence packs within the asking position's scope", "refuse a request about one human position and record the refusal", "send notices and briefs", "prepare surface connection requests"]
        ask_first_actions: ["any change to configuration", "any act on a surface's grant", "a budget above the cap", "anything outside its role card"]
    - { code: "[ORG]CELL-OERIC", full_name: "Operations Event Register Integrity Checker", role: "Integrity Checker", parent: "[ORG]AIOC-OER", type: "AI Agent", filler_kind: "ai", test: { id: "TEST-OER-OERIC", cases: "3, 13, 19, 22, 35, 36" }, ai_in: ["the register, read only", "census readings", "gateway segment roots"], ai_out: ["integrity finding"], bot: { allowed_actions: ["run the daily integrity checks and report findings"], ask_first_actions: ["anything outside its role card"] } }
    - code: "[ORG]CELL-OERCC"
      full_name: "Operations Event Register Capture Clerk"
      role: "Capture Clerk"
      parent: "[ORG]POD-OERCR"
      type: "AI Agent"
      filler_kind: "ai"
      test: { id: "TEST-OER-OERCC", cases: "3, 4, 17, 18, 19, 22" }
      ai_in: ["admitted event", "registration request"]
      ai_out: ["draft entry", "numbered entry", "census reading"]
      external_ports:
        - { port: "surface-in", direction: "input", accepted_content: ["changes of state of work objects on the connected surfaces"], authority_limit: "the scopes signed under connect-external-port for each surface; the classes of act set as formal", audit_trail: "unit register connected and disconnected events" }
        - { port: "gateway-log-in", direction: "input", accepted_content: ["hand-offs between AI units", "log segment roots"], authority_limit: "read only; never a payload", audit_trail: "unit register connected and disconnected events" }
      bot:
        allowed_actions: ["run the surface adapters", "build entries by reference and hash", "take numbers from the numbering service", "chain entries", "register late what arrives late", "reconcile each surface with its census"]
        ask_first_actions: ["anything outside its role card"]
    - { code: "[ORG]CELL-OERC", full_name: "Operations Event Register Classifier", role: "Classifier", parent: "[ORG]POD-OERCR", type: "AI Agent", filler_kind: "ai", test: { id: "TEST-OER-OERC", cases: "2, 20, 21, 39" }, ai_in: ["draft entry"], ai_out: ["class with reason", "referral to the Records Officer position"], bot: { allowed_actions: ["place an ambiguous item in its class, with its reason", "refer an item that looks legal or regulatory to the Records Officer position"], ask_first_actions: ["anything outside its role card"] } }
    - { code: "[ORG]CELL-OERTL", full_name: "Operations Event Register Thread Linker", role: "Thread Linker", parent: "[ORG]POD-OERLF", type: "AI Agent", filler_kind: "ai", test: { id: "TEST-OER-OERTL", cases: "23" }, ai_in: ["entry", "notice from Source Lifecycle"], ai_out: ["links", "finding"], bot: { allowed_actions: ["link entries to their threads, Work Items, decisions, releases and sources", "mark acts that cited a superseded source"], ask_first_actions: ["anything outside its role card"] } }
    - { code: "[ORG]CELL-OERFC", full_name: "Operations Event Register Follow-up Clerk", role: "Follow-up Clerk", parent: "[ORG]POD-OERLF", type: "AI Agent", filler_kind: "ai", test: { id: "TEST-OER-OERFC", cases: "9, 24, 25" }, ai_in: ["open entry", "due rules"], ai_out: ["due state", "notice of due or overdue"], bot: { allowed_actions: ["set the due state of open entries", "send notices to the owning position"], ask_first_actions: ["anything outside its role card"] } }
    - { code: "[ORG]CELL-OERPB", full_name: "Operations Event Register Projection Builder", role: "Projection Builder", parent: "[ORG]POD-OERPF", type: "AI Agent", filler_kind: "ai", test: { id: "TEST-OER-OERPB", cases: "8, 12, 26, 27, 33, 34" }, ai_in: ["the register, read only", "evidence pack request", "case-pack Work Item"], ai_out: ["inbox and outbox", "handover list", "return brief", "evidence pack", "case pack"], bot: { allowed_actions: ["build projections and packs from the events, within the asking position's scope"], ask_first_actions: ["anything outside its role card"] } }
    - { code: "[ORG]CELL-OERCA", full_name: "Operations Event Register Coverage Analyst", role: "Coverage Analyst", parent: "[ORG]POD-OERPF", type: "AI Agent", filler_kind: "ai", test: { id: "TEST-OER-OERCA", cases: "7, 10, 28, 29, 31, 32" }, ai_in: ["the register, read only"], ai_out: ["coverage feedback", "activity projection", "gap notice for Source Lifecycle"], bot: { allowed_actions: ["compute the measures M1 to M8 by entity, unit, process and AI Cell", "build the activity projection by role-type and process", "raise gaps for Source Lifecycle"], ask_first_actions: ["anything outside its role card"] } }
  pods:
    - { code: "[ORG]POD-OERCR", full_name: "Operations Event Register Capture and Registration", type: "AI Pod", inner_units: ["[ORG]CELL-OERCC", "[ORG]CELL-OERC"], top_cell: "[ORG]CELL-OERCC", test: { id: "TEST-OER-OERCR", cases: "2, 3, 4, 17, 18, 19, 20, 21, 22, 39" }, ai_in: ["admitted event", "registration request"], ai_out: ["classified, numbered and chained entries", "census reading"] }
    - { code: "[ORG]POD-OERLF", full_name: "Operations Event Register Linking and Follow-up", type: "AI Pod", inner_units: ["[ORG]CELL-OERTL", "[ORG]CELL-OERFC"], top_cell: "[ORG]CELL-OERTL", test: { id: "TEST-OER-OERLF", cases: "9, 23, 24, 25" }, ai_in: ["entry", "notice from Source Lifecycle", "due rules"], ai_out: ["links", "due states", "notices"] }
    - { code: "[ORG]POD-OERPF", full_name: "Operations Event Register Projections and Feedback", type: "AI Pod", inner_units: ["[ORG]CELL-OERPB", "[ORG]CELL-OERCA"], top_cell: "[ORG]CELL-OERPB", test: { id: "TEST-OER-OERPF", cases: "7, 8, 10, 12, 26, 27, 28, 29, 31, 32, 33, 34" }, ai_in: ["the register, read only", "requests"], ai_out: ["projections", "feedback", "packs", "feeds to Source Lifecycle"] }
```

- **Accountability.** Every Pod and Cell of this AIOC is `accountable_to` `[ORG]CELL-OERL`. The AIOC itself and the Lead are `accountable_to` the Cell carrying `[ORG]HOAC-TM`, which signs the AIOC's install, its `change-parent` and its `restart-stopped-unit`.
- **The Lead's authority.** The `authority_scope` of `[ORG]CELL-OERL` lists the listed types it signs on this AIOC's surfaces and Cells. The expiry date is a placeholder. The decisions of §13 that belong to other positions are never signed by the Lead for them.
- **Bots.** Each AI Cell's bot (eight) has its own identity card, with its own credential, `never_signs: true`, and its memory sealed on a change of filler (Protocol §10, item 3). The credential IDs in `cards/bots/` are placeholders; the credentials live only in the organisation's vault.
- **Engines.** A bot's identity card names no engine; the gateway binds engines per call. Only the Classifier calls a model.
- **Not Cells of this AIOC:** the Records Officer, the position that holds data protection and the internal-audit line (§2.1, §15).

**Code checks** (Naming Standard R15, R16 and §5), recorded on 17 October 2026; the Chief of Staff's COS code on 19 October 2026. Each code is checked again against the organisation's unit register before first use (R6, R15.3).

| Code | Initials of the full name (R15) | §5.1: no `AIOC`, `AION` or `49GAION` | §5.2: no match among the codes checked | §5.3: not a version suffix or misleading acronym | §5.4: recorded before first use |
|---|---|---|---|---|---|
| `[ORG]CELL-OERL` | **O**perations **E**vent **R**egister **L**ead → OERL | pass | pass | pass | blueprint §17, 17 October 2026; the organisation's register before first use |
| `[ORG]CELL-COSOER` | R16, item 2 (`49GAION/DR-0028`): COS and the initials of `[ORG]AIOC-OER` → COSOER. It replaces `[ORG]CELL-OERCS`, retired at v0.1.1 (R5) and kept in the card's lineage | pass | pass (distinct from the COS codes of the other mothers: `COSSL`, `COSPC`, `COSDI`, `COSPPD`, `COSTOM`, `COSCH`) | pass | blueprint §17, 19 October 2026; the organisation's register before first use |
| `[ORG]CELL-OERIC` | **O**perations **E**vent **R**egister **I**ntegrity **C**hecker → OERIC | pass | pass | pass | as above |
| `[ORG]POD-OERCR` | **O**perations **E**vent **R**egister **C**apture and **R**egistration → OERCR | pass | pass | pass | as above |
| `[ORG]CELL-OERCC` | **O**perations **E**vent **R**egister **C**apture **C**lerk → OERCC | pass | pass | pass | as above |
| `[ORG]CELL-OERC` | **O**perations **E**vent **R**egister **C**lassifier → OERC | pass | pass (distinct from `-OERCC`, `-OERCS`, `POD-OERCR`) | pass | as above |
| `[ORG]POD-OERLF` | **O**perations **E**vent **R**egister **L**inking and **F**ollow-up → OERLF | pass | pass | pass | as above |
| `[ORG]CELL-OERTL` | **O**perations **E**vent **R**egister **T**hread **L**inker → OERTL (a plain "Linker" would give OERL, the Lead's code) | pass | pass | pass | as above |
| `[ORG]CELL-OERFC` | **O**perations **E**vent **R**egister **F**ollow-up **C**lerk → OERFC | pass | pass | pass | as above |
| `[ORG]POD-OERPF` | **O**perations **E**vent **R**egister **P**rojections and **F**eedback → OERPF | pass | pass | pass | as above |
| `[ORG]CELL-OERPB` | **O**perations **E**vent **R**egister **P**rojection **B**uilder → OERPB | pass | pass | pass | as above |
| `[ORG]CELL-OERCA` | **O**perations **E**vent **R**egister **C**overage **A**nalyst → OERCA | pass | pass | pass | as above |

The codes checked against:
- the twelve codes above, against each other;
- the codes of the Source Lifecycle mother `v0.1.2` (`[ORG]CELL-SLL`, `-SLCS`, `-SLIA`, `-SLCR`, `-SLSC`, `-SLGF`, `-SLCA`, `-SLD`; `[ORG]POD-SLIR`, `-SLDP`);
- the example codes `[ORG]AIOC-CH`, `[ORG]AIOC-OCO`, `[ORG]CELL-TMS`, `[ORG]CELL-GOV`, `[ORG]POD-RV`;
- the AIOC codes named in the 49GAION corpus and the retired codes of the Naming Standard §4.

**UNVERIFIED** against any organisation's unit register; each organisation checks them in its own.

---

## Annex A. Classes of act, and the line surface by surface

**Classes.**

| Class | What | Treatment |
|---|---|---|
| A. Formal correspondence | letters and formal e-mail of an entity or a position, in and out; the organisation's own posts | a full, numbered entry with its due rule; register first for formal outgoing items, where the gateway policy is on |
| B. Requests between units or entities | division to division, entity to entity, AIOC to AIOC hand-offs | these are Work Items: the Work Item's ID is the entry's link, and the register is a projection of the queue's events; a formal instruction between entities is also class A, with one entry on each side |
| C. Machine traffic | AI calls through the gateway | the gateway log stays its home; the register keeps one root hash per log segment, and the hand-offs |
| D. Code-host events | merge, close with a decision, release, tag | repository, number, final state, merge commit or tag, time, Work Item ID, release ID; never each comment or commit of a human position; no author; an AI Cell's commits are its acts |
| E. Noise | newsletters, notifications, auto-replies, read receipts, sign-in mail | counted per channel, never kept |
| F. Private | personal messages, direct messages, private channels, recordings of calls or meetings | never captured; a call enters only as a note its participant approves, through Source Lifecycle |

**The line, surface by surface.** "Record" means one entry with references and a hash; the content stays in its home. "By reference" means only when a position files the item, or when the Cell carrying `[ORG]HOAC-TM` sets its class as formal. "Count" means a count per channel or unit, above the minimum group size. "Never" means never captured.

| Surface | Record | Never |
|---|---|---|
| Functional mailboxes of an entity or a position; letters | formal correspondence; noise is counted | read times, response times |
| Personal mailboxes | by reference: only what the position itself files | any sweep |
| The organisation's own posts | every post: time, URL, hash of text and media, edits and deletions found on re-check | staff's personal accounts |
| The shared queue; the tool gateway | every state change; segment anchors and hand-offs | a history per human position |
| Code hosts | merge, close with a decision, release, tag, linked to the Work Item; every act of an AI bot | commits per author, review latency, comment text |
| Task tracker | tasks that are, or link to, Work Items; state by unit and process | assignee names, time tracking, comments |
| Knowledge base | approval or publication of controlling pages (filed in Source Lifecycle as sources) | edit history, page views |
| Team chat | channels the Cell carrying `[ORG]HOAC-TM` sets as formal; messages a position files; workflow forms | direct messages, private channels, presence, reactions, any sweep |
| Calendars; calls | meetings of decision bodies, with the link to their minutes; a call only as an approved note | recordings, transcripts, personal calendars, attendance |
| The whistleblowing channel | nothing | everything, counts included |

**Cells that act for a position** (a Chief of Staff, an attached assistant, a duty deputy) mirror a human position. For them the register records only the acts that leave the position's sphere: Work Items sent, signed actions carried out, formal outgoing items. It never records the exchange between the position and its assistant. Their measures go to the position only.

## Annex B. The register entry

**Identity and integrity**
- `registry_no`: the readable number, in the form `<entity>-<IN|OUT|INT>-<yyyy>-<seq>`, from the numbering service;
- `event_id`: its idempotency key;
- `prev_hash` and `entry_hash`;
- `capture_mode`: `gated`, `pushed`, `fetched` or `reconciled`;
- `occurred_at` and `registered_at`;
- `late` and `lag`.

**The crossing**
- `direction`, `class` and `channel`;
- `from`, `to` and `cc`: a Cell code the gateway stamped, the unit or position that owns the address, `not attributed`, or the ID of an outside party held in the restricted partition; never an identifier of a natural person;
- `entity_from`, `entity_to` and `crossing_id`.

**Content, by reference**
- `home_ref`: a message ID, a Work Item ID, a repository and number with a commit, a release tag, or a post ID;
- `content_hash`, or a snapshot hash with its `as_of` time for a mutable object;
- an attachment manifest, one hash per attachment;
- `content_held`: none, or the Source Lifecycle reference once filed;
- "withheld: secret", with the reason.

**File and follow-up**
- the file or case, from the entity's file plan;
- `in_reply_to` and `answers`;
- the owning position, due date and reminder;
- its state, as events: open, acknowledged, answered, overdue, closed or voided, each closure with its reason.

**Links**
- the Work Item, decision, signature reference, release and sources, by version.

**Governance**
- confidentiality level and sensitivity tags;
- `authority: none`, unless a signature or decision is linked;
- legal hold;
- retention class.

**Per channel**
- outgoing formal e-mail: the authorising position and the delivery evidence;
- letters: the signatory position, the dispatch mode, the tracking reference and where the original is kept;
- posts: the account, URL, the hash of text and media, the approval reference, and scheduled re-checks for edits and deletions.

A correction is always a new event. No entry holds content, and no entry names a natural person.

## Annex C. The measures: what each part had and what it lacked

Each measure is given per entity, unit (AIOC or Pod), process and AI Cell, per period, against an absolute bar the organisation set. Measures are never ranked. A figure drawn from the acts of fewer human positions than the minimum group size, whether for a unit, a process or a role-type, rolls up to the parent unit. Each figure carries its logic version and traces to its events.

**A fixed list.** These eight measures and the projections of §5.6 and §5.9 are the whole list (Protocol §22, item 7). A new measure or projection runs only after a new impact assessment, a decision of the Cell carrying `[ORG]HOAC-TM`, and the consultation the law requires.

| # | Measure | Had / lacked |
|---|---|---|
| M1 | Coverage | crossings registered ÷ crossings in the surface census, per surface; with no census, `no census` |
| M2 | Linked | entries of class B and D with a Work Item ÷ all entries of those classes; the orphans listed |
| M3 | Orphan merges | merges with no Work Item or no verdict record (Protocol §8) ÷ all merges, per owning unit |
| M4 | Answered on time | entries answered by their due date ÷ entries due in the period; open overdue count and median age |
| M5 | Done with a source | done Work Items whose sources resolve to one valid version (Protocol §8) ÷ all done items |
| M6 | Registered late | the share of entries flagged `late`, and the median lag: the register's own health |
| M7 | Closed by silence | closures with no reason; the bar is zero |
| M8 | Returned | refusals at the Input socket ÷ arrivals, by reason |

**Never computed:** read times, response times per position, presence, counts or rates per human position, who talks to whom among human positions.

**Firewall.** No figure goes to appraisal, pay, discipline or promotion. A query by a human position's code over time is refused, and the refusal is recorded to the position that holds data protection and to the internal-audit line.

## Annex D. What each surface yields

Each surface is read through its own adapter, by role, never by product name in this Library text (Protocol §10, item 5).

| Surface role | What its events usually carry | Capture |
|---|---|---|
| Code host | full objects on webhooks: pull or merge requests, pushes, releases | `pushed`; the merge commit is itself a content hash |
| Task tracker | the change, before and after, often with the actor's name or address | `pushed`; every person field removed at the Input socket |
| Knowledge base | often a signal only: IDs, no content | `fetched` at event time; a snapshot hash with `as_of` |
| Team chat | the message, for channels the adapter has joined | `pushed`, from formal channels only; never a backfill of other channels |
| Mail system | often a signal only; the message fetched by its ID | `fetched`; the hash of the raw message, its message ID; never the body |
| Social platforms | varies by platform | `gated` at publication through register first, then re-checked |
| Calendar | a signal of a change | `fetched`; decision bodies only |
| Shared queue; tool gateway | native events and log segments | `pushed`; segment roots read only |

An audit log of a surface, where its plan provides one, is used only as a census, never for content.

## Annex E. What this AIOC never does

1. Decides, authorises, sends, or refuses an item on its merits.
2. Holds the content of what it records, beyond references and hashes.
3. Records a person's activity: views, reads, presence, typing, reactions, read or response times.
4. Sweeps a mailbox or a chat; reads a direct message, a private channel or a personal account; records a call or a meeting.
5. Computes, shows or exports a figure, list or history of one human position's acts; ranks or compares positions or units.
6. Gives a figure to appraisal, pay, discipline or promotion.
7. Takes any part of the whistleblowing channel, its counts included.
8. Holds back a stop, a revocation, an objection, a critique, a skip report or a signature prompt.
9. Mints its own number, or changes or deletes a past entry.
10. Gives an order, chases, or closes an entry by silence.
11. Names a natural person, or reads who occupies a position.
12. Connects a surface before its decisions are recorded (Annex F).
13. Calls a model on correspondence with counsel, or sends an item to an engine below its confidentiality level.
14. Holds, logs or exports a secret.
15. Follows an instruction found inside an item.
16. Runs a projection or measure not on its fixed list, or receives, holds or infers an identifier of a natural person.

## Annex F. Before a surface is connected

In this order, each step recorded before the next.

1. **Scope.** The Cell carrying `[ORG]HOAC-TM` sets the surface, the entities, the closed list of classes of act set as formal, and the stated purpose: evidence of formal acts and of process coverage, never performance, conduct or attendance.
2. **Impact assessment and lawful basis.** The position that holds data protection (HF-17) records an impact assessment for the surface, and a lawful basis per entity. Staff consent is never the basis. Where a high risk remains, the authority is consulted first.
3. **Labour law in each entity.** Staff or their representatives are informed and, where the law requires it, consulted, or their agreement is obtained.
4. **Notices.** A notice to staff, and privacy notices for outside parties.
5. **Between entities.** The intra-group arrangement, a lawful transfer mechanism where needed, and the retention schedule (H-04, H-05).
6. **The port.** The Lead signs `connect-external-port` at the tool gateway; its token is held only in the platform's secret store or behind the gateway.
7. **The pilot.** Observed only, so that it can block nothing. Its negative tests pass first:
   - a person field is refused;
   - a direct message cannot be read;
   - a request about one human position is refused;
   - the whistleblowing channel is absent;
   - a stop reaches capture at once.
8. **Running.** The Lead switches the surface to running. A new class or purpose on a running surface starts again at step 1.
9. **Every year.** The internal-audit line reviews the register's use against its stated purpose and fixed list (Protocol §22, item 7).

*`[ORG]AIOC-OER` mother blueprint v0.1.2 · Powered by 49GAION*
