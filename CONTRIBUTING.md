# Contributing to SFSpeckit

Thank you for your interest in contributing to **SFSpeckit (Salesforce Spec-Kit Extension)**! Evernorth welcomes contributions from the open-source community.

## Code of Conduct

All contributors are expected to uphold the [Evernorth Code of Conduct](CODE_OF_CONDUCT.md).

## Getting Started

1. **Prerequisites & Setup**:
   * See the [README Prerequisites & Installation](README.md#prerequisites) sections for required tooling and local setup instructions.
2. **Fork and Clone**:
   * Fork the repository on GitHub.
   * Clone your fork locally:
     ```bash
     git clone https://github.com/<your-username>/spec-kit-sf.git
     ```
3. **Commit Guidelines**:
   * We follow [Conventional Commits](https://www.conventionalcommits.org/):
     * `feat: add new command for ...`
     * `fix: correct scoring gate logic in ...`
     * `docs: update deployment lifecycle documentation`
   * **Private Email Requirement**: Ensure your git commits use your GitHub noreply email address (`<username>@users.noreply.github.com`).

## Developing Extension Commands

* Extension commands reside under `commands/*.md`.
* Each command must include standard YAML frontmatter with a `description`.
* Command instructions must adhere to the 555-point quality rubric documented in `docs/scoring.md`.

## Submitting a Pull Request

1. Create a feature branch: `git checkout -b feat/my-new-feature`
2. Validate changes against Salesforce DX best practices.
3. Push to your fork and submit a PR to `main`.
4. Ensure all CI checks (Private Email Policy, Greetings) pass.