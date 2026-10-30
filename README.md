# Facilitator Guide Builder

This example uses an agentic AI system to build facilitator guides from your materials and check them against your requirements.

This sample is part of my [Agentic Framework for Learning Programs](https://clairebrittain.com/ai-workflow-for-learning-programs/) portfolio project.

You can try the sample without writing your own prompts.

## Start here

You need Visual Studio Code and a GitHub account with Copilot access.

<details>
<summary>Setup: open the project in Visual Studio Code</summary>

1. If needed, [download and install Visual Studio Code](https://code.visualstudio.com/download).
2. [Sign in to GitHub Copilot](https://code.visualstudio.com/docs/setup/copilot) in Visual Studio Code.
3. On this repository's main page, select **Code → Download ZIP**, then extract the ZIP.
4. In Visual Studio Code, choose **File → Open Folder…**. Select the extracted project folder containing `README.md` and `.github`.
5. Open GitHub Copilot Chat and select **Agent** mode.

**File → Open Folder…**

<img src="docs/images/visual-studio-code-open-folder.png" alt="Visual Studio Code File menu showing Open Folder below Open File." width="300">

</details>

In Copilot Chat, select **Agent** and paste:

```text
Read README.md and .github/copilot-instructions.md, then help me get started.
```

Copilot asks:

> Would you like to try the fictional sample or start with your own materials?

Select an option, or type your choice if no options appear:

- **Try the sample:** Copilot drafts and checks a guide using the included notes, then asks you to resolve any questions.
- **Use my own materials:** Copilot asks about your goal and files, then helps you organize them and develop the requirements and skills.

Copilot waits for your choice before creating files.

To run the sample without the welcome, expand **Run the sample directly** below.

## Sample output

The sample creates two files:

- **Draft guide:** AI writes a guide from the sample slide notes and planning notes.
- **Review table:** Copilot lists requirements met, issues to resolve, and your next step.

The goal is a guide you can use to lead a session, with an agenda, instructions, timing, and resources.

### Review and revise

1. Read both files. Answer the questions and explain what to change.
2. Ask Copilot to revise the guide and check it again.
3. When you approve the guide, ask Copilot to save a copy in `finished-guides/`.

<details>
<summary>Use it for your own project</summary>

Tell Copilot what you want to create and what files you have. Ask it to help organize the files and develop the requirements and skills.

> Help me organize these materials and work out the requirements and skills for this project.

Provide:

- **Source materials:** Session outlines, slide and speaker notes, planning notes, activity instructions, resource links, and relevant feedback.
- **Context and goal:** Who will use the guide, what the session should achieve, and how it will run.
- **Examples:** A guide or template you like. Explain which structure, tone, or detail to follow. Keep its content separate from facts about your session.
- **Requirements:** What the guide must include, such as timing, materials, delivery details, and writing or accessibility standards.

Add files Copilot can read under `source-materials/` and tell it which ones to use. Ask it to help update `standard/guide-requirements.md` and `standard/template.md` for your project.

The Build Guide and Check Guide skills tell Copilot how to draft and review. As you review results, update instructions that should apply to future guides. Save context and instructions in the project files. Keep decisions for one session in that session's review.

</details>

## About the sample

- The sample uses fictional text notes, not an actual slide deck.
- It includes filler text (Lorem Ipsum) and a timing conflict to test the review.
- The draft and review record are starter files. The example guide shows the format.
- The sample is not ready for live delivery.

Guides are Markdown (`.md`) files. Use Markdown Preview in Visual Studio Code to see the formatted guide. No Word-export tool or PowerPoint template is included.

<details>
<summary>What's here</summary>

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

- [Guide requirements](standard/guide-requirements.md): What a guide must include and how to check it.
- [Template](standard/template.md): The guide layout.
- [Example guide](standard/example-guide.md): The expected detail.
- [Build Guide](.github/skills/build-guide/SKILL.md) and [Check Guide](.github/skills/check-guide/SKILL.md): Agent skills with instructions for drafting, revising, and reviewing guides.

The five review labels are **Meets requirement, Missing, Conflicting, Needs clarification, and Inferred**. The guide requirements explain each label. **Meets requirement** applies to one check. You decide when the whole guide is ready to approve.

</details>

<details>
<summary>Run the sample directly</summary>

Paste this prompt into Copilot Chat in Agent mode to build and check the sample without the welcome:

```text
Read README.md and .github/copilot-instructions.md.

First check that both skill files below exist. If either is missing, report its path and stop.

Use .github/skills/build-guide/SKILL.md to draft a guide from source-materials/sample-session/. Replace the starter in drafts/sample-guide-draft.md.

Then use .github/skills/check-guide/SKILL.md to check the draft against the sources and requirements. Replace the example in records/review-findings.md with your findings.

Save new versions of any existing work. Report the output paths.

Keep source files and project instructions unchanged. Leave unresolved questions visible. Do not approve the guide.

Show me the draft and review. List the questions I need to resolve, then stop.
```

</details>
