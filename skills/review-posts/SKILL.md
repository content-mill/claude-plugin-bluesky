---
name: review-posts
description: Show the user's Bluesky posts in Content Mill, meaning what is scheduled, published, failed or still a draft, and cancel a scheduled one. Use when the user asks what is scheduled, what went out, or whether something failed.
user-invocable: true
---

# /content-mill-bluesky:review-posts

Answers "what is happening with my Bluesky posts".

Arguments passed: `$ARGUMENTS` (an optional status such as Scheduled, Published, Failed or Draft, or a time range in words).

## Steps

1. `list_posts` (newest first). Filter with `status` (Draft, Scheduled, Publishing, Published, PartiallyFailed, Failed) when the user asked about one; use `limit` for more or fewer than 20.
2. Summarise by status, with each post's time and the first line of its text. `PartiallyFailed` means some accounts failed.
3. For detail on one post, including the full text and the link to the live post, call `get_post`.
4. To cancel a scheduled post, a draft, or clear a failed one, confirm with the user first, then call `delete_post`. A post that is Publishing, Published or PartiallyFailed cannot be deleted here.

This skill only reads, except for the `delete_post` the user has just approved.
