---
name: pr-description
description: Write or update a pull request description from the diff, or draft a bug report from investigation notes. Use when someone asks for a PR body or issue description.
---

# PR and issue descriptions

## Pull requests

Read the final diff and any verification notes. If you're editing an existing PR, read its current body first. Preserve automated review sections from Greptile, Cursor and other tools exactly, including their markers. Edit only the human-written sections. Before saving, check the latest body so a bot update survives the edit.

Under **What changed**, give each distinct change a numbered heading. One heading is enough for a simple PR. Group commits that fix the same problem. Write for a reviewer who hasn't read the conversation. Keep each bullet to one short sentence, ideally one line on GitHub. Use a concrete example when it helps. Skip em dashes and keep implementation detail to what explains the fix or its risk.

```markdown
## What changed

### 1. [Short description of the change]

- **Problem:** [What was broken or unexpected?]
- **Expected:** [What should the user experience?]
- **Fix:** [What changed to make that happen?]

## Validation

[One or two sentences on the checks performed and any material limitation.]
```

Keep test counts, command logs and individual cases out of the summary. Be precise about what you verified. Passing tests, checking a live flow, deploying and being ready to merge are separate claims.

## Bug reports

Title the issue with the problem someone would recognize. Use the five headings below, with one short paragraph each. Give enough context to follow the report without reading code or the investigation chat.

```markdown
## What happens

[What does the user see, and how does it affect them?]

## When it happens

[Which action, data or condition triggers it?]

## Why

[Explain the confirmed cause in plain language. Say what's still unknown.]

## How often

[Give the observed scope or frequency, with verified counts, dates and evidence links where available. If frequency is unknown, say so.]

## Expected

[What should the user experience instead?]
```

A local reproduction establishes what you could trigger. Connecting it to a customer's report or estimating production frequency takes separate evidence. Save implementation checklists, test inventories and validation results for the PR.
