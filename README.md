# zenteiq-research/.github

This repository holds the organisation-wide defaults for [github.com/zenteiq-research](https://github.com/zenteiq-research).

GitHub uses these files for every public repository in the organisation that does not have its own copy, so a single change here updates the whole organisation. A repository can override any default by adding its own file of the same name.

| Path | Purpose |
| :--- | :--- |
| `profile/README.md` | The public organisation profile shown at github.com/zenteiq-research |
| `profile/assets/` | Logo files used by the profile (light and dark variants), plus the square avatar to upload under Settings → Profile |
| `CODE_OF_CONDUCT.md` | Expected behaviour and how conduct concerns are handled |
| `CONTRIBUTING.md` | How to contribute, including testing standards and DCO sign-off |
| `GOVERNANCE.md` | Roles, decision-making, repository admission and release rules |
| `SECURITY.md` | How to report vulnerabilities privately |
| `SUPPORT.md` | Where to get help |
| `.github/ISSUE_TEMPLATE/` | Default issue forms and contact links |
| `.github/PULL_REQUEST_TEMPLATE.md` | Default pull request checklist |
| `workflow-templates/` | Starter GitHub Actions workflows offered to all repositories |

Two things to know before editing:

1. This repository must stay **public**, or the defaults stop applying.
2. If a repository has *any* file in its own `.github/ISSUE_TEMPLATE/` folder, none of the default issue templates are used there. Repositories that customise templates should copy the ones they still need.

Changes to this repository follow the same review rules as any other repository in the organisation (see [GOVERNANCE.md](GOVERNANCE.md)), with approval from an organisation owner.
