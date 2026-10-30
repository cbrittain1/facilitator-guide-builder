---
name: check-guide
description: Review a facilitator guide against its sources and this repository's design standard, record findings, and recheck confirmed corrections. Use when checking a draft or revised guide for accuracy, completeness, and facilitator usability.
---

# Check a guide

Objective: determine whether the draft follows the standard, uses the source accurately, and gives facilitators actionable guidance.

All project paths below are relative to the repository root.

1. Read `.github/copilot-instructions.md`. Compare the draft with `standard/guide-requirements.md`, `standard/template.md`, `standard/example-guide.md`, the task's session source materials, and applicable confirmed decisions in `records/decision-log.md`. Report sources or speaker notes you cannot access; do not claim to have reviewed them.
2. Check for omissions, unsupported additions, timing conflicts, unclear responsibilities, vague actions, and misplaced preparation tasks. Check whether agenda and segment timings agree; leave unresolved values visible.
3. Read relevant human comments and corrections, if available. Preserve unresolved questions and do not assume every suggestion is an approved change.
4. Leave the draft unchanged during a check unless the user also asks for revisions. Record results in `records/review-findings.md` using the short format below. Replace the labeled starter when asked; otherwise preserve earlier human resolutions when updating the results.

## Write a short review

Identify the draft and version in one line, then write one table:

| Requirement | Result | Finding / next action |
|---|---|---|
| [What was checked] | [Review result] | [Brief finding, source reference, and any question to resolve] |

- Check all applicable requirements. Group straightforward requirements that are met into a concise row where the coverage remains clear. Give each distinct unresolved issue its own row; report it only once.
- Use Meets requirement, Missing, Conflicting, Needs clarification, and Inferred as defined in `standard/guide-requirements.md`. Use only the results supported by this review; do not invent issues to display every label. Briefly explain inapplicable requirements where needed.
- Keep each finding cell to one or two short sentences, with a compact reference such as "Slide 2 notes" or "planning agenda." Preserve enough evidence to locate the issue, without copying full source excerpts.
- After the table, add one **Your next step** sentence naming the decisions or actions needed. Mention an access limitation briefly if it affects the check.
- Do not add separate finding write-ups, repeated summaries, finding IDs, status sections, or a long methods description unless the user requests a detailed audit. Use `records/review-findings.md` as the format example.

## Create the browser review

After saving the review, create or refresh `drafts/sample-review.html` using `standard/review-template.html` and the **Create the HTML review automatically** rules in `.github/copilot-instructions.md`. Include the full draft and this review, with the actual result labels in both sections. Link to the HTML page first. This is part of the check, not an optional follow-up.

Keep the draft unchanged during a review-only task. Formatting the HTML must not change the draft or the review record. Preserve earlier runs when needed, and verify that the HTML shows the files just checked rather than older versions.

## After human feedback

Apply corrections only when requested and confirmed. Recheck affected requirements, record the person's resolution and the recheck briefly in the same table row, and refresh the HTML review. Do not describe an issue as resolved while it remains in the guide. Keep results distinct from progress: a resolution/recheck note does not replace the content result, and Meets requirement is not approval of the whole guide.

Suggest a decision-log entry only when a finding implies a change that applies to future guides. Update the decision log, instructions, or requirements only when authorized. Save a finished guide only after the person approves it, retaining any stated limitations.
