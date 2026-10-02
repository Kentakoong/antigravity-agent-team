# Plan B — Use Gemini without Skills access

If your Gemini account has no Skills option, give the Builder instructions directly to the chat. Use **Gemini Flash**. This does not install a Skill, but lets you follow the same workshop prompts.

## 1. Start a new chat

Open [the starter prompt](STARTER_PROMPT.md), then paste the complete [Builder instructions](../00-gemini-setup/SKILL.md) into the same chat. You can attach that instruction file if supported. A filename or link alone is not enough.

You do not need to attach a quiz source document here; that belongs in the later Antigravity run.

## 2. Design and build the team

Use the design and build prompts in [Build your quiz team](../01-gemini-skill/README.md). Skip its Skill-selection step because you have already supplied the instructions.

Review Gemini's plan before asking it to build. Download each Markdown file, move it to its exact location under `my-team/`, and rename it if needed. Save the complete file before sending `Continue`.

Finish when all four files are saved, every component says **CURRENT**, and **Next Pending Component: None**.

## 3. Add the interactive page

Follow [Add an interactive quiz page](../03-debug-and-improve/README.md) in this same chat. It adds `quiz-html-builder.md` and replaces `quiz-generation-team/SKILL.md`; keep the existing method, creator and verifier files.

## Try your team

Use [the Antigravity walkthrough](../02-antigravity-setup/README.md) with **Gemini 3.6 Flash** to create the project and test the five saved files.

If a file is incomplete, request the complete file before moving on. If you restart Gemini, supply the Builder instructions again along with the current plan and files already generated.
