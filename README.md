# 5G NR PUSCH Simulation (Sionna + TensorFlow)

Notebook-based experiments for 5G NR PUSCH link-level simulations using **Sionna** (TensorFlow backend).
This repository is prepared for reproducible runs: clone → install → run notebooks.

---

## Contents
- `5G_NR_PUSCH.ipynb` — baseline PUSCH pipeline
- `snr_sweep.ipynb` — BER/BLER vs Eb/N0 (or SNR) sweep
- `atenna_speed.ipynb` — parameter variation (antenna/speed)
- `requirements.txt` — pinned Python environment
- `README.md`

---

## Environment
- OS: Ubuntu 22.04.5 LTS
- Python: 3.10.12
- pip: 25.3
- NVIDIA GPU: GeForce RTX 4060 (Driver 560.94, CUDA 12.6) — optional
- TensorFlow: 2.19.1 (GPU enabled)
- Sionna: 1.2.1
- NumPy: 1.26.4
- Matplotlib: 3.10.8
- Jupyter Server: 2.17.0

> Note: If no GPU is available, notebooks can still run on CPU but will be slower.

---

## Installation via pip

### 1) Create a virtual environment
```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -U pip
```
### 2) Install dependencies 
```bash
pip install -r requirements.txt
```
## Quick start (run)

### Run with Jupyter
Launch Jupyter from the repo folder:
```bash
jupyter notebook

