# CLAUDE.md: Credit Initiation Report

> Sanitized version of the project file Claude read at the start of every session.
> Issuer, firm and file names are generalized.

## Purpose

Manages all work for an end-to-end Credit Initiation Report (CIR) on one issuer. Two parts:
(1) data extraction into Excel; (2) report writing based on that data plus industry metrics,
the credit scorecard methodology, mentor instructions and house style.

## Tree

```
project/
├── CLAUDE.md
├── Lessons shown after manual editing.docx   # my manual-edit notes; standing rules
├── context/
│   ├── Color_Typography_Reference.docx       # brand colors + typography
│   ├── Mentor_Rules.docx                     # mentor rules, must follow
│   ├── CIR_Standard_TOC.pdf                  # exact TOC (table of contents), check every section against it
│   ├── Industry_Specific_Metrics.xlsx        # per-industry metrics
│   ├── Benchmark_Reports/                    # mentor-approved past reports
│   ├── Scorecard_Methodology/                # credit scorecard formula, by sector
│   ├── Reference_Report.docx                 # style reference only, NOT a data source
│   ├── Workflow.docx                         # step-by-step workflow
│   ├── Format_References/                    # table formats for snapshot and peer tables
│   ├── Learnings.docx                        # log of mistakes/process, read at session start
│   └── Pending_Requirements_From_User.md     # blocked items log
├── data/
│   ├── annual reports/                       # issuer 10-Ks, 5 years
│   ├── quarterly reports/                    # issuer 10-Qs (filenames mislabelled; verify cover page)
│   ├── competitors annual and quarterly reports/
│   ├── credit agreements/
│   └── rating agency reports
└── drafts/
    ├── Issuer_Data_Extraction.xlsx           # source of truth for all financials
    ├── Issuer_Key_Financial_Snapshot.xlsx
    ├── Issuer_Financial_Credit_Analysis.xlsx
    ├── Issuer_Peer_Comparison.xlsx
    ├── Issuer_Re_Rating_Parameters.xlsx
    ├── Issuer_Scorecard_Supporting_Data.xlsx
    ├── Issuer_Capital_Structure_Covenant_Analysis.xlsx
    ├── Issuer_<Section>.docx                 # one Word file per report section
    ├── Issuer_CIR.docx                       # assembled master report
    └── errors by ai fund manager.md          # AI fund-manager review notes
```

## Rules

- Read the entire `context/` folder once at the start of the project.
- Project flow: (1) data extraction, (2) report sections + appendices, (3) investment thesis,
  (4) credit outlook. Follow `context/Workflow.docx` step by step.
- After finishing each task/section, check with me before moving on.
- If a step is blocked on user input, log it in `context/Pending_Requirements_From_User.md`
  and move on; use the item once supplied and log the resolution in Learnings.
- Save all drafts to `drafts/`, named descriptively by progress.
- Never modify files in `context/` or this `CLAUDE.md` without my approval.
- Always check `context/` and the root folder for newly added files; ask me before using.
- Update the Tree section above when files are created or discovered.
- Conventions (FY labeling, capex formula, live-formula requirement) live in
  `context/Learnings.docx`, not here. Read it at session start.
- If I edit a draft file myself after you deliver it, my saved version is the new source of
  truth. Build your next edits on top of it, don't regenerate and silently overwrite.
- CURRENT LATEST-PERIOD CONVENTION: the issuer's latest 10-K is the latest annual period; the
  latest quarter is derived as full-year totals minus the 9-month year-to-date. All workbooks
  and the report use the issuer's own filing FY labels. Peer comparison is on a
  latest-annual-per-company basis, not LTM.
- Keep this file under 100 lines.

## Note-taking

- After each task, log corrections/mistakes/patterns to `context/Learnings.docx`: one dated,
  one-sentence bullet per entry, most recent first within its section.
- Read `context/Learnings.docx` at session start.
- 3+ related notes on one topic → split into a focused `context/` file, leave a pointer in
  Learnings.docx, update the Tree.
