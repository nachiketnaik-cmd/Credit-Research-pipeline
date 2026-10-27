> Used as-is during the project. Only the firm name was removed.

# Instructions for AI — Mentor Corrections Folder

> **This file is portable.** Drop it into any folder where mentor comments are being processed. It does not depend on any specific project path.

---

## What this folder is

This folder holds mentor feedback on a report I have already submitted. Inside it you will find one or more of the following:
- Marked-up copies of the report (Word, PDF, screenshots).
- Standalone comment files (text, email dumps, voice-note transcripts).
- Sometimes both, sometimes a mix.

Mentor comments are **the single most important input in this folder.** They tell us:
- Exactly where a change is needed.
- What the change should be.
- Sometimes why (tone, sourcing, ratio choice, formatting standard).

Comments range from trivial (fix a typo, right-align a column, change a heading level) to heavy (swap out a ratio family across the whole report, re-pull a peer set, restructure a section). Do not judge by length. A one-line comment can trigger a report-wide sweep.

---

## What you must do the moment you enter this folder

Run this sequence in order. Do not skip and do not reorder.

### Step 1 — Read every file in this folder end to end
- Every mentor-marked document. Every comment file. Every screenshot caption.
- If there are two versions (round 1 and round 2), read **both**. Round 2 comments often reference or override round 1.
- Read cover to cover before writing anything. Do not start extracting mid-read.

### Step 2 — Create `mistakes mentor found.md` in this same folder
- A flat, numbered list of every distinct mistake the mentor flagged.
- One line per mistake. Include:
  - The section / page / table / figure it applies to.
  - The exact mistake in the mentor's own words (or a faithful paraphrase if the wording is long).
  - The round it came from (`R1` or `R2`) if both rounds exist.
- If only one round exists, just list those.
- Do not deduplicate across rounds by silently dropping the R1 version. If R2 restates or extends an R1 point, list both and note the linkage (`R2 extends #4`).
- Do not add commentary, fixes, or opinions. This file is a **register**, nothing else.

### Step 3 — Create `steps to take.md` in this same folder
- Ordered list of the actions I need to take to address every item in `mistakes mentor found.md`.
- **Ordering: hardest / most invasive at the top, easiest / most cosmetic at the bottom.**
  - Hardest = anything that ripples across multiple sections, changes a number set, forces re-extraction from filings, or reshapes an argument.
  - Middle = single-section rewrites, table restructures, adding or removing a chart.
  - Easiest = format tweaks, alignment, font, typo, heading level, source-line wording.
- For each step, write:
  - A one-line action.
  - Which files / sections / drafts it touches.
  - Which mistake numbers from `mistakes mentor found.md` it resolves (e.g. `resolves #3, #7, #12`).
- Keep it action-oriented. Verbs first. No prose paragraphs.

### Step 4 — Stop
- Do **not** start making any changes to the report.
- Do **not** touch anything outside this folder.
- Wait for me to review both files and hand you the go-ahead instruction. I will write the actual "now do X" prompt myself.

---

## Rules while you work in this folder

- **Do not invent mistakes.** If the mentor did not flag it, it does not go into `mistakes mentor found.md`. That file is a mentor-only register.
- **However, if you personally spot an error** (a wrong number, a broken source, a formatting inconsistency, a contradiction between sections, anything the mentor missed), **surface it to me in chat** — do not silently fix it, do not add it to the register, do not bury it in `steps to take.md`. Just tell me: what you found, where, and why you think it is wrong. I decide whether it becomes a step.
- **Do not soften or reinterpret mentor wording.** Their phrasing is the source of truth. If they said "this is wrong," write "this is wrong," not "this could be improved."
- **Do not merge distinct mistakes into one line.** Two comments on the same table are two entries.
- **Preserve mentor files as-is.** Read them, quote from them, but do not edit or "clean up" the source comment files.
- **If a comment is ambiguous,** list it verbatim in `mistakes mentor found.md` and add a bracketed `[AMBIGUOUS — needs user clarification]` tag. Put its step at the top of `steps to take.md` with `BLOCKED — clarify before starting`.
- **Follow the project's standing writing rules** (no em dashes, USD millions, sourcing discipline, brand palette, Arial 9, etc.) when you eventually make the changes — but that comes later, not in this folder.

---

## Verification layers (mandatory reading)

Once the changes are underway, verification does **not** happen in one pass. There are **three distinct verification layers** in this folder, defined in full in `verification.md`. Read `verification.md` before running any of them. Short version:

- **Layer 1 — Mentor-comment compliance.** Did every mistake in `mistakes mentor found.md` actually get fixed in the report?
- **Layer 2 — TOC + past-report benchmarking.** Does the report match the official TOC (highest weight) and hold up against previously-passed reports?
- **Layer 3 — Fund manager / professional read.** A brutally critical cover-to-cover read as if a bond fund manager just opened it. Formatting messes, irrelevant text, missing values, missing context, weak arguments — all flagged, no softening.

Each layer is invoked by me explicitly (`run layer 1`, `run layer 2`, `run layer 3`). Do not run a layer on your own.

## `output.md` — the live open-issue file

Every verification layer writes its findings into a single file: `output.md` in this folder. Rules:

- **One file, cumulative.** Layer 1 findings, layer 2 findings, and layer 3 findings all live in the same file, sectioned by layer.
- **Every line is an open issue.** If a line is in `output.md`, it is not yet fixed.
- **Read `output.md` at the start of every single prompt in this folder.** No exceptions. Before you do anything I ask, open `output.md`, see what is still open, and factor it in.
- **After every prompt where you touched the report,** re-check `output.md` against the current state of the report. Every issue you can confirm is now resolved: delete that line. Every issue still present: leave it. Do not add new findings during this pass — that is layer work, not prompt work.
- **Never mark an issue "done" without checking.** Deletion requires you to open the actual file/section referenced and verify the fix landed. A verbal "I did that" is not enough.
- **Do not silently rewrite or reorder lines** you did not resolve. The file is append-and-delete, not restructure.

Full `output.md` format and update protocol is in `verification.md`.

## Anti-repeat-mistake discipline

- If the same issue shows up in two consecutive verification layers, **flag it in chat** the moment you notice — this means something in your fix loop is broken.
- If I correct you on the same class of mistake twice in this folder, add a one-line note to the top of `output.md` under a `## Recurring — do not repeat` block. Keep that block until the round is closed.
- Do not treat any mentor comment or verification finding as "minor and skippable." If it is in `mistakes mentor found.md` or `output.md`, it is in scope.

## File outputs from this folder (recap)

1. `mistakes mentor found.md` — flat register of every mentor-flagged mistake, tagged by round.
2. `steps to take.md` — ordered action list, hardest at top, easiest at bottom, cross-referenced to the mistake register.
3. `verification.md` — the three verification layers, in full.
4. `output.md` — live open-issue file, cumulative across layers, read at start of every prompt, updated after every prompt.

That is all. Nothing else gets created in this folder unless I tell you to.
