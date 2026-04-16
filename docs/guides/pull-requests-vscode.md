# Managing pull requests from VS Code

This guide explains how to create, review, and merge pull requests without leaving VS Code, using the [`GitHub Pull Requests`](https://marketplace.visualstudio.com/items?itemName=GitHub.vscode-pull-request-github) extension.

## Prerequisites

- [VS Code](https://code.visualstudio.com/) installed.
- [`GitHub Pull Requests`](https://marketplace.visualstudio.com/items?itemName=GitHub.vscode-pull-request-github) extension installed.
- Your fork cloned locally and a branch ready to submit.

## Step by step

1. **Sign in to GitHub**: Open the Accounts menu (bottom-left of VS Code) and sign in with your GitHub account if you have not done so already.

2. **Push your branch**: In the Source Control panel, click the cloud icon or run:

   ```bash
   git push origin feature/feature-name
   ```

3. **Create the pull request**: A notification will appear offering to create a PR. Alternatively, click the **GitHub Pull Requests** icon in the Activity Bar (left sidebar), then click **Create Pull Request**.

4. **Fill in the details**: Set the target branch (`main`), write a title and description, and click **Create**.

5. **Review the PR**: The pull request opens inside VS Code. You can read comments, browse changed files, and reply to reviewers without leaving the editor.

6. **Merge the pull request**: Once approved, click **Merge Pull Request** inside the PR view. Choose your merge strategy (merge commit, squash, or rebase) and confirm.

7. **Clean up**: After merging, delete the remote branch when prompted and run:

   ```bash
   git checkout main
   git pull origin main
   git branch -d feature/feature-name
   ```
