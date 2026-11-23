# PR comments

Use this when you want feedback you can leave on a specific line of a pull request. Give it a PR to review or findings you've already reproduced, including findings from [adversarial-review](../adversarial-review/).

```text
Use $pr-comments on PR #42 and draft the comments.
```

By default, you get drafts in chat. Each starts with the exact file and line, followed by three short paragraphs covering what breaks, how to reproduce it, and the change you're asking for.

When you're ready to post, say `Leave the comments on PR #42`. The skill checks the current diff and existing threads, posts new findings together, and requests changes if a verified issue should block the merge.
