# v0.3: in preparation

QuScope 0.3 is not released and its scope is not final. This folder collects what the examples will cover and how a notebook should be written, so new examples can land as the features stabilise.

## Scope

**CBED first.** Convergent-beam electron diffraction is the first new technique, built on the multislice circuits that already exist in v0.2. SAED, nanobeam diffraction, Kikuchi and EBSD are not planned.

**Thermal vibrations through the whole stack.** Frozen-phonon configurations and thermal diffuse scattering (TDS) become an option wherever the simulation is multislice, to get closer to real specimens (compare abTEM's `FrozenPhonons`): CTEM, STEM (HAADF and ADF are dominated by TDS), and CBED. The module `quantum_frozen_phonon` is experimental in 0.2 and is the starting point.

**Not in v0.3.** The Bloch-wave eigensolver (`quantum_bloch_wave`, QPE) moves to the next version: it is about the fundamental physics of scattering rather than image simulation.

## Planned examples

| example | what it shows | reference |
|---|---|---|
| CBED of SrTiO3 [001] | CBED pattern from the quantum multislice, thickness series | abTEM `PixelatedDetector` |
| frozen-phonon STEM of SrTiO3 | HAADF and ADF with thermal vibrations, convergence with the number of configurations | abTEM `FrozenPhonons` |
| CBED with TDS | diffuse background of the CBED pattern from frozen-phonon averaging | abTEM |
| thermal vibrations in CTEM | frozen-phonon CTEM image | abTEM |

QuScope notebooks to start from: `08_fully_quantum_tem_advanced`, `09_quantum_multislice_circuit_test`, `12_quantum_diffraction`, `13_bloch_wave_and_frozen_phonon` (in `docs/notebooks` of the QuScope repo; the frozen-phonon part only).

Notebook 13 in [`../v0.2`](../v0.2) has no thermal scattering, so its absolute HAADF and ADF levels are idealised; the second example above is its direct follow-up.

Image analysis (encoding, filters, denoising) and EELS analysis (QRLD, QKKT, low-loss, core-loss) were listed as "coming soon" in the old README and are not scheduled.

## Writing a notebook

Copy [`00_template.ipynb`](00_template.ipynb). Checklist:

1. Name it `NN_topic.ipynb`, continuing the numbering, and state the minimum QuScope version in the first cell.
2. Validate against a classical reference (abTEM, py4DSTEM, or a closed form) with numbers and an `assert`, not only a picture.
3. Execute it top to bottom and commit the outputs; it must run without errors in a clean environment.
4. No local paths in outputs (`grep -l "/Users/" *.ipynb` should be empty); data files go in a `datasets/` folder next to it.
5. Say what is idealised (periodic cell, no thermal scattering, grid size) and what the run costs in qubits and time.
6. Keep the kernel spec as `python3`.
