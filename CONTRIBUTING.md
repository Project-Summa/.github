# Contributing to Summa

> Thank you for your interest in contributing to Summa.

This document explains how to contribute to the Summa project. Please read it before submitting issues or pull requests.

---

## Table of Contents

- [Code of Conduct](#code-of-conduct)
- [Getting Started](#getting-started)
- [Repository Structure](#repository-structure)
- [How to Contribute](#how-to-contribute)
- [Reporting Issues](#reporting-issues)
- [Branch Naming](#branch-naming)
- [Commit Messages](#commit-messages)
- [Pull Requests](#pull-requests)
- [Code Style](#code-style)
- [Testing](#testing)
- [AI-Generated Code](#ai-generated-code)
- [Documentation](#documentation)
- [Community](#community)

---

## Code of Conduct

All contributors must follow the [Code of Conduct](CODE_OF_CONDUCT.md). Please report unacceptable behavior to the project maintainers.

---

## Getting Started

1. Fork the repository you want to contribute to
2. Clone your fork locally
3. Create a feature branch
4. Make your changes
5. Write or update tests
6. Submit a pull request

---

## Repository Structure

Summa uses a multi-repo structure:

| Repository | Description |
|---|---|
| `summa` | Central documentation, design files and project coordination |
| `summa-android` | Android application |
| `summa-ios` | iOS application |
| `summa-backend` | Optional self-hosted synchronization server |
| `.github` | Organization-wide GitHub configuration |

Each platform repository has its own issue tracking and release cycle.

---

## How to Contribute

### Reporting Bugs

- Search existing issues first
- Use the **Bug Report** issue template
- Include reproduction steps
- Include expected and actual behavior
- Include device, OS and app version where applicable

### Suggesting Features

- Use the **Feature Request** issue template
- Describe the problem you want to solve
- Describe your proposed solution
- Consider local-first implications

### Improving Documentation

- Use the **Documentation** issue template
- Point out unclear, outdated or missing information
- Suggest concrete improvements

### Submitting Code

- Pick an existing issue or create one
- Comment on the issue to let others know you are working on it
- Follow the branch naming and commit message conventions below
- Write tests for new functionality
- Update documentation if needed

---

## Branch Naming

Use the following format:

```text
<type>/<issue-number>-<short-description>
```

### Types

| Type | Purpose | Example |
|---|---|---|
| `feat` | New feature | `feat/42-add-transactions` |
| `fix` | Bug fix | `fix/87-crash-on-launch` |
| `chore` | Maintenance task | `chore/103-update-deps` |
| `docs` | Documentation | `docs/56-api-guide` |
| `refactor` | Code restructuring | `refactor/71-clean-repos` |
| `test` | Test additions or fixes | `test/95-sync-tests` |
| `design` | Design or UI work | `design/12-dashboard-layout` |
| `ci` | CI/CD pipeline | `ci/15-lint-workflow` |
| `release` | Release preparation | `release/1.0.0-beta.1` |

---

## Commit Messages

Use the Conventional Commits specification:

```text
<type>(<scope>): <short description>
```

### Examples

```text
feat(database): add transaction entity with sync metadata
fix(auth): correct token refresh race condition
docs(api): update endpoint documentation
chore(deps): update room to 2.7.0
test(sync): add idempotency integration test
```

### Rules

- Use imperative mood: "add feature" not "added feature"
- Keep the subject line under 72 characters
- Separate subject from body with a blank line
- Use the body to explain what and why, not how
- Reference the issue number when applicable

```text
fix(auth): prevent token reuse after revocation

The refresh token rotation did not invalidate previously issued
tokens when a new token was used. This could allow a stolen token
to be reused within the rotation window.

Closes #142
```

---

## Pull Requests

### Before Submitting

- Run all tests
- Run linters
- Update documentation if needed
- Rebase on the latest target branch
- Ensure CI passes

### PR Title

Follow the same format as commit messages:

```text
feat(transactions): add transaction creation screen
```

### PR Description

Include:

- What the PR does
- Why the change is needed
- Link to the related issue
- Screenshots or recordings for UI changes
- Testing steps

### Review Process

- All PRs require at least one review
- Address review comments promptly
- Keep PRs focused and reasonably sized
- Split large changes into multiple PRs when practical
- Maintainers may request changes before merging

### Merge Strategy

- **Main branches**: Use merge commits to preserve history
- **Feature branches**: Squash commits before merging
- **Release branches**: Merge commits only

---

## Code Style

### Kotlin (Android)

- Follow the Kotlin Coding Conventions
- Use ktlint for formatting
- Use Detekt for static analysis
- Prefer `val` over `var`
- Prefer sealed classes for state
- Use meaningful names over short abbreviations
- Write KDoc for public APIs

### Swift (iOS)

- Follow Swift API Design Guidelines
- Use SwiftLint for formatting
- Prefer value types where practical
- Use meaningful names

### Go (Backend)

- Follow Effective Go and Go Code Review Comments
- Use `gofmt` and `golangci-lint`
- Handle all errors explicitly
- Write godoc comments for exported types and functions
- Keep functions focused and short

### General

- Write self-documenting code
- Add comments only when the why is not obvious
- Avoid unnecessary abstractions
- Follow the existing patterns in the codebase

---

## Testing

### Requirements

- New features must include unit tests
- Bug fixes must include a regression test
- Critical paths must have integration tests
- UI changes should include screenshot tests where practical

### What to Test

- Business logic
- Data transformations
- Repository implementations
- Sync conflict resolution
- Authorization rules
- Input validation
- Error handling

### What Not to Test

- Framework boilerplate
- Trivial getters and setters
- Third-party library behavior

---

## AI-Generated Code

AI tools may be used to assist development. However:

- You are responsible for every line of code you submit
- Review all AI-generated code thoroughly
- Ensure it follows project conventions
- Ensure it includes appropriate tests
- Never submit AI-generated code without understanding it
- Do not include AI prompt artifacts in commits
- Treat AI as a tool, not an author

---

## Documentation

- Update relevant documentation when changing behavior
- Use clear, concise language
- Include code examples where helpful
- Follow existing documentation formatting
- Link to related documents rather than duplicating content

---

## Security

- Never commit secrets, tokens or passwords
- Never log sensitive financial data
- Follow the [Security Policy](SECURITY.md) for vulnerability reports
- Use environment variables for configuration
- Validate all external input

---

## Community

- Be respectful and constructive
- Help others when you can
- Ask questions if you are unsure
- Follow the project principles:
  - Local First
  - User Owns the Data
  - Privacy by Default
  - Cloud is Optional
  - Open Source

---

## Questions?

If you have questions about contributing, open a discussion or reach out to the maintainers.