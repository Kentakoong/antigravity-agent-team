# Step 03 — Add an interactive quiz page

Turn the reviewed quiz into a page where students can select answers and see their score and explanations.

## 1. Ask Gemini for the change

Return to the **same Gemini chat** used in Step 01. Keep **Flash** selected and send:

```text
Could we extend it so that, after the quiz passes review, it becomes a standalone interactive HTML quiz?
```

Check that Gemini proposes creating the page **after** the quiz has been checked.

![Gemini proposes the interactive quiz page](../assets/gemini/03-html-proposal.png)

## 2. Apply and download the new file

When the proposal looks right, send:

```text
apply
```

Gemini generates `quiz-html-builder.md`. This file tells the team how to turn a checked quiz into an interactive page.

Click **Download** beside the copy icon on the Markdown block. Move the downloaded file to:

```text
my-team/.agents/agents/quiz-html-builder.md
```

Rename it to `quiz-html-builder.md` if needed.

![Gemini generates the new HTML-builder file](../assets/gemini/03-html-apply.png)

## 3. Download the updated team instructions

In the same Gemini chat, send:

```text
Continue
```

Gemini generates an updated `SKILL.md`. This tells the team to create the interactive page after the quiz passes review.

Keep a backup of the old file outside the `.agents` folder. Download the new file and replace:

```text
my-team/.agents/skills/quiz-generation-team/SKILL.md
```

Name it exactly `SKILL.md`. Keep the existing quiz method, creator and verifier files unchanged.

## 4. Check that Gemini is finished

Download and save each file before requesting the next one. Send `Continue` only while something remains pending.

You are finished when:

- All five team files are saved, including the new HTML builder and updated team instructions.
- Every listed component says **CURRENT**.
- Gemini says **Next Pending Component: None**.

![All five files are current and nothing remains pending](../assets/gemini/03-html-complete.png)

If a file is missing or incomplete, ask Gemini for the complete file before moving on. These screenshots show the example conversation; your own files still need to be downloaded and saved.

## Try the updated team in Antigravity

Use [the Antigravity walkthrough](../02-antigravity-setup/README.md) to open your project and test the updated team with **Gemini 3.6 Flash**. If you already ran the team, start a fresh chat, select `quiz-generation-team`, and try the same quiz request again. Check the saved page's answers, score and explanations.

For other changes, [these optional prompts](repair-prompts.md) explain what to send in Gemini and what to ask directly in Antigravity.
