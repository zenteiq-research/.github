# Contributing to ZenteiQ Research projects

Thank you for helping to improve ZenteiQ's open-source research software. This guide applies to every repository in the [zenteiq-research](https://github.com/zenteiq-research) organisation. A repository may add its own `CONTRIBUTING.md` with project-specific details, such as build commands, and that file takes precedence where the two differ.

By taking part, you agree to follow our [Code of Conduct](CODE_OF_CONDUCT.md).

## Ways to contribute

- **Report bugs**, including incorrect numerical results, using the issue forms in the relevant repository.
- **Suggest features** or new methods, problems or benchmarks.
- **Improve documentation**, examples and tutorials. These are some of the most valuable contributions.
- **Submit code**: bug fixes, new solvers or models, performance work and tests.
- **Review pull requests** and help answer questions from other users.

For anything larger than a small fix, please open an issue first and describe what you plan to do. This avoids duplicated effort and lets maintainers confirm the change fits the project's direction before you invest time in it.

## Development workflow

1. **Fork** the repository and create a branch from `main` with a descriptive name, such as `fix/neumann-bc-assembly` or `feat/fno-3d`.
2. **Set up** the development environment as described in the repository's README or its own `CONTRIBUTING.md`.
3. **Make focused changes.** One logical change per pull request is much easier to review.
4. **Add or update tests and documentation** alongside the code.
5. **Run the test suite and linters** locally before pushing.
6. **Sign off every commit** (see [Developer Certificate of Origin](#developer-certificate-of-origin-dco)).
7. **Open a pull request** against `main` and complete the pull request template.

## Standards for scientific code

Our software is used to produce scientific and engineering results, so correctness matters as much as functionality.

- **Validate against a reference.** New solvers, models and numerical methods need tests that compare results with an analytical solution, a manufactured solution, or a trusted numerical solver. State the tolerance used and why it is appropriate.
- **Show convergence where it applies.** For discretisation methods, include a convergence check against the expected order.
- **Make results reproducible.** Fix random seeds in tests, record the configuration used, and avoid hidden dependence on hardware or library versions where possible.
- **Never loosen a tolerance just to make a test pass.** If a tolerance has to change, explain the reason in the pull request.
- **Flag performance-sensitive changes.** Include before-and-after timings and the hardware used.
- **Keep the public API stable.** Breaking changes need a deprecation path and a changelog entry. Maintainers will decide on the version bump.

## Contributing benchmarks and data

Benchmark repositories such as Dhīr-Bench have extra requirements, because a benchmark is only useful if its results can be trusted.

- **Document provenance.** Record where every dataset, problem and reference solution came from, how it was generated, and under what licence it may be redistributed.
- **Only submit data you have the right to share.** Do not contribute confidential, client-owned, personal or export-controlled data, even in anonymised form.
- **Protect held-out data.** Do not publish held-out test sets or reference answers in a place or form that would allow models to be trained on them.
- **Make scoring deterministic.** Scoring code must produce the same score for the same output, and its metrics must be documented.
- **Report results honestly.** Claimed results must be reproducible with the published harness, configuration and model version.
- **Store large files elsewhere.** Large datasets and model weights belong in the external storage named in each repository's README, not in Git history.

## Commit messages

Write commit messages in the imperative mood, with a short summary line of 72 characters or less, followed by a blank line and an explanation of *why* the change was made if it is not obvious.

```
Fix sign error in Neumann boundary assembly

The boundary integral was subtracted instead of added, which produced
wrong fluxes on curved boundaries. Adds a manufactured-solution test.

Signed-off-by: Your Name <you@example.com>
```

## Developer Certificate of Origin (DCO)

All contributions must be signed off under the [Developer Certificate of Origin 1.1](https://developercertificate.org/). By signing off, you certify that you wrote the contribution or otherwise have the right to submit it under the repository's open-source licence.

Add the sign-off by committing with the `-s` flag:

```bash
git commit -s -m "Your commit message"
```

This adds a line like `Signed-off-by: Your Name <you@example.com>` using your Git name and email. Pull requests with unsigned commits cannot be merged. To sign off commits you have already made:

```bash
git rebase --signoff main
git push --force-with-lease
```

If you contribute as part of your job or studies, make sure your employer or institution allows you to contribute under the repository's licence.

## Licensing of contributions

Contributions are licensed under the licence in the `LICENSE` file of the repository you contribute to. Do not copy code, text, figures or data from sources whose licence is incompatible with it. If you include third-party material, keep its copyright notice and note its licence in the pull request.

## AI-assisted contributions

You may use AI coding assistants. You remain fully responsible for everything you submit: you must understand it, test it, and have the right to contribute it under the DCO. Please mention substantial AI assistance in the pull request description so reviewers know what to look for.

## Review and merging

- Every pull request needs passing CI and approval from at least one maintainer listed in the repository's `CODEOWNERS` file.
- Maintainers may ask for changes, additional tests or validation evidence. Please respond within a few weeks, or the pull request may be closed. It can be reopened at any time.
- Pull requests are usually merged by squashing, so the pull request title becomes the commit summary.
- Release timing and version numbers are decided by the maintainers (see [GOVERNANCE.md](GOVERNANCE.md)).

## Questions

See [SUPPORT.md](SUPPORT.md) for where to ask questions. Please do not use issues for general usage questions if the repository has Discussions enabled.
