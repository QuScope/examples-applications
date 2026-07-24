# QuScope Example Applications

**Welcome to the official example and tutorials repository for [QuScope](https://github.com/QuScope/QuScope)** - a quantum-enhanced electron microscopy analysis framework.

This repository contains interactive notebooks, reproducible demos, and educational materials designed to showcase how to use QuScope for a range of quantum-enhanced tasks, including:

Image Analysis:
- Encoding, Decoding, Filters & Denoising

EELS Analysis:
- Quantum Richardson-Lucy Deconvolution (QRLD) - *coming soon*
- Quantum Kramers-Kronig Transformation (QKKT) - *coming soon*
- Low-Loss Analysis - *coming soon*
- Core-Loss Analysis - *coming soon*

Electron Diffraction:
- Phase Analysis - *coming soon*
- Space Group Analysis - *coming soon*
- Convergent Beam Electron Diffraction (CBED) - *coming soon*

Simulations:
- Quantum-Enhanced Weak Phase Object Approximation
- Quantum-Enhanced Multislice Algorithm
- Quantum CTEM & STEM simulations

General:
- Quantum encoding and transformations
- Unified backend abstraction (simulator & IBM Quantum hardware)
- Material workflows (MoS2, Graphene, and more)

---

## Installation

To use these examples, install QuScope v0.2.0:

```bash
pip install quscope==0.2.0
```

---

## 📁 Repository Structure

```bash
examples-applications/
├── notebooks_v0.2.0/                   # Tutorials for QuScope v0.2.0
│   ├── 01_getting_started.ipynb        # Backends, materials, quantum encoding
│   ├── 02_quantum_ctem_advanced.ipynb  # Advanced CTEM simulation
│   ├── 03_material_workflows.ipynb     # Material loading and parameter access
│   ├── 05_fully_quantum_ctem.ipynb     # Fully quantum CTEM pipeline
│   ├── 06_quantum_ctf_envelope.ipynb   # Quantum CTF envelope functions
│   ├── 07_si3n4_quantum_multislice.ipynb # Si3N4 quantum multislice
│   ├── 10_quantum_ctem.ipynb           # Quantum CTEM end-to-end
│   ├── 11_quantum_stem.ipynb           # Quantum STEM simulation
│   └── legacy/                         # Legacy notebooks (pre-v0.2.0)
├── notebooks/                          # Earlier tutorial notebooks
│   ├── images_01_denoising.ipynb       # Image denoising tutorial
│   ├── simulations_01_ctem.ipynb       # CTEM simulation tutorial
│   └── Quantum_ctem_paper_full_example.ipynb
├── datasets/                           # Supporting datasets
├── LICENSE.txt                         # MIT License
└── README.md