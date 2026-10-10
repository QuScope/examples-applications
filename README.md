# QuScope Example Applications

Notebooks and tutorials for [QuScope](https://github.com/QuScope/QuScope), an open-source Python framework for quantum algorithms in (transmission) electron microscopy. The electron wavefunction is amplitude-encoded on qubits, and every optical element (phase grating, Fresnel propagation, objective lens) is a diagonal unitary between quantum Fourier transforms. Results are validated against classical references such as abTEM.

Website: https://quscope.github.io · Docs: https://quscope.readthedocs.io

## Pick your version

| folder | QuScope | status | contents |
|---|---|---|---|
| [`v0.3/`](v0.3) | 0.3 (not released) | in preparation | planned examples, notebook template and checklist |
| [`v0.2/`](v0.2) | 0.2.0 and 0.2.1 | **current** | CTEM and STEM pipelines, CTF, Si3N4 multislice, SrTiO3 STEM imaging vs abTEM |
| [`v0.1/`](v0.1) | 0.1.x | archived | first tutorials, paper example and legacy notebooks |

Each folder has its own README with the notebook list, the QuScope version each notebook needs, and install instructions.

## Layout

```
examples-applications/
├── v0.3/    planned examples, 00_template.ipynb
├── v0.2/    notebooks 01-13, figures/ (reference outputs)
├── v0.1/    notebooks, legacy/, datasets/
├── LICENSE.txt
└── README.md
```

**Developed by** [Sean D. Lam](https://arxiv.org/search/quant-ph?searchtype=author&query=Lam,+S+D) and [Roberto dos Reis](https://arxiv.org/search/quant-ph?searchtype=author&query=Reis,+R+d), Northwestern University.

**Papers**
- [*QuScope: An Open-Source Python Framework for Quantum-Circuit Simulation of Transmission Electron Microscopy*](https://arxiv.org/abs/2608.02782), arXiv:2608.02782 [quant-ph], Aug 2026
- [*Quantum Algorithm Framework for Phase-Contrast Transmission Electron Microscopy Image Simulation*](https://arxiv.org/abs/2602.13438), arXiv:2602.13438 [quant-ph], Feb 2026

Contributions are welcome; see the [contributor guide](https://quscope.readthedocs.io/en/latest/contributing.html). MIT license.
