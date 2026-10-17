# Facilitator Guide Builder

A demonstration of using project context, design requirements, and AI skills to turn source materials into facilitator guides, with human review throughout development.

This is the guide-building example from [my AI System for Learning Programs portfolio project](https://clairebrittain.com/ai-workflow-for-learning-programs/).

## What you get

- **A draft facilitator guide**, built from the sample slide notes and planning notes.
- **A short results table**, showing what meets the requirements and what needs your attention, followed by your next step.

You resolve the open questions, request corrections, and review the revised guide before approving it.

## What's here

```text
.github/
  copilot-instructions.md       Shared project guidance
  skills/
    build-guide/SKILL.md        How to build or revise a guide
    check-guide/SKILL.md        How to review a guide
standard/
  guide-requirements.md         Required content and review labels
  template.md                   Guide structure
  example-guide.md              Fictional worked example
source-materials/
  sample-session/               Slide notes and planning notes
drafts/                        Guides being worked on
records/
  review-findings.md             Short results table and next step
  decision-log.md                Decisions for future guides
finished-guides/                 Where approved guides go
```

Start with the [guide requirements](standard/guide-requirements.md), [template](standard/template.md), and [example guide](standard/example-guide.md). The [Build Guide](.github/skills/build-guide/SKILL.md) and [Check Guide](.github/skills/check-guide/SKILL.md) skills explain how to use them.

The requirements define five review results: **Meets requirement, Missing, Conflicting, Needs clarification, and Inferred**. Findings stay visible for human review; a positive result does not approve the whole guide.

## Try it

1. Open the repository in an assistant that can read and write project files, such as VS Code with Copilot in agent mode. Have it read `.github/copilot-instructions.md` and the relevant skill if they aren't discovered automatically.
2. Ask it to build the sample:

   > Use `.github/skills/build-guide/SKILL.md` to build a facilitator guide from the slide notes and planning notes in `source-materials/sample-session/`. Replace the starter in `drafts/sample-guide-draft.md` and keep unresolved issues flagged.

3. Ask it to check the draft:

   > Use `.github/skills/check-guide/SKILL.md` to review `drafts/sample-guide-draft.md` against the sources and requirements. Replace the illustrative example in `records/review-findings.md` with one short results table and a Your next step sentence. Leave the draft unchanged and open questions for me to resolve.

4. Review the findings, confirm corrections, and check the revised guide. Once you approve it, ask the assistant to save a copy in `finished-guides/`. Decide separately whether a finding should change the instructions or requirements for future guides.

To use your own materials, add a session folder under `source-materials/`, adapt the standard, and use those paths in the prompts.

## Sample status

This is a demonstration starter with fictional notes and Lorem Ipsum placeholders. The example guide and review record are illustrative; the sample draft has not yet been generated or approved. The sample includes a timing conflict for trying the review process.

The starter produces Markdown guides. No PowerPoint template or Word-export tool is included.
