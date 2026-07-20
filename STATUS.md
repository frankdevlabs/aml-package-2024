# Status snapshot — EU AML Package (AMLR / AMLA / AMLD6)

| Field | Value |
|---|---|
| **Instruments** | **AMLR** (Reg (EU) [2024/1624](https://eur-lex.europa.eu/eli/reg/2024/1624/oj/eng)) · **AMLA** (Reg (EU) [2024/1620](https://eur-lex.europa.eu/eli/reg/2024/1620/oj/eng)) · **AMLD6** (Dir (EU) [2024/1640](https://eur-lex.europa.eu/eli/dir/2024/1640/oj/eng)) — see [digests](docs/instruments/) |
| **Status** | **Adopted and in force.** OLP concluded May 2024 (OJ L, 19.6.2024). Not a pending file. |
| **Legal basis** | Article 114 TFEU (all three) |
| **Applies / transposes from** | **10 July 2027** (AMLR + AMLD6 general date); AMLR football sub-set from **10 July 2029**. **AMLA operational since 1 July 2025** (Frankfurt). |
| **Latest live workstream** | AMLA **Level-2/3 pipeline** — first-wave draft RTS consultations closed; finals due to the Commission **10 July 2026**. See [AMLA pipeline](docs/amla-pipeline.md). |
| **As of** | **17 July 2026** (= `data/tracker-state.yaml` `last_run`) |

> Living snapshot — **not legal advice** ([`DISCLAIMER.md`](DISCLAIMER.md)). The three instruments are sourced
> from [`docs/instruments/`](docs/instruments/) + EUR-Lex; the live implementation workstream from AMLA's
> [consultations hub](https://www.amla.europa.eu/policy/public-consultations_en) (mirrored in
> [`docs/amla-pipeline.md`](docs/amla-pipeline.md)) and NL transposition ([`docs/netherlands.md`](docs/netherlands.md)).
> Forward-looking dates (e.g. "final RTS by 10 Jul 2026", "direct supervision from 2028") are AMLA targets, not
> completed events — verify before relying on them.

## One-line status

The AML Package is **adopted and in force**: AMLR and AMLD6 apply/transpose from **10 July 2027** and AMLA has
been operational in Frankfurt since **1 July 2025**. The live action is no longer the legislature but **AMLA's
Level-2/3 single-rulebook pipeline** — the first three draft RTS consultations have closed and finals are due to
the Commission by **10 July 2026**, with three further consultations (group-wide RTS, business-wide risk
assessment GL, ongoing-monitoring GL) open or just closed — plus **national transposition**, where the Dutch
Iwt sits at the Raad van State for advice (no Tweede Kamer dossier yet).

## Where each institution stands

<!-- POST-ADOPTION: the OLP co-legislators (Council, Parliament) concluded their role on adoption in May 2024.
     The live actors are the Commission (Level-2 delegated acts), AMLA (the implementation engine) and the
     Member States (transposition). The five-field skeleton is kept for cross-tracker comparison. -->

### European Commission — Level-2 / delegated-act adopter
- **Stage:** Awaiting AMLA's draft RTS/ITS; will adopt them as delegated/implementing acts.
- **Latest act:** No package delegated regulation adopted yet — first-wave drafts arrive from AMLA by 10 Jul 2026.
- **Owner:** DG FISMA.
- **Position:** Endorses the single-rulebook architecture; may set a lower UBO threshold (15% or below) for high-risk sectors under Art 52 AMLR.
- **Next:** Adopt the first delegated regulations (CDD, business-relationship triggers, pecuniary sanctions) after AMLA submission; publication in the OJ is the benchmark that changes status. — [pipeline](docs/amla-pipeline.md)

### AMLA — Authority for Anti-Money Laundering (the implementation engine)
- **Stage:** Operational since 1 Jul 2025; building the single rulebook (Level-2/3) and preparing direct supervision.
- **Latest act:** First-wave RTS consultations closed (CDD + business relationships 8 May 2026; pecuniary sanctions 9 Mar 2026); group-wide RTS closed 15 Jun 2026; BWRA + ongoing-monitoring guidelines open. On **8–9 Jul 2026** AMLA **finalised the first-wave enforcement RTS** (pecuniary sanctions, Art 53(10) AMLD6): a press release announcing a **common EU approach to enforcing AML rules** (four-step methodology, four gravity levels), the consultation feedback (9 Jul), and the **final report** — the final RTS goes to the Commission; its operative text (Commission Delegated Regulation) is not yet published. Also on **8 Jul 2026** the regulatory-instruments tracker moved **six mandates to "Final report published"** — the pecuniary-sanctions RTS plus the EPPO-reporting ITS (Art 81(1) AMLR / 41(2) AMLAR), FIU-to-FIU ITS (Art 31(2) AMLD6) and the two end-2025 RTS (risk profile Art 40(2), selection Art 12(7)) — and **two new consultations opened** (reporting-format ITS Art 69(3) AMLR; FIU cross-border-exchange RTS Art 31(3) AMLD6). AMLA **concluded the ongoing-monitoring guidelines public hearing** (Art 26(5) AMLR) on **2 Jul 2026**. AMLA also held its **first conference** (9 Jun 2026, Frankfurt) and published **direct-supervision eligibility-reporting webinar** materials (10 Jun 2026), and an **advisory note on ML/TF risks as the MiCAR transitional period ends** (29 Jun 2026; no blanket de-risking of transferring CASP customers). On **1 Jul 2026** AMLA and the **EDPB** announced a joint Level-3 workstream — **Guidelines on information-sharing partnerships** (Art 75 AMLR; consultation expected H1 2027). — [pipeline](docs/amla-pipeline.md) · [consultations hub](https://www.amla.europa.eu/policy/public-consultations_en)
- **Owner:** Chair **Bruna Szego**; Executive Director **Nicolas Vasse**; Frankfurt (MesseTurm).
- **Position:** Deliver 24 of 40 mandates in 2026 (financial sector first, then non-financial); ~430 staff "cruising capacity" by end-2027.
- **Next:** Submit first-wave final draft RTS to the Commission by **10 Jul 2026**; select ~40 high-risk entities for direct supervision during 2027; direct supervision from **2028**. — [AMLA digest](docs/instruments/amla-2024-1620.md)

### Co-legislators (Council & Parliament) — concluded
- **Stage:** OLP concluded. AMLR/AMLA/AMLD6 adopted 31 May 2024, published OJ L 19.6.2024. No further co-legislator role on the basic acts.

### Advisory bodies & Member States

| Body | Latest act (date) | Position |
|---|---|---|
| **EBA** | AML/CFT mandates & functions transferred to AMLA (end-Dec 2025 / Jan 2026) | Legacy EBA AML guidelines remain valid until replaced (Art 54(5) AMLAR) |
| **Netherlands** | Iwt at the Raad van State for advice (adviesaanvraag aanhangig 7 May 2026; advice not yet issued); cash limit €3,000 for goods in force 1 Jan 2026 | Transposing via the **Iwt** (replaces the Wwft 10 Jul 2027); "lastenluw" intent contested by ATR — [`docs/netherlands.md`](docs/netherlands.md) |

## Next milestones to watch

- [ ] **10 July 2026** — AMLA submits first-wave final draft RTS (CDD Art 28(1), business relationships Art 19(9), pecuniary sanctions Art 53(10) AMLD6) to the Commission. *Pecuniary-sanctions RTS finalised 8–9 Jul 2026 (press release + consultation feedback).*
- [ ] **Pecuniary-sanctions RTS (Art 53(10) AMLD6) — final operative text pending.** AMLA finalised it (8–9 Jul 2026) but the Commission Delegated Regulation is not yet published; when it appears in the OJ, build `extracts/amla/RTS-pecuniary-sanctions-art53-10_final.md` against the consulted draft and clear `pending_operative_text`. — [pipeline](docs/amla-pipeline.md)
- [ ] Commission adopts the first AML **Delegated Regulation(s)** and publishes in the OJ (benchmark: any final RTS appears as a Commission Delegated Regulation).
- [ ] **Final draft to Commission by 30 Sep 2026** — group-wide requirements RTS (Arts 16(4)/17(3) AMLR).
- [ ] **Q4 2026** — final business-wide risk assessment guidelines (Art 10(4) AMLR).
- [ ] **3 September 2026** — ongoing-monitoring guidelines consultation closes.
- [ ] **H1 2027** — AMLA/EDPB public consultation on the **information-sharing-partnerships joint Guidelines** (Art 75 AMLR); stakeholder event expected later in 2026.
- [ ] **NL Iwt** — Raad van State advice, then submission to the Tweede Kamer (a Kamerstuk **36XXX** number appears on submission). *Verify against the institution — wetgevingskalender blocks automated access.*
- [ ] **NL implementatiebesluit** — secondary legislation under the Iwt, to be consulted separately.
- [ ] Re-verify the [AMLA consultations hub](https://www.amla.europa.eu/policy/public-consultations_en) at least monthly (11 consultations were planned for Q2 2026 alone).
- [ ] **Transcribe the retrieved final reports / consultation drafts** into `extracts/amla/`. On **19 Jul 2026** the four new-to-final final reports — **pecuniary-sanctions RTS** (Art 53(10) AMLD6), **EPPO-reporting ITS** (Art 81(1) AMLR / 41(2) AMLAR), **FIU-to-FIU ITS** (Art 31(2) AMLD6) — and the two new consultation papers (ITS Art 69(3) AMLR; RTS Art 31(3) AMLD6) were retrieved and [registered](sources/README.md); the `..._final.md` / `..._consultation-paper.md` extract siblings are still to be written. The **Home-Host RTS** (Art 46(4) AMLD6) remains **Consultation closed** with no text published — register + transcribe once a PDF surfaces. — [pipeline](docs/amla-pipeline.md#additional-index-listed-instruments-regulatory-instruments-tracker-not-on-the-consultations-hub)
- [ ] **Transcribe two new consultations opened early Jul 2026** — reporting-format ITS (Art 69(3) AMLR, closes **20 Sep 2026**) and FIU cross-border-exchange RTS (Art 31(3) AMLD6, closes **6 Oct 2026**): download the draft PDFs, register + add `extracts/amla/` slices. — [pipeline](docs/amla-pipeline.md)
- [ ] **2027** — AMLA selects ~40 high-risk financial groups for direct supervision; **2028** — direct supervision begins.
- [ ] **10 July 2029** — AMLR football-agents/clubs sub-set applies; AMLD6 Article 18 deadline.

## What changed: from the Wwft/AMLD4 regime to the AML Package

<!-- The myth-buster for a compliance audience: the operational shifts from the current (AMLD4/Wwft) regime to
     the adopted AMLR. "Latest text" = the adopted AMLR/AMLD6, not a Council compromise. Full table:
     docs/what-changed.md; provision detail: data/positions.csv + docs/provisions/. -->

Each row traces a provision **current law (AMLD4 / Wwft) → adopted AML Package (in force; applies 10 Jul 2027)**.
Headline subset only; the full table is in [`docs/what-changed.md`](docs/what-changed.md). Positions:
[`data/positions.csv`](data/positions.csv).

| Provision | Current law (AMLD4 / NL Wwft) | Adopted AML Package |
|---|---|---|
| [**Single rulebook**](docs/provisions/cdd-harmonisation.md) | Directive (AMLD4) transposed into the Wwft; national divergence | **AMLR directly applicable**; most of the Wwft revoked 10 Jul 2027 |
| [**UBO threshold**](docs/provisions/ubo-threshold.md) | "**more than 25%**" | "**25% or more**" (Art 52 AMLR); Commission may set 15% (or lower) for high-risk sectors |
| [**Cash limit**](docs/provisions/cash-limit.md) | No EU-wide cap | EU cap **€10,000**; NL applies **€3,000** (goods since 1 Jan 2026; services from 10 Jul 2027) |
| [**Obliged-entity scope**](docs/provisions/scope-expansion-casps.md) | Limited | + all CASPs, crowdfunding, certain credit intermediaries, football clubs/agents, high-value goods dealers; **virtual IBANs** in scope |
| [**Reporting trigger (NL)**](docs/provisions/reporting-suspicious.md) | "ongebruikelijke" (unusual) transactions | shift toward "verdachte" (suspicious); FIU 5-working-day deadline; FIU-NL broader powers |
| [**Supervision**](docs/provisions/amla-direct-supervision.md) | National supervisors only | **AMLA direct supervision** of ~40 high-risk groups (selected 2027, supervised from 2028) |

**Full diff** (every provision, deep-linked to the operative text): [`docs/what-changed.md`](docs/what-changed.md).
