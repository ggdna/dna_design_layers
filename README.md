# dna_design_layers

English | [Deutsch](README.de.md)

Gives a repo the guides and skills to work through the seven layers of
product design, from observed behaviour to the surface.

## Motivation

Product decisions build on each other: what users do and what the domain
holds come before needs, needs before strategy, strategy before the
conceptual model, the flow and the surface. A weak lower layer creates
debt in every layer above. The layer gives a repo a method to make these
decisions one layer at a time, with a skill per layer that an agent can
run in a design session, and to record the decisions instead of
transcripts. The guides and skills started in dna_plan and moved here as
a layer of their own.

## Usage

Declare it as a dev-dependency and initialize once:

```bash
pnpm add -D @ggdna/dna-design-layers   # TypeScript projects
dart pub add dev:dna_design_layers     # Dart projects
gg dna init
```

`gg dna init` places a test that instantiates and verifies the DNA on
every test run. It copies the guides to `doc/guides/` and
`doc/guides/layers/`, and the skills to `.claude/skills/layers-*/`.

Type `/layers-intro` in Claude Code at the start of a design session.
Run `/layers-orient` when it is unclear which layer needs attention: it
audits all seven layers and recommends one. Then run the skill of the
layer you work on.

## Guides

- `dna/doc/guides/layers-guide.md` — the layer system, design as decision
  making, how to use the skills, where the results are recorded
- `dna/doc/guides/layers/` — one short guide per layer, each a library of
  techniques for that layer's decisions: `observed-behaviour-guide.md`,
  `domain-guide.md`, `user-needs-guide.md`, `product-strategy-guide.md`,
  `conceptual-model-guide.md`, `interaction-flow-guide.md`,
  `surface-guide.md`, plus `orient-guide.md` for the audit across all
  layers

## Skills

- `/layers-intro` — the orientation in the layer system; load it first,
  the other skills depend on it
- `/layers-orient` — audits all seven layers, names the bottleneck layer
  and recommends where to focus
- `/layers-observed-behaviour` — plans user research and turns it into
  confidence-rated findings about what users actually do
- `/layers-domain` — maps the concepts, conflicting terms and bounded
  contexts of a domain
- `/layers-user-needs` — elicits and prioritises the needs, pains and
  desires that feed the product strategy
- `/layers-product-strategy` — connects user opportunities to business
  outcomes and solution bets, and tests the riskiest assumptions cheaply
- `/layers-conceptual-model` — defines the objects, relations, states and
  vocabulary of the product, independent of any interface
- `/layers-interaction-flow` — maps the places, affordances, edge cases
  and failure paths of a flow, without committing to a visual form
- `/layers-surface` — audits the surface against the layers below:
  vocabulary, consistency, feedback, hierarchy, accessibility

Each skill reads the guide of its layer.

## Scope

The layer ships the method, not the results. Where the results of a
design session land — one decision per file in a project management repo
— is the job of [dna_plan](https://github.com/ggdna/dna_plan); the layers
guide links its PM repo guide when the repo has it. The guides follow
[layers-skills](https://github.com/jamiemill/layers-skills) by Jamie Mill
(MIT).

## Layers

The layer is orthogonal: `dna/_dna.json` lists no parent layers, and it
stays parent-less on purpose — a parent here would reach every consumer
of this topic whether that repo asked for it or not, and taking an
umbrella back would close a cycle as soon as that umbrella lists this
layer.

No umbrella layer lists it yet, `dna_ggdna` included: a repo that wants
the topic lists `dna_design_layers` in its own `dna/_dna.json`.

## Variables

- `dnaCopyrightHolder` — the name in the license header of every file;
  `dna/_dna.json` declares no `mustOverride`, so a consuming repo is not
  forced to set it, and one that does not set it in its own
  `dna/_vars.json` gets the default `ggdna`

## Development

The `dna/` folder is hand-authored source and is never generated. The repo
instantiates its own DNA — run `dart test` after changes; commit first, a
file the DNA would overwrite must not carry uncommitted work.

Edit the files below `dna/`, not their copies in `doc/` and `.claude/`,
which the test overwrites.

## License

MIT — see [LICENSE](LICENSE).
