# `.github`

This repository holds the organisation-wide GitHub configuration for **gaia-hazlab**.
Nothing here is project code.

| Path | What it does |
|---|---|
| `profile/README.md` | Renders as the organisation profile at <https://github.com/gaia-hazlab> |
| `CODE_OF_CONDUCT.md` | Applies to every repository that does not define its own |
| `CONTRIBUTING.md` | Same |
| `SECURITY.md` | Same |
| `LICENSING.md` | The licence decision table, and which repositories are missing one |
| `ISSUE_TEMPLATE/` | Default issue forms for every repository without its own |

Files here cascade: a repository that defines its own copy overrides this one. That makes this
the right place for policy that should be identical everywhere, and the wrong place for
anything specific to one repository.

Governance, the repository taxonomy, and the decisions of record live in the book —
<https://gaia-hazlab.github.io/book/how-we-work> — not here. This repository is the machinery;
the book is the reasoning.
