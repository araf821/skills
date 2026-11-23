---
name: adversarial-review
description: Review a PR, branch, commit, or local diff for consequential bugs. Trace real callers, challenge suspected failures, and report only issues you can reproduce.
---

# Adversarial review

Start with the problem the change is meant to solve. Read the full diff at the exact base and head. For local work, include the intended uncommitted changes and keep the author's checkout intact.

Follow a real caller through the changed code to the result someone depends on. Look twice at writes, retries and old data that the new code still has to read. Skip low-risk issues and very rare edge cases, even when you can make a test fail.

Review the change before reading other reviewers' findings. Where independent review is available, have one reviewer follow the intended behavior and another look for ways it breaks. Otherwise make both passes yourself. For each suspected bug, look for the guard, caller contract or fallback that would disprove it.

Recreate the failure on the reviewed revision. Run a focused test, a minimal local example or the actual user flow. Record the steps, expected result and observed result. Use a nearby working case to check the setup. For a regression, run the same steps on the base when possible. If the base also fails, establish what the change makes worse before reporting it. A mock that supplies the failure you predicted proves nothing about whether the application produces it.

Keep findings that meet all three conditions:

- A supported, realistic workflow reaches the changed behavior.
- The failure costs someone data, money, access, time on a core task or another material outcome.
- You observed that failure and can tell the author how to repeat it.

Check existing threads for duplicates and refresh the head before reporting. Recheck affected findings if it moved. Lead with the highest-impact finding. Give the exact file and line, consequence, reproduction and requested change. Group symptoms with the same cause. If nothing qualifies, say so. If a check was blocked, briefly name the untested flow and why.

Return the review in chat by default. When used with pr-comments, use its comment format and posting rules.

The independent review approach draws on [ng/adversarial-review](https://github.com/ng/adversarial-review/tree/6aff53cbc1e66e7b5f588fb5526da52b77695f54).
