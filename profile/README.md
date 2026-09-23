<div align="center">

# GAIA HazLab

**G**eophysical **A**I-driven **I**ntegration and **A**ssimilation
for climate-compounded geohazards

[Website](https://gaia-hazlab.github.io) ·
[How we work](https://gaia-hazlab.github.io/book/how-we-work) ·
[Decisions of record](https://gaia-hazlab.github.io/book/decisions) ·
[Dashboard](https://gaia-hazlab.github.io/dashboard.html) ·
[Discussions](https://github.com/orgs/gaia-hazlab/discussions)

</div>

---

## What this is

Landslides, liquefaction, floods and post-fire debris flows are usually studied one hazard
at a time, with the weather that triggers them treated as an external boundary condition.
GAIA is built on the opposite premise: that the atmosphere, the hydrosphere and the solid
Earth are one coupled system, and that the predictability of a hillslope failure is set as
much by the atmospheric river days earlier as by the slope itself.

We build the cyberinfrastructure that makes working across those boundaries practical — a
data layer that puts seismic, geodetic, SAR, hydrological and atmospheric holdings on a
common footing; a model layer for AI weather and hazard models; an evaluation layer that
scores them honestly against baselines; and a set of research agents that translate between
the disciplines involved. The science that exercises it is a geohazard digital twin for
Washington and Alaska.

GAIA is a collaboration of the University of Washington, the University of Alaska Fairbanks
and EarthScope Consortium, supported by three linked NSF awards:
**OAC-2608509, OAC-2608510 and OAC-2608511**. Earlier and continuing support comes from the
Fund for Future Science and Technology and the Jerome and Linda Paros Geohazard Center.

## How to read this organisation

Thirty-four repositories is already too many to browse. At least four GitHub topics on every
public repository make the collection readable without anyone maintaining a list by hand.

| Axis | Values | Rule |
|---|---|---|
| **Umbrella** | `gaia` | every repository |
| **Category** | `gaia-coordination` · `gaia-data` · `gaia-agent` · `gaia-eval` · `gaia-science` · `gaia-template` · `gaia-container` | exactly one |
| **Relationship** | `gaia-core`, or `gaia-level-1` … `gaia-level-4` | exactly one |
| **Maturity** | `gaia-stable` · `gaia-incubating` · `gaia-archived` | exactly one |
| **Provisioning** | `gaia-hpc` · `gaia-cloud` · `gaia-hybrid` · `gaia-agent-api` | at most one of `gaia-hpc`/`gaia-cloud`/`gaia-hybrid`; `gaia-agent-api` is independent |

**Category** says what a repository *is*. **Relationship** says how it came to be here —
`gaia-core` for work the project builds and maintains, or a rung of the ladder below for
software that joined from outside. **Maturity** exists because a list of repositories is not
a recommendation: without it, a newcomer cannot tell established work from an experiment
started last month. **Provisioning** says where a repository's workflow runs — it's the
only axis a repository can skip entirely (a STAC catalog runs nowhere in particular) or, for
`gaia-hybrid`, the only one recording that two backends (HPC and cloud) are used together in
one pipeline rather than as alternatives. Full definitions, including why `gaia-hybrid` isn't
just two independent tags, are in [the organisation page](https://gaia-hazlab.github.io/book/organization).

`gaia-incubating` means exactly what it says — the interface may change without warning.
Check the tag before you build on something.

Browse by topic: [`gaia-data`](https://github.com/search?q=org%3Agaia-hazlab+topic%3Agaia-data&type=repositories) ·
[`gaia-agent`](https://github.com/search?q=org%3Agaia-hazlab+topic%3Agaia-agent&type=repositories) ·
[`gaia-science`](https://github.com/search?q=org%3Agaia-hazlab+topic%3Agaia-science&type=repositories) ·
[`gaia-stable`](https://github.com/search?q=org%3Agaia-hazlab+topic%3Agaia-stable&type=repositories) ·
[`gaia-hpc`](https://github.com/search?q=org%3Agaia-hazlab+topic%3Agaia-hpc&type=repositories) ·
[`gaia-cloud`](https://github.com/search?q=org%3Agaia-hazlab+topic%3Agaia-cloud&type=repositories) ·
[`gaia-hybrid`](https://github.com/search?q=org%3Agaia-hazlab+topic%3Agaia-hybrid&type=repositories)

Existing repositories are tagged, never renamed — renaming breaks clones, bookmarks, and any
URL already printed in a paper. New software products follow a naming convention
(`gaia-<thing>`), while science and coordination repositories keep descriptive names, since
those are the ones most likely to be cited.

## How outside work joins GAIA

Five levels. Each is a larger commitment by us than the one before, so each is agreed rather
than assumed. A group choosing to stay at level 0 indefinitely is a success, not a failure.

| | Level | What it means | What GAIA commits to |
|---|---|---|---|
| 0 | **Listed** | A line in [awesome-gaia](https://github.com/gaia-hazlab/awesome-gaia), proposed by anyone through a pull request | Curation, and a link check |
| 1 | **Containerised** | We publish a tested image; the software stays with its authors and is never forked | Scheduled rebuilds, CI on the image |
| 2 | **Demonstrated** | A template repository shows a complete workflow using it | Keeping that template passing |
| 3 | **Benchmarked** | It becomes a task or baseline in the evaluation hub | Maintaining the task and its held-out data |
| 4 | **Adopted** | The repository moves into this organisation | Long-term maintenance — requires a named maintainer and a numbered decision |

If you maintain a tool and want it listed, that is level 0 and it needs nobody's permission
beyond a pull request against `awesome-gaia`.

## Where things happen

**[Discussions](https://github.com/orgs/gaia-hazlab/discussions)** are the org's front door
for questions that are not bugs — "has anyone tried X", design debates, calls for
collaborators, and the weekly digest of project Slack. Anyone with a GitHub account can post.
Slack is where we think out loud; Discussions is where the thinking that mattered gets a
permanent, searchable, citable address.

**[Projects](https://github.com/orgs/gaia-hazlab/projects)** — one org-level board per
research or cyberinfrastructure thrust, drawing issues from every repository. Fields:
*Thrust*, *Milestone*, *Status*. Work that is not on a board is not tracked, and that is a
legitimate state for exploratory work.

**Milestones** are per-repository and correspond to project deliverables, not to sprints.

**[Issues](https://github.com/orgs/gaia-hazlab/repositories)** live in the repository the work
belongs to. Cross-cutting work goes in
[gaia-hazlab.github.io](https://github.com/gaia-hazlab/gaia-hazlab.github.io/issues).

**Decisions** that constrain later choices get a permanent number in the
[decisions register](https://gaia-hazlab.github.io/book/decisions). If a choice lives only in
a Doc, a Slack thread, or someone's memory of a call, it is still a proposal.

**The [dashboard](https://gaia-hazlab.github.io/dashboard.html)** publishes the metrics we
committed to NSF, including the ones we are behind on. Figures below target stay visible.

## Citing our software

Every public repository carries a `CITATION.cff`, so GitHub's *Cite this repository* button
works. That gives you an author list and a version; it does not give you a permanent
identifier.

Repositories tagged **`gaia-stable`** also have a DOI. They are archived to Zenodo on every
tagged release through the [GAIA community](https://zenodo.org/communities/gaia-hazlab), and
their README carries a badge. Cite the version DOI in a paper; the concept DOI in the badge
always resolves to the latest.

Repositories tagged **`gaia-incubating`** have no DOI, by design. A DOI on a moving target is
worse than no DOI. If you need to cite one, open an issue asking for a release — we would
rather cut a version than have you cite a commit hash.

Software citation is not a courtesy here. Infrastructure work is chronically invisible in the
citation record, and a project whose purpose is to build infrastructure should not reproduce
that.

## Acknowledging the project

If GAIA infrastructure, data or software materially shaped your result, please use this
wording verbatim — all three award numbers, regardless of which institution you worked with:

> This material is based upon work supported by the U.S. National Science Foundation under
> Grant Nos. OAC-2608509, OAC-2608510 and OAC-2608511. Any opinions, findings, and
> conclusions or recommendations expressed in this material are those of the author(s) and do
> not necessarily reflect the views of the National Science Foundation.

Where the seed work for the Paros Center contributed, append: *"…, the Fund for Future
Science and Technology and the Jerome and Linda Paros Geohazard Center."*

## Licensing

Code is MIT unless a repository says otherwise. Documentation, vocabularies and curated data
products are CC BY 4.0. A repository with no `LICENSE` file is not open, whatever its README
claims, and we treat a missing license as a bug.

## Getting in touch

Open an issue on the repository concerned, start a
[Discussion](https://github.com/orgs/gaia-hazlab/discussions) if it does not belong to one, or
write to the Lead PI. The monthly project-wide update is open to anyone; the
[FAQ](https://gaia-hazlab.github.io/book/faq) explains how to join.

<div align="center">
<sub>NSF OAC-2608509 · OAC-2608510 · OAC-2608511 —
University of Washington · University of Alaska Fairbanks · EarthScope Consortium</sub>
</div>
