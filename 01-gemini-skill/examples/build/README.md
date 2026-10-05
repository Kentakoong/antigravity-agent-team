# Example — Download the quiz-team files

Use this optional reference after reviewing the plan in your **Gemini Flash** Builder chat. These are file locations, not a prebuilt team; download the complete files Gemini gives you.

## Ask Gemini to build

```text
Use that flow. Build the team now.
```

For each reply, read what the file does, click **Download**, and move/rename the file to its exact location under `my-team/`. Check the contents before sending `Continue` for the next file. If a file is incomplete, ask for a complete replacement.

![Gemini gives a file and its location](../../../assets/gemini/01-build-copy.png)

| Save here | What it does |
| --- | --- |
| `my-team/.agents/skills/quiz-generator/SKILL.md` | Explains how to write the quiz. |
| `my-team/.agents/agents/quiz-creator.md` | Writes the questions and answers. |
| `my-team/.agents/agents/quiz-verifier.md` | Independently checks the quiz. |
| `my-team/.agents/skills/quiz-generation-team/SKILL.md` | Collects your inputs and runs the team. |

Stop when all four complete files are saved, every component is **CURRENT**, and **Next Pending Component: None**.

![The completed four-file list](../../../assets/gemini/01-build-complete.png)

## Try the saved team

Use [the save reference](../../../02-antigravity-setup/SAVE-REFERENCE.md) to check the four file locations, then [try the initial team in Antigravity](../../../02-antigravity-setup/README.md) with **Gemini 3.6 Flash**. A CURRENT label does not mean the team has been tested.

## Then add HTML

After testing the initial team, follow [Step 03 — Add an interactive quiz page](../../../03-debug-and-improve/README.md) in the same Gemini Builder chat. Review the proposal, send `apply`, download the new `quiz-html-builder.md`, then send `Continue` and download the replacement team `SKILL.md`.

Keep the original quiz method, creator and verifier. Back up the old team instructions outside `.agents` before replacing them. The HTML builder should receive only a quiz that passed review. Start a fresh Antigravity chat to test the extended team and its page, following Step 03.
