# 🚀 FPGA Challenge 2025 - Qualifying Round

Welcome to the **FPGA Challenge 2025 Qualifying Round**!  
This competition challenges participants to optimize machine learning models for FPGA deployment using **hls4ml**.  
Your goal is to design efficient models that **maximize accuracy** while **minimizing latency** under FPGA resource constraints.

---

## 📚 Benchmark Background

This challenge focuses on the **image classification** task using the **CIFAR-10** dataset, based on the MLPerf TinyML Benchmark using hls4ml.

It is adapted from the following reference:

> *Borras, Hendrik, et al. "Open-source FPGA-ML codesign for the MLPerf Tiny Benchmark." arXiv preprint arXiv:2206.11791 (2022)*

---

## 📁 Repository Structure

This repository contains two main Jupyter Notebooks:

1. **End-to-End Example for the Kaggle Competition**  
   - Path: [`End_to_end_examples/imageclassifiaction-qat-hls4ml-end-to-end-example.ipynb`](https://github.com/nycu-pcs-lab/FPGA_Challenge2025_Qualifying_Round_Challenge/blob/main/End_to_end_examples/imageclassifiaction-qat-hls4ml-end-to-end-example.ipynb)  
   - Includes: model training, quantization-aware training, HLS conversion, and prediction submission workflow  
   - To use: **Download and import the notebook into Kaggle**
    
2. **Hands-on Lab Notebook**  
   - Task: Jet Tagging (for guided lab session)  
   - Path: `Hands-on_Lab/JetTaggingHandOnLab.ipynb`  
   - You can open it directly in Colab:  
     👉 [Open in Colab](https://colab.research.google.com/github/nycu-pcs-lab/FPGA_Challenge2025_Qualifying_Round_Challenge/blob/main/Hands-on_Lab/JetTaggingHandOnLab.ipynb)
     > ⚠️ Note: Opening the notebook via Colab will create a personal copy for each participant.  
      > You are free to modify and execute it without affecting others.


---

## 🧮 Scoring Criteria

Your submission will be evaluated based on the following three components:

1. **Accuracy**  
   - Evaluated using the same **synthetic CIFAR-10 test set** as the Kaggle competition
   - Accuracy is measured using the **C simulation results of the HLS model**

2. **Resource Utilization Constraints**  
   - Measured using results from **Vivado Logic Synthesis** (not C-Synthesis)  
   - All four key FPGA resources must remain **below 75% utilization**:
     - LUTs  
     - DSPs  
     - Flip-Flops (FFs)  
     - Block RAMs (BRAMs)  
   - The 75% threshold ensures a sufficient margin for successful **Place-and-Route** in potential downstream FPGA implementation

3. **Latency**  
   - Measured using **RTL simulation**  
   - Computed by taking the **average cycle count** from 5 inference samples,  
     then multiplying by the **estimated clock period** reported in the **HLS C-Synthesis** output

> To be eligible for final scoring, your HLS model must satisfy both the **resource constraint** and provide a valid **RTL latency measurement**.

---

## 📊 Accuracy Scoring System & Dataset

You can access detailed information about the scoring system and datasets on Kaggle for the task via the following links:

- 🖼️ **[Image Classification Task Competition- Kaggle Page](https://www.kaggle.com/t/6d1444ed9f804d379d13c68a18a2cf58)** *(for testing your model and flow)*  
  → *Note: Final evaluation will be conducted separately and is not based on Kaggle leaderboard.*

---

## 💻 Technical Rules and Constraints

- **Target FPGA Board:** `PYNQ-Z2`  
  <img src="./Figures/PYNQ-Z2-Large-scaled.jpg" alt="PYNQ-Z2 FPGA" width="400">

- **hls4ml Version:** `1.1.0`  
- **HLS Toolchain:** `Xilinx Vitis HLS 2023.2`  
  - **Installation Guide:** *Coming Soon*

---

## 📣 Official Announcements and Q&A

- All official updates, rule clarifications, and Q&A will be posted in the **[Discussions tab](https://github.com/nycu-pcs-lab/FPGA_Challenge2025_Qualifying_Round_Challenge/discussions)** of this repository.
- Please **watch** this repository to receive timely notifications.
- Do **not** use the Kaggle page for discussion or rule updates.

---

