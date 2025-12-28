# MSF for HP Ecological Networks

This repository contains numerical implementation of Master Stability Function analysis for synchronized Hastings-Powell ecological networks under different **linear (diffusive) pairwise migration schemes**.

The simulations correspond to the preliminary stage of my PhD research, where the goal is to establish **reference synchronizability regimes** using the classical MSF framework, before extending the study to more sophisticated pairwise couplings and higher-order (triadic) ecological interactions.

---

## Folder structure
- `code/` → notebooks to compute MSF and generate .txt data
- `data/` → numerical output files, r vs Λ(r)
- `figures/` → PDF plots produced by the plotter notebook

---

## Migration schemes considered
We analyze:
- **Single-species migration**
  - x → basal resource
  - y → intermediate predator
  - z → top predator

- **Pairwise combinations**
  - xy, xz, yz

- **Fully coupled migration**
  - xyz

For each case, the MSF Λ(r) is computed as a function of the normalized coupling parameter r, and the synchronization stability regions are identified from the sign of Λ(r).

---

## Numerical methodology (very short summary)
- HP system integrated via 4th-order Runge-Kutta  
- Time step: Δt = 10⁻³  
- Integration time: 0 ≤ t ≤ 10³  
- Largest transverse Lyapunov exponent computed from the variational equation  
- Synchronizability intervals extracted from MSF zero crossings (bisection method)


---

## Requirements
- Python ≥ 3.11
- NumPy
- SciPy
- Matplotlib
- Jupyter Notebook

---

## How to use
1. Open any notebook in `code/`
2. Run the notebook to reproduce the MSF computation
3. Corresponding data and figures are in the `data/` and `figures/` folders

---

## Status
This is **work in progress** and corresponds to the *pairwise diffusive coupling stage* of the project.  
Higher-order interactions and nonlinear ecological couplings will be explored in the next stages.

---

## License
MIT License


