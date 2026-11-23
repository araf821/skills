---
name: pr-comments
description: Review a PR or take a bug someone has reproduced and write a short comment for the line that caused it. Draft in chat and post when asked.
---

# PR comments

Read the PR for intent. What problem does it solve? Does the whole flow work? Is the new code needed? Which existing callers depend on the behavior it changes?

For each finding, verify the trigger on the current head with a focused test or a run through the affected flow. If someone supplied a reproduction, check its revision, steps and observed result. Credit whoever ran it. Skip low-risk issues, very rare edge cases and anything you couldn't verify.

Return one draft per root cause, most consequential first. Put the exact `path/to/file:line` above each comment. Anchor it to the changed line responsible for the failure. For a deletion, identify the base-side line. Write three short paragraphs in a plain teammate voice:

1. Say what breaks for the person using it.
2. Give one sentence with the steps and the result you observed.
3. Ask for the behavior that would fix it. Leave room for the author to choose the implementation.

Example draft:

> `src/drafts/save.ts:42`
>
> Saving an existing draft clears its title.
>
> e.g. after I changed one word in the body and saved the draft, I reopened it and found the title blank.
>
> Can we keep the saved title when only the body changes?

Leave drafts in chat unless the user asks to post them. “Leave comments” authorizes posting. Before submitting, refresh the PR head, verify the anchors against the diff and check existing threads for the same issue. Re-test findings affected by new commits.

Submit the new comments together in one review. Request changes when an outstanding verified issue should block merging. Otherwise use a comment review. If there's nothing to raise, say so in chat. If submission fails or times out, check what landed before retrying. Return the review link and mention any comments you couldn't place.
