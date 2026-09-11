# Managing pull requests from VS Code

This guide explains how to create, review, and merge pull requests without leaving VS Code, using the [`GitHub Pull Requests`](https://marketplace.visualstudio.com/items?itemName=GitHub.vscode-pull-request-github) extension.

## Prerequisites

- [VS Code](https://code.visualstudio.com/) installed.
- [`GitHub Pull Requests`](https://marketplace.visualstudio.com/items?itemName=GitHub.vscode-pull-request-github) extension installed.
- Your fork cloned locally and a branch ready to submit.


## Part 1 — Creator: open a pull request

These steps are done by the person who made the changes and wants them reviewed.

1. **Sign in to GitHub**: Open the Accounts menu (bottom-left of VS Code) and sign in with your GitHub account if you have not done so already.

2. **Push your branch to the remote**: Make sure your branch is published and up to date on the remote repository.

3. **Create the pull request**: In the **GitHub Pull Requests** panel (Activity Bar, left side), click **Create Pull Request**. A form opens inside VS Code.

4. **Fill in the details**: Set the target branch (`main`), write a title and description, and click **Create**.

   > **Tip**: Click the ✨ button next to the title field to let GitHub Copilot suggest a title. The suggestion will follow the Conventional Commits convention configured in `.vscode/settings.json`.
   >
   > The description field will be pre-filled with the project template from `.github/pull_request_template.md` once it is merged into `main`.

## Part 2 — Reviewer: review the pull request

These steps are done by the person responsible for approving the changes.

5. **Open the PR**: In the **GitHub Pull Requests** panel, find the PR and click it. The PR view opens in the editor.

6. **Review the changes**: In the **CHANGES IN PULL REQUEST** panel, click any file to open its diff and inspect the changes. No need to mark them — it is just for reading.

7. **Leave a review comment**: In the **REVIEW PULL REQUEST** panel (left side, below the files list), write an optional comment and click **Comment**.

## Part 3 — Creator: merge and clean up

Once the PR is approved, the creator merges it.

8. **Merge the pull request**: There are two places to do this:

   - **Left panel** (REVIEW PULL REQUEST): click the dropdown arrow next to **Create Merge Commit**, select **Squash and Merge**, then click **Merge Pull Request**.
   - **Right panel** (scrolling down): find the **Merge Pull Request** section, change the method to **Squash and Merge**, then click **Merge Pull Request**.

   In both cases, a confirmation step appears where you can review and edit the commit message and description. Once ready, click **Squash and Merge** to confirm. This produces a single commit in `main`.

9. **Clean up**: After merging, click **Delete Branch...** at the bottom of the left panel in the **GitHub Pull Requests** view. It will offer to delete both the local and remote branch — confirm both. Then pull the latest `main`:

   ```bash
   git checkout main
   git pull origin main
   ```

---

## Simplified workflow: when you don't know what the branch will contain yet

With **Squash and Merge**, the commit messages inside your branch do not matter — the only commit that reaches `main` is the PR title you write at merge time. This means you can work freely without worrying about branch names or commit messages upfront.

1. **Create a temporary branch** including your username, the date, and a short description:

   ```bash
   git checkout -b wip/$(git config user.name | tr ' ' '-')/$(date +%Y%m%d)-your-description
   ```

   For example: `wip/jesus/20260416-update-docs`.

2. **Commit freely** as you work — message quality does not matter here, they will be squashed.

3. **Push the branch** to the remote when ready.

4. **Create the PR** and use the ✨ button to let Copilot suggest the title. That title will become the single commit message in `main`.

5. **Merge with Squash and Merge** — review and edit the commit message if needed, then confirm.

The branch name and intermediate commits disappear after the merge. Only the PR title survives in `main`.

