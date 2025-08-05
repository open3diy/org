# Contributing to open3diy.org

Thank you for your interest in contributing to the DIY-experiences repository!

This project is licensed under the [**Creative Commons Zero v1.0 Universal (CC0)**](https://creativecommons.org/publicdomain/zero/1.0/) license, dedicating the work to the public domain and helping expand a freely accessible knowledge base for all.

## Guidelines for Contributions

### Attribution

Always provide proper credit if you are including material or content from external sources.

### Style

- Keep documentation concise but informative.
- Use proper `markdown` syntax for readability.
- File or folder structure convention `camel case`, separating sections or hierarchies with `-`. Example:

```plaintest
solution1-userInstall-fixes
```

- Keep keywords and references in English; content may be in your preferred language.

  > **Let's make everyone feel comfortable with their language.**

### Licensing

- By contributing, you agree that your work will be dedicated to the public domain under the **Creative Commons Zero v1.0 Universal (CC0)** license.

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

  > Internal repository documentation, instruction-based documentation is a feature.

- **Experiments**: To test ideas or experiments that might not be included. Example:`experiment/test-alternativeInstallation`.

Branch names should use English keywords in `camel case`, with sections separated only by `-`.

#### Adding new repositories

Currently is not available.

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

## Recommended Tools

We recommend the following tools:

1. [`vscode`](https://code.visualstudio.com/).
   > Although you can use your favorite editor.
2. Using `vscode` as a reference, you need the following extensions:
   - [`Markdown Preview Mermaid Support`](https://marketplace.visualstudio.com/items?itemName=bierner.markdown-mermaid) or any other that allows you to use `Mermaid`.
3. [markdownlint](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint) to detect errors or bad practices when writing in [markdown](https://es.wikipedia.org/wiki/Markdown).
4. [Code Spell Checker](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker) to correct spelling.
5. [Jupyter](https://marketplace.visualstudio.com/items?itemName=ms-toolsai.jupyter) for creating and running interactive notebooks that combine code, text, and graphics. Ideal for testing, calculations, analysis, and documentation in a single `.ipynb` file.
   - In addition to having python installed, you will need to install the ipykernel package.
   - From [binder](https://notebooks.gesis.org/binder/) you can load the notebooks.

## How to Install Jekyll and Test the <open3diy.org> Documentation Page

Jekyll is used to generate the main site page, leveraging GitHub Pages integration for automatic documentation publishing.

To install and run Jekyll on Linux, follow these steps:

1. Check the official guide at [jekyllrb.com/docs](https://jekyllrb.com/docs/) and, for Ubuntu, see [jekyllrb.com/docs/installation/ubuntu](https://jekyllrb.com/docs/installation/ubuntu/).
2. Install the required dependencies (only the first time) from the terminal, in the project's root folder:

   ```bash
   bundle install
   ```

3. To start the documentation server, run:

   ```bash
   bundle exec jekyll serve --source docs
   ```

4. Access the local page at [http://localhost:4000](http://localhost:4000).

5. For the `githubdoc` plugin, if you are an authorized user, create a **classic token** at <https://github.com/settings/tokens> and add it to your `~/.bashrc` with the following content:

   ```bash
   export JEKYLL_GITHUB_TOKEN=your_token
   source ~/.bashrc
   ```

> If you encounter dependency issues, check the official documentation or seek help from the Jekyll community.

### GitHub Pages Configuration

Although this setup is usually done when creating the repository and enabling GitHub Pages, here are the steps to configure GitHub Pages and use the latest version of Minima, the base Jekyll theme that is not limited by classic GitHub Pages.

1. In the `org` repository of `open3diy`, go to **Settings → Pages → Build and deployment**.

2. Under **Build**, in the **Source** option, select **GitHub Pages Jekyll** and click **Configure**. A valid configuration will be proposed, so click **Commit changes...**.
