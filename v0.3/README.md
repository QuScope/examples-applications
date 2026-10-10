# v0.3: in preparation

QuScope 0.3 is not released and its scope is not final. This folder collects what the examples will cover and how a notebook should be written, so new examples can land as the features stabilise.

## Planned examples

From the QuScope roadmap: the modules below are experimental in 0.2 (APIs may change) and are the candidates to join the stable release.

| area | QuScope module | starting point |
|---|---|---|
| diffraction: SAED, CBED, nBD, Kikuchi, EBSD | `quantum_diffraction` | QuScope `docs/notebooks/12_quantum_diffraction.ipynb` |
| frozen phonon, thermal diffuse scattering | `quantum_frozen_phonon` | `13_bloch_wave_and_frozen_phonon.ipynb` |
| Bloch-wave QPE eigensolver | `quantum_bloch_wave` | `13_bloch_wave_and_frozen_phonon.ipynb` |
| advanced fully quantum TEM, multislice circuit | `quantum_multislice_circuit` | `08_fully_quantum_tem_advanced.ipynb`, `09_quantum_multislice_circuit_test.ipynb` |

Natural follow-ups from v0.2: thermal vibrations in the SrTiO3 STEM images (notebook 13 has none, so absolute HAADF levels are idealised), and larger cells, which need more qubits.

Still undecided: image analysis (encoding, filters, denoising) and EELS analysis (QRLD, QKKT, low-loss and core-loss), listed as "coming soon" in the old README.

## Writing a notebook

Copy [`00_template.ipynb`](00_template.ipynb). Checklist:

1. Name it `NN_topic.ipynb`, continuing the numbering, and state the minimum QuScope version in the first cell.
2. Validate against a classical reference (abTEM, py4DSTEM, or a closed form) with numbers and an `assert`, not only a picture.
3. Execute it top to bottom and commit the outputs; it must run without errors in a clean environment.
4. No local paths in outputs (`grep -l "/Users/" *.ipynb` should be empty); data files go in a `datasets/` folder next to it.
5. Say what is idealised (periodic cell, no thermal scattering, grid size) and what the run costs in qubits and time.
6. Keep the kernel spec as `python3`.
