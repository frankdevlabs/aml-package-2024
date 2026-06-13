# EU AML Package Tracker — AMLR / AMLA / AMLD6

A personal, open tracker for the **EU Anti-Money Laundering Package**: the AML single rulebook (**AMLR**,
Reg (EU) 2024/1624), the EU AML Authority (**AMLA**, Reg (EU) 2024/1620) and **AMLD6** (Dir (EU) 2024/1640) —
with the live focus on AMLA's **Level-2/3 implementation pipeline** and **national transposition** (the Dutch Iwt).

> **Built from the EU legislative-tracker template**, but **repurposed for a post-adoption file.** The template
> tracks a file mid-Ordinary-Legislative-Procedure; this package is *already adopted and in force* (2024), so
> the spine here is **implementation** (AMLA RTS/ITS/Guidelines + transposition), not co-legislator
> negotiation. Identity is set in [`tracker.yaml`](tracker.yaml).

> **Scope.** This repo tracks the **adopted AML Package** (AMLR 2024/1624 · AMLA 2024/1620 · AMLD6 2024/1640).
> "AMLD6" here = **Directive (EU) 2024/1640** — **not** the criminal-law Directive (EU) 2018/1673 (also
> informally "6AMLD"). See [`tracker.yaml`](tracker.yaml) (`file_id` vs `keep_apart`).

**Current status (high level):** see the full snapshot in **[`STATUS.md`](STATUS.md)**.

---

## How this repo is organised

Three layers, so links stay stable over time:

| Layer | Folder | What it is | Mutable? |
|---|---|---|---|
| **Primary sources** | [`sources/`](sources/) | Register of every official document; the adopted acts are link-only (EUR-Lex), AMLA's consultation papers + SPD are committed under [`sources/amla/`](sources/amla/) | append-only |
| **Operative-text extracts** | [`extracts/`](extracts/) | Diffable plain-text of the live **draft** Level-2/3 instruments out for AMLA consultation ([`extracts/amla/`](extracts/amla/)) — the moving parts; diff baseline for the eventual final RTS | versioned |
| **Analysis** | [`docs/`](docs/) | The human-readable analysis that links *to* the layers above | living |

### Navigation

- **[`STATUS.md`](STATUS.md)** — where the package stands right now (one screen).
- **[`TIMELINE.md`](TIMELINE.md)** — full chronology, every entry linked to a source.
- **[`docs/summary.md`](docs/summary.md)** — the plain-language summary.
- **[`docs/amla-pipeline.md`](docs/amla-pipeline.md)** — the live spine: AMLA's Level-2/3 consultation pipeline.
- **[`docs/netherlands.md`](docs/netherlands.md)** — national transposition (the Iwt, cash limit, UBO, "lastenluw").
- **[`docs/instruments/`](docs/instruments/)** — digest per instrument (AMLR, AMLA, AMLD6, TFR, repealed AMLD4).
- **[`docs/provisions/`](docs/provisions/)** — one file per tracked substantive change.
- **[`docs/what-changed.md`](docs/what-changed.md)** — full provision-by-provision diff (Wwft/AMLD4 → AML Package).
- **[`docs/institutional-positions.md`](docs/institutional-positions.md)** — the implementation actors.
- **[`docs/fault-lines.md`](docs/fault-lines.md)** / **[`docs/stakeholders.md`](docs/stakeholders.md)** — contested issues / industry positions.
- **[`sources/README.md`](sources/README.md)** — the document register.
- **[`extracts/amla/`](extracts/amla/)** — operative text of the draft RTS/ITS/Guidelines.

---

## Linking conventions

1. **Relative links only** inside the repo (survive renames/forks/mirrors).
2. **Deep-link into extracts, not PDFs** — GitHub's PDF viewer has no reliable `#page=` anchors; link the
   markdown extract instead (e.g. `extracts/amla/RTS-cdd-art28-1_consultation-paper.md`).
3. **Source PDFs are committed in [`sources/amla/`](sources/amla/)** for offline reference and diffing; the
   register records the authoritative URL. The adopted acts themselves are link-only (EUR-Lex ELI).

## Naming convention for documents

`<INSTITUTIONAL-ID>_<short-description>_<ISO-date>.<ext>` — stable id first, ISO date last (e.g.
`RTS-CDD-art28-1_consultation-paper_2026-02-09.pdf`).

## Adding a document

Run the `register-document` skill (it appends to [`data/documents.yaml`](data/documents.yaml) and re-renders
[`sources/README.md`](sources/README.md)); a new AMLA draft instrument gets a matching extract under
[`extracts/amla/`](extracts/amla/) (see its [`_TRANSCRIPTION_GUIDE.md`](extracts/amla/_TRANSCRIPTION_GUIDE.md)).

## Disclaimer & licence

A **personal project**, published in a personal capacity. **Not legal advice**; not any employer's view —
see **[`DISCLAIMER.md`](DISCLAIMER.md)**. Original analysis is **CC BY 4.0** ([`LICENSE`](LICENSE)); EU
documents and third-party works are **not** ([`NOTICE`](NOTICE)).
