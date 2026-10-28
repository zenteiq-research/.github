# Security Policy

This policy covers every repository in the [zenteiq-research](https://github.com/zenteiq-research) organisation, unless a repository has its own `SECURITY.md`.

## Supported versions

Security fixes are made for the **latest released minor version** of each project. Older versions may receive fixes at the maintainers' discretion. Please check that a problem still exists in the latest release, or on the `main` branch, before reporting it.

## Reporting a vulnerability

**Please do not report security vulnerabilities through public issues, discussions or pull requests.**

Report privately using one of these methods:

1. **GitHub private vulnerability reporting (preferred).** Open the affected repository, go to the **Security** tab, and click **Report a vulnerability**.
2. **Email.** Write to **info@zenteiq.ai** with the subject line `[SECURITY] <repository name>`.

Please include as much of the following as you can:

- the affected repository, version or commit
- a description of the vulnerability and its potential impact
- steps to reproduce, or a proof of concept
- any suggested fix or mitigation

## What to expect

| Step | Target time |
| :--- | :--- |
| Acknowledgement of your report | Within 3 working days |
| Initial assessment and severity rating | Within 10 working days |
| Progress updates | At least every 14 days until resolved |

We follow coordinated disclosure. We will agree a disclosure date with you, normally within 90 days of the report, or sooner once a fix is released. Fixed vulnerabilities are published as GitHub Security Advisories, with a CVE where appropriate. Unless you ask us not to, we will credit you in the advisory.

## Scope

**In scope:**

- source code, build scripts and CI workflows in this organisation's repositories
- released packages built from these repositories
- integrity issues in published benchmark data, reference solutions or scoring code, such as tampering or leaked held-out data

**Out of scope:**

- ZenteiQ commercial products and services, and the zenteiq.ai website (please report these to info@zenteiq.ai separately)
- vulnerabilities in third-party dependencies that are already publicly known, unless our use of the dependency makes them exploitable
- results of automated scans with no demonstrated impact

## Safe harbour

We will not take legal action against anyone who researches and reports vulnerabilities in good faith under this policy. Good faith means avoiding privacy violations, data destruction and service disruption, and giving us reasonable time to respond before any public disclosure.
