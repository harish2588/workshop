---
name: Hello Agent # Human-readable workflow name shown in GitHub Actions
on: # Events that can start this workflow
  workflow_dispatch: # Lets you run the workflow manually while testing
permissions: # GitHub token access the agent needs
  contents: read # Read repository contents
safe-outputs:
  create-issue:
    deduplicate-by-title: true
---

# Community Support Prioritization

Search for all open issues in the repository and find the one with the most 👍 reactions.

If open issues exist:
1. Find the issue with the highest number of 👍 (thumbs up) reactions
2. Post a comment on that issue saying: "This issue has the most community support! We'll prioritise it in our next planning session."

If no open issues exist:
1. Create a new issue titled "Community Voting Test"
2. Post the same comment on the newly created issue