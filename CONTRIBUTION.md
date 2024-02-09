# Step-by-Step Guide for Code Contribution

## Step 1: Declare Your Work

### Identify the Story

Before starting your work, ensure you have a story assigned to you that details the change. The story should include a clear description of the work, acceptance criteria, and any relevant context. The story should also be linked to the relevant Epic or Sprint.

The description should include a user story, such as:\
```As a [type of user], I want [an action] so that [a benefit].```

Example:\
```As a user, I want to be able to search for products so that I can find what I need quickly.```

Note the story ID, such as `ABCD-1234`, which will be used in your branch name and commit messages.

### Create the Feature Branch

From the main branch, create a new branch for your work. Name the branch by following the convention:
```feature/JIRA-ID-description-of-work```
Replace type with the change type (feature, fix, hotfix, bugfix.)\
Example: If you're working on a new feature to improve XYZ and your story ID is ABCD-1234, your branch name would be: `feature/ABCD-1234-improve-xyz`

## Step 2: Work on Your Feature

1. Perform the necessary code changes within your feature branch.
2. Commit Your Changes: Use the conventional commit format for your commit messages. This includes a prefix (feat, fix, etc.), a concise description, and the Jira story ID in square brackets.
Example commit message:
```feat: improve xyz [ABCD-1234]```
3. Push your changes to your repository regularly to ensure your work is backed up and accessible to the team. While actively working on a feature, multiple commits are expected even if they undo or refactor prior work. However, ensure each commit is a logical unit of work and follows the commit message format.

## Step 3: Create a Pull Request (PR)

In your repository, create a new PR from your feature branch to the main branch. Ensure the PR title follows the same format as your commits, with the type, description, and Jira story ID.
Example PR title:
```feat: improved xyz [ABCD-1234]```

Complete the following PR body template to provide context and details about your changes. This will help reviewers understand the purpose of your work and how to test it. Include any relevant screenshots if applicable.

```markdown
# type: description [ABCD-1234]

## What does this PR do?

A brief description of the changes and why they were made.

## Why are we doing this?

A brief explanation of the problem or opportunity.

## How can this be tested?

A brief description of how to test the changes.

## Any background context you want to provide?

Any additional information that may be helpful.

## Screenshots (if appropriate)

If applicable, add screenshots to help explain or verify the changes.
```

## Step 4: Code Review and Approval

1. Request Reviewers: Select at least two team members to review your PR. Ensure they are aware of the policy requiring two approvals.
2. Address Feedback: If any reviewer requests changes, make the necessary updates to your branch. Continue to communicate within the PR until all concerns are resolved and approvals are given.

## Step 5: CI/CD Checks and Merging

1. Pass CI/CD Pipeline: Ensure your PR triggers the CI/CD pipeline and passes all automated tests and checks.
2. Final Approval: Once your PR has at least two approvals, all checks pass, and it's linked to a successfully passed CI/CD build, you can merge the PR. By default, merge the PR using the "Squash and Merge" option to keep the commit history clean and concise.
3. Close the Story: After merging, ensure the corresponding Story is updated to reflect the completion of the work and then close the story.

## Step 6: Cleanup

Delete the Feature Branch: After the PR is merged, delete the feature branch to keep the repository clean.
