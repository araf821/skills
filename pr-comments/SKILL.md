---
name: pr-comments
description: Turn findings from a completed code review into short, line-specific PR comments. Requires existing findings. Draft in chat and post when asked.
---

# PR comments

Start with findings from an earlier review. Use the review already in the conversation, a linked report, or findings the user pastes. If all you have is a PR link, ask for the review findings and stop. If the review found nothing, say there are no comments to draft.

Work through the supplied findings only. Check each reproduction against the current PR head. Re-run the relevant steps if the code changed or the evidence is incomplete. Credit whoever ran the check. Skip low-risk issues, very rare edge cases and anything you couldn't verify.

Return one draft per root cause, most consequential first. Put the exact `path/to/file:line` above each comment. Anchor it to the changed line responsible for the failure. For a deletion, identify the base-side line. Write three lines, one sentence each. Use these lengths as a guide:

1. **Issue** (about 5–15 words). Say what breaks for the person using it.
2. **Example** (about 10–30 words). Start with “e.g.” and give the trigger and observed result.
3. **Ask** (about 5–20 words). Ask for one change in behavior. Leave the implementation to the author.

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
