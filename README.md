# Build a reusable quiz team

Use Gemini to create your team's instructions, then run the team in Antigravity to write and check a quiz. After that, extend the team to turn the checked quiz into an interactive page.

## Prerequisites

1. Use a **personal Google account** for [Gemini web](https://gemini.google.com/). [Skills are currently unavailable](https://support.google.com/gemini/answer/17094296?hl=en) on school or business accounts.
2. Download and install [**Antigravity 2.0**](https://www.antigravity.google/download).

> **Gemini warning:** Use **Flash**.

> **Antigravity warning:** Use **Gemini 3.6 Flash**.

## Follow the workshop

| Open | What you will do |
| --- | --- |
| [00 — Set up Gemini](00-gemini-setup/README.md) | Upload the Builder Skill. |
| [01 — Build the quiz team](01-gemini-skill/README.md) | Describe the workflow and download four instruction files. |
| [02 — Try it in Antigravity](02-antigravity-setup/README.md) | Create a project and test the four-file team by writing and checking a quiz. |
| [03 — Add an interactive page](03-debug-and-improve/README.md) | Add the HTML builder, update the team's main instructions and test the quiz page. |

Follow **00 → 01 → 02 → 03**. Step 01 creates four instruction files; Step 02 tests that initial team. In Step 03, return to the same Gemini Builder chat to add `quiz-html-builder.md` and update the team instructions, then test the extended team in Antigravity.

An **Agent** handles a job, such as writing or checking questions. A **Skill** gives reusable instructions for doing the work.

## Where your files go

Save the downloaded files inside [my-team](my-team/), following each lesson's exact locations. See [Step 02's folder layout](02-antigravity-setup/README.md#1-prepare-your-folder) if needed.

No Gemini Skills access? Use [Plan B](99-no-gemini-skills-fallback/README.md).

## About the screenshots

The Gemini images are cropped from the supplied screenshots. See [the example conversation](https://gemini.google.com/app/db985e0c4d7b9dbf) and [image details](assets/gemini/README.md). Antigravity has eight screenshot spaces ready for our walkthrough; its live test has not started. Generated instructions still need to be saved and tested.
