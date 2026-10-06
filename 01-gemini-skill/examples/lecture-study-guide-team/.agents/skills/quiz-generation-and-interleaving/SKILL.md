---
name: quiz-generation-and-interleaving
description: "Generates active-recall comprehension quizzes and interleaves them at conceptual boundaries within study summaries, complete with explanations, distractor rationales, and slide references."
---

# Purpose

Provide a systematic method for creating pedagogical checkpoint quizzes and embedding them directly into structured summary modules. This skill ensures questions target deep comprehension (application, discrimination, and misconception avoidance) rather than superficial keyword matching, reinforcing slide content retention.

# When to Use

Use when:
- Creating formative active-recall checkpoints embedded within technical or academic summaries.
- Generating diagnostic questions with full answer keys, distractor breakdowns, and source slide references.
- Transforming static lecture summaries into interactive study modules.

Do not use for standalone summative exams detached from slide materials or trivia-style memorization quizzes.

# Procedure

## 1. Input Gate
Recover the current task, settled criteria and inputs, original source or explicit topic basis, artifact, source/artifact versions, current gate and owner, evidence, and same-issue repair history from the latest handoff and readable artifacts. Retain settled answers; separate a new run from a continuation or correction. Verify actual readability and available tool access; a recap is reported context, not source or artifact access. For missing context, input, or capability, pause only the affected gate as `MANUAL`/`BLOCKED`, state the exact missing portion and usable manual transfer, then resume that gate after recovery. Unknown repair history cannot be reset to zero or used to authorize another correction.

## 2. Work
1. **Module Boundary Identification:** Inspect the synthesized summary and identify natural cognitive stopping points (e.g., transition between theoretical principles and implementation details, or shifts across slide topics).
2. **Item Construction:** For each checkpoint, construct targeted question items:
   - **Question Varieties:** Focus on conceptual discrimination, edge cases, formulas/mechanisms, and scenario-based application.
   - **Distractor Rationale:** Ensure every distractor reflects a plausible misconception, miscalculation, or inverted causal relationship found in the topic domain.
   - **Answer Explanations:** Include a detailed explanation specifying why the correct answer holds and why each alternative is invalid, referencing exact source slide numbers.
3. **Interleaving Assembly:** Merge each quiz checkpoint directly following its parent summary section. Format questions with clear separation between the problem prompt, multiple-choice options, and a spoiler-protected or structured answer/rationale block.

## 3. Change
Separate reusable scope from run criteria and source. Retain compatible work and history. Mark only affected content and evidence `STALE` and resume the earliest affected gate. A new source or criteria invalidates the old overall `PASS`; retain unaffected evidence only when identity and traceability are checked, then recheck changed, added, and deleted material.

## 4. Correction
Report the finding, owner, and correction for independent recheck against the original source and criteria, or explicit topic basis and criteria. Only the main coordinator increments same-issue repair `0→1→2`, after a complete corrected artifact is delivered; diagnosis and review never increment. Independently recheck correction two. If it fails, retain `BLOCKED`, stop automation, and give one manual correction-plus-independent-review handoff. Rename, restart, source, criteria, and requirement changes do not reset the same issue.

## 5. Handoff
Report a compact context checkpoint containing task/criteria, settled inputs, artifact and source/artifact versions, completed/current gate, checks, evidence basis, uncertainty, `READY`/`PASS`/`REVISE`/`BLOCKED`, repair count/history, and next owner/action. Workers report. The independent reviewer compares directly to the original source and criteria, or explicit topic basis and criteria. The coordinator accepts; the human decides use. Team `PASS` requires usable output and current independent checks. A checkpoint cannot substitute for readable originals, complete artifacts, or actual review evidence.

## 6. Stop/resume
Stop after accepted responsibility output, a missing capability, or exhausted repair. Resume only the dependent gate on usable input or authorized change after reconciling the checkpoint with current source/artifact identity, with history intact. Missing context requires the relevant handoff and artifacts, never a guessed restart, duplicate output, or inferred old `PASS`. A responsibility result is not whole-team completion.

# Quality Checks

- **Unambiguous Correctness:** Verify that the keyed answer is demonstrably correct according to the source slides.
- **Cognitive Depth:** Check that questions test reasoning, definitions, and application rather than verbatim sentence recall.
- **Comprehensive Explanations:** Verify that every option has an explicit rationale explaining why it is correct or incorrect.
- **Structural Integrity:** Confirm the original summary text remains intact and uninterrupted except for the insertion of distinct checkpoint blocks.

# Failure Cases

- **Ambiguous Answer Key:** If multiple options could be construed as correct based on slide wording, rewrite distractors to eliminate ambiguity.
- **Superficial Recall:** If a question merely tests slide headings or trivial keywords, replace it with a scenario-based or mechanism-testing item.
- **Broken Mapping:** If a question cites a slide number not covered in the preceding section, realign the question to its proper module.

# Output Expectations

Output consists of:
1. The intact summary text seamlessly interleaved with `### Checkpoint Quiz [Section Title]` blocks.
2. Formatted questions containing:
   - Stem and options (A, B, C, D).
   - Correct Answer Key.
   - Slide Source Reference.
   - Comprehensive Explanation & Distractor Analysis.
