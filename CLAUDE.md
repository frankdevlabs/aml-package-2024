# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

> **Built from the EU legislative-tracker template.** The file this repo follows is defined once in
> [`tracker.yaml`](tracker.yaml); the `<PLACEHOLDER>` tokens below are filled from it by
> `python3 bootstrap.py`. Starting a fresh file? Read `SETUP.md` first.

## What this repo is

A personal, open **legislative tracker** — not a software project. It follows the adopted **EU AML Package**:
**AMLR** (Reg (EU) 2024/1624), **AMLA** (Reg (EU) 2024/1620) and **AMLD6** (Dir (EU) 2024/1640) — the AML
single rulebook, the EU AML Authority, and the directive Member States transpose. (Identity: [`tracker.yaml`](tracker.yaml).)

**This is a POST-ADOPTION tracker.** The package is already adopted and in force (2024); the Ordinary
Legislative Procedure is concluded. So this repo's spine is **implementation**, not co-legislator negotiation:
(1) AMLA's **Level-2/3 pipeline** (draft RTS/ITS/Guidelines out for consultation — the live moving parts, in
[`docs/amla-pipeline.md`](docs/amla-pipeline.md) and [`extracts/amla/`](extracts/amla/)), and (2) **national
transposition** ([`docs/netherlands.md`](docs/netherlands.md)). The template's OLP framing (Council compromise
texts, `extracts/council/`, trilogue) does **not** apply here — it has been repurposed.

**Scope guard:** "AMLD6" here = **Directive (EU) 2024/1640**. It is *not* `Directive (EU) 2018/1673` (the
criminal-law "6AMLD"). Keep them apart. Authoritative scope: [`tracker.yaml`](tracker.yaml) (`file_id` vs `keep_apart`).

There is no build, no app, no test suite. The "code" is Markdown + YAML + three Python skill drivers.

## Three-layer architecture (the big picture)

The repo deliberately separates three layers so links stay stable as the file evolves:

| Layer | Folder | What it is | Mutability |
|---|---|---|---|
| **Primary sources** | `sources/` | Register of every official document; PDFs/DOCX committed (incl. LIMITE — see `NOTICE` §2) | append-only |
| **Operative-text extracts** | `extracts/` | Diffable plain-text transcriptions of the operative articles, one set per version | versioned |
| **Analysis** | `docs/` | Human-readable analysis linking *down* into the two layers above | living |

`extracts/amla/` holds one file **per AMLA draft Level-2/3 instrument** out for consultation
(`<TYPE>-<topic>-art<NN>_consultation-paper.md`) — the diffable operative text. When AMLA publishes a
**final** instrument, add it as a sibling (`..._final.md`) so `git diff` against the consulted draft is
meaningful. The slices are listed in [`tracker.yaml`](tracker.yaml) (`extract_slices`). AMLA drafts are
**clean** PDFs (no tracked changes), so plain `pdftotext` suffices.

## Single sources of truth (don't hand-edit downstream copies)

- **`data/documents.yaml`** is the canonical document register. `sources/README.md` is its *rendered*
  table — edit the YAML, then update the table to match. Never edit the table alone.
- **`data/tracker-state.yaml`** is **auto-maintained by the daily tracker routine** (a scheduled remote
  agent that hashes watched source pages T1-*/T2-*/T3-*). The header says "Do not edit by hand" — respect it.
- **`data/positions.csv`** backs the institutional/provision comparison; keep it in sync with the
  `docs/provisions/*` and `docs/institutional-positions.md` prose.
- **`STATUS.md`** is the one-screen current snapshot (format spec: `docs/reporting-standard.md`);
  **`TIMELINE.md`** is the full sourced chronology. `STATUS.md`'s "What changed" table (headline subset) and
  its full counterpart **`docs/what-changed.md`** (every tracked provision, deep-linked to the operative
  extracts) are the authority on what moved vs earlier reporting — consult them before asserting a feature
  of the proposal (features are routinely deleted/moved between compromise versions).

## Adding an AMLA draft instrument (the core workflow)

When AMLA opens a new consultation (or publishes a final instrument), add it under `extracts/amla/`. Read
[`extracts/amla/_TRANSCRIPTION_GUIDE.md`](extracts/amla/_TRANSCRIPTION_GUIDE.md) first.

Unlike Council compromise PDFs, AMLA consultation drafts are **clean** (no strikethrough/bold tracked
changes), so plain `pdftotext` is sufficient — the `transcribe-council-extract` skill's `pdf_changes.py` /
`render_pdf.py` drivers (which need `pymupdf`, **not installed on this host** — no pip) are not required.

Steps:

```bash
# 1. Download the consultation paper PDF into sources/amla/ (naming: <TYPE>-<topic>-art<NN>_consultation-paper_<ISO>.pdf)
# 2. Extract the operative draft instrument (the "COMMISSION DELEGATED/IMPLEMENTING REGULATION" block for an
#    RTS/ITS, or the numbered Guidelines section), omitting background/questions/cost-benefit annexes:
pdftotext -layout "sources/amla/<file>.pdf" /tmp/x.txt
# 3. Write extracts/amla/<TYPE>-<topic>-art<NN>_consultation-paper.md (header + operative text). Register it
#    in data/documents.yaml + sources/README.md, add a row to docs/amla-pipeline.md and data/positions.csv.
# 4. Internal link + #anchor check (must end "0 broken") — mirrors the lychee CI
python3 .claude/skills/transcribe-council-extract/linkcheck.py .
```

Preserve the draft's **own** article/recital numbering and bracketed placeholders (`…/...`, `of XXX`,
`[OP: …]`); mark illegible passages `[illegible in source]`. A later **final** instrument → sibling
`..._final.md` so `git diff` against the consulted draft is meaningful.

## Conventions

- **Relative links only** inside the repo — never `github.com/...` absolute URLs (they break on rename/fork/mirror).
- **Deep-link into `extracts/*.md#anchor`, not `sources/*.pdf#page`** — GitHub's PDF viewer can't anchor to a page.
- **Document naming:** `<INSTITUTIONAL-ID>_<short-description>_<ISO-date>.<ext>` — stable id first, ISO
  date last, so chronological sort works (e.g. `RTS-CDD-art28-1_consultation-paper_2026-02-09.pdf`).
- **Link checking (CI):** `lychee` runs on push/PR/weekly via `.github/workflows/link-check.yml`, configured
  by `lychee.toml`. Internal links are checked strictly; some external hosts (consilium register, EUR-Lex,
  Oeil, LinkedIn) are excluded because they bot-block or 404 for unreleased LIMITE docs.

## Disclaimer

Personal project, **not legal advice**, not any employer's view (`DISCLAIMER.md`). Original commentary is
CC BY 4.0 (`LICENSE`); EU documents and third-party works are not (`NOTICE`). Extracts are working
transcriptions — verify against the authoritative source before relying on them.
