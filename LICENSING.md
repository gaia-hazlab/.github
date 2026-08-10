# Licensing in GAIA

One page. If your repository does not match one of the rows below, ask before inventing
something.

## The rule

| What it is | Licence |
|---|---|
| Software written by the project | **MIT** |
| Software written by the UW eScience **Scientific Software Engineering Center** | **whatever SSEC used** — currently BSD-3-Clause, as in `gaia-agentic-ai` |
| Documentation, the book, vocabularies, curated indexes, model cards | **CC BY 4.0** |
| Curated data products we generate | **CC BY 4.0**, with upstream terms restated |
| Data we merely redistribute | **upstream terms**, restated — we cannot relicense USGS, ASF or NASA holdings |
| Container images | inherit the base image; state it in the image label |

MIT is the default because it is short, permissive, and a facility can adopt MIT code without
a legal review. SSEC-authored code keeps the licence SSEC chose, because it is theirs and
relicensing someone else's work is not ours to do.

## Two things worth being precise about

**"More permissive than MIT" has a specific meaning, and it is probably not what you want.**
Apache-2.0 is often described that way; it is not more permissive. It adds an express patent
grant and a requirement to carry a NOTICE file — more *protective*, and slightly more
paperwork. Genuinely more permissive means 0BSD, CC0 or the Unlicense, which drop the
attribution requirement altogether. If you want the software to be citable, dropping
attribution works against you. Use MIT unless you have a reason you can state.

**One repository is out of family.** `usgs-gauge-utils` is GPL-3.0. GPL is not compatible with
MIT in the direction that matters: pull that gauge code into an MIT repository and the result
must be distributed under GPL. Its README already says development moved to
`gaia-data-downloaders`, so the safe move is to archive it rather than copy from it. If any of
it is genuinely needed, rewrite rather than paste.

## Every repository needs an actual LICENSE file

A README that says "MIT" is not a licence. Absent a `LICENSE` file, default copyright applies
and nobody may legally reuse the code, however public the repository is and however clearly it
invites reuse.

Eight public repositories currently have none:

`awesome-gaia` · `gaia-data-downloaders` · `gaia-translate-QA` · `seis-hydro-2-sed` ·
`landlab-debrisflow` · `da-seis-groundfailure` · `shred-landlab-prototypes` ·
`mt-rainier-smart-sensing`

Two of those are the awkward case. `seis-hydro-2-sed` asserts MIT in its README *and* in its
`CITATION.cff`, and `gaia-translate-QA` asserts "MIT for code, CC-BY-4.0 for content" — both
without the file. An assertion of openness with no legal instrument behind it is worse than a
plain omission, because it invites reliance.

`awesome-gaia` is a curated list rather than code, so it takes CC BY 4.0, not MIT.

**Treat a missing licence as a bug.** File it, do not tolerate it.

## The copyright line

The repositories that do have licences disagree about who holds the copyright. Five say
"Geophysical AI-driven Integration and Assimilation - Climate Compounded Geohazards", which is
a project name and not a legal entity; one says "Climate and Geohazards"; one says "Gaia
Hazlab"; one names an individual; `gaia-agentic-ai` carries a 2024 UW eScience/SSEC line.

Proposed, so that new repositories stop adding variants:

```
Copyright (c) 2026 GAIA HazLab contributors
```

This is the standard pattern for a project spanning several institutions, and it avoids
asserting an entity that does not exist. It is a one-line change if UW's licensing office
later prefers "the University of Washington" or "the Regents of the University of Washington",
so it is not worth blocking on — but it is worth asking, once, in the background.

SSEC-authored repositories keep the SSEC copyright line as written.

## Adding a licence

```bash
# MIT, for software
gh api repos/gaia-hazlab/<repo>/contents/LICENSE \
  --method PUT -f message="Add MIT licence" \
  -f content="$(base64 -w0 LICENSE-MIT.txt)"
```

Or simply use GitHub's web UI: **Add file → Create new file → type `LICENSE` → "Choose a
licence template"**, which fills in the year and holder for you. For 25 repositories the web
UI is faster than it sounds, and it gets the SPDX identifier right so GitHub displays the
licence in the sidebar.

Whatever you use, check afterwards that the licence shows in the repository's About panel — if
it does not, GitHub did not recognise the file, and neither will anything else.
