# Optional reference — Quiz workflow variation

This variation follows the quiz workflow used in the workshop. It is illustrative guidance,
not a ready-made team or runtime proof.

Start with a natural brief in Gemini:

```text
Design a reusable team that turns a topic list or readable reference material
into a quiz for a defined audience. Ask for missing topics, source material or
question count; use an independent verifier; and leave the final use decision
to a human.
```

The source material belongs to the later Antigravity run. Do not attach a PDF
or other runtime document to Gemini while designing or building the team.

## Design choices

The Builder should help settle:

- required source/topic, audience, question count and format;
- how the input gate pauses and asks for a missing value;
- how `quiz-creator` drafts from supplied material without inventing facts;
- how `quiz-verifier` checks the complete draft against the original source;
- how `REVISE` returns to the creator with a bounded correction count;
- how a human decides whether to use or share a verified quiz; and
- whether `quiz-html-builder` runs only after verifier `PASS`.

Keep the optional HTML worker separate from the verifier. It can format a
verified quiz as one standalone HTML/CSS/JavaScript page, but it must not turn
an unreviewed draft into a publishable result.

## Continue the conversation

When the design is settled:

```text
That flow looks good. Build it for me.
```

When Gemini reports another complete pending file:

```text
Continue.
```

Keep the same chat and the same Gemini Flash model. Download complete Markdown blocks,
not visible excerpts, and save them under the exact paths relative to
`my-team/`.

Later changes remain ordinary conversation. For example:

```text
After the quiz passes review, add a separate worker that produces a standalone
interactive HTML quiz. Preserve the current creator, verifier and human
handoff, and show me the exact file path for every new or replaced definition.
```

Treat a changed definition as a new version. Do not call it installed or
runtime-tested until the complete files pass the static audit and a separate
Antigravity run provides evidence.

## Next

Use the [build example](../build/README.md) to check the file inventory and
save paths, then continue to [Step 02 — Run the quiz team in Antigravity](../../../02-antigravity-setup/README.md).
