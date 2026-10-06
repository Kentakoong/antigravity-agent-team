---
name: slide-study-guide-builder
description: "Coordinates the end-to-end transformation of slide decks into comprehensive study guides with intact detail and interleaved active-recall quizzes, audited by independent review."
---

# Purpose

Guide the main runtime coordinator in transforming slide decks into high-fidelity study modules. This skill oversees input validation, task delegation across specialized subagents, enforcement of independent slide-fidelity review, bounded correction routing, and filesystem persistence of the approved study guide.

# When to Use

Use when:
- Running the slide-to-study-guide agent team to synthesize slides and interleave comprehension quizzes.
- Orchestrating `slide-synthesizer`, `quiz-interleaver`, and `fidelity-auditor` runtime subagents.
- Processing presentation decks (PDF, exports, or transcripts) where zero information loss and active-recall testing are required.

Triggers automatically if required slide inputs or parameters are missing, prompting the user for necessary files.

# Procedure

## 1. Input Gate
1. Recover the current task, settled criteria, source files, and same-issue repair history from the latest context handoff.
2. Collect and validate essential inputs:
   - **Slide Source:** A readable file path, uploaded document (PDF, presentation export), or full slide transcript.
   - **Student / Depth Level:** Target conceptual depth (e.g., Undergraduate, Graduate, Professional Exam, Certification).
   - **Output Destination:** Resolve project root and default to `<project-root>/outputs/` (or explicit user destination override).
3. If the slide input is unreadable, missing, or unsupported by available runtime tools, halt the gate as `MANUAL`/`BLOCKED`, state the exact missing portion and usable manual transfer, then resume that gate after recovery. Unknown repair history cannot be reset to zero or used to authorize another correction.

## 2. Work
Execute the coordinated subagent workflow in strict sequential order:
1. **Extraction & Synthesis:**
   - Delegate slide source to `slide-synthesizer` using `skills/slide-extraction-and-synthesis`.
   - Verify receipt of the comprehensive draft summary and the full page-to-summary coverage mapping table.
2. **Pedagogical Interleaving:**
   - Delegate the synthesized summary and coverage table to `quiz-interleaver` using `skills/quiz-generation-and-interleaving`.
   - Receive the combined artifact with embedded active-recall checkpoint quizzes, answer keys, and slide references.
3. **Independent Fidelity Audit:**
   - Deliver the original slide source and the combined draft artifact to `fidelity-auditor` using `skills/fidelity-and-pedagogy-review`.
   - Ensure the auditor independently confirms direct source inspection. Receive the audit verdict (`PASS`, `REVISE`, or `BLOCKED`).
4. **Persistence & Verification:**
   - Upon receiving `PASS`, save the approved study guide to the verified output directory (e.g., `<project-root>/outputs/<deck-name>-study-guide.md`).
   - Reopen and read back the saved file to verify content integrity against the reviewed artifact before issuing completion.

## 3. Change
Separate reusable scope from run criteria and source. Retain compatible work and history. Mark only affected content and evidence `STALE` and resume the earliest affected gate. A new source or criteria invalidates the old overall `PASS`; retain unaffected evidence only when identity and traceability are checked, then recheck changed, added, and deleted material.

## 4. Correction
Report the finding, owner, and correction for independent recheck against the original source and criteria, or explicit topic basis and criteria. Only the main coordinator increments same-issue repair `0→1→2`, after a complete corrected artifact is delivered; diagnosis and review never increment. Independently recheck correction two. If it fails, retain `BLOCKED`, stop automation, and give one manual correction-plus-independent-review handoff. Rename, restart, source, criteria, and requirement changes do not reset the same issue.

## 5. Handoff
Report a compact context checkpoint containing task/criteria, settled inputs, artifact and source/artifact versions, completed/current gate, checks, evidence basis, uncertainty, `READY`/`PASS`/`REVISE`/`BLOCKED`, repair count/history, and next owner/action. Workers report. The independent reviewer compares directly to the original source and criteria, or explicit topic basis and criteria. The coordinator accepts; the human decides use. Team `PASS` requires usable output and current independent checks. A checkpoint cannot substitute for readable originals, complete artifacts, or actual review evidence.

## 6. Stop/resume
Stop after accepted responsibility output, a missing capability, or exhausted repair. Resume only the dependent gate on usable input or authorized change after reconciling the checkpoint with current source/artifact identity, with history intact. Missing context requires the relevant handoff and artifacts, never a guessed restart, duplicate output, or inferred old `PASS`. A responsibility result is not whole-team completion.

# Quality Checks

- **Pre-execution Verification:** Confirm all subagents (`slide-synthesizer`, `quiz-interleaver`, `fidelity-auditor`) and method skills are present and accessible.
- **Independent Audit Guarantee:** Verify that `fidelity-auditor` inspected original slide pages directly, rather than intermediate worker summaries.
- **Persistence Verification:** Verify that the output markdown file exists on disk, is non-empty, and matches the audited text.
- **Bounded Repairs:** Ensure same-issue repair counter is correctly managed and halts at count 2 if defects persist.

# Failure Cases

- **Missing Slide Input:** Prompt user for the slide file path or pasted deck text; keep input gate blocked.
- **Auditor `REVISE`:** Route specific discrepancy findings to `slide-synthesizer` (if missing content) or `quiz-interleaver` (if faulty question key), increment repair count, and re-audit.
- **Repair Exhaustion:** If review fails after correction 2, mark status `BLOCKED` and provide a manual remediation report.
- **Filesystem Write Failure:** Retain the approved artifact in chat context, report `MANUAL`/`BLOCKED` for the persistence gate, and provide the text directly.

# Output Expectations

Final deliverable reported to the participant:
1. Summary metadata: Total slides processed, modules generated, and checkpoint quizzes interleaved.
2. Verified absolute file path of the saved study guide (e.g., `/workspace/outputs/study-guide.md`).
3. Auditor verification summary confirming 100% detail retention and question validity.
4. Human use handoff.
