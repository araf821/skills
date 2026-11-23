# Adversarial review

Use this when you want to find consequential bugs in a PR, branch, commit, or local diff. It's a good fit when a change touches saved data, retries, or behavior that several callers rely on.

```text
Use $adversarial-review on my local changes. Check whether existing drafts still open after the migration.
```

Each finding includes the exact file and line, what broke, how to reproduce it, and what needs to change. The reviewer skips low-risk issues and very rare edge cases. If a blocked check leaves a flow untested, the review says which one.

To turn the findings into inline review comments, pair it with [pr-comments](../pr-comments/).
