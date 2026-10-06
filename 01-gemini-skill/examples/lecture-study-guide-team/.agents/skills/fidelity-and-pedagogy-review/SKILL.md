---
name: fidelity-and-pedagogy-review
description: "Audits synthesized slide summaries and interleaved quizzes directly against original slides for complete detail retention, factual precision, question validity, and distractor accuracy."
---

# Purpose

Establish an independent, non-negotiable review procedure to verify that synthesized slide summaries preserve 100% of substantive slide points and that embedded checkpoint quizzes are pedagogically valid, clearly referenced, and factually accurate with respect to the source materials.

# When to Use

Use when:
- Auditing a generated slide study guide before final coordinator acceptance.
- Verifying page-by-page coverage against original slide decks (PDF, exports, or slide transcripts).
- Validating question stems, answer keys, distractor rationales, and slide references for embedded quizzes.

Do not use for generating primary summary text or authoring initial quiz items.

# Procedure

## 1. Input Gate
Recover the current task, settled criteria and inputs, original source or explicit topic basis, artifact, source/artifact versions, current gate and owner, evidence, and same-issue repair history from the latest handoff and readable artifacts. Retain settled answers; separate a new run from a continuation or correction. Verify actual readability and available tool access; a recap is reported context, not source or artifact access. For missing context, input, or capability, pause only the affected gate as `MANUAL`/`BLOCKED`, state the exact missing portion and usable manual transfer, then resume that gate after recovery. Unknown repair history cannot be reset to zero or used to authorize another correction.

## 2. Work
1. **Source Inspection & Accessibility Verification:** Confirm direct inspection access to all original slide pages. If any slide or visual diagram cannot be read directly, mark the gate `MANUAL`/`BLOCKED` and demand the missing slide inputs.
2. **Page-by-Page Fidelity Audit:** Compare each original slide against the summary and its coverage mapping table:
   - Identify any missing metrics, definitions, caveats, or sub-bullets.
   - Detect unsupported additions or unflagged external generalizations.
   - Flag any distortion of causal links, taxonomies, or sequence steps.
3. **Pedagogical & Quiz Integrity Check:**
   - Verify every quiz question against the specific cited slide numbers.
   - Confirm the designated correct answer is indisputably supported by the source text.
   - Verify that distractors are genuinely incorrect or suboptimal, not accidentally correct due to vague wording.
   - Check that explanations comprehensively explain both correct and incorrect choices.
4. **Findings & Verdict Formulation:**
   - If zero discrepancies exist: Issue an explicit `PASS` with inspected page count.
   - If omissions, factual distortions, or quiz key errors exist: Issue a `REVISE` finding containing exact slide locations, identified defects, and mandatory corrective actions.

## 3. Change
Separate reusable scope from run criteria and source. Retain compatible work and history. Mark only affected content and evidence `STALE` and resume the earliest affected gate. A new source or criteria invalidates the old overall `PASS`; retain unaffected evidence only when identity and traceability are checked, then recheck changed, added, and deleted material.

## 4. Correction
Report the finding, owner, and correction for independent recheck against the original source and criteria, or explicit topic basis and criteria. Only the main coordinator increments same-issue repair `0→1→2`, after a complete corrected artifact is delivered; diagnosis and review never increment. Independently recheck correction two. If it fails, retain `BLOCKED`, stop automation, and give one manual correction-plus-independent-review handoff. Rename, restart, source, criteria, and requirement changes do not reset the same issue.

## 5. Handoff
Report a compact context checkpoint containing task/criteria, settled inputs, artifact and source/artifact versions, completed/current gate, checks, evidence basis, uncertainty, `READY`/`PASS`/`REVISE`/`BLOCKED`, repair count/history, and next owner/action. Workers report. The independent reviewer compares directly to the original source and criteria, or explicit topic basis and criteria. The coordinator accepts; the human decides use. Team `PASS` requires usable output and current independent checks. A checkpoint cannot substitute for readable originals, complete artifacts, or actual review evidence.

## 6. Stop/resume
Stop after accepted responsibility output, a missing capability, or exhausted repair. Resume only the dependent gate on usable input or authorized change after reconciling the checkpoint with current source/artifact identity, with history intact. Missing context requires the relevant handoff and artifacts, never a guessed restart, duplicate output, or inferred old `PASS`. A responsibility result is not whole-team completion.

# Quality Checks

- **Direct Source Verification:** Ensure audit findings stem from inspecting original slide pages, not from trusting the worker's intermediate recap.
- **Coverage Exhaustiveness:** Check that every slide in the source deck has been verified in the coverage table.
- **Answer Key Rigor:** Confirm that each quiz key is uniquely correct and supported without ambiguity.
- **Actionable Findings:** Ensure all `REVISE` findings specify slide number, exact discrepancy, and required fix.

# Failure Cases

- **Inaccessible Source Slides:** If slide files or attachments are unreadable by available tools, report `BLOCKED` immediately.
- **Repeated Discrepancy (Repair Loop):** If a defect persists across two repair attempts, halt execution as `BLOCKED` and provide a manual handoff.
- **Unverified Assertions:** Never issue a `PASS` if any slide page was skipped or assumed.

# Output Expectations

Output consists of:
1. Audit summary with total slides audited and verdict (`PASS`, `REVISE`, or `BLOCKED`).
2. Page-by-page verification notes.
3. Itemized Discrepancy and Correction Report (if `REVISE`), citing slide number, error type, and required correction.
