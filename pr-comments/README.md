# PR comments

Run a code review first. Then give this skill the findings you want written up as PR comments. It can use findings already in the chat, a pasted list, or a linked report from another agent or review skill, including [adversarial-review](../adversarial-review/).

```text
Use $pr-comments to turn the findings above into draft comments for PR #42.
```

Each draft gives the exact file and line, then three sentences:

- **Issue** (about 5–15 words). What broke?
- **Example** (about 10–30 words). Start with “e.g.” and say what happened when someone tried it.
- **Ask** (about 5–20 words). What should change?

Drafts stay in chat. Say `Leave the comments on PR #42` to post them. The skill checks the latest code, skips issues already covered in a thread, and requests changes if something needs fixing before merge.
