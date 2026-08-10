# Security policy

GAIA repositories are research software. Most of them read public geoscientific data and
write files; few handle credentials, and none handle personal data.

**Report a vulnerability privately.** Use GitHub's *Report a vulnerability* button on the
repository's Security tab, which opens a private advisory. If that is not available, email
the Lead PI. Please do not open a public issue for a vulnerability.

We aim to acknowledge within five working days. Because this is a research project rather
than a product, we cannot promise a patch timeline; what we will do is tell you honestly what
we can and cannot fix, and mark the repository archived if the answer is that we cannot.

**In scope:** credential leakage in a repository or container image; a dependency with a known
advisory in an image we publish; code execution from untrusted input in a published tool.

**Not in scope:** vulnerabilities in upstream software we merely point at from
`awesome-gaia` — report those to their maintainers, and tell us so we can annotate the index.
