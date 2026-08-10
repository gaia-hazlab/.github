# Contributing to GAIA

The short version: open an issue before large work, keep pull requests small enough to review
in one sitting, and expect a real review rather than a rubber stamp.

## Where to put things

File an issue on the repository the work belongs to. If it spans several, file it on
[gaia-hazlab.github.io](https://github.com/gaia-hazlab/gaia-hazlab.github.io/issues) and link
outward. Questions that are not bugs belong in
[Discussions](https://github.com/orgs/gaia-hazlab/discussions).

## Before you start something large

Say so in an issue first. Not for permission — to find out whether someone is already doing
it, which in a four-institution project happens more often than you would think.

Anything that constrains later choices — a data format, an interface, a dependency everyone
will inherit — goes through the *proposal* issue template and, if adopted, becomes a numbered
entry in the [decisions register](https://gaia-hazlab.github.io/book/decisions).

## Pull requests

Branch from `main`. One idea per pull request. Describe what changes and why; if the reasoning
is longer than the diff, that is a good sign the reasoning is worth writing down. Tests where
tests make sense — for research code that often means one worked example that runs, not
coverage targets.

Reviews are technical, and disagreement is normal and useful. The person who wrote the code
usually merges it.

## From outside the project

Pull requests are welcome on every public repository. Check the maturity topic first:
`gaia-incubating` means the interface may change without warning, so ask before building on
it. To get a tool listed, use the *List my tool* issue template — that is level 0 and it needs
nobody's permission.

## Licensing and citation

Contributions are licensed under the repository's `LICENSE`. If a repository has none, say so
in an issue — we treat a missing licence as a bug.

If your contribution is substantial, add yourself to the repository's `CITATION.cff`. Software
citation is not a courtesy here; infrastructure work is chronically invisible in the citation
record and this project should not reproduce that.
