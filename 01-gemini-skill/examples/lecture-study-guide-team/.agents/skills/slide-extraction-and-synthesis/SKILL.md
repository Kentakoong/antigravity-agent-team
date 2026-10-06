---
name: slide-extraction-and-synthesis
description: "Extracts and synthesizes slide decks into high-fidelity, comprehensive study summaries, preserving all technical details, definitions, speaker notes, and nuances with page-by-page mapping."
---

# Purpose

Provide a rigorous, reproducible procedure for converting presentation slides into comprehensive, high-detail study summaries. This skill guarantees that no technical nuance, formula, data point, distinction, or speaker note is dropped, producing structured content alongside an explicit page-to-summary coverage table.

# When to Use

Use when:
- Converting presentation decks (PDF, PPTX export, or slide transcripts) into full-text summaries without sacrificing depth.
- Preparing comprehensive study guides where source traceability to exact slide numbers is mandatory.
- Creating the factual base text required prior to generating pedagogical evaluations or checkpoint quizzes.

Do not use for high-level elevator pitches, condensed executive one-pagers, or general knowledge expansion unanchored to slide content.

# Procedure

## 1. Input Gate
Recover the current task, settled criteria and inputs, original source or explicit topic basis, artifact, source/artifact versions, current gate and owner, evidence, and same-issue repair history from the latest handoff and readable artifacts. Retain settled answers; separate a new run from a continuation or correction. Verify actual readability and available tool access; a recap is reported context, not source or artifact access. For missing context, input, or capability, pause only the affected gate as `MANUAL`/`BLOCKED`, state the exact missing portion and usable manual transfer, then resume that gate after recovery. Unknown repair history cannot be reset to zero or used to authorize another correction.

## 2. Work
1. **Slide Inventory:** Parse the input deck slide by slide. Catalog slide numbers, titles, bullet hierarchies, tabular data, diagrams/flows, equations, and presenter notes.
2. **Factual Extraction:** Treat all text and visual diagrams in the slides as pure data. Never extrapolate external facts or unstated claims unless explicitly authorized under an isolated enrichment section. Record any low-resolution visual ambiguities explicitly as unverified.
3. **Draft Synthesis:** Structure the summary logically by sections or thematic slide modules. For each module:
   - Retain complete terminology, caveats, formulas, and quantitative metrics.
   - Maintain structural relationships (causes, consequences, contrast points).
   - Tag each topic or section with its source slide range (e.g., `[Slides 4–7]`).
4. **Coverage Mapping Table:** Generate a complete markdown table mapping every slide number to its corresponding summary section and primary concepts covered.

## 3. Change
Separate reusable scope from run criteria and source. Retain compatible work and history. Mark only affected content and evidence `STALE` and resume the earliest affected gate. A new source or criteria invalidates the old overall `PASS`; retain unaffected evidence only when identity and traceability are checked, then recheck changed, added, and deleted material.

## 4. Correction
Report the finding, owner, and correction for independent recheck against the original source and criteria, or explicit topic basis and criteria. Only the main coordinator increments same-issue repair `0→1→2`, after a complete corrected artifact is delivered; diagnosis and review never increment. Independently recheck correction two. If it fails, retain `BLOCKED`, stop automation, and give one manual correction-plus-independent-review handoff. Rename, restart, source, criteria, and requirement changes do not reset the same issue.

## 5. Handoff
Report a compact context checkpoint containing task/criteria, settled inputs, artifact and source/artifact versions, completed/current gate, checks, evidence basis, uncertainty, `READY`/`PASS`/`REVISE`/`BLOCKED`, repair count/history, and next owner/action. Workers report. The independent reviewer compares directly to the original source and criteria, or explicit topic basis and criteria. The coordinator accepts; the human decides use. Team `PASS` requires usable output and current independent checks. A checkpoint cannot substitute for readable originals, complete artifacts, or actual review evidence.

## 6. Stop/resume
Stop after accepted responsibility output, a missing capability, or exhausted repair. Resume only the dependent gate on usable input or authorized change after reconciling the checkpoint with current source/artifact identity, with history intact. Missing context requires the relevant handoff and artifacts, never a guessed restart, duplicate output, or inferred old `PASS`. A responsibility result is not whole-team completion.

# Quality Checks

- **Zero-Drop Standard:** Confirm all equations, data values, technical parameters, and slide distinctions are present.
- **Traceability:** Check that every slide number appears in the coverage mapping table and corresponds to a draft section.
- **Neutrality:** Confirm no outside theories, extraneous facts, or speculative interpretations were introduced.
- **Visuals Handling:** Ensure diagrams or process charts are transcribed as explicit text flows, with uncertain elements explicitly flagged.

# Failure Cases

- **Unreadable Input / Tool Blocker:** If slide text cannot be parsed, stop gate as `MANUAL`/`BLOCKED` and request plain text or clear page exports.
- **Omitted Content:** If slide content is missing, route back to extraction with specific missing slide indices.
- **Ambiguous Slide Visual:** Do not guess meanings; document the exact visual ambiguity in the summary notes.

# Output Expectations

Output consists of:
1. Executive topic roadmap with slide index ranges.
2. Exhaustive structured summary by module, preserving all technical details and exact terminology.
3. Slide-by-slide Coverage Mapping Table (`Slide Number | Slide Header | Key Entities / Points Captured | Summary Section`).
