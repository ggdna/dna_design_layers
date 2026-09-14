# Example

`dna_design_layers` is a DNA layer: it ships the guides of the seven layers
of product design and the `/layers-*` skills, no code. Declare it as a dev
dependency and instantiate it once:

```bash
dart pub add dev:dna_design_layers     # Dart projects
pnpm add -D @ggdna/dna-design-layers   # TypeScript projects
gg dna init
gg dna build
```

The placed test instantiates the layer on every test run.
