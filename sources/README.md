# Document register

> The *rendered* table of [`data/documents.yaml`](../data/documents.yaml) — the single source of truth.
> **Edit the YAML, then mirror the table here; never edit the table alone.** The `register-document` skill does
> both. Committed source files live under `sources/<body>/` with the naming convention
> `<INSTITUTIONAL-ID>_<short-description>_<ISO-date>.<ext>`. Link the markdown extracts
> (`extracts/...md#anchor`), not PDF pages.
>
> This is a **post-adoption** tracker: the three adopted acts are link-only (EUR-Lex); the committed PDFs are
> AMLA's Level-2/3 consultation papers + SPD (the live workstream).

## Adopted acts (EUR-Lex, link-only)

| ID | Title | Date | Hosted file | Provenance |
|---|---|---|---|---|
| `REG-2024-1624` | AMLR — Regulation (EU) 2024/1624 | 2024-05-31 | link-only | [EUR-Lex ELI](https://eur-lex.europa.eu/eli/reg/2024/1624/oj/eng) · [digest](../docs/instruments/amlr-2024-1624.md) |
| `REG-2024-1620` | AMLA Regulation (EU) 2024/1620 | 2024-05-31 | link-only | [EUR-Lex ELI](https://eur-lex.europa.eu/eli/reg/2024/1620/oj/eng) · [digest](../docs/instruments/amla-2024-1620.md) |
| `DIR-2024-1640` | AMLD6 — Directive (EU) 2024/1640 | 2024-05-31 | link-only | [EUR-Lex ELI](https://eur-lex.europa.eu/eli/dir/2024/1640/oj/eng) · [digest](../docs/instruments/amld6-2024-1640.md) |
| `REG-2023-1113` | Transfer of Funds Regulation (recast) | 2023-05-31 | link-only | [EUR-Lex ELI](https://eur-lex.europa.eu/eli/reg/2023/1113/oj/eng) · [digest](../docs/instruments/tfr-2023-1113.md) |
| `REG-2025-2088` | Reg (EU) 2025/2088 — reporting-simplification omnibus (amends AMLAR, Art 7) | 2025-10-08 | link-only | [EUR-Lex ELI](https://eur-lex.europa.eu/eli/reg/2025/2088/oj) · [digest](../docs/instruments/amla-2024-1620.md#amendments-in-force) |

## AMLA — strategic programming & Level-2/3 consultation papers

| ID | Title | Date | Hosted file | Provenance |
|---|---|---|---|---|
| `AMLA-SPD-2026-2028` | Single Programming Document 2026–2028 | 2026-02-04 | `sources/amla/` | [AMLA](https://www.amla.europa.eu/amla-sets-strategic-priorities-2026-28-single-programming-document_en) |
| `AMLA-SPD-2026-2028-ANNEX-XI` | Annex XI (RTS/ITS/GL planning) | 2026-02-04 | `sources/amla/` | [AMLA](https://www.amla.europa.eu/system/files/2026-02/Annex%20XI%20to%20AMLA%20SPD%202026-2028.pdf) |
| `AMLA-ITS-SUPCOOP-ART15` | Draft ITS — supervisory-system cooperation (Art 15(3) AMLAR) | 2025-12-16 | `sources/amla/` | [consultation](https://www.amla.europa.eu/policy/public-consultations/consultation-draft-its-under-art-153-amlar_en) · [extract](../extracts/amla/ITS-supervisory-cooperation-art15-3_consultation-paper.md) |
| `AMLA-RTS-CDD-ART28` | Draft RTS — customer due diligence (Art 28(1) AMLR) | 2026-02-09 | `sources/amla/` (+ track-changes) | [consultation](https://www.amla.europa.eu/policy/public-consultations/consultation-draft-rts-customer-due-diligence_en) · [extract](../extracts/amla/RTS-cdd-art28-1_consultation-paper.md) |
| `AMLA-RTS-BIZREL-ART19` | Draft RTS — business relationships / occasional / linked (Art 19(9) AMLR) | 2026-02-09 | `sources/amla/` | [consultation](https://www.amla.europa.eu/policy/public-consultations/consultation-draft-rts-criteria-identifying-business-relationships-occasional-and-linked_en) · [extract](../extracts/amla/RTS-business-relationships-art19-9_consultation-paper.md) |
| `AMLA-RTS-SANCTIONS-ART53` | Draft RTS — pecuniary sanctions etc. (Art 53(10) AMLD6) | 2026-02-09 | `sources/amla/` | [consultation](https://www.amla.europa.eu/policy/public-consultations/consultation-draft-rts-pecuniary-sanctions-administrative-measures-and-periodic-penalty-payments_en) · [extract](../extracts/amla/RTS-pecuniary-sanctions-art53-10_consultation-paper.md) |
| `AMLA-RTS-SANCTIONS-ART53-FEEDBACK` | Consultation feedback — pecuniary-sanctions RTS (Art 53(10) AMLD6); final RTS to Commission (operative text pending) | 2026-07-09 | `sources/amla/` | [consultation](https://www.amla.europa.eu/policy/public-consultations/consultation-draft-rts-pecuniary-sanctions-administrative-measures-and-periodic-penalty-payments_en) · [PDF](amla/RTS-pecuniary-sanctions-art53-10_consultation-feedback_2026-07-09.pdf) |
| `AMLA-RTS-GROUPWIDE-ART16-17` | Draft RTS — group-wide requirements (Arts 16(4)/17(3) AMLR) | 2026-04-16 | `sources/amla/` | [consultation](https://www.amla.europa.eu/policy/public-consultations/consultation-draft-rts-group-wide-minimum-requirements-and-additional-measures-subsidiaries-and_en) · [extract](../extracts/amla/RTS-group-wide-art16-17_consultation-paper.md) |
| `AMLA-GL-BWRA-ART10` | Draft Guidelines — business-wide risk assessment (Art 10(4) AMLR) | 2026-04-16 | `sources/amla/` | [consultation](https://www.amla.europa.eu/policy/public-consultations/consultation-draft-guidelines-business-wide-risk-assessment_en) · [extract](../extracts/amla/GL-business-wide-risk-assessment-art10-4_consultation-paper.md) |
| `AMLA-GL-MONITORING-ART26` | Draft Guidelines — ongoing monitoring (Art 26(5) AMLR) | 2026-06-03 | `sources/amla/` | [consultation](https://www.amla.europa.eu/policy/public-consultations/consultation-draft-guidelines-ongoing-monitoring-business-relationship_en) · [extract](../extracts/amla/GL-ongoing-monitoring-art26-5_consultation-paper.md) |
| `AMLA-ITS-REPORTING-ART69` | Draft ITS — format for reporting suspicions & transaction records (Art 69(3) AMLR) | 2026-07-02 | `sources/amla/` | [consultation](https://www.amla.europa.eu/policy/public-consultations/consultation-draft-its-format-reporting-suspicions-and-providing-transaction-records_en) · [extract](../extracts/amla/ITS-reporting-format-art69-3_consultation-paper.md) |
| `AMLA-RTS-FIU-XBORDER-ART31` | Draft RTS — cross-border information exchange between FIUs (Art 31(3) AMLD6) | 2026-07-06 | `sources/amla/` | [consultation](https://www.amla.europa.eu/policy/public-consultations/consultation-draft-rts-cross-border-information-exchange-between-financial-intelligence-units_en) · [extract](../extracts/amla/RTS-fiu-cross-border-art31-3_consultation-paper.md) |
| `AMLA-RTS-NONFIN-RISK-ART40` | Draft RTS — inherent & residual risk profile, non-financial sector (Art 40(2) AMLD6) | 2026-07-13 | `sources/amla/` (+ data-point annexes) | [consultation](https://www.amla.europa.eu/policy/public-consultations/consultation-draft-rts-assessment-inherent-and-residual-risk-profile-obliged-entities-non-financial_en) · [extract](../extracts/amla/RTS-nonfin-risk-profile-art40-2_consultation-paper.md) |
| `AMLA-ADVISORY-MICAR` | Advisory note — ML/TF risks as the MiCAR transitional period ends | 2026-06-29 | `sources/amla/` | [AMLA](https://www.amla.europa.eu/advisory-note-money-laundering-risks-micar-transitional-period-ends_en) · [PDF](amla/AMLA-ADVISORY-MICAR_advisory-note_2026-06-29.pdf) |
| `AMLA-RTS-SANCTIONS-ART53-FINAL` | **Final report** — pecuniary-sanctions RTS (Art 53(10) AMLD6) | 2026-07-08 | `sources/amla/` | [tracker](https://www.amla.europa.eu/policy/regulatory-instruments_en) · [PDF](amla/RTS-pecuniary-sanctions-art53-10_final-report_2026-07-08.pdf) |
| `AMLA-ITS-FIU-EPPO-ART81-FINAL` | **Final report** — FIU→EPPO reporting-format ITS (Art 81(1) AMLR) | 2026-07-08 | `sources/amla/` | [tracker](https://www.amla.europa.eu/policy/regulatory-instruments_en) · [PDF](amla/ITS-fiu-eppo-reporting-art81-1_final-report_2026-07-08.pdf) |
| `AMLA-ITS-AMLA-EPPO-ART41-FINAL` | **Final report** — AMLA→EPPO reporting-format ITS (Art 41(2) AMLAR) | 2026-07-08 | `sources/amla/` | [tracker](https://www.amla.europa.eu/policy/regulatory-instruments_en) · [PDF](amla/ITS-amla-eppo-reporting-art41-2_final-report_2026-07-08.pdf) |
| `AMLA-ITS-FIU-TO-FIU-ART31-FINAL` | **Final report** — FIU-to-FIU exchange-format ITS (Art 31(2) AMLD6) | 2026-07-08 | `sources/amla/` | [tracker](https://www.amla.europa.eu/policy/regulatory-instruments_en) · [PDF](amla/ITS-fiu-to-fiu-art31-2_final-report_2026-07-08.pdf) |

## Netherlands (transposition)

| ID | Title | Date | Hosted file | Provenance |
|---|---|---|---|---|
| `NL-IWT-CONSULTATIE` | Implementatiewet (Iwt) — internet consultation | 2025-07-04 | link-only | [internetconsultatie](https://www.internetconsultatie.nl/implementatiewettervoorkomingvanwitwassenenterrorismefinanciering/b1) · [wetgevingskalender](https://wetgevingskalender.overheid.nl/Regeling/WGK027204) |
| `NL-IWT-CONSULTATIEVERSLAG` | Consultatieverslag Iwt (Min. Financiën) | 2026-05-11 | `sources/nl/` | [PDF](nl/NL-IWT-CONSULTATIEVERSLAG_consultation-report_2026-05-11.pdf) · [internetconsultatie](https://www.internetconsultatie.nl/implementatiewettervoorkomingvanwitwassenenterrorismefinanciering/b1) |
| `NL-MR-BESLUITENLIJST-2026-04-24` | Besluitenlijst ministerraad (Iwt → Raad van State) | 2026-04-24 | link-only | [open.overheid.nl](https://open.overheid.nl/documenten/16cf634e-a9e2-4411-b302-b1264198c3a5/) |
| `NL-ATR4058` | ATR4058 — "niet lastenluw" | 2025-09-29 | link-only | [open.overheid.nl](https://open.overheid.nl/documenten/497b3bd5-6966-41e3-aa7a-7fb1e8a4870a/file) |
| `NL-36228-CASHLIMIT` | Wet plan van aanpak witwassen (cash limit), dossier 36.228 | 2025-06-10 | link-only | [Eerste Kamer](https://www.eerstekamer.nl/wetsvoorstel/36228_wet_plan_van_aanpak) |
