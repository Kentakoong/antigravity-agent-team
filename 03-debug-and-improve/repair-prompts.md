# Optional — Change the reusable team in Gemini

These are optional examples, not extra workshop steps. Choose one only when you want to change how the team behaves on future runs.

## Where to send these prompts

1. Return to the **original Gemini conversation** where you selected `design-reusable-agent-team` and generated the quiz-team files in Step 01. For the workshop example, this is [the Builder conversation](https://gemini.google.com/app/db985e0c4d7b9dbf).
2. Keep **Gemini Flash** selected. Continue in that same chat; you do not need to select the Builder again for a follow-up.
3. Send one relevant change request below. Review Gemini's proposal before sending `apply`.

If you only want a different topic, student level or question count for **one quiz**, tell the running team in **Antigravity**, using **Gemini 3.6 Flash**. That is a runtime input change; you do not need to regenerate the reusable definitions.

## Example 1 — Make future quizzes easier for beginners

**Use when:** you want the reusable method to explain unfamiliar terms consistently, across future quizzes. The team already asks for student level; keep that input question.

**Send in:** the original Gemini Builder chat.

```text
Update the reusable quiz team so quizzes for beginners explain unfamiliar terms in the answer explanations. Keep the existing student-level input question and independent review. Propose the changes first.
```

For just one beginner quiz, instead tell Antigravity: `For this quiz, use beginner-level language and explain unfamiliar terms.`

## Example 2 — Fix a problem found during an Antigravity run

**Use when:** an actual run exposed a recurring problem in the team definitions, such as a verifier accepting an unsupported answer.

**Send in:** the original Gemini Builder chat. First paste the actual incorrect question/answer, the verifier's report and the relevant source excerpt. Include only the material needed to explain the failure; Gemini is diagnosing the definitions, not running the quiz.

```text
During an Antigravity run, the verifier accepted an answer that the source does not support. I have pasted the incorrect question and answer, the relevant source excerpt and the actual verifier report above. Find the cause and propose a change to the reusable team definitions so this is caught next time. Do not claim a runtime retest has passed.
```

If you only need the current quiz corrected, report the specific mistake in the **same Antigravity conversation** first. Return to Gemini when the reusable instructions need changing.

## Example 3 — Simplify the reusable workflow

**Use when:** repeated runs show unnecessary roles or handoffs, and you want a smaller reusable team.

**Send in:** the original Gemini Builder chat.

```text
What is the smallest team design that still creates useful multiple-choice quizzes and independently checks the questions, answer key and explanations? Propose the changes before replacing any files.
```

## After Gemini proposes a change

1. Check which definitions will change and why. If you disagree, explain the adjustment in the same chat.
2. When the proposal fits, send `apply`.
3. Use **Download** on each new or replacement Markdown block. Move/rename it to the exact `FILE:` destination under `my-team/`. Preserve an old version outside the active `.agents/` folder before replacing it; keep unaffected files.
4. Send `Continue` while another component remains pending. Finish when the complete inventory is **CURRENT** and **Next Pending Component: None**.
5. Return to [Step 02](../02-antigravity-setup/README.md), start a **fresh Antigravity conversation** with **Gemini 3.6 Flash**, select `quiz-generation-team`, and repeat the affected scenario. Check the actual result before calling the fix successful.

Changing definitions in Gemini does not update an already-running Antigravity conversation by itself. The downloaded replacements must be saved in the project before the fresh test.
