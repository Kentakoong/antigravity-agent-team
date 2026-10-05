# Build a reusable quiz team

Use Gemini to create your team's instructions, then run the team in Antigravity to write and check a quiz. After that, extend the team to turn the checked quiz into an interactive page.

Use **Flash in Gemini** and **Gemini 3.6 Flash in Antigravity**.

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

Save the downloaded files inside [my-team](my-team/), following each lesson's exact locations. Use [the save reference](02-antigravity-setup/SAVE-REFERENCE.md) if you need the folder layout.

No Gemini Skills access? Use [Plan B](99-no-gemini-skills-fallback/README.md).

## About the screenshots

The Gemini images are cropped from the supplied screenshots. See [the example conversation](https://gemini.google.com/app/db985e0c4d7b9dbf) and [image details](assets/gemini/README.md). Antigravity has eight screenshot spaces ready for our walkthrough; its live test has not started. Generated instructions still need to be saved and tested.
