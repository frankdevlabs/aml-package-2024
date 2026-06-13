# Transcription guide — AMLA Level-2/3 draft extracts

Internal standard for every file in `extracts/amla/`. Goal: a faithful, **diffable** record of the operative
text of each AMLA draft instrument (RTS / ITS / Guidelines) out for consultation, so that when AMLA publishes
the **final** instrument it can be added as a sibling file and `git diff` shows what changed.

## Source of truth
The committed consultation paper under [`../../sources/amla/`](../../sources/amla/), cross-checked against the
AMLA consultation page (see each file's header) and, on adoption, the final OJ text. Transcribe from the
committed PDF on disk — never from memory or a web summary.

## These are DRAFTS, not tracked-changes texts
Unlike Council compromise PDFs, AMLA consultation drafts are **clean** (no strikethrough/bold tracked changes).
So `pdftotext` is sufficient — the `transcribe-council-extract` skill's `pdf_changes.py`/`render_pdf.py`
(which need `pymupdf`, not installed on this host) are **not required** here. The CDD draft also ships a
separate "track changes from EBA draft" PDF — useful to see deltas from the EBA legacy draft, but the
authoritative consulted text is the clean consultation paper.

## What to extract
Only the **draft operative instrument** — for an RTS/ITS the "COMMISSION DELEGATED/IMPLEMENTING REGULATION"
block (recitals + articles + annexes), for Guidelines the numbered guidelines section. **Omit** the
consultation paper's background, "questions for consultation" and cost-benefit/impact-assessment annexes.

## How the shipped files were produced
Auto-extracted with `pdftotext -layout`, sliced to the operative section, and lightly cleaned (form feeds,
bare page numbers and the repeating page footer removed). They are presented inside a ```text fence to stay
faithful to the source layout. This is a **working** transcription: when refining a file, prefer converting
`Article N - Title` lines to `### Article N — Title` headings with stable `<a id="article-N"></a>` anchors so
`docs/` can deep-link, and verify article text against the PDF.

## Faithfulness rules (hard)
- Operative wording is primary legal text — never paraphrase.
- Preserve the draft's own article/recital numbering and bracketed placeholders (e.g. `…/...`, `of XXX`,
  `[OP: …]`) exactly — those are undecided in the source, not `[illegible]`.
- Mark a genuinely illegible passage `[illegible in source]` — never guess.

## Naming & cross-links
- One file per consultation: `<TYPE>-<topic>-art<NN>_consultation-paper.md`. A later final instrument →
  sibling `<TYPE>-<topic>-art<NN>_final.md`.
- Relative links only. Link the matching [`../../docs/amla-pipeline.md`](../../docs/amla-pipeline.md) row and
  the [`../../sources/README.md`](../../sources/README.md) register entry. Verify with
  `python3 ../../.claude/skills/transcribe-council-extract/linkcheck.py ../..`.
