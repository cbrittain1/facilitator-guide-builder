# Facilitator Guide Builder

This example shows how an agentic AI system uses project context, instructions, and source materials to develop facilitator guides and check them against defined requirements.

This is the guide-building example from my [Agentic Framework for Learning Programs](https://clairebrittain.com/ai-workflow-for-learning-programs/) portfolio project.

## Start the sample

1. Select **Code → Download ZIP** on this repository's main page, then extract the ZIP.
2. In VS Code, open the extracted project folder that contains this `README.md`.
3. Open GitHub Copilot Chat and select **Agent** mode.
4. Copy the whole prompt below into the chat and send it.

```text
Read README.md and .github/copilot-instructions.md.

First verify that both skill files below exist. If either is missing, report the missing path and stop.

Use the Build Guide skill at .github/skills/build-guide/SKILL.md to create a facilitator guide from source-materials/sample-session/. Replace the starter in drafts/sample-guide-draft.md.

Then use the Check Guide skill at .github/skills/check-guide/SKILL.md to review it. Replace the illustrative review in records/review-findings.md with the actual findings.

If an output already contains work from a previous run, save a new version rather than overwriting it. Report the paths you used.

Keep the source files and project instructions unchanged. Leave unresolved questions visible and keep the guide unapproved.

Show me the draft and review, explain which decisions you need from me, and stop.
```

## What it produces

The prompt creates two files:

- **An AI-generated draft facilitator guide** from the sample slide notes and planning notes.
- **A review table** showing which requirements are met, which issues need attention, and what to do next.

The agent creates a first draft from your materials. You review and refine it into a guide for leading the session, with an agenda, clear instructions, timing, and resources.

### After the first run

1. Read the guide and review table. Answer the open questions and confirm any corrections.
2. Ask Copilot to apply those decisions and recheck the revised guide.
3. Once you approve it, ask Copilot to save a copy in `finished-guides/`.

## Use it for your own project

You bring the content and work with the agent to explain the project and define the result you want. Four inputs help:

- **Source materials — what to work from:** Session outlines, slide and speaker notes, planning or meeting notes, activity instructions, and resource links. Relevant feedback and debrief notes can also inform the work.
- **Context and goal — what the work is for:** Who will use the guide, what the session should achieve, and how it will be delivered.
- **Examples — what a good result looks like:** A finished guide you like, a template, or sample instructions. Explain what to follow, such as the structure, tone, or level of detail. Example content should not become facts about a different session.
- **Requirements — what the result must include:** Required fields, timing, materials, delivery details, and any writing or accessibility standards relevant to the project.

Add your session content under `source-materials/`, provide files your assistant can read, and tell it which files to use. This sample uses text notes. Update `standard/guide-requirements.md` and `standard/template.md` to reflect your project.

Build Guide and Check Guide hold the instructions for how the agent works. You can develop these skills further as you review results, adding or refining guidance that should apply to future guides. Keep one-session corrections with that session's review.

## About the sample

The notes are fictional and include Lorem Ipsum placeholders and a timing conflict to try the review process. The included draft is a starter file; the example guide and review table are illustrative. There is no actual slide deck in this sample, only text notes. Its placeholders and missing deck mean it is not ready for live delivery.

Guides are saved as Markdown (`.md`) files. You can open them in VS Code's Markdown preview to see the headings, lists, and tables. This repository does not include a Word-export tool or PowerPoint template.

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

The [guide requirements](standard/guide-requirements.md), [template](standard/template.md), and [example guide](standard/example-guide.md) define the expected content, structure, and detail. [Build Guide](.github/skills/build-guide/SKILL.md) and [Check Guide](.github/skills/check-guide/SKILL.md) are agent skills: sets of instructions for drafting, revising, and reviewing a guide.

The review uses five labels: **Meets requirement, Missing, Conflicting, Needs clarification, and Inferred**. Their meanings are defined in the guide requirements. A result of **Meets requirement** applies to that check; it does not approve the whole guide.
