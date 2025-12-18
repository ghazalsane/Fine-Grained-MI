# Fine-Grained Motor Imagery (MI)

This repository contains the code for fine-grained upper-limb motor imagery (MI) classification using EEG and fNIRS data.

## Pipeline Overview

The workflow is organized into three main parts and is designed to be simple to reproduce.

### 1. Dataset Download and Extraction

Run the **first notebook/script** to automatically:

- Download the dataset
- Save it to your Google Drive
- Extract and organize the raw files into the expected directory structure

No manual dataset handling is required.

---

### 2. EEG and fNIRS Preprocessing

Run the **second notebook/script** to perform preprocessing on both modalities, including:

- EEG preprocessing
- fNIRS preprocessing
- Trial alignment between EEG and fNIRS
- Generation of clean, model-ready inputs

The output of this step is used directly for training and evaluation.

---

### 3. Binary Task Pair Experiments

Run **Part 3** to train and evaluate the model on **binary task pairs**.

- The dataset contains **8 fine-grained MI tasks**
- This results in **~50 possible binary task combinations**
- You can freely change the selected task pair to analyze different classification scenarios

Because the proposed network is **lightweight** and training is **very fast**, **pretrained models are not provided**. All experiments are intended to be trained from scratch.

---

## Notes

- The code is modular and easy to adapt to new task pairs
- Training time is short due to the compact network design
- Suitable for rapid experimentation and ablation studies
