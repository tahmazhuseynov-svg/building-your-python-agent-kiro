---
name: "draft-release-notes"
description: "Draft release notes for the app from its pull requests. Invoke with /draft-release-notes <version> when you want to produce release notes."
---

## Steps
1. Fetch the pull requests from the repository using the GitHub MCP server.
2. Apply the `pr-label-format` skill to categorize each PR.
3. Delegate description cleanup to the `ticket-fetcher` subagent. Pass the PR numbers, titles, and descriptions as the task prompt. Receive the cleaned list.
4. Draft each entry as a single user-facing sentence. Do not invent details, use only what's in the PR title or description.
5. Present the complete draft to the user with the version number `$ARGUMENTS`. Ask: "Review complete. Approve to publish, or reply with edits."
6. Only publish to GitHub releases after receiving explicit approval.