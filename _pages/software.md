---
layout: archive
permalink: /software/
title: "Software"
author_profile: true
redirect_from:
  - /sw
---

**AMS/DFTB**: Spin-Orbit Coupling in SCC-DFTB/GFN-xTB
  (Commercial code)
  * **Role:** Contributor — implemented self-consistent spin-orbit coupling in AMS/DFTB end to end, released in AMS2025.
  * SCC-DFTB and GFN-xTB; molecules and periodic systems; MPI-parallel; from input to SOC band structures and DOS in the AMS GUI.
  * [Software for Chemistry & Materials B.V. (SCM)](https://www.scm.com)
  * Relevant publication: [W. Li, P. Philipsen, T. Brumme, T. Heine. *Advanced Quantum Technologies* 9(4), e01001 (2026)](https://advanced.onlinelibrary.wiley.com/doi/full/10.1002/qute.202501001)
  * **ml_soc_xtb**: A physics-constrained ML protocol that learns environment-dependent SOC parameters inside the Hamiltonian from DFT
    * The goal is SOC parameters for AMS/DFTB. AMS can supply DFT references natively; the open-source GPAW + DFTB+ stack keeps the protocol reproducible outside AMS.

**twistHS**: Builds commensurate moiré supercells for twisted van der Waals bilayers, with moiré analysis and an MLIP relaxation workflow.
  * **Role:** Sole developer.
  * Coincidence-lattice search over Hermite-normal-form sublattices that preserves the moiré wave vectors, up to higher order, rather than strain alone; a polar decomposition separates each layer's rotation from its strain.
  * Vectorized construction builds a 1.3M-atom supercell in 0.15 s (~4,000× faster); optional JAX backend for GPU.
  * MLIP workflow: MACE-MP-0 relaxation and fine-tuning; inexpensive FF labels test whether small cells capture moiré local environments, and pre-registered criteria set a go/no-go decision and DFT budget before any DFT is spent.
  * [Download](https://github.com/i-wli/twistHS)
  * Relevant publication: [W. Li, T. Brumme, T. Heine. *npj 2D Mater Appl* 8, 43 (2024)](https://www.nature.com/articles/s41699-024-00477-6)

**Dftb2pi**: A DFTB+ patch to compute generalized momentum operator for optical selection rules and exciton g-factor
  (Open source soon)
  * [DFTB+](https://dftbplus.org)
  * Relevant publication: [W. Li, G. Jha, T. Brumme, T. Heine. *ChemRxiv*, doi:10.26434/chemrxiv-2023-g6v5r-v2 (2025)](https://doi.org/10.26434/chemrxiv-2023-g6v5r-v2)
