
# Contributing to OpenDrone

[![Discord](https://img.shields.io/badge/Discord-join-5865F2?logo=discord&logoColor=white)](https://discord.gg/v3sWmTcx3R)
[![YouTube](https://img.shields.io/badge/YouTube-JustFPV-FF0000?logo=youtube&logoColor=white)](https://www.youtube.com/@justfpv1432)
[![Shop](https://img.shields.io/badge/Shop-opendrone.be-ffb700)](https://opendrone.be)
[![Licence](https://img.shields.io/badge/Hardware-CERN--OHL--S--2.0-blue)](https://ohwr.org/cern_ohl_s_v2.txt)

---

> <picture>
>   <source media="(prefers-color-scheme: dark)" srcset="profile/incutec-ondark.svg">
>   <img src="profile/incutec-onlight.svg" alt="incutec" width="150">
> </picture>
>
> A startup in Belgium. Incutec started OpenDrone, but
> the project is not owned by us: the designs are open and the direction belongs
> to the people.
>
> Our intent is to sell the products of OpenDrone and use those profits to
>
> **A** &nbsp; Invest in development by ordering samples, testing, providing foundational hardware to build from
>
> **B** &nbsp; Invest in manufacturing, detailed on [opendrone.be/production](https://opendrone.be/production)
>
> Incutec handles: production, quality control, sourcing parts, building supply
> chains, putting things in a box with accessories and shipping it, and the legal
> responsibility for a product sold.
>
> The company needs revenue, this is how it is different from code repositories.
> But if Incutec disappears tomorrow, OpenDrone lives on.

## Why Contribute?

The world of open source hardware is not short of people with good intentions, but it is constrained by chaos and complicated production. With open source software, if you want to use someone else's work, you just download it. With hardware, it is only after the download that the real work begins. This is why so many open source hardware projects end up as one-off designs nobody else can build on. That is something we want to change, and to prove it is possible, we made OpenDrone.

We believe OpenDrone can be the pioneer that open source hardware needs, and show that it can be just as good as "traditional" commercial hardware, or better.

An open source design means everyone can see and learn how something works, and eventually they can even contribute to making the product more suitable for themselves. That leads to a product people really want: by the people, for the people.

And as an added bonus, the products are repairable by design. If you want an update, you can just collab with the community and build it yourself. And if we ever stop supporting a product, you are not left with dead hardware. The files are yours, and the community can keep it alive as long as people still care about it.

Here at Incutec we believe that design files are not a trade secret worth keeping. Closed hardware does make money, we know that, but it makes money through lock-in, not because the schematic is a secret. Unless you are genuinely doing something state of the art, the design was never the hard part. We would rather earn it by making our hardware easy to build, easy to fix and easy to buy.

So come work on it. Learn from the people already there, argue about problems in the open, stay close to the firmware devs. You get named for what you do. And your design might actually get built and sold on opendrone.be.

## Two kinds of designs

| | Electronics | Mechanical |
|---|---|---|
| Authored in | KiCad | Onshape or FreeCAD, whichever the repo declares |
| The Repository | The design itself | The CAD source, plus the exports suppliers get: STEP and drawings |
| Version Control | git | git, or Onshape's own versions and branches |
| Getting access | Fork the repo | Fork the repo. Onshape documents are by invite |

New to the tools? Explore their documentation here.

[![KiCad](https://img.shields.io/badge/KiCad-10-314CB0?logo=kicad&logoColor=white)](https://www.kicad.org/)
[![KiCad docs](https://img.shields.io/badge/KiCad-documentation-314CB0)](https://docs.kicad.org/)
[![FreeCAD](https://img.shields.io/badge/FreeCAD-1.1-CB333B)](https://www.freecad.org/)
[![FreeCAD docs](https://img.shields.io/badge/FreeCAD-documentation-CB333B)](https://wiki.freecad.org/)
[![Onshape](https://img.shields.io/badge/Onshape-CAD-1A1A1A)](https://www.onshape.com/)
[![Onshape docs](https://img.shields.io/badge/Onshape-learning%20centre-1A1A1A)](https://learn.onshape.com/)

The firmware is not ours but just like the hardware, it's Open Source. Here's the repos.

[![Betaflight](https://img.shields.io/badge/Betaflight-flight%20controller-E4002B)](https://github.com/betaflight/betaflight)
[![AM32](https://img.shields.io/badge/AM32-ESC-00875A)](https://github.com/am32-firmware/AM32)
[![ExpressLRS](https://img.shields.io/badge/ExpressLRS-radio%20link-6C3FC9)](https://github.com/ExpressLRS/ExpressLRS)

## How to contribute

> You don't need permission. Have fun. Just communicate what you're up to. We trust
> in the idea that this will stabilise in a feedback loop where designs are iterated on
> and developed in a democratic, distributed way. If you see something you think you can improve, do it!

**1. Say it on Discord.** What you want to change. Someone may
already be on it, might have experience or good ideas.

**2. Fork it and change it.**

```sh
gh repo fork OpenDrone-hw/<repo> --clone   # your own copy, cloned locally
cd <repo>
git checkout -b my-change                  # work on a branch, not on main
```

**3. Open a pull request.** Say what you changed and why.

**4. Someone reviews it.** Please discuss issues openly in the right discord channel. Someone else might be able to help.

You do not have to design anything to be useful here. Reading a schematic and asking
"why is this pull-up 10k" is a real contribution.

---

# The life of a project

Every repo starts as a copy of
[hardware-template](https://github.com/OpenDrone-hw/hardware-template)

What changes is how much of it is real, and the `status-*` topic says
how far along that is. It drives the roadmap on opendrone.be, and more: see
[What opendrone.be reads from a repo](#what-opendronebe-reads-from-a-repo).

| | Stage | Buyable | What is real | What it needs |
|---|---|---|---|---|
| 1 | [Planned](#1-planned) | no | The specification | Research, parts, opinions |
| 2 | [In progress](#2-in-progress) | no | The design | Drawing, review |
| 3 | [Alpha](#3-alpha) | no, sign-up only | The board | Flying it, breaking it |
| 4 | [Beta](#4-beta) | yes, priced | The product | Reports from real use |
| 5 | [Launched](#5-launched) | yes | All of it | Revisions |

> [!NOTE]
> Moving status is generally reserved for Admins or members of the Incutec team
> as it has an impact on the OpenDrone.be website.

## 1. Planned

No design exists yet. The specification is being argued out on Discord.

`README.md` is the one file that is properly written: what we want built, why,
the constraints it has to meet, prior art and the open questions. The spec and
architecture get argued into shape there.
A `research/` folder may collect inspiration: competing products,
teardowns, candidate parts. 

**Proposing one.** Anyone can. Say it on Discord with a paragraph of what and
why; if it holds up, an admin creates the repo and you write the README, or you
write it in a repo under your own account and it is transferred into the
organisation. A planned repo is on the roadmap and the vote ballot once it has
an entry on the site, see
[What opendrone.be reads from a repo](#what-opendronebe-reads-from-a-repo).

<details>
<summary>Starting a new product repo</summary>

1. `Use this template` on
   [hardware-template](https://github.com/OpenDrone-hw/hardware-template).
2. Clone it with `git clone --recurse-submodules`. The template carries the
   shared library as the submodule `hardware/KiCad-Library`, see
   [Parts](#parts-reduce-reuse-recycle).
3. Write the specification into `README.md`. The template README is the
   planned-stage skeleton: fill the brackets, keep the section order.
4. `git rm AGENTS.md`. It comes back from the template when the design starts.
5. `gh repo edit OpenDrone-hw/<repo> --add-topic status-planned` (admin), and
   the shared topics `open-hardware`, `kicad` (or `cad`), plus one for the
   product kind: `esc`, `flight-controller`, `receiver`, `vtx`, `remote-id`,
   `aio`, `charger`, `frame`.
6. Ask an admin for the roadmap entry on opendrone.be. It is one small pull
   request on the site, so a name and a one-line note are all that is needed.

</details>

**Moves on when someone claims it and starts a KiCad project.** 

## 2. In progress

The design is being drawn. Prototypes may be ordered. Schematics may change.

> [!IMPORTANT]
> KiCad files cannot be merged. 
> If two people edit the same `.kicad_pcb`, one of them loses their work.
> That's why communication is so important. We think Discord is the right platform for this.

### Don't start from nothing

| Mechanism | Where | Purpose |
|---|---|---|
| Project template | `hardware-template`, via `File > New Project from Template` | A new board starts from the template |
| Board Setup > Import Settings from Another Board | One-off, from the template | Brings stackup, constraints, presets, rules |
| `.kicad_dru` | Per project, committed, canonical block copied from the template | Custom rules as reviewable text |
| Lib tables | Project-local, `${KIPRJMOD}` relative | Portable paths. Global libraries are never used |
| Shared library | Submodule `hardware/KiCad-Library`, nickname `OpenDrone` | The manufactured-parts catalogue. Its 3D paths resolve through the project text variable `OPENDRONE_LIB` |

`.kicad_dru` holds custom rules only: for example ESCs run 2 oz outer
copper and need 0.16 mm clearance and track width on the outer copper layers.

### Parts: Reduce, !Reuse!, Recycle?

[OpenDrone-hw/KiCad-Library](https://github.com/OpenDrone-hw/KiCad-Library) is
the catalogue of parts that have actually been manufactured.

A symbol, footprint or 3D model is in there only if it is used on a board at
`status-alpha` or beyond, so everything has probably survived at least one production run.

`PARTS-USED.md` lists every part and which boards use it. Every repo made from
the template carries the catalogue as the git submodule `hardware/KiCad-Library`,
registered in the lib tables as `OpenDrone`. Place parts from `OpenDrone`; import
into the repo's own `lib` only what the catalogue lacks.

```sh
git clone --recurse-submodules <repo>       # new clone
git submodule update --init                 # existing clone, hardware/KiCad-Library empty
git submodule update --remote hardware/KiCad-Library && git add hardware/KiCad-Library
                                            # pull the newer catalogue in, then DRC and commit
```

Pulling a newer catalogue is a reviewed change like any other. If a repo
predates the submodule, add it: `git submodule add
https://github.com/OpenDrone-hw/KiCad-Library.git hardware/KiCad-Library`, then
copy the two `OpenDrone` lib table lines and the `OPENDRONE_LIB` text variable
from the template. A multi-board repo puts the one submodule at its root and
points both at `${KIPRJMOD}/../KiCad-Library`. To browse the catalogue outside a repo, install it through
the Plugin and Content Manager: the
[library README](https://github.com/OpenDrone-hw/KiCad-Library#usage) has the
repository URL.

Boards are assembled by [JLCPCB](https://jlcpcb.com/) from
[LCSC](https://www.lcsc.com/) parts, so each component needs an `LCSC` field.
A manufacturer part number (`MPN`) field alongside it is a plus: it keeps the
BOM usable beyond one distributor.

We don't want it to stay that way, read: https://opendrone.be/production

<details>
<summary>Repository structure from here on</summary>

| File | Audience | Contains |
|---|---|---|
| `README.md` | Consumers, curious learners | Renders, one paragraph, where it sits in the product line, what it does and basic specifications |
| `AGENTS.md` | Developers or agents | Architecture, key parts, power, connectors, layout constraints, revisions. |
| `FLASHING.md` | A user at the bench | How to flash this product. |
| `CONTRIBUTING.md` | A contributor | A stub pointing here. |
| `LICENSE` | Everyone | CERN-OHL-S-2.0, identical across repos. |

`AGENTS.md` is [an open format](https://agents.md) most agentic tools read. Keep it up to date with the KiCad files as a technical write-up of the design.

**Single Board.** Examples: [OpenFC-Lite](https://github.com/OpenDrone-hw/OpenFC-Lite), [OpenFC-Lite-Mini](https://github.com/OpenDrone-hw/OpenFC-Lite-Mini), [OpenESC-30x30](https://github.com/OpenDrone-hw/OpenESC-30x30), [OpenESC-20x20](https://github.com/OpenDrone-hw/OpenESC-20x20)

```
<repo>/
├── README.md  AGENTS.md  CONTRIBUTING.md  LICENSE
├── .gitignore  .gitattributes
├── images/                     # README renders
└── hardware/                   # the KiCad project, exactly one level down
    ├── <project>.kicad_pro / .kicad_sch / .kicad_pcb
    ├── <project>.kicad_dru            # committed
    ├── fabrication-toolkit-options.json
    ├── fp-lib-table  sym-lib-table    # project-local only
    ├── lib.kicad_sym  lib.pretty/  lib.3dshapes/
    ├── KiCad-Library/ # shared catalogue, git submodule
    ├── datasheets/    # gitignored
    ├── production/    # gitignored working exports
    └── tools/         # board-specific scripts only
```

**Multi-Board designs.** Example: [OpenRX](https://github.com/OpenDrone-hw/OpenRX). One directory per variant at repo root,
each with its own KiCad project.

**Mechanical.** Example: [OpenFrame](https://github.com/OpenDrone-hw/OpenFrame). One directory per size or variant, holding the CAD source, the STEP files and the drawings. 

**Fixtures, jigs and test boards** go in
[OpenDrone-Fixtures](https://github.com/OpenDrone-hw/OpenDrone-Fixtures).
The board's `AGENTS.md` links to its fixtures.

The project directory sits **exactly one level below the repo root**, the shape
every script and doc in the line assumes.

**Commit:** schematic, PCB and project source; project-local libraries; the
`hardware/KiCad-Library` submodule pointer; `.kicad_dru`;
`fabrication-toolkit-options.json`; the four root files; `hardware/tools/`;
`images/`.

**Ignore:** backups, autosave, locks, `*.kicad_prl`, `*.net`, `fp-info-cache`,
`.history`, `datasheets/`, working `production/`, `*.glb`, `export/`, analysis
dumps, and vendor-specific agent files.

</details>

**Moves on when boards have been made** and are in the hands of testers.

## 3. Alpha

Produced. Community testers and firmware maintainers.
Not on sale: the product page carries no price, only a sign-up to be told when
it goes on sale. Ask a sample if you'd like to help test.

`images/` gets real renders and the
repo gets its first `rev*` tag with the fab set and STEP attached. Its parts join
the shared library, having survived a production run.

Somewhere between alpha and beta a board gets a video on
[JustFPV](https://www.youtube.com/@justfpv1432): what it is, how it works in a fun 
educational manner. If you designed part of it, you are named for it or featured, depending on what you'd like.

One board revision is one tag and one GitHub release. The procedure and the shared
tooling are in
[OpenDrone-Scripts/README.md](https://github.com/OpenDrone-hw/OpenDrone-Scripts/blob/main/README.md#release-procedure)
under "Release procedure".

**Moves on when the design is settled, tested and reviewed enough to sell.**

## 4. Beta

On sale at a price, first production batch.

The repo is complete by now: `README.md` reads as a product page, `AGENTS.md`
describes the board that is actually in the box. 

**Moves on when the design stops changing between batches.**

## 5. Launched

Buyable, design will not change. A change from here is a new product.

---

# What opendrone.be reads from a repository

The website is a mirror of the repos. Edit the
fact here and the product page follows.

| Fact | Where it lives in the repo | How the site gets it |
|---|---|---|
| Status | The `status-*` topic | Fetched live: roadmap column, whether the page shows a price, and the README status badge itself (`opendrone.be/api/status/<Repo>.json`, a shields.io endpoint) |
| Product page | The repo's `homepage` field | `https://opendrone.be/products/<handle>`; several repos may share one page |
| Specifications | The first two-column table under `## Specifications` in `README.md` | Imported by `sync:specs` at release step 9. Plain ASCII, one fact per row: `2-6S`, `20 x 20 mm`, `4x DShot`; the site sets the marks. Multiboard repos (eg OpenRX) is hand-maintained on the site |
| Downloads | Release assets, named `<Repo>-<rev>-fab.zip`, `<Repo>-<rev>.step`, `<Repo>-<rev>-schematic.pdf` | Imported by `sync:downloads` when the downloads chapter is switched on |
| Provenance | Commits and contributors | Fetched live: latest commit, the contributors chapter on the product page |

A repo is on the roadmap, and on the vote ballot, once it has an entry in
[OpenDrone-Web](https://github.com/OpenDrone-hw/OpenDrone-Web):
`app/lib/roadmap-data.ts` for the structure and `content/copy/roadmap.json`
for its name and one-line note. That list is hand-maintained by admins; the
five facts above are read from the repo from then on. Before alpha the roadmap
card links to the repo, so the README is what a visitor lands on. The status
badge needs no entry: it fetches any public OpenDrone-hw repo directly.

Renders, teardown art and schematic viewers are exported from the KiCad files
by the release procedure. Everything else on a product
page (intros, pin call-outs, what is in the box) is editorial and lives on the
site.

Keep the `## Specifications` heading and the table shape when restructuring a
README.

---

# Who can change what

| Role | How you get it | What it lets you do |
|---|---|---|
| **Anyone** | A GitHub account | Open issues, open pull requests from a fork, review anyone's pull request, argue on Discord. |
| **Contributor** | One merged pull request | Named in the contributors chapter of the product page. How you work does not change. |
| **Board maintainer(s)** | Named in that repo's `AGENTS.md`| You hold the board. You approve or refuse design changes to it, decide what constitutes a revision. |
| **Organisation member** | Invitation, after sustained contribution. | Push branches directly instead of working from a fork |
| **Admin** | Incutec Staff | Releases, fab orders, secrets, org settings. Anything with money or legal exposure attached. |

# AI usage

You are responsible for what you commit. If you do not personally understand what and why an AI did something, do not commit it.

| | |
|---|---|
| ✅ | Research and datasheet reading, component search and sourcing, BOM work, library management, running ERC, DRC checks and explaining what came back, documentation, and project management. |
| ❌ | It does not (yet) make schematics, place parts or route a board. |

# Licensing

Hardware is licensed [CERN-OHL-S-2.0](https://ohwr.org/cern_ohl_s_v2.txt), a
reciprocal copyleft licence: modify a board, ship your version, and if someone
asks for your sources you hand them over on the same terms. The point is not to
stop clones but for everybody to share their improvements.

GitHub does not auto-detect CERN-OHL-S, so it reports our repos as
`NOASSERTION`. The `LICENSE` file at the repo root is the authoritative text.

**Names.** *incutec* is a registered trademark. *OpenDrone* is not.
So: build the designs, sell them, call them what
you like. What you cannot do is present your product as an official incutec
product, or use incutec branding in a way that suggests we made, tested or
support it. Describing what your board is based on is fine and always will be.

**Bundled third-party assets.** A handful of 3D models carry their own upstream
licences, CC-BY-SA-4.0 or GPL, in a notice embedded in the file itself. Those
notices still apply to those files; the repository licence does not replace
them. Where a repo bundles any, it says so in its README.

# Questions

Discord first: https://discord.gg/v3sWmTcx3R

A GitHub issue on the relevant repo works too, and is the right place for
anything that should be findable later.
