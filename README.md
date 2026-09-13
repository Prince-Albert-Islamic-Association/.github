# .github

Welcome to the Prince Albert Islamic Association organization-wide GitHub configuration repository.

This repository centralizes templates, automation, and configuration that apply across the Prince Albert Islamic Association's projects. By providing organization-level defaults here, we make it easier for maintainers and contributors to follow consistent processes and reduce duplicated configuration in every repository.

What you'll find here

- ISSUE_TEMPLATE/ — Issue templates to guide reporters and help triageers get the right information faster.
- PULL_REQUEST_TEMPLATE/ — Pull request templates to standardize PR descriptions and checklist items.
- workflows/ — GitHub Actions workflows intended for organization-level automation or to serve as shared examples.
- CODEOWNERS — (optional) File and path owners that help route reviews to the correct teams or maintainers.
- FUNDING.yml — (optional) Funding links for the organization or projects.
- README.md — This overview and contribution guide.

Why this repository exists

Maintaining organization-level GitHub settings in a single `.github` repository provides:

- Consistency: Contributors see the same issue/PR templates and guidance across repositories.
- Efficiency: Shared CI/CD workflows and templates reduce duplicated work and make maintenance easier.
- Discoverability: Central place for organization conventions, required approvals, and automation.

How templates and workflows work

- Issue and PR templates in ISSUE_TEMPLATE/ and PULL_REQUEST_TEMPLATE/ are discovered by GitHub and offered as defaults when creating new issues or pull requests in organization repositories that do not override them locally.
- Workflows placed in `.github/workflows/` can be used as organization-level automation. Some workflows may require repository-level secrets or organization settings to be enabled by admins.
- A repository’s own `.github/` directory or templates in the repository root take precedence over these organization-level defaults.

Contributing

We welcome improvements and additions. To propose changes:

1. Fork or branch this repository (or create a branch if you have push access).
2. Add or edit files under the appropriate folders: `ISSUE_TEMPLATE/`, `PULL_REQUEST_TEMPLATE/`, `.github/workflows/`, etc.
3. For issue/PR templates, keep prompts short and concrete — provide examples where helpful.
4. For workflows, document required repository permissions and secrets in the PR description.
5. Open a pull request explaining the change, the rationale, and which repositories will be affected.

Recommended templates and example files

- ISSUE_TEMPLATE/bug_report.md — Steps to reproduce, expected vs actual behavior, environment, and minimal reproduction.
- ISSUE_TEMPLATE/feature_request.md — Motivation, proposed design, and any backwards-compatibility notes.
- PULL_REQUEST_TEMPLATE/pull_request_template.md — Summary, linked issues, testing done, and checklist (e.g., lint, tests, docs).
- workflows/ci.yml — Example continuous-integration workflow with caching, matrix jobs, and artifact upload.
- workflows/release.yml — Example release automation (tagging, changelog generation, or publishing).

Best practices

- Keep templates focused — ask only for information you will actually use.
- Link to CONTRIBUTING.md or project-specific docs instead of pasting long policies into templates.
- Make workflows fast and idempotent; use caching to speed repeated builds.
- Require as few repository secrets as possible; prefer organization-level secrets managed by admins.

Security and secrets

- Never store secrets or credentials in repository files. Use GitHub repository or organization secrets for workflows that require credentials.
- Only organization owners or delegated administrators should add organization secrets. Document required secrets and their intended scope in the workflow PR description.

Impact and coordination

Changes here can affect many repositories. When opening a PR that changes templates or automation, include a brief impact statement listing which repositories or teams will be affected and why. For breaking or high-impact changes, request review from the relevant maintainers or teams.

Support

If you need help or guidance:
- Open an issue in this repository describing your question or proposed change.
- Reference CODEOWNERS (if present) to tag the right reviewers or teams.

Maintainers

This repository is maintained by the Prince Albert Islamic Association maintainers and volunteers. Please refer to CODEOWNERS or the MAINTAINERS file (if present) for the current list of maintainers and contact points.

License

Files in this repository are subject to the organization’s licensing policy. If a LICENSE is present in this repository, it applies to files here; otherwise, refer to each project's repository for per-project licensing.

Notes

- Organization-level defaults are helpful but not mandatory: individual repositories can opt to override templates and workflows by adding their own `.github/` configuration.
- Review the impact of changes and document required secrets, permissions, and settings in your PR.

Thank you for helping keep our projects consistent, secure, and welcoming to contributors.
