# 5G NR PUSCH Simulation (Sionna + TensorFlow)

Notebook-based experiments for 5G NR PUSCH link-level simulations using Sionna (TensorFlow backend).
This repository is prepared so that it can be cloned and reproduced.

---

## Mục tiêu
- Mô phỏng pipeline 5G NR PUSCH bằng Sionna.
- Đánh giá BER/BLER theo Eb/N0 (hoặc SNR) và kiểm chứng ảnh hưởng của tham số mô phỏng.

---

## Nội dung repo
- `5G_NR_PUSCH.ipynb`: baseline PUSCH pipeline (cấu hình gốc)
- `snr_sweep.ipynb`: quét SNR/EbN0 để vẽ BER/BLER
- `atenna_speed.ipynb`: thay đổi tham số (antenna/speed) để so sánh
- `requirements.txt`: danh sách package + version để tái lập môi trường

---

## Môi trường 
- OS: Ubuntu 22.04.5 LTS
- Python: 3.10.12
- TensorFlow: 2.19.1 (GPU enabled)
- Sionna: 1.2.1
- NumPy: 1.26.4
- Matplotlib: 3.10.8
- Jupyter Server: 2.17.0

---

## Cài đặt
```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -U pip
pip install -r requirements.txt

