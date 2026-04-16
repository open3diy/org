# Contributing to open3diy.org

Thank you for your interest in contributing to the DIY-experiences repository!

This project is licensed under the [**Creative Commons Zero v1.0 Universal (CC0)**](https://creativecommons.org/publicdomain/zero/1.0/) license, dedicating the work to the public domain and helping expand a freely accessible knowledge base for all.

## Contribution Guidelines

### Attribution

Always provide proper credit if you are including material or content from external sources.

### Style

Please review the style guidelines in `.github/copilot-instructions.md`.

Keep the style and structure in English, but content may be in your preferred language.

  > **Let's make everyone feel comfortable with their language.**

### License

- By contributing, you agree that your work will be dedicated to the public domain under the **Creative Commons Zero v1.0 Universal (CC0)** license.

## Code of Conduct

See our [Code of Conduct](CODE_OF_CONDUCT.md) document.

## How to Contribute

### Reporting Issues

- If you find errors or have suggestions for improvement, please create an issue in the repository.
- Clearly describe the problem, including steps to reproduce if applicable.

### If you contribute to the source code

Please review how to create branches in `.github/copilot-instructions.md`.

#### Creating git branches

The following details how to make change requests in existing repositories or create new repositories following the [GitHub Flow](https://docs.github.com/en/get-started/using-github/github-flow). Inspired by **[a successful Git branching model](https://nvie.com/posts/a-successful-git-branching-model/)**, the following branch naming convention will be used:

- **Feature branches**: For new functionalities. Example: `feature/chapter-1-ipfs` or `feature/install-proxy`.
- **Bugfix branches**: For fixing issues. Example: `bugfix/issue-123` or `bugfix/review-inconsistent-steps`.
- **Repository documentation**: For changes to repository documentation. Example: `docs/initial-documentation`.

  > Internal repository documentation, instruction-based documentation is a feature.

- **Experiments**: For testing ideas or experiments that might not be included. Example: `experiment/test-alternative-installation`.

Branch names must use English keywords in `kebab-case`, with sections separated only by `-`.

#### Making git commits

[Conventional Commits](https://www.conventionalcommits.org/) is used to write commit messages in English. Note that `init` and `security` are local extensions to the Conventional Commits specification. Examples:

- `init`: for the start of a project or module, creating the structure, if no actual content has been added:

   ```plaintext
   init: initialize project with base structure
   ```

- `feat`: for new functionalities:

   ```plaintext
   feat: first draft section on how to create ipfs node
   ```

   > Even if the functionality is documentation or instructions, it is understood as functional content.

- `refactor`: for restructuring without changing functionality:

   ```plaintext
   refactor: clarify explanation instructions module xyz
   ```

- `revert`: to revert a previous change:

   ```plaintext
   revert: revert commit 1234abcd due to causing errors
   ```

- `fix`: to specify a correction of a `bug`:

   ```plaintext
   fix: resolve issue 123 section xyz
   ```

- `security`: to specify that security features or aspects are reviewed:

   ```plaintext
   security: critical security indication for section xyz
   ```

- `docs`: changes in repository documentation, not in the content itself:

   ```plaintext
   docs: update getting started guide in README.md
   ```

- `style`: for formatting changes without affecting the code:

   ```plaintext
   style: adjust indentation in instructions
   ```

- `test`: to add or modify tests to the content itself:

   ```plaintext
   test: add tests
   ```

   > If part of the end-user instructions includes described tests, that would be `feat`, as these are tests helping the content creation itself.

- `ci`: for changes related to GitHub delivery:

   ```plaintext
   ci: fix GitHub Actions pipeline for deployment
   ```

- `chore`: for minor tasks or maintenance that do not warrant indicating otherwise:

   ```plaintext
   chore: fix folder name
   ```

   ```plaintext
   chore: add xyz to .gitignore
   ```

**When you commit**, you may have made a mistake and just want to correct the previous commit, so in that case, follow these steps:

- Correct a previous commit and put a new message (if you want it that way):

   ```bash
   git commit --amend -m "New message"
   ```

   > If you don't want to put a new message, omit `-m "New message"`

- If you already pushed the change to the remote:

   ```bash
   git push origin <Branch_Name> --force-with-lease
   ```

   > Using `--force-with-lease` is safer, as it verifies that no one else has updated the remote while you were working, minimizing the risk of overwriting someone else's changes.

**Rules:**

- Use the imperative mood in the description ("add" instead of "added" or "adds").
- Limit the subject line to 72 characters.
- Separate subject from body with a blank line.
- Reference issues and pull requests when relevant.

#### Adding new repositories

Currently not available.

#### Contributing via Forks

1. Fork the repository (create your own copy of this repository in your GitHub account).
2. Create a new branch for your contribution following the Git Flow methodology. Example:

```bash
git checkout -b feature/feature-name
```

3. Remember to periodically fetch changes from the `main` branch using `rebase`:

- Fetch changes from main:

```bash
git fetch origin main
```

- Perform a `rebase` on the local branch:

   ```bash
   git rebase main
   ```

- Resolve conflicts (if any): If there are conflicts, resolve them and then continue:

   ```bash
   git add <resolved_file>
   git rebase --continue
   ```

4. Commit your work periodically with each significant activity.

   > **Tip**: If you use VS Code, the Source Control panel shows a ✨ button to generate commit messages automatically with GitHub Copilot.

5. Push the changes to your remote git branch and check from there that everything is correct. Things often look different if you take the time to review the instructions as if you were the end user.

6. Make sure to perform a `git rebase -i` on your branch to:

- Merge small or related commits (`squash`).
- Rewrite commit messages to make them clear and descriptive.

7. Submit a `pull request` to the `main` branch:

- Ensure your changes are well-documented and formatted clearly.
- Provide a clear description of your changes in the pull request.
- Reference any external sources if applicable.

   > **Tip**: If you use VS Code with the [`GitHub Pull Requests`](https://marketplace.visualstudio.com/items?itemName=GitHub.vscode-pull-request-github) extension, you can create, review, and merge pull requests directly from the editor — no need to open a browser. See the full step-by-step guide in [docs/guides/pull-requests-vscode.md](docs/guides/pull-requests-vscode.md).

## Recommended Tools

We recommend the following tools:

1. [`vscode`](https://code.visualstudio.com/).
   > Although you can use your favorite editor.
2. Using `vscode` as a reference, you need the following extensions:
   - [`GitHub Pull Requests`](https://marketplace.visualstudio.com/items?itemName=GitHub.vscode-pull-request-github) to create, review, and merge pull requests without leaving VS Code.
   - [`Markdown Preview Mermaid Support`](https://marketplace.visualstudio.com/items?itemName=bierner.markdown-mermaid) or any other that allows you to use `Mermaid`.
   - [markdownlint](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint) to detect errors or bad practices when writing in [markdown](https://en.wikipedia.org/wiki/Markdown).
   - [Code Spell Checker](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker) to correct spelling.
