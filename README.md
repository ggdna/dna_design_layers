# dna_design_layers

DNA layer: the seven layers of product design — guides and `/layers-*`
skills.

## What it ships

- `doc/guides/layers-guide.md` — the layer system, design as decision
  making, how to use the skills, where results are recorded
- `doc/guides/layers/*-guide.md` — one short guide per layer plus the
  orient audit
- `.claude/skills/layers-*` — nine skills that load the matching guide

The guides follow
[layers-skills](https://github.com/jamiemill/layers-skills) by Jamie Mill
(MIT). [dna_plan](https://github.com/ggdna/dna_plan) tells where the
results of a design session land in a project management repo.

## Layers

Orthogonal: this layer carries only its own topic and is combined with the
other layers by [dna_ggdna](https://github.com/ggdna/dna_ggdna). It declares no
parent, and it must not — the umbrella lists every topic layer, so taking the
umbrella back would close a cycle, and a parent here would reach every consumer
of this topic whether that repo asked for it or not.

## Variables

- `dnaCopyrightHolder` — the name in the license header of every file

## Development

The `dna/` folder is hand-authored source and is never generated. The repo
instantiates its own DNA — run `dart test` after changes; commit first, a file
the DNA would overwrite must not carry uncommitted work.
