# Quiz design prompt

Use this natural-language brief after selecting the Builder in a fresh Gemini
chat. It describes the future runtime input contract without attaching a
source file to Gemini.

```text
Design a reusable team that generates quizzes from topics or reference files.
It should collect missing topics or source material and question count, use an
independent reviewer, and leave the use decision to a human.
```

If you want the optional HTML result included in the design, add this only as
a requirement:

```text
After the quiz passes independent review, make the verified quiz available to
a separate worker that creates a standalone interactive HTML page. Keep HTML
generation downstream of review and keep the final use decision with me.
```

Do not attach a PDF or other runtime source during this Gemini design/build
conversation. Supply the actual topic or reference material later to the
installed entry in Antigravity.

When the Builder asks to build, authorize it explicitly:

```text
Use that flow. Build the team now.
```

Then follow its exact pending-file instructions. Download every complete Markdown block and save each file at the stated path relative to `my-team/`.
