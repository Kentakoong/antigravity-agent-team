# Save reference — Gemini-generated quiz definitions

Use **Flash in Gemini** while generating and changing these definitions. Later, execute the saved team in Antigravity with **Gemini 3.6 Flash**. Use [Step 02](README.md) to create the Antigravity project from this folder, select the entry and run it.

## One designated root

Use the workshop's `my-team/` folder. In this checkout it is `/Users/kentakoong/Desktop/University/clubs/gdgoc/agentteams/my-team/`. The paths after Gemini's `FILE:` label are relative to that root.

| Emitted destination | Save as |
| --- | --- |
| `.agents/skills/quiz-generator/SKILL.md` | `my-team/.agents/skills/quiz-generator/SKILL.md` |
| `.agents/agents/quiz-creator.md` | `my-team/.agents/agents/quiz-creator.md` |
| `.agents/agents/quiz-verifier.md` | `my-team/.agents/agents/quiz-verifier.md` |
| `.agents/skills/quiz-generation-team/SKILL.md` | `my-team/.agents/skills/quiz-generation-team/SKILL.md` |
| `.agents/agents/quiz-html-builder.md` — added in Step 03 | `my-team/.agents/agents/quiz-html-builder.md` |

Click **Download** (the circled downward arrow beside the copy icon) on each Markdown block. Move the downloaded file to the exact destination above, creating missing folders and renaming it to match the `FILE:` label. Remove browser-added suffixes such as `(1)`; both Skill files must be named `SKILL.md` in their separate folders. Open each download and check its frontmatter and complete contents before prompting `Continue`. If a file is incomplete, request its complete replacement before moving to the next dependency.

Step 03 adds the HTML builder and replaces `quiz-generation-team/SKILL.md` at the same destination. Retain the compatible method, creator and verifier. Preserve the earlier entry version outside the active `.agents` directory.

After Step 01, save the first four files in the table. After Step 03, the folder has all five:

```text
my-team/
└── .agents/
    ├── skills/
    │   ├── quiz-generator/SKILL.md
    │   └── quiz-generation-team/SKILL.md
    └── agents/
        ├── quiz-creator.md
        ├── quiz-verifier.md
        └── quiz-html-builder.md   ← added in Step 03
```

The initial team is complete at four saved CURRENT definitions and None pending. In Step 02, create an Antigravity project using this existing `my-team/` folder and test the initial team. Its `.agents` directory must be directly inside the selected project folder. Use Local mode and the original entry from Step 01.

In Step 03, add the HTML builder and replace the team entry, then start a fresh Antigravity chat to test all five files and the interactive page.

[00 Gemini setup](../00-gemini-setup/README.md) · [01 Generate and save](../01-gemini-skill/README.md) · [02 Test the initial team](README.md) · [03 Add and test HTML](../03-debug-and-improve/README.md)
