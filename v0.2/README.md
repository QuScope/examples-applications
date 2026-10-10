# v0.2: current examples

| notebook | topic | needs QuScope |
|---|---|---|
| `01_getting_started` | backends, materials, quantum encoding | 0.2.0 |
| `02_quantum_ctem_advanced` | advanced CTEM simulation | 0.2.0 |
| `03_material_workflows` | material loading and parameter access | 0.2.0 |
| `05_fully_quantum_ctem` | fully quantum CTEM pipeline | 0.2.0 |
| `06_quantum_ctf_envelope` | CTF envelope functions | 0.2.0 |
| `07_si3n4_quantum_multislice` | Si3N4 quantum multislice | 0.2.0 |
| `10_quantum_ctem` | CTEM end to end | 0.2.0 |
| `11_quantum_stem` | quantum STEM on a toy MoS2 potential | 0.2.0 |
| `12_stem_ctf_vs_abtem` | STEM CTF and the quantum-circuit probe vs abTEM | 0.2.1 |
| `13_srtio3_stem_imaging` | SrTiO3 [001]: HAADF, ADF, BF, ABF, iDPC vs abTEM | 0.2.1 plus [PR #28](https://github.com/QuScope/QuScope/pull/28) |

Notebooks 08 and 09 live in the QuScope repository and there is no 04. QuScope's own 12 and 13 are the experimental diffraction and Bloch-wave notebooks (planned for [v0.3](../v0.3)); 12 and 13 here are separate examples.

## Install

Notebooks 01-11 run on the released package:

```bash
pip install quscope==0.2.0
```

Notebooks 12 and 13 need the 0.2.1 fixes (not on PyPI yet) and [abTEM](https://abtem.readthedocs.io) >= 1.0:

```bash
pip install git+https://github.com/QuScope/QuScope.git abtem
```

QuScope declares `qiskit>=2`, abTEM still needs NumPy 1.x. If pip reports a conflict, install QuScope with `--no-deps` into an environment that already has `qiskit`, `abtem` and `numpy<2`.

## Notes

* Notebooks save their figures into the working directory. The copies in `figures/` are reference outputs from earlier runs.
* 12 and 13 are executed and assert their agreement with abTEM. 13 simulates 1024 probe positions (about 5 minutes); set `SCAN = 16` for a quick run.
