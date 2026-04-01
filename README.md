# xSFF Data

Simulation data and plotting notebook for the cross spectral form factor (xSFF), a diagnostic for detecting hidden symmetries in quantum many-body systems.

Companion to: *Bootstrapping Symmetries in Quantum Many-Body Systems from the Cross Spectral Form Factor*, Chen Bai, Zihan Zhou, Bastien Lapierre & Shinsei Ryu.

## Contents

- **`plot_xSFF.ipynb`** — Jupyter notebook that reproduces all xSFF figures from the data below.
- **`plot_style.mplstyle`** — Matplotlib style file used by the notebook.
- **`xSFF_code/`** — Precomputed xSFF data (`.npz` files) for each model:

| Directory | Model | Visible symmetry | Parameters |
|-----------|-------|-------------------|------------|
| `S3_Chain_L8_th0.00_n200` | S3 spin chain | Z_3 | L=8, 200 samples |
| `D4_Chain_L8_s0.25_n200` | D4 / Kennedy-Tasaki chain | Z_2 x Z_2 | L=8, sigma=0.25, 200 samples |
| `AT_Potts_L7_h1.0_n200` | Ashkin-Teller Potts | Z_2 x Z_2 | L=7, h=1.0, 200 samples |
| `QTC_L9_th0.5236_n200` | Quantum Tensor Chain | Z_3^2 ⋊ Z_2 | L=9, theta=pi/6, 200 samples |
| `QTC_L9_th0.7854_n200` | Quantum Tensor Chain | Z_3^2 ⋊ Z_2 | L=9, theta=pi/4, 200 samples |
| `Hubbard_U1xU1_L8_U4.0_t3.0_s0.5_n200` | Fermi-Hubbard (disordered hopping) | U(1) x U(1) | L=8, U=4, t0=3, sigma=0.5, 200 samples |
| `Hubbard_U1xU1_L8_U4.0_t3.0_s0.0_n1` | Fermi-Hubbard (clean) | U(1) x U(1) | L=8, U=4, t0=3, no disorder |

- **`floquet_system/`** — Floquet model data:

| Directory | Model | Visible symmetry | Parameters |
|-----------|-------|-------------------|------------|
| `KDBH_N9_L8_k0.9_s0.25_n200` | Kinetically-Driven Bose-Hubbard | D_8 | N=9, L=8, kappa=0.9, sigma=0.25, 200 samples |

## Usage

```bash
git clone https://github.com/ZihanZhou26/xSFF_data.git
cd xSFF_data
jupyter notebook plot_xSFF.ipynb
```

Requirements: `numpy`, `matplotlib`, `scipy`.
