# Contributing to open3diy.org

Thank you for your interest in contributing to the DIY-Experiences repository!

This project is licensed under the [**Creative Commons Attribution-ShareAlike (CC-BY-SA) 4**](https://creativecommons.org/licenses/by-sa/4.0/deed.en) license, which means your contributions will help expand a freely accessible knowledge base for everyone.

## Guidelines for Contributions

### Attribution

- Always provide proper credit if you are including material or ideas from external sources.

### Style

- Keep documentation concise but informative.
- Use proper `markdown` syntax for readability.
- File or folder structure convention `camel case`, separating sections or hierarchies with `-`. Example:
   ```plaintest
   solution1-userInstall-fixes
   ```
- Keywords or key references always in English, but the content can use your own language!!!

> **Let's make everyone feel comfortable with their language.**


### Licensing

- By contributing, you agree that your work will be licensed under the **Creative Commons Attribution-ShareAlike (CC-BY-SA)** license.

## Code of Conduct

- Be respectful and collaborative.
- Avoid offensive or inappropriate content.

> **We appreciate your time and effort in making this repository a valuable resource for open3diy.org!**

## How to Contribute

### Reporting Issues

- If you find any errors or have suggestions for improvement, please create an issue in the repository.
- Clearly describe the problem, including steps to reproduce if applicable.

### If you contribute to the source code

Making change requests in existing repositories or creating new repositories will follow the [github flow](https://docs.github.com/en/get-started/using-github/github-flow). Inspired by **[a successful Git branching model](http://nvie.com/posts/a-successful-git-branching-model/)**, the following branch naming convention will be used:

- **Feature branches**: For new functionalities. Example: `feature/chapter-1-ipfs` or `feature/install-proxy`.
- **Bugfix branches**: For fixing issues. Example: `bugfix/issue-123` or `bugfix/review-inconsistent-steps`.
- **Repository documentation:**: For changes to repository documentation. Example: `docs/initial-documentation`.
> Internal repository documentation, instruction-based documentation is a feature,
- **Experiments**: To test ideas or experiments that might not be included. Example:`experiment/test-alternativeInstallation`.

> In English, branch names should be `camel case` with separation only using `-`.

#### Adding new repositories

Currently is not available.

#### Contributing via Forks

1. Fork the repository (create your own copy of this repository in your GitHub account).
2. Create a new branch for your contribution following the Git Flow methodology. Example:
   ```bash
   git checkout -b feature/nombre-de-la-funcionalidad
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
4. Commit your work periodically with each significant activity, using [conventional Commits](https://www.conventionalcommits.org/) to write commit messages in English. Examples:
 
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
   bugfix: resolve issue 123 section xyz
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
- `ci`: for changes related to GitHub delivery or documentation publication:
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
   - Correct an old commit and put a new message (if you want it that way):
      ```bash
      git commit --amend -m "New message"
      ```
      > If you don't want to put a new message, omit `-m "New message"`

   - If you already pushed the change to the remote:
      ```bash
      git push origin <Branch_Name> --force-with-lease.
      ```
      > Using `--force-with-lease` is safer, as it verifies that no one else has updated the remote while you were working, minimizing the risk of overwriting someone else's changes.

5. Push the changes to your remote git branch and check from there that everything is correct. Things often look different if you take the time to review the instructions as if you were the end user.
6. Make sure to perform a `git rebase -i` on your branch to:
   - Merge small or related commits (`squash`).
   - Rewrite commit messages to make them clear and descriptive.
7. Submit a `pull request` to the `main` branch. Please, make sure that:
   - Ensure your changes are well-documented and formatted clearly.
   - Provide a clear description of your changes in the pull request.
   - Reference any external sources if applicable.
