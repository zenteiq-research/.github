# Governance

This document describes how the [zenteiq-research](https://github.com/zenteiq-research) organisation and its repositories are run. A repository may add its own `GOVERNANCE.md` for project-specific detail, but it may not weaken the rules set out here.

## Purpose and scope

`zenteiq-research` is ZenteiQ's home for **public, open-source research software**: scientific machine learning frameworks, evaluation and benchmark tools, and code that reproduces published results.

**Every repository in this organisation is public.** Proprietary code, commercial products (including ScireX Enterprise), client work and internal tooling are kept in separate, private ZenteiQ organisations and are never developed here.

## Roles

| Role | Who | Responsibilities |
| :--- | :--- | :--- |
| **Organisation owner** | Two to three named ZenteiQ staff, appointed by the Founder & Chief Scientist | Organisation settings, membership, security policy, creating and archiving repositories, final escalation |
| **Maintainer** | Named per repository in `CODEOWNERS` | Technical direction of the repository, reviewing and merging pull requests, triage, releases |
| **Reviewer** | Trusted contributors nominated by maintainers | Reviewing pull requests and triaging issues; cannot merge |
| **Contributor** | Anyone | Opening issues, discussions and pull requests under the [Code of Conduct](CODE_OF_CONDUCT.md) |

Maintainers are usually ZenteiQ staff. External researchers, including academic collaborators, may become maintainers once they have a sustained record of high-quality contributions and reviews, if nominated by an existing maintainer and approved by an organisation owner.

Maintainers who are inactive for six months may be moved to emeritus status, keeping their credit but losing write access. They can be reinstated on request.

## Decision-making

- **Day-to-day decisions**, such as accepting a pull request, are made by the repository's maintainers through code review.
- **Significant changes**, such as new major features, breaking API changes or changes to benchmark methodology, start as an issue or design proposal. They stay open for comment for at least five working days, and are accepted when maintainers reach consensus with no unresolved objections.
- **If maintainers cannot agree**, the organisation owners decide.
- **Scientific direction** across ZenteiQ Research projects is set by the Founder & Chief Scientist.

## Access and security policy

- Two-factor authentication is required for all organisation members.
- Members have **read** access by default. Write and maintain access are granted per repository through teams, on the principle of least privilege.
- Only organisation owners can create, delete, transfer or rename repositories, or change repository visibility.
- External collaborators contribute through forks and pull requests. Exceptions are granted per repository by an owner.
- Secret scanning with push protection, Dependabot alerts, and private vulnerability reporting are enabled on every repository.
- Access is reviewed every quarter. Access is removed promptly when someone leaves ZenteiQ or a collaboration ends.

## Branch protection

The default branch (`main`) of every repository is protected by an organisation ruleset:

- Changes go through pull requests only. Direct pushes and force pushes are blocked.
- At least one approving review from a code owner is required.
- Required CI checks must pass.
- All commits must carry a DCO sign-off.
- Branches must be up to date before merging, and conversations must be resolved.

Organisation owners may bypass these rules only in an emergency, such as a security fix, and must record the reason in the pull request.

## Admitting a new repository

Before a repository is created in, or transferred into, this organisation, an organisation owner confirms that:

1. **IP clearance is complete.** The code is free of confidential, client-owned or export-controlled material, and any rights held by universities, funders or partners have been cleared.
2. **The history is clean.** The Git history contains no secrets, credentials or internal material. If in doubt, the repository starts from a cleaned snapshot rather than a transfer.
3. **It has a licence.** The repository contains an OSI-approved `LICENSE` file, and a data licence where data is included.
4. **The basics are in place:** a `README.md` describing purpose, installation and usage; a `CODEOWNERS` file naming at least two maintainers; a `CITATION.cff` file; and working CI.
5. **It does not leak product code.** The release does not expose code from ZenteiQ's proprietary products.

## Releases

- Projects use [Semantic Versioning](https://semver.org/). Releases are created from signed, annotated Git tags.
- Every release has release notes listing changes, fixes and any breaking changes, with migration guidance.
- Releases are cut by a maintainer and approved by a second maintainer.
- Where a project publishes packages, for example to PyPI, publishing runs from CI using trusted publishing, never from a personal machine or personal token.
- Release archives are linked to Zenodo, where enabled, so that each version has a citable DOI.

## Benchmarks

Benchmark repositories, such as Dhīr-Bench, follow additional rules to protect their integrity:

- Changes to scoring methodology, metrics or held-out data are significant changes (see *Decision-making*) and are recorded in a versioned changelog.
- Results are always reported with the benchmark version used to produce them.
- ZenteiQ models are evaluated using the same published harness and rules as any other model.

## Changes to this document

Changes to this governance document are proposed through a pull request to the [`.github`](https://github.com/zenteiq-research/.github) repository and require approval from an organisation owner.
