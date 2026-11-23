---
name: pr-description
description: Write or update a pull request description from its diff and verification notes.
---

# PR descriptions

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
