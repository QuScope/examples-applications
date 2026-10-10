# v0.1: archived tutorials

Written for QuScope 0.1.x (`pip install quscope==0.1.2`). They are kept for reference and were **not** re-run against newer releases; start from [`../v0.2`](../v0.2) for current code.

| notebook | topic |
|---|---|
| `Quantum_ctem_paper_full_example.ipynb` | full example from the CTEM paper (arXiv:2602.13438) |
| `simulations_01_ctem.ipynb` | CTEM simulation tutorial |
| `images_01_denoising.ipynb` | image denoising tutorial (uses `datasets/noisy_image_example.png`) |
| `legacy/` | earlier experiments: image encoding, image processing, 1D weak phase object, EELS analysis |

`datasets/` holds the images used by these notebooks (`duck_image.jpeg`, `noisy_image_example.png`) and a crystal structure file (`ICSD_CollCode59159-K1_33Mn8O16.cif`) that no notebook currently reads.

The paper example uses `quscope.ctem.KirklandPotential`, which newer QuScope versions no longer have (replaced by `AtomicPotential`, abTEM's potentials), so it needs a 0.1.x or 0.2.x install.
