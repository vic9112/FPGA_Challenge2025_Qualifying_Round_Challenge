# 🚀 FPGA Challenge 2025 - Qualifying Round

Welcome to the **FPGA Challenge 2025 Qualifying Round**!  
This competition challenges participants to optimize machine learning models for FPGA deployment using **hls4ml**.  
Your goal is to design efficient models that **maximize accuracy** while **minimizing latency** under FPGA resource constraints.

---


## 🛠 Challenge Overview
- 
- Develop and optimize machine learning models for FPGA implementation.
- Target task: **Image Classification (CIFAR-10)**.
- Final results will be evaluated based on the performance of the **hls4ml-converted HLS model**:
  - Accuracy
  - FPGA resource usage
  - Inference latency

---

## 📊 Performance Scoring System & Dataset

You can access detailed information about the scoring system and datasets on Kaggle for the task via the following links:

- 🖼️ **[Image Classification Task Competition- Kaggle Page](#)** *(for testing your model and flow)*  
  → *Note: Final evaluation will be conducted separately and is not based on Kaggle leaderboard.*

---

## 💻 Competition Environment Rules on FPGA and hls

- **Target FPGA Board:** `PYNQ-Z2`  
  <img src="./Figures/PYNQ-Z2-Large-scaled.jpg" alt="PYNQ-Z2 FPGA" width="400">

- **hls4ml Version:** `1.1.0`  
- **HLS Toolchain:** `Xilinx Vitis HLS 2023.2`  
  - **Installation Guide:** *Coming Soon*

---

## 🧮 Scoring Criteria

Your final score will be based on three key components:

- **Accuracy**:  
  Evaluated using the CIFAR-10-based test set that is same as the one on Kaggle.

- **HLS Synthesis Results** *(provided by your submission)*:
  - **C Synthesis Results**:
    - **Resource Usage**: LUTs, DSPs, BRAMs
    - **Latency**: Inference delay (in seconds)

---

## 📣 Official Announcements and Q&A

- All official updates, rule clarifications, and Q&A will be posted in the **[Discussions tab](https://github.com/nycu-pcs-lab/FPGA_Challenge2025_Qualifying_Round_Challenge/discussions)** of this repository.
- Please **watch** this repository to receive timely notifications.
- Do **not** use the Kaggle page for discussion or rule updates.

---

