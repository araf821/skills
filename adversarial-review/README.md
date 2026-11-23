# Adversarial review

Use this when you want a second pair of eyes on what a PR might break. Say a PR changes how drafts are saved. I'd want to know if I can still open a draft I wrote yesterday, edit it, and get my changes back when I refresh.

```text
Use $adversarial-review on this PR. Try editing a draft saved before the migration.
```

You can give it a branch, a commit, or your local changes too. It only flags a bug if it can make it happen in a scenario people would reasonably run into. You get the line that caused it, the steps to see it yourself, and what needs fixing. Small stuff and very rare edge cases get skipped.

Use [pr-comments](../pr-comments/) if you want those findings written up for the PR.
