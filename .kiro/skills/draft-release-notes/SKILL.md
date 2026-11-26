---
name: "draft-release-notes"
description: "Draft release notes for the app from its pull requests. Invoke with /draft-release-notes <version> when you want to produce release notes."
---

## Steps
1. Fetch the pull requests from the repository using the GitHub MCP server.
2. Apply the `pr-label-format` skill to categorize each PR.
3. Group PRs into Features, Fixes, and Improvements.
4. Draft each entry as a single user-facing sentence. Do not invent details, use only what's in the PR title or description.
5. Present the complete draft to the user with the version number `$ARGUMENTS`. Ask: "Review complete. Approve to publish, or reply with edits."
6. Only publish to GitHub releases after receiving explicit approval.