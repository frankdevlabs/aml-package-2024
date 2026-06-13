# AMLA extracts — working rules

Before adding or editing any file in this directory, read [`_TRANSCRIPTION_GUIDE.md`](./_TRANSCRIPTION_GUIDE.md)
and follow it.

This directory holds the operative text of AMLA's **Level-2/3 draft instruments** (RTS / ITS / Guidelines) out
for consultation — the live "moving parts" of this post-adoption tracker. One file per consultation, named
`<TYPE>-<topic>-art<NN>_consultation-paper.md`. Each is the diff baseline for the eventual `_final` instrument.

The pipeline these track is indexed in [`../../docs/amla-pipeline.md`](../../docs/amla-pipeline.md); the source
PDFs are registered in [`../../sources/README.md`](../../sources/README.md) and committed under
[`../../sources/amla/`](../../sources/amla/).

Note: AMLA drafts are **clean** PDFs (no tracked changes), so plain `pdftotext` suffices — the
`pymupdf`-based drivers in the `transcribe-council-extract` skill are not needed here.
