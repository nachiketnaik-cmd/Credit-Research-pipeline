# Learnings Log (excerpt)

> Claude kept this log during the project and read it at the start of every session: one dated line per correction, most recent first. About 60 entries in total; a selection is shown here, generalized to remove report content.

## Conventions (apply every time, no need to re-derive)

- **Aug 31:** The latest standalone quarter is derived as full-year totals minus the 9-month YTD. All workbooks and the report use the issuer's own filing labels.
- **Aug 24:** LTM = sum of the four most recent fiscal quarters for flow items, with balance-sheet items as of the latest quarter-end. Applied across every workbook and cross-checked so they agree exactly.
- **Aug 24:** No em dashes in any draft. Paired dashes become commas; a dash before a clause becomes a colon.
- **Aug 22:** Capex and FCF each have one fixed definition, written down and used everywhere.
- **Aug 22:** Never write "n.m." in a table. Show the real computed value.
- **Aug 22:** The extraction workbook is the verified source of truth. Raise any discrepancy with me; never resolve it alone.
- **Aug 22:** Every derived Excel cell is a live formula. If I edit a delivered draft, my file becomes the new source of truth.

## Mistakes made and the correct process

- **Aug 31:** *Self-caught.* A new workbook computed FCF as `CFO − capex`, but capex is stored as a negative number, so capex was being added. Correct: `CFO + capex_signed`.
- **Aug 25:** Cited the wrong note number in a footnote. **Verify note numbers against the filing itself,** not memory or an earlier draft.
- **Aug 25:** Claimed a metric was "not disclosed." An independent re-extraction found it disclosed every period. **Verify every "not disclosed" claim against the filing text.**
- **Aug 24:** Asserted "no change" on an item from a headline row alone, missing a footnote that disclosed the change. **Read the footnotes, not just the headline row.**
- **Aug 24:** After a method fix in the workbooks, stale figures were still in four Word sections. **A project-wide change needs a full search across every draft.**
- **Aug 24:** Used a one-off shortcut for one calculation instead of the project's standard method. **Apply the established method consistently; don't reason out special cases.**
- **Aug 24:** A bulk em-dash replacement also hit formula cells and broke `IFERROR(...,"—")` placeholders. Fixed by separating prose from placeholders and re-running on the original files.
- **Aug 24:** Left peer data as "n.a." Fixed by extracting it from each peer's own filings (pdftotext for PDFs, pandas for inline-XBRL HTML).
- **Aug 22:** openpyxl strips cached formula values on save, and a LibreOffice recalc resets column widths. Order: recalculate and verify first, then apply formatting last.
- **Aug 21:** Sign-convention bug: peer lines stored with the filing's sign, silently producing wrong net income. **Reconcile every built-up figure to the company's own reported total.**
- **Aug 21:** Capex took two wrong guesses before the right formula was confirmed. **When I flag a number as wrong, ask which interpretation I mean, quoting the source figures, before recalculating everything.**
- **Aug 21:** Pasted pre-computed Python values into Excel. **Every derived cell must be a live formula.**

## General process

- **Aug 31:** For a report-wide sweep, first build a change inventory: each old snippet quoted next to its replacement, grouped by type. Self-check the inventory against the source data, then get approval before editing. The self-check alone caught four errors.
- **Aug 25:** Used two parallel subagents to independently re-extract inputs from the filings with citations. This surfaced two real gaps the main session had missed.
- **Aug 22:** Data gaps that only I can fill are logged in the pending-requirements file, and work continues on the next step. Unavailable figures are flagged, never invented.
- **Aug 21:** Before relabeling anything with financial impact, quote the figures from the filing back to me. When two readings of an instruction give very different numbers, stop and ask with a concrete example.
