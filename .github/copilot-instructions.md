---
applyTo: "**"
---
# Project general coding standards

## Naming Conventions
- Use PascalCase for component names, interfaces, and type aliases
- Use camelCase for variables, functions, and methods
- Use kebab-case for file names, folder names, and branch names
- Prefix private class members with underscore (_)
- Use ALL_CAPS for constants
- All file names, class names, method names, and any type names must be in English, although comments can be in Spanish

## Commit Message Guidelines

All commit messages must follow the [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/) specification. This ensures clarity and consistency in the project history.

**Format:**

```
<type>[optional scope]: <description>

[optional body]

[optional footer(s)]
```

**Types:**
- feat: A new feature
- fix: A bug fix
- docs: Documentation only changes
- style: Changes that do not affect the meaning of the code (white-space, formatting, missing semi-colons, etc)
- refactor: A code change that neither fixes a bug nor adds a feature
- perf: A code change that improves performance
- test: Adding missing tests or correcting existing tests
- build: Changes that affect the build system or external dependencies
- ci: Changes to CI configuration files and scripts
- chore: Other changes that don't modify src or test files
- revert: Reverts a previous commit

**Examples:**

```
feat(auth): add login functionality

fix(api): handle null response from server

docs: update README with setup instructions
```

**Rules:**
- Use the imperative mood in the description ("add" not "added" or "adds").
- Limit the subject line to 72 characters.
- Separate subject from body with a blank line.
- Reference issues and pull requests when relevant.

## Branch Naming Convention

Follow the Git Flow methodology with these branch types:

- **Feature branches**: For new functionalities. Example: `feature/chapter-1-ipfs` or `feature/install-proxy`
- **Bugfix branches**: For fixing issues. Example: `bugfix/issue-123` or `bugfix/review-inconsistent-steps`
- **Documentation branches**: For repository documentation changes. Example: `docs/initial-documentation`
- **Experiment branches**: For testing ideas that might not be included. Example: `experiment/test-alternative-installation`

Branch names must use English keywords in `kebab-case`, with sections separated only by `-`.
