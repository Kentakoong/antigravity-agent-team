# Quiz build prompts

Use these in the same Gemini Flash conversation after the design is accepted.
They are prompts for definition generation; runtime source material is
provided later in Antigravity.

Authorize the original build:

```text
Use that flow. Build the team now.
```

When the Builder has emitted a complete file, download the Markdown block and
move/rename the file at its exact path relative to `my-team/`. If it reports another pending
component, continue:

```text
Continue.
```

After the original quiz definitions are complete, request the optional
extension:

```text
Could we extend it so that, after the quiz passes review, it becomes a standalone interactive HTML quiz?
```

Review the proposed architecture before sending:

```text
apply
```

Download the complete new `.agents/agents/quiz-html-builder.md`, then send:

```text
Continue.
```

Download the complete replacement `.agents/skills/quiz-generation-team/SKILL.md`.
The HTML worker must receive the complete verifier-`PASS` quiz; it must not
draft or self-approve the quiz. Preserve the original three files, record each
purpose and hash, and stop if any response is partial or spliced.
