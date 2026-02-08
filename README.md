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
- Quantum-Enhanced Multislice Algorithm - *coming soon*

General:
- Quantum encoding and transformations

---

## Installation

To use these examples, first install QuScope:

```bash
pip install quscope
```

---

## 📁 Repository Structure

```bash
example_applications/
├── notebooks/                          # Jupyter notebooks organized by version
│   ├── v1.0/                           # Tutorials for QuScope v1.0
│   ├── images_01_denoising.ipynb       # Tutorial for denoising images
│   ├── simulations_01_ctem.ipynb       # Tutorial for simulating CTEM images
│   ├── Quantum_ctem_paper_full_example.ipynb  # Full CTEM paper example
├── datasets/                           # Supporting datasets or synthetic examples
├── LICENSE.txt                         # MIT License
└── README.md