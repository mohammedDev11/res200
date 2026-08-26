# RES200 Workspace

This directory is the durable working home for RES200. Keep project context,
research materials, datasets, reports, and implementation files here so future
work can be continued from one place.

## Structure

- `context/` — shared project context, decisions, terminology, and progress.
- `docs/` — briefs, meeting notes, and supporting documents.
- `literature/` — papers, references, and literature notes.
- `reports/weekly/` — dated weekly progress reports.
- `paper/` — iterative drafts and the final main paper.
- `datasets/` — raw, intermediate, processed, and documented data.
- `project/` — source code, analyses, experiments, and project assets.
- `outputs/` — generated charts, tables, exports, and other results.

Start with [`context/PROJECT_CONTEXT.md`](context/PROJECT_CONTEXT.md). Update it
whenever the topic, goals, requirements, or major decisions change.

## Working conventions

1. Preserve original data in `datasets/raw/`; never edit it in place.
2. Put cleaned or transformed data in `datasets/processed/`.
3. Record dataset origins and transformations in `datasets/DATA_DICTIONARY.md`.
4. Name weekly reports `YYYY-MM-DD_week-NN_topic.ext`.
5. Keep editable paper drafts in `paper/drafts/`, using versioned names such as
   `res200_paper_v001.docx`; never overwrite a submitted version.
6. Record important decisions in `context/DECISIONS.md`.
7. Keep generated files separate from source material by using `outputs/`.
