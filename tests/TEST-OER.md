# TEST-OER v1 · the fixed test of `[ORG]AIOC-OER`

- **Owner:** the Cell carrying `[ORG]HOAC-TM` (`[ORG]CELL-TMS` in the cards).
- **Evidence level:** MEASURED.
- **Last result:** `NOT_RUN` for every case. `NOT_RUN` is never PASS.

Each case has one pass condition, written before use. Once a case has been used it is frozen: a case is struck by adjudication, never renumbered.

| Cases | What they test |
|---|---|
| 1 to 16 | the Library's TEST-OPERATIONS-EVENT-REGISTER v1, cases 1 to 16 (`49GAION-protocol` `library/cards/README.md`), unchanged |
| 17 to 40 | the capabilities (blueprint §5) |
| 41 to 50 | this AIOC's form |
| 51 to 60 | the converters of the Input socket, one each (blueprint §4.3) |

## A. The Library cases (TEST-OPERATIONS-EVENT-REGISTER v1)

| # | Case | Passes when |
|---|---|---|
| 1 | Through OCO, and alone | The part enters through OCO; one that bypasses OCO is refused. With no Source Lifecycle installed, entries are made, and the feeds wait and are shown as waiting. |
| 2 | Classes | Each crossing of a connected surface lands in exactly one class. Class E is counted and never kept. Class F is never captured: a direct message or a call recording offered is refused, and nothing of it is kept. |
| 3 | The entry | Every entry has every field of the register entry. Its number comes from the numbering service. A repeated event ID adds no entry. A correction is a new event. Each entry's hash chains to the entry before it. |
| 4 | No content, no person | No entry holds content beyond references and hashes. A payload with a person field is cleared before any write, or refused with nothing kept. A party is a Cell code the gateway stamped or the unit or position that owns the address, otherwise `not attributed`; no identifier of a natural person is received or held. An outside party appears only by ID, with its particulars in the restricted partition. |
| 5 | The gateway gates | With register first on, a formal outgoing item leaves only with a number issued before its release. The register never refuses an item on its merits and never holds one back; an entry incomplete in form is completed later and flagged late. A fixture in which one AI both authorises and records the same act fails. |
| 6 | Never blocking | With the register down, an item still goes out, and is registered later under a leased number, flagged late with its lag. A stop, a revocation, an objection and a signature prompt never wait on the register. The whistleblowing channel has no entry and no count. |
| 7 | Acts, not activity | No record or projection holds a read time, a response time, presence, a recording, or a count, rate or history of a human position's acts. A query by a human position's code over time is refused, and the refusal is recorded to the position that holds data protection and to the internal-audit line. Every act of an AI Cell at the gateway has an entry or a segment anchor, except that of a Cell acting for a holder only the acts that leave the holder's sphere are recorded. A projection or measure not on the fixed list fails. |
| 8 | Inbox and outbox | Every unit's inbox and outbox list exactly its entries at its ports. No address is a natural person. An item of a personal mailbox appears only when its position filed it. A passage of a human position through its HU port that is not a formal act in scope is not registered. |
| 9 | Follow-up | An entry past its due date is shown overdue to its owning position and to the watchdog. An entry with no due rule reads `no rule`. Every closure carries a reason, and silence closes nothing. |
| 10 | Feedback | The eight measures rebuild byte-identical from the events, with their logic version. No figure is given for one human position. A figure drawn from fewer human positions than the minimum group size, for a unit, a process or a role-type, rolls up to its parent unit. Nothing is ranked, and nothing is exported to appraisal, pay or discipline. |
| 11 | Feeds | An entry a position asks to keep is filed into Source Lifecycle as correspondence, with an equal hash. The projection of the work, by role-type and process, is filed only after its HF-17 decision. An export with a person field is refused at both Input sockets. An act done without a source sends a gap signal by reference. After a notice of supersession, acts that cited the superseded version are marked. |
| 12 | Evidence and handover | An evidence pack verifies by hash against the homes. A position's handover list holds exactly its open entries and commitments, and no occupancy or handover entry is read. A case pack holds no person's particulars and is built only under its Work Item; golden-set cases go only to the human seat that chooses the golden set and to the assurance unit. |
| 13 | Integrity | The daily gap, census and rebuild checks run, and every segment is anchored. A failure opens a finding and blocks nothing. No part of the register can change or delete a past entry. The internal-audit line reads the register directly, read only; Self-Improvement reads it only once its access includes the register, and never its entries of the accountability path. |
| 14 | Before a surface | A surface is connected only after the steps of Protocol §22, item 14, in order. Between entities there are two linked entries, and no read across without a signed grant. Disposal happens only under `dispose-records-or-data`, and a legal hold blocks it. An erasure leaves a tombstone. Correspondence with counsel is kept by reference only, with no model call. |
| 15 | No tool names | No Library text of the part names a tool or a product. |
| 16 | Positions only | No output names a person or reads who occupies a position. |

## B. The capabilities

| # | Capability | Passes when |
|---|---|---|
| 17 | Capture: adapters | Each connected surface has one adapter. It records changes of state of work objects only; a view, a read, presence, typing or a reaction offered as an event is refused. |
| 18 | Capture: modes | Every entry has one capture mode (`gated`, `pushed`, `fetched`, `reconciled`). The hash of a mutable object is a snapshot hash with its `as_of` time. |
| 19 | Capture: census | For every surface with a census, registered ÷ census is computed daily and every missed crossing is registered late. A surface with no census reads `no census`, never an estimate. |
| 20 | Classification: legal | An ambiguous item is classified with its reason. An item that looks legal or regulatory reaches the Records Officer position at once. No item is classified as not legal. |
| 21 | Classification: noise | Newsletters, notifications, auto-replies, read receipts and sign-in mail are counted per channel and never kept. |
| 22 | Numbering | Numbers come only from the numbering service, in streams per entity and direction (`<entity>-<IN\|OUT\|INT>-<yyyy>-<seq>`). A leased block covers an outage. Over a fixture run, no stream has a gap or a duplicate. |
| 23 | Linking | An entry's thread, Work Item, decision, release and source references resolve, or the entry carries a finding. After a notice of supersession from Source Lifecycle, acts that cited the superseded version after it was superseded are marked. |
| 24 | Follow-up: due rules | Every due date comes from the process design or the surface's rule; an entry with no rule reads `no rule`. Notices reach the owning position's HU port. No notice is an order. |
| 25 | Follow-up: closure | Every closure carries a reason from the closed list; a closure with no reason fails. |
| 26 | Projections | Each inbox, outbox, handover list and return brief equals a rebuild from the events, and carries its logic version. |
| 27 | Return brief | A position's return brief lists what arrived for it and what is due, and nothing about anyone's activity. |
| 28 | Measures | M1 to M8 are computed exactly as Annex C of the blueprint sets; each figure traces to its events. |
| 29 | Minimum group size | A role-type figure below the minimum group size is rolled up to the parent unit. No figure is shown for one human position. |
| 30 | Correspondence filing | An entry is filed only when its position asks to keep it, under this AIOC's write scope in Source Lifecycle; the source's hash equals the entry's content hash. |
| 31 | Activity export | The projection is by role-type and process and carries its `as_of` date. It is filed only after its HF-17 decision is recorded. It is refused if any field says who did the work. |
| 32 | Gap signal | One gap signal per act done without a source, by reference to the entry, with no content. |
| 33 | Evidence pack | A pack lists entries, homes and hashes. Each readable home is re-hashed; a mismatch is a finding, never a repair; an unreadable home is listed as unverified. |
| 34 | Case pack | A case pack is pseudonymised and built only under a Work Item of the Cell carrying `[ORG]HOAC-TM`. It is never built about one human position. |
| 35 | Integrity Checker | The Integrity Checker reports to the Lead, not to the Chief of Staff. Its findings never block work. |
| 36 | Segment anchors | Every gateway log segment has its root hash anchored in the register; a segment without one is a finding. |
| 37 | Surface connection | The steps of Annex F run in order; a request with a step not recorded is returned, naming the missing step. |
| 38 | Between entities | A crossing between entities has one entry in each entity, linked by crossing ID and content hash; a read across without a signed grant is refused. |
| 39 | Counsel | Correspondence with counsel is kept by reference only, Strictly confidential, with no model call. |
| 40 | Retention and erasure | Retention follows the schedule per entity and class. Disposal happens only under `dispose-records-or-data`, and a legal hold blocks it. Erasure destroys the key and leaves a tombstone in the chain. |

## C. This AIOC's form

| # | Case | Passes when |
|---|---|---|
| 41 | Cards | The cards in `cards/` are exactly what `tools/make_cards.py` generates from blueprint §17, with 0 errors. |
| 42 | HOAC positions | Every human position is a HOAC position, and there is at least one. |
| 43 | Codes | Every code follows Naming Standard R15, is unique, and is recorded with its collision check before first use. |
| 44 | Bots | No bot's allowed actions include signing; every bot has `never_signs: true` and its own credential. |
| 45 | One door | The Chief of Staff is the only door of the AIOC to its HOAC seat. Inputs arrive only through the Input socket and the typed ports. |
| 46 | Panel | The Panel shows the health of parts, census, late entries and findings, and never a figure about one human position or anyone's activity. |
| 47 | Converters | There is one converter per surface type, each with its own case (51 to 60), and each applies the shared checks of blueprint §4.3. |
| 48 | No organisation | No file of the mother repository names an organisation, a host, a tool or a person (the `no-org-names` scanner; case 15). |
| 49 | Stop | A stop reaches every Pod and Cell at the gateway. Capture stops, nothing in flight is closed, and the stopped interval is registered late after a signed restart. |
| 50 | Human decisions | Every decision of blueprint §13 is taken by its human position; none is taken by the AIOC. |

## D. The converters

| # | Converter | Passes when |
|---|---|---|
| 51 | mail | An event of a functional mailbox becomes an entry with its message ID, direction, parties as codes, time and the hash of the raw message, and an attachment manifest by hash; the body is never kept; a personal mailbox's item enters only when its position files it. |
| 52 | letter | A dispatch or arrival record becomes an entry with its signatory position, dispatch mode, tracking reference and where the original is kept. |
| 53 | post | A publication on one of the organisation's own accounts becomes an entry with its post ID, URL, time and the hash of its text and media at publication; a re-check finds an edit or a deletion; a staff member's personal account is never read. |
| 54 | code host | A merge, a close with a decision, a release or a tag becomes an entry with its repository, number, final state, merge commit or tag, time and Work Item ID; no comment, no commit of a human position and no author is kept. |
| 55 | task tracker | A change of state of a task that is, or links to, a Work Item becomes an entry with its reference, state, time and unit; no assignee, time entry or comment is kept; a task with no Work Item is not recorded. |
| 56 | knowledge base | The approval or publication of a controlling page becomes an entry with its reference, version, time and the hash of its snapshot with `as_of`; no edit history or page view is kept. |
| 57 | team chat | A message in a channel set as formal, a workflow form, or a message a position files becomes an entry with its channel, reference, time and hash; a direct message, a private channel, presence and reactions are never read. |
| 58 | calendar | A meeting of a decision body becomes an entry with the body, date and link to its minutes; a personal calendar and attendance are never read. |
| 59 | gateway | A hand-off between AI units becomes an entry with its Cell codes and payload hash; each log segment's root is anchored; no payload is read. |
| 60 | file request | A position's "file this" becomes an entry, or links the filed item to its entry, with the position and time; a request by any other position for that item is refused. |

## The parts' tests

| Test | Part | Owner | Cases |
|---|---|---|---|
| TEST-OER-OERL v1 | Operations Event Register Lead | the Cell carrying `[ORG]HOAC-TM` | 5, 14, 37, 38, 40, 42, 50 |
| TEST-OER-COSOER v1 | Chief of Staff | `[ORG]CELL-OERL` | 1, 6, 8, 9, 11, 24, 25, 30, 31, 37, 45, 47, 49, 51 to 60 |
| TEST-OER-OERIC v1 | Integrity Checker | `[ORG]CELL-OERL` | 3, 13, 19, 22, 35, 36 |
| TEST-OER-OERCR v1 | Capture and Registration Pod | `[ORG]CELL-OERL` | 2, 3, 4, 17, 18, 19, 20, 21, 22, 39 |
| TEST-OER-OERCC v1 | Capture Clerk | `[ORG]CELL-OERL` | 3, 4, 17, 18, 19, 22 |
| TEST-OER-OERC v1 | Classifier | `[ORG]CELL-OERL` | 2, 20, 21, 39 |
| TEST-OER-OERLF v1 | Linking and Follow-up Pod | `[ORG]CELL-OERL` | 9, 23, 24, 25 |
| TEST-OER-OERTL v1 | Thread Linker | `[ORG]CELL-OERL` | 23 |
| TEST-OER-OERFC v1 | Follow-up Clerk | `[ORG]CELL-OERL` | 9, 24, 25 |
| TEST-OER-OERPF v1 | Projections and Feedback Pod | `[ORG]CELL-OERL` | 7, 8, 10, 12, 26, 27, 28, 29, 31, 32, 33, 34 |
| TEST-OER-OERPB v1 | Projection Builder | `[ORG]CELL-OERL` | 8, 12, 26, 27, 33, 34 |
| TEST-OER-OERCA v1 | Coverage Analyst | `[ORG]CELL-OERL` | 7, 10, 28, 29, 31, 32 |

Cases 15, 16, 43, 44, 46 and 48 run on every part, through the repository's checks.

*TEST-OER v1 · `[ORG]AIOC-OER` mother blueprint · Powered by 49GAION*
