# Plan B starter prompt

Paste the complete [Builder instructions](../00-gemini-setup/SKILL.md) into an
ordinary Gemini chat, then send this natural brief:

```text
Design a reusable team that generates quizzes from topics or reference files.
It should collect missing topics or source material and question count, use an
independent reviewer, and leave the use decision to a human.
```

Use Gemini only for design, build and concrete definition feedback. Do not
attach a PDF or other runtime source during this conversation. Save each
complete Agent/Skill Markdown definition at its stated destination relative
to `my-team/`. The Builder generates instructions; Antigravity later produces
quiz content or HTML.

Keep the latest context checkpoint with the downloaded definitions. If the
chat loses context, supply the checkpoint and relevant current definition
bytes before continuing. For a fresh chat, supply the complete Builder
instructions again. The checkpoint helps recover scope and pending work;
it does not restore missing instructions or prove saved files or runtime checks.

When the original three quiz definitions are complete, an optional extension
can be requested with:

```text
Could we extend it so that, after the quiz passes review, it becomes a standalone interactive HTML quiz?
```

After reviewing the proposal, send `apply`, download the complete
`.agents/agents/quiz-html-builder.md`, send `Continue`, and download the complete
replacement `.agents/skills/quiz-generation-team/SKILL.md`. Keep the original
`quiz-generator`, `quiz-creator` and `quiz-verifier` files unchanged, and keep
the original coordinating entry as a baseline until its replacement is saved.

Only after the static five-file audit should you transfer the team to
Antigravity, select the actual entry Skill and provide runtime topic/source
inputs there. This fallback does not claim installation or execution.
