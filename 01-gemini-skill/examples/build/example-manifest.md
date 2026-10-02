# Quiz team file manifest

This is an illustrative inventory for the quiz workflow. It is not a tested
package and does not replace the files delivered by Gemini. Every path is
relative to `my-team/`.

```text
my-team/
└── .agents/
    ├── agents/
    │   ├── quiz-creator.md
    │   ├── quiz-verifier.md
    │   └── quiz-html-builder.md       # optional, after verifier PASS
    └── skills/
        ├── quiz-generator/
        │   └── SKILL.md              # original method, retained
        └── quiz-generation-team/
            └── SKILL.md              # replacement coordinating entry
```

| File | Purpose | Required input | Handoff |
|---|---|---|---|
| `skills/quiz-generator/SKILL.md` | Existing quiz-generation method | Topic/reference material, count and criteria | `quiz-creator` |
| `agents/quiz-creator.md` | Drafts questions and explanations | Validated source and count | `quiz-verifier` |
| `agents/quiz-verifier.md` | Independently checks the draft | Original source, draft and criteria | `PASS` or `REVISE` |
| `agents/quiz-html-builder.md` | Formats a passed quiz as one interactive HTML file | Complete quiz plus verifier `PASS` | HTML artifact for human decision |
| `skills/quiz-generation-team/SKILL.md` | Entry that gates input, dispatches review and then HTML | User request and current evidence | Human use/share decision |

Save the complete Markdown emitted for each file. Do not attach the runtime
source to Gemini, and do not treat a filename or inventory as proof that the
file exists or is installed.
