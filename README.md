# BoltzGen target–binder complex

This repository contains one BoltzGen design in which the target is fully
specified from PDB `1G13`, chain A, while the binder sequence and structure are
unknown. The only binder input is a length range of 80–140 residues.

## Interactive viewer

Open the GitHub Pages site:

**https://oliverwang0908.github.io/02741/**

Controls:

- Left drag: rotate
- Mouse wheel: zoom
- Right drag: pan
- Buttons: cartoon, sticks, molecular surface, spin, and reset

## Result

- Generated binder: chain A, 110 residues
- Target in generated complex: chain B, 162 residues
- Binder input sequence: unknown
- Generation method: BoltzGen 0.3.2 all-atom diffusion
- Upstream BoltzGen revision: `a07fea1153111ef453aaea7a15697ee05de9291f`
- Slurm GPU job: `57665060`
- Diffusion design time: 174.1 seconds for the design stage; zero failed examples

The chain identifiers in the generated complex are assigned by the BoltzGen
writer and therefore differ from the input specification: input target chain A
becomes chain B in the generated complex, and the generated binder is chain A.

## Files

- [`design_spec.yaml`](design_spec.yaml): target and unknown-binder specification
- [`assets/1g13_target.cif`](assets/1g13_target.cif): known target input
- [`assets/1g13prot_complex.cif`](assets/1g13prot_complex.cif): generated complex
- [`assets/1g13prot_overview.png`](assets/1g13prot_overview.png): static overview
- [`index.html`](index.html): interactive 3Dmol.js viewer

## Scope

This is one generated demonstration sample. It has not undergone experimental
validation, and only the core BoltzGen design stage was run; inverse folding,
independent refolding, affinity estimation, and wet-lab validation are outside
the scope of this example.

BoltzGen source and paper:

- https://github.com/HannesStark/boltzgen
- https://doi.org/10.1101/2025.11.20.689494
