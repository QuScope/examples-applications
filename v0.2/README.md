# v0.2: current examples

| notebook | topic | written for QuScope |
|---|---|---|
| `01_getting_started` | backends, materials, quantum encoding | 0.2.0 |
| `02_quantum_ctem_advanced` | advanced CTEM simulation | 0.2.0 |
| `03_material_workflows` | material loading and parameter access | 0.2.0 |
| `06_quantum_ctf_envelope` | CTF envelope functions | 0.2.0 |
| `07_si3n4_quantum_multislice` | Si3N4 quantum multislice vs abTEM and a NumPy multislice (about 35 min, 14 qubits); optional IBM section, off by default | 0.2.0 |
| `10_quantum_ctem` | CTEM end to end | 0.2.0 |
| `12_stem_ctf_vs_abtem` | STEM CTF and the quantum-circuit probe vs abTEM | 0.2.1 |
| `13_srtio3_stem_imaging` | SrTiO3 [001]: HAADF, ADF, BF, ABF, iDPC vs abTEM | 0.2.1 plus the STEM fixes merged in [PR #28](https://github.com/QuScope/QuScope/pull/28) |

Numbers follow the QuScope docs. QuScope's own 12 and 13 are the experimental diffraction and Bloch-wave notebooks (see [v0.3](../v0.3)); 12 and 13 here are separate examples.

Left out on purpose, because they are copies of tutorials in QuScope's `docs/notebooks` (which have executed outputs): `05_fully_quantum_ctem` (long paper companion: 128x128 CTEM, through-focus series, resource estimates, a 4x4 run on IBM hardware) and `11_quantum_stem` (toy-potential STEM, replaced by 13). 08 and 09 are also only in the QuScope docs.

## Install

Notebooks 01-10 were written for QuScope 0.2.0 and re-run on 0.2.1; they should also work on the released package (`pip install quscope==0.2.0`), which was not re-tested.

Notebooks 12 and 13 need the 0.2.1 fixes (not on PyPI yet) and [abTEM](https://abtem.readthedocs.io) >= 1.0. These also cover 01-10:

```bash
pip install git+https://github.com/QuScope/QuScope.git abtem
```

QuScope's dependencies (`qiskit>=2`) and abTEM install together: pip resolves them to Qiskit 2.5, NumPy 2.5 and abTEM 1.0.10, and QuScope's test suite passes in that environment. (An earlier version of this README said abTEM needs NumPy 1.x; that was wrong.)

Notebooks 02 and 07 import `quscope.ctem.KirklandPotential`, QuScope's own potential table. That class was removed after 0.2.1 in favour of `AtomicPotential`, which takes potentials from abTEM ([QuScope PR #32](https://github.com/QuScope/QuScope/pull/32)); the old potentials were 1.2 to 1.9 times larger than abTEM's. Their stored outputs come from the old potentials, so run them on QuScope 0.2.x as written, or switch the import to `AtomicPotential` (and expect different numbers).

## Notes

* Notebooks save their figures into the working directory. The copies in `figures/` are reference outputs from earlier runs.
* All notebooks were re-run on QuScope 0.2.1 with no errors; 07 takes about 35 minutes.
* 12 and 13 are executed and assert their agreement with abTEM. 13 simulates 1024 probe positions (about 5 minutes); set `SCAN = 16` for a quick run.
