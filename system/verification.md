> Used as-is during the project. Only the firm name was removed.

# Verification — Mentor Corrections Folder

> **Portable file.** Belongs next to `instructions.md`. It defines the three verification layers used on the report after mentor corrections have been applied. Read this file before running any layer.

---

## Ground rules (apply to all three layers)

1. **A layer runs only when I explicitly invoke it.** Trigger phrases: `run layer 1`, `run layer 2`, `run layer 3`. Never run a layer on your own initiative.
2. **Every finding, from every layer, is written into `output.md` in this folder.** One file, cumulative, sectioned by layer.
3. **A finding stays in `output.md` until the fix is verified in the actual report file.** No verbal "done."
4. **Read `output.md` at the start of every prompt in this folder.** After any prompt where you touched the report, re-check each open finding against the current file and delete only the ones you can confirm are fixed.
5. **No softening.** Do not paraphrase harsh feedback into gentler language. Do not merge two distinct findings into one. Do not drop a finding because it feels small.
6. **No inventing.** Each finding must be traceable: to a mentor comment (Layer 1), to a TOC clause or past-report precedent (Layer 2), or to a specific reader concern (Layer 3, with the reasoning stated).
7. **No fixing during verification.** A verification layer produces findings only. Fixes come afterwards, when I ask.

---

## Layer 1 — Mentor Comment Compliance

**Purpose:** confirm that every mistake logged in `mistakes mentor found.md` has actually been addressed in the report.

**When invoked:** `run layer 1`.

**Inputs required:**
- `mistakes mentor found.md` (this folder)
- The current report / drafts / deliverables files (in the project's `drafts/` and `deliverables/` folders)
- The original mentor-marked files (this folder)

**Procedure:**
1. Load `mistakes mentor found.md`. Walk each numbered mistake.
2. For each, open the specific report file / section / table / figure it points to.
3. Verify the fix landed. Be strict:
   - Wording matches mentor's ask.
   - Number matches the source they cited (if numeric).
   - Formatting matches the standing project rules (no em dashes, USD millions, Arial 9, palette).
   - If it was a report-wide change (ratio family, terminology), sweep **every** occurrence — not just the flagged one.
4. Write result to `output.md` under a `## Layer 1 — Mentor compliance (run YYYY-MM-DD)` section:
   - `- [OPEN] #N — <mentor mistake> — <what is still wrong / where>`
   - Do not list resolved items. Silence = fixed.
5. If nothing is open, write a single line `- All mentor findings resolved.` under the layer heading.

**Guardrails:**
- Do not add non-mentor observations here. Those belong in chat (per `instructions.md`) or Layer 3.
- Do not close a mentor finding based on partial coverage. Report-wide asks require report-wide confirmation.

---

## Layer 2 — TOC + Past-Report Benchmarking

**Purpose:** confirm the report matches the official Table of Contents and holds up next to previously-passed reports. **TOC always wins** if the two conflict.

**When invoked:** `run layer 2`.

**Inputs required:**
- The official / firm-standard TOC (in `knowledge/` — the report template / guidelines file).
- Past passed reports (in `knowledge/finalised reports by me/` and `knowledge/`).
- The current report.

**Procedure:**
1. **TOC pass (weight: high).** Walk the TOC top to bottom. For each required section / subsection:
   - Does it exist in the current report?
   - Is it in the right order?
   - Does it cover the mandated content (subheadings, tables, charts, appendix items)?
   - Is the numbering / naming consistent with the TOC?
2. **Past-report pass (weight: supporting).** Compare the current report against the last two or three passed reports for:
   - Depth of coverage per section (are we thinner than precedent?).
   - Table and chart conventions (columns, headers, ordering).
   - Tone, sourcing style, appendix layout.
3. **Conflict rule:** if a past report does something the TOC does not require, TOC wins. Note the divergence but do not treat past practice as a mandate.
4. Write result to `output.md` under `## Layer 2 — TOC + past-report benchmark (run YYYY-MM-DD)`:
   - `- [OPEN] TOC:<section> — <what's missing / misordered / mislabelled>`
   - `- [OPEN] PAST:<section> — <how current falls short of precedent>` (only when the gap is material)
5. If clean, write `- Report aligns with TOC and precedent.` under the heading.

**Guardrails:**
- Do not restructure the report to match a past report if it already matches the TOC.
- Do not import stylistic quirks from past reports that contradict the standing writing rules.
- Cite the specific TOC clause or past-report file when logging a finding, so I can trace it.

---

## Layer 3 — Fund Manager / Professional Read

**Purpose:** simulate a brutally critical read by the actual audience — a bond fund manager or senior credit professional who does not care about feelings and will kill a report over sloppy formatting or missing context.

**When invoked:** `run layer 3`.

**Inputs required:**
- The current full report (all sections, all appendices, all deliverable Excels referenced by the report).

**Procedure:**
1. Read the report **cover to cover**, in the order a fund manager would: cover → credit outlook → investment thesis → financials → credit scorecard → appendices.
2. At every page, ask:
   - Is the argument actually made, or hinted at?
   - Is every number sourced, and is the source specific enough to trust?
   - Is every claim defensible under a follow-up question?
   - Are the tables readable? Alignment, units, headers, source lines.
   - Are the charts telling the same story as the text? Any contradictions?
   - Are ratios, deltas, and trends explained, or just dumped?
   - Is there any section that feels like filler, off-topic, or copy-pasted?
   - Are there missing values, "TBD", empty cells, unresolved gaps?
   - Is anything ambiguous, hedged in a way that hides a real weakness, or overclaimed?
3. Be blunt. Do not soften. Write findings the way a mentor would in red pen. Examples of acceptable tone:
   - `Section 5.2 — leverage jump from 2.32x to 4.32x has no explanation. This is the single biggest number in the report and it is unaddressed.`
   - `Table 4.1 — right column mislabelled "FY25" but numbers are LTM. Kills trust immediately.`
   - `§7 — three paragraphs on packaging strategy. Not relevant to credit thesis. Cut or move.`
4. Write result to `output.md` under `## Layer 3 — Fund manager read (run YYYY-MM-DD)`:
   - `- [OPEN] <section/page> — <blunt finding>`
   - Group findings by severity: `### Critical`, `### Material`, `### Cosmetic`. Every finding gets a severity.
5. If clean (rare), write `- Report is submission-ready per critical read.` — but only if you would genuinely stake your name on it.

**Guardrails:**
- Do not repeat findings already open from Layer 1 or Layer 2 unless the same issue is materially worse than logged — in which case reference the prior line and escalate severity.
- Do not add findings driven by personal preference alone. Every finding must be defensible in front of a professional reader: "a fund manager would push back on this because…".
- Do not use compliments or padding. This layer is for problems only.

---

## `output.md` — format and update protocol

**File location:** this folder, root level.

**Sections (in order):**

```
# Output — Open Verification Findings

## Recurring — do not repeat
(Appears only when I have corrected you on the same class of mistake more than once. One line per pattern. Cleared when I close the round.)

## Layer 1 — Mentor compliance (run YYYY-MM-DD)
- [OPEN] #3 — table 4.1 alignment still mixed
- [OPEN] #7 — top-5 language not applied in §5.2

## Layer 2 — TOC + past-report benchmark (run YYYY-MM-DD)
- [OPEN] TOC:6.4 — subsection "Liquidity runway" missing
- [OPEN] PAST:appendix D — capital structure table thinner than precedent

## Layer 3 — Fund manager read (run YYYY-MM-DD)
### Critical
- [OPEN] §5 — leverage jump from 2.32x to 4.32x unexplained
### Material
- [OPEN] §7 — packaging strategy paragraph off-thesis
### Cosmetic
- [OPEN] §2.1 — Diluted EPS row missing bold
```

**Update rules:**

1. **On start of every prompt in this folder:** open `output.md`, note open items, factor them into whatever I asked.
2. **After a prompt where you edited the report:** walk each open item. If verifiably fixed (you opened the file and confirmed), delete the line. If not, leave it.
3. **Never edit the layer heading dates** on a resolve pass. Dates belong to the layer run that logged the finding.
4. **Never re-order findings** on a resolve pass. Delete or leave.
5. **When a layer is re-run,** append a new dated section for that layer. Do not overwrite the previous run's section — leave any of its still-open findings in place, and add newly discovered issues under the new run's date. When you delete a resolved line, delete it from wherever it lives.
6. **When every finding across every layer is closed,** collapse the file to a single line: `# Output — Open Verification Findings\n\n(none)` and wait for the next layer invocation.

**Anti-drift guardrails:**

- **Never mark closed what you have not physically verified in the report file.** Not the docx you last built, not the version in memory — open the actual current file.
- **Never bulk-close.** One item, one check, one delete.
- **If unsure whether a fix landed,** leave the line and flag it in chat: `output.md item X — cannot confirm, need you to point me to where the fix should be visible`.
- **If the report state has changed since a layer ran** (new draft version, new deliverable), do **not** silently invalidate the layer's findings. Re-check each one against the new version; delete only what is genuinely resolved. Report-wide changes get a note in chat.
