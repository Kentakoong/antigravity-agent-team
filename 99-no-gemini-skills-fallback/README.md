# Plan B — Use Gemini without Skills access

If your Gemini account has no Skills option, give the Builder instructions directly to the chat. This does not install a Skill, but lets you follow the same workshop prompts.

> **Warning:** Use **Flash** in Gemini.

## 1. Start a new chat

Paste the complete [Builder instructions](../00-gemini-setup/SKILL.md) into an ordinary Gemini chat. You can attach that instruction file if supported. A filename or link alone is not enough. Then send:

```text
I want a reusable team that generates multiple-choice quizzes for students from topics I provide or documents I attach. It should check the questions and answer key before delivering the quiz. Help me design the workflow first.
```

You do not need to attach a quiz source document here; that belongs in the later Antigravity run.

## 2. Design and build the team

Use the design and build prompts in [Build your quiz team](../01-gemini-skill/README.md). Skip its Skill-selection step because you have already supplied the instructions.

Review Gemini's plan before asking it to build. Download each Markdown file, move it to its exact location under `my-team/`, and rename it if needed. Save the complete file before sending `Continue`.

Finish when all four files are saved, every component says **CURRENT**, and **Next Pending Component: None**.

## 3. Test the initial team

> **Warning:** Use **Gemini 3.6 Flash** in Antigravity.

Use [the Antigravity walkthrough](../02-antigravity-setup/README.md) with **Gemini 3.6 Flash** to create the project and test the four saved files.

## 4. Add the interactive page

Follow [Add an interactive quiz page](../03-debug-and-improve/README.md) in this same chat. It adds `quiz-html-builder.md` and replaces `quiz-generation-team/SKILL.md`; keep the existing method, creator and verifier files.

## Test the extended team

Start a fresh Antigravity chat and follow [Step 03's test steps](../03-debug-and-improve/README.md#5-run-the-extended-team-in-antigravity) with **Gemini 3.6 Flash** to test the five saved files and interactive page.

If a file is incomplete, request the complete file before moving on. Keep the latest checkpoint with your downloads. If you restart Gemini, supply the complete Builder instructions, checkpoint and relevant current definitions again; see [the recovery guidance](../03-debug-and-improve/README.md#recover-a-long-or-restarted-builder-chat).
