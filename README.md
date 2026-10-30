# Facilitator Guide Builder

This example shows how an agentic AI system uses project context, instructions, and source materials to develop facilitator guides and check them against defined requirements.

This is the guide-building example from [my AI System for Learning Programs portfolio project](https://clairebrittain.com/ai-workflow-for-learning-programs/).

## What it produces

Use the sample to create:

- **A draft facilitator guide** from the sample slide notes and planning notes.
- **A review table** showing which requirements are met, which issues need attention, and what to do next.

## What's here

```text
.github/
  copilot-instructions.md      Project context and instructions
  skills/
    build-guide/SKILL.md       How to build or revise a guide
    check-guide/SKILL.md       How to review a guide
standard/
  guide-requirements.md        Required content and review labels
  template.md                  Guide structure
  example-guide.md             Fictional worked example
source-materials/
  sample-session/              Slide notes and planning notes
drafts/                        Guides being worked on
records/
  review-findings.md           Review table and next step
  decision-log.md              Confirmed decisions for future guides
finished-guides/               Approved guides
```

Start with the [guide requirements](standard/guide-requirements.md), [template](standard/template.md), and [example guide](standard/example-guide.md). [Build Guide](.github/skills/build-guide/SKILL.md) and [Check Guide](.github/skills/check-guide/SKILL.md) are agent skills: sets of instructions for drafting, revising, and reviewing a guide.

The review uses five labels: **Meets requirement, Missing, Conflicting, Needs clarification, and Inferred**. Their meanings are defined in the guide requirements. A result of **Meets requirement** applies to that check; it does not approve the whole guide.

## About the sample

The notes are fictional and include Lorem Ipsum placeholders and a timing conflict to try the review process. The example guide and review table are illustrative. The sample draft is a starter file; it has not yet been generated or approved.

Guides are saved as Markdown (`.md`) files. This repository does not include a Word-export tool or PowerPoint template.

## Try it

1. Download or clone this repository. Open the folder in a tool that lets an AI assistant read and edit project files, such as VS Code with GitHub Copilot in agent mode. Ask it to read `.github/copilot-instructions.md` before building.
2. Ask it to build the sample:

   > Use `.github/skills/build-guide/SKILL.md` to build a facilitator guide from the slide notes and planning notes in `source-materials/sample-session/`. Replace the starter in `drafts/sample-guide-draft.md` and keep unresolved issues flagged.

3. Ask it to check the draft:

   > Use `.github/skills/check-guide/SKILL.md` to review `drafts/sample-guide-draft.md` against the sources and requirements. Replace the illustrative example in `records/review-findings.md` with one short results table and a **Your next step** sentence. Leave the draft unchanged and tell me which questions I need to resolve.

4. Resolve the open questions. Ask the assistant to apply the corrections you confirm, then recheck the revised guide against the sources and requirements.
5. Review the revised guide. Once you approve it, ask the assistant to save a copy in `finished-guides/`. Decide which findings should change the project instructions or requirements for future guides, and record those decisions in `records/decision-log.md`.

To use your own materials, add a session folder under `source-materials/`, update the requirements and template for your project, and use the new source paths in the prompts.
