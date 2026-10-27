# Mentor Review Round (example)

> What Claude produced when the first round of mentor comments arrived, following [`review-instructions.md`](../system/review-instructions.md). Wording is generalized and report content is removed.

## Step 1: Mistake register

A flat list of every mentor comment, kept in the mentor's own wording. **19 entries** in this round, ranging from cosmetic to structural. The kinds of issues:

- **Consistency:** the same date or figure stated differently in two places.
- **Formatting:** font size not consistent across tables and sections.
- **Missing content:** a table without the metrics it should carry; a table with no commentary below it.
- **Sourcing:** a table built from the wrong type of source, to be re-created from the right one.
- **Unclear method:** a ratio shown without the inputs needed to derive it.
- **Wrong numbers:** figures that didn't match the filings, flowing into the narrative and a chart.
- **Quality:** one section flagged as "all AI generated content," to be reworked from a specific source.

## Step 2: Fix plan

The 19 mistakes became 13 actions, **ordered from most invasive to most cosmetic**, each linked to the mistakes it resolves.

| Order | Type of action | Example |
|---|---|---|
| Top | Rebuild a section from a new source | Rework a section from a named source, with a chart |
| | Re-extract numbers and update everything downstream | Workbook → narrative → chart |
| Middle | Add missing content | Commentary block, metrics block |
| | Reconcile labels across the report | Sweep every place a label appears |
| Bottom | Formatting and dates | Font size, date alignment |

## Step 3: Stop

Claude does not touch the report until I review both files and give the go-ahead.

## Step 4: Verification

After the fixes, I ran the verification layers. For example, the TOC (table of contents) audit, layer 2, logged about 25 open findings, such as missing sub-section headings and content in the wrong place. Each line stays in the open-issue file until Claude confirms the fix in the actual report.
