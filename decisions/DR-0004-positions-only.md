# DR-0004 · Operations Event Register mother: positions only, brought into line with 49GAION/DR-0048 and DR-0049

- **Date:** 2026-10-28
- **Decided by:** the governing seat (GOV) of 49GAION
- **Source:** `49GAION/DR-0048`, the complete definition `v2.1.0`: the system recognises only AI, organised in AIOCs, and human positions carrying a HOAC label; no natural person and no person's name is recorded in it; each organisation's own mechanism, outside the system, decides how its positions are assigned and administered and who holds them. `49GAION/DR-0049` brings the texts into line. The record is prepared by the AI hub; the governing seat's merge is the decision.
- **Relation:** builds on DR-0003. Where an earlier record of this repository sets the mechanism behind a human position (who occupies it, an acting filler, a deputy, "the governance seat appoints Top Management directly"), this record supersedes it; those records are frozen and are read with this one.

## Decision

1. **Positions only.** Every human place in this repository is a position. Who holds it, and how (successors, deputies, boards and the credentials with which a position signs included), is the organisation's own mechanism, outside the system; this AIOC never sees it.
2. **Withdrawn.** The acting filler and the signature type `appoint-acting-filler`, which leaves every `authority_scope`; deputies of human seats (the positions table's Deputy column becomes Cover, which stays meaningful for AI positions); occupancy, handover and arrangement entries; the holders register; a compensating control for one person behind several positions. What stays: two positions are two parties; the Overseen link between positions; `succeeded_by`; the duty deputy, an AI part.
3. **The changes.** Each place below is changed in its file; its former wording is kept here, verbatim.

   - `blueprint/OER-BLUEPRINT.md`, under “Blueprint · `[ORG]AIOC-OER` · Operations Event Register · `v0.1.1`”, the one-page summary, acts not activity:
     ```text
     except that a Cell acting for a holder is recorded only for the acts that leave the holder's sphere.
     ```
   - `blueprint/OER-BLUEPRINT.md`, under “2.2 Placement”, the unit register:
     ```text
     | reads the `position` and `arrangement` entries of each unit and position | writes it, or reads an occupancy or handover entry |
     ```
   - `blueprint/OER-BLUEPRINT.md`, under “Role card”, tools and access:
     ```text
     the unit register, read only (positions and arrangements, never occupancy);
     ```
   - `blueprint/OER-BLUEPRINT.md`, under “Definition”, inbox and outbox, the handover list:
     ```text
     The handover list holds a position's open entries and commitments, ready for top management's handover entry when the occupant changes.
     ```
   - `blueprint/OER-BLUEPRINT.md`, under “Process (SOP)”, inbox and outbox, step 2:
     ```text
     build the position's handover list: its open entries and commitments, for top management's handover entry. It never reads an occupancy or handover entry (Protocol §4.10, item 17)
     ```
   - `blueprint/OER-BLUEPRINT.md`, under “13. For the `[ORG]HOAC-ACS` seat, and every decision only a human seat can take”, H-01:
     ```text
     | **Top management's own mechanism.** Arrange the Lead position (`[ORG]CELL-OERL`) and set the positions of §15 (Records Officer, data protection, internal-audit line). Nothing of who occupies them enters this blueprint | the Cell carrying `[ORG]HOAC-TM` | the position is vacant:
     ```
   - `blueprint/OER-BLUEPRINT.md`, under “Annex A. Classes of act, and the line surface by surface”, cells that act for a position:
     ```text
     **Positions that act for a holder** (a Chief of Staff, an attached assistant, a duty deputy) mirror a human position. For them the register records only the acts that leave the holder's sphere: Work Items sent, signed actions carried out, formal outgoing items. It never records the exchange between the holder and its assistant. Their measures go to the holder only.
     ```
   - `tests/TEST-OER.md`, under “A. The Library cases (TEST-OPERATIONS-EVENT-REGISTER v1)”, TEST-OER, case 12:
     ```text
     and no occupancy or handover entry is read.
     ```
   - `blueprint/OER-BLUEPRINT.md`, under “3. Positions”, the Deputy cell of the accountable position:
     ```text
     | as top management arranges (`appoint-acting-filler`, Standard §4.1, item 12) |
     ```
   - `blueprint/OER-BLUEPRINT.md`, under “3. Positions”, the positions table, the Deputy column:
     ```text
     | Position (standard title) | Purpose | Reports to | Run today by | Deputy |
     ```
   - `blueprint/OER-BLUEPRINT.md`, under “3. Positions”, the positions table, Run today by:
     ```text
     Who occupies it, and how, is top management's own mechanism; this AIOC never sees it
     ```
   - `blueprint/OER-BLUEPRINT.md`, under “3. Positions”, the positions table, the empty position:
     ```text
     While the position shows no occupant, the Chief of Staff only advises
     ```
   - `blueprint/OER-BLUEPRINT.md`, under “0. Identity and lineage”, the accountable seat:
     ```text
     Who occupies it is top management's own mechanism; this AIOC never sees it
     ```
   - `blueprint/OER-BLUEPRINT.md`, under “7. Records and where things live”, records, the link between positions and persons:
     ```text
     | The link between positions and the natural persons who occupy them | not in this AIOC: top management's own mechanism
     ```

4. **The cards** are regenerated by `tools/make_cards.py` from the blueprint.
5. **The version.** Unreleased. The blueprint keeps its version label; the version and the Library pin move at the next release, by a pull request, on the governing seat's word.

*Powered by 49GAION*
