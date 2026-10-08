# Facilitator Guide Builder

A starter workflow for turning slide notes and planning notes into facilitator-ready session guides with AI assistance and human review.

The goal is repeatability: define a standard, apply it to source materials, check the draft, and carry useful review decisions into future guides.

## Status

This is a portfolio prototype. The sample materials are fictional and include Lorem Ipsum placeholders. The worked example is illustrative; it is not evidence of an actual program delivery or completed review. The sample draft and records are starter files to replace as you try the workflow.

## How it works

**Sources + standard + instructions → draft → review findings → finished guide**

AI flags missing, conflicting, or inferred information. A person resolves the findings and checks the revised guide. Decisions that apply to future guides are recorded and incorporated into the instructions.

## What's here

```text
README.md
.github/
  copilot-instructions.md        Where Copilot starts
standard/
  template.md                   The guide structure
  example-guide.md              A fictional worked example
ai-instructions/
  build-guide.md                How to build
  check-guide.md                How to check
source-materials/
  sample-session/
    slide-notes.md              Sample slide content and speaker notes
    planning-notes.md           Timing, roles, and logistics
drafts/
  sample-guide-draft.md          Starter draft to replace on the first run
records/
  review-findings.md             What needs checking and how it was resolved
  decision-log.md                Decisions that apply to future guides
finished-guides/
  README.md                     Where reviewed guides go
```

## Try it

1. Download or clone the repo and open it in an AI-enabled editor, such as VS Code with GitHub Copilot. You can also use another assistant that can read and write the project files; explicitly tell it to read the instructions.
2. Look at [the template](standard/template.md) and [the example guide](standard/example-guide.md).
3. Ask the assistant to build the sample:

   > Read `.github/copilot-instructions.md`, `ai-instructions/build-guide.md`, and the files in `standard/`. Build a guide from `source-materials/sample-session/`. Replace the labeled starter in `drafts/sample-guide-draft.md`. Keep uncertainty visible.

4. Ask it to check the result:

   > Check `drafts/sample-guide-draft.md` using `ai-instructions/check-guide.md`, the standard, and the source materials. Replace the illustrative finding in `records/review-findings.md` with findings from this draft. Do not resolve open questions on my behalf.

5. Read the findings, add your own feedback, and tell the assistant what to correct. For example:

   > For F-001, use [confirmed duration] because [reason]. Apply that correction to the draft and record my resolution. Leave the other findings open.

6. Check the revision yourself. When satisfied, ask:

   > I have reviewed and approved this draft. Save a copy in `finished-guides/sample-guide.md`. Suggest any reusable decisions for `records/decision-log.md`; add them and update the instructions only after I confirm them.

The sample intentionally contains different durations for one activity. A successful check should surface that conflict rather than silently choose a duration.

## Use your own materials

Create a new session folder in `source-materials/` and add slide content, speaker notes, and planning notes. Adapt the standard to your program, then repeat the build and check prompts with the new paths. Identify the session and draft version in the review records.

Use content you can share. Remove private names, working links, participant information, and internal program details before publishing source materials or outputs.

## File format

This starter produces Markdown guides. No Word-export script is included. A future version can use a Word template and a documented export tool, with a check that the exported document preserves the approved content and layout.

## What this demonstrates

- A visible standard for facilitator guidance.
- Instructions for transforming sources into practical actions.
- Guardrails that surface uncertainty and avoid unsupported additions.
- A review process that distinguishes fixes to one guide from changes to the workflow.

The finished walkthrough will show an actual generated draft, documented review, and the resulting guide once that sample run is complete.
