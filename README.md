# 5G NR PUSCH Tutorial (Sionna + TensorFlow)

This repository reproduces the **5G NR PUSCH** tutorial using **Sionna** (TensorFlow-based) and provides additional parameter variations to verify the system behavior via **BER/BLER** curves.

---

## Goal
- Rebuild and run the official **5G NR PUSCH** pipeline in Sionna.
- Understand the main signal processing chain: **coding → modulation → channel → decoding**.
- Validate performance by sweeping/adjusting key parameters (e.g., Eb/N0 (SNR), number of layers, mobility speed) and observing **BER/BLER**.

---

## Repository contents
- `5G_NR_PUSCH.ipynb`  
  Baseline PUSCH tutorial run (reference configuration), including BER/BLER simulations.
- `snr_sweep.ipynb`  
  Eb/N0 (or SNR) sweep and comparison across different settings (e.g., layers).
- `antenna_speed.ipynb`  
  Parameter variation (e.g., mobility speed / antenna-related settings depending on the notebook configuration).
- `requirements.txt`  
  Python dependencies (pinned to the verified working versions).

---

## Installation
Tested environment:
- OS: Ubuntu 22.04.5 LTS
- Python: 3.10.12
- TensorFlow: 2.19.1 (CUDA build)
- Sionna: 1.2.1
- NumPy: 1.26.4
- Matplotlib: 3.10.8
- Jupyter Server: 2.17.0

> **CPU-only note:** If no GPU is available, notebooks can still run on **CPU**, but simulations will be **slower**.

Install with pip (recommended: use a virtual environment):
```bash

python3 -m venv .venv
source .venv/bin/activate
pip install -U pip
pip install -r requirements.txt
```
### How to run
From the repo folder:

`jupyter notebook --ip=0.0.0.0 --port=8888`

The terminal will print a URL such as:

`http://127.0.0.1:8888/tree?token=...`

Copy the URL into your browser, then:
Open a notebook (.ipynb)
Run: Kernel > Restart & Run All

