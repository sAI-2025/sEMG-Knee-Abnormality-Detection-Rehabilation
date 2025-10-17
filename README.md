 
 
#   sEMG-Knee-Abnormality-Detection

### **Detecting Knee Abnormalities and Human Activities using Convolutional Transformer Capsule Networks**

 
<!-- Badges -->
<p align="center">
  <!-- Programming Language -->
  <img src="https://img.shields.io/badge/Python-3.11-blue?logo=python" alt="Python 3.11"/>
  
  <!-- Frameworks -->
  <img src="https://img.shields.io/badge/TensorFlow-ML-orange?logo=tensorflow" alt="TensorFlow"/>
  <img src="https://img.shields.io/badge/PyTorch-DL-red?logo=pytorch" alt="PyTorch"/>

  <!-- Model Types -->
  <img src="https://img.shields.io/badge/CNN%20%2B%20Transformer%20%2B%20CapsNet-Hybrid%20Model-purple?logo=deepin" alt="CNN Transformer Capsule Network"/>
  
  <!-- Signal Type -->
  <img src="https://img.shields.io/badge/sEMG-Biomedical%20Signals-lightgrey?logo=heartbeat" alt="sEMG Signals"/>

  <!-- Application Domains -->
  <img src="https://img.shields.io/badge/Rehabilitation-Use%20Case-success?logo=mediatemple" alt="Rehabilitation Use Case"/>
  <img src="https://img.shields.io/badge/Prosthetics-Control-yellow?logo=android" alt="Prosthetics Control"/>

  <!-- UI / Deployment -->
  <img src="https://img.shields.io/badge/Notebook-Jupyter-orange?logo=jupyter" alt="Jupyter Notebook"/>
  <img src="https://img.shields.io/badge/Deployment-Local%20%7C%20Offline-informational?logo=raspberrypi" alt="Offline Deployment"/>

  <!-- Project Meta -->
  <img src="https://img.shields.io/badge/License-MIT-green?logo=opensourceinitiative" alt="MIT License"/>
  <img src="https://img.shields.io/badge/Status-Beta-orange?logo=github" alt="Beta Status"/>
</p>

##   Overview

This repository presents my undergraduate **research work** on analyzing **surface Electromyography (sEMG)** signals to detect **knee abnormalities** and recognize **human activities** such as **walking**, **sitting**, and **standing**.  

The project integrates **signal processing** and **deep learning architectures** — combining **Convolutional Neural Networks (CNNs)**, **Transformers**, and **Capsule Networks** — to model both local and temporal dependencies in EMG signals.  

The system achieved **67% generalization accuracy** in identifying lower-limb disorders, providing foundational work for **rehabilitation**, **prosthetic limb control**, and **assistive robotics**.

---

##   Research Objectives

- Detect **knee joint abnormalities** from sEMG signals using deep learning.
- Predict **human activity states** — sitting, standing, walking — based on muscle electrical signals.
- Support the development of **prosthetic legs** and **rehabilitation systems** by interpreting muscle movement patterns.
- Explore advanced architectures like **Capsule Networks** and **Transformers** for biomedical time-series analysis.

---

##   Research Motivation

The project aims to contribute to **intelligent prosthetics** and **rehabilitation engineering**.  
By decoding muscle activation signals, a prosthetic or robotic limb can:
- Understand the **intent** of motion (e.g., start walking, sit down).
- Adjust its movement accordingly.
- Support people recovering from injuries or with movement disabilities.

This work bridges **deep learning**, **biomedical signal processing**, and **assistive robotics**.

---

##   Technical Implementation

###   **Model Architecture**
- **Input:** 1-D sEMG time-series data
- **Processing:**
  - Convolutional layers → extract local spatial patterns.
  - Transformer Encoder → capture temporal dependencies across signals.
  - Capsule Network → preserve hierarchical spatial relationships.
- **Output:** Classified activity / abnormality state.

###   **Key Techniques Used**
| Technique | Description |
|------------|--------------|
| **Signal Preprocessing** | Normalization, segmentation, and feature scaling of EMG data |
| **CNN Layers** | Capture local activation features |
| **Transformer Encoder** | Understand long-term dependencies |
| **Capsule Layers** | Retain spatial hierarchy and reduce information loss |
| **Softmax Output** | Classifies activity and abnormality type |

### 🧪 **Performance**
- **Accuracy:** 67% (Cross-subject generalization)
- **Dataset:** Custom sEMG dataset collected across multiple subjects and activities
- **Frameworks:** TensorFlow / PyTorch, NumPy, Pandas, Matplotlib

---

##   Results and Visualizations
 
| Metric | Result |
|--------|--------|
| **Generalization Accuracy** | 67% |
| **Classes** | Walking, Sitting, Standing |
| **Use Case** | Rehabilitation and Prosthetic Control |

####   Example Outputs
- Confusion Matrix visualizations (`original_paper/confusion matrix.png`)
- Model results and performance curves (`original_paper/results.csv`)
- Generalized test results (`original_paper/Generalised data.png`)

---

## 📂 Repository Structure

```

sEMG-Knee-Abnormality-Detection/
│
├── Capasule_Network.ipynb          # Main model implementation (Conv + Transformer + Capsule Network)
├── P.ipynb                         # Data preprocessing & visualization notebook
│
├── Data/                           # Preprocessed EMG data files
│   ├── 1gait.txt
│   ├── 1sitting.txt
│   ├── 1standing.txt
│   └── ...
│
├── Original EMG datasets/          # Raw datasets (collected signals)
│   ├── 1gait.txt
│   ├── 2gait.txt
│   └── ...
│
├── papers/                         # Research and reference papers
│   ├── Capsule_Network_for_1-D_Biomedical_signals_A_Review.pdf
│   ├── SSRN-id4789200.pdf
│   ├── vijayvargiya2020.pdf
│   └── reference_papers.pdf
│
├── original_paper/                 # My written research paper and report files
│   ├── Advancements in Knee Abnormality Diagnosis Leveraging sEMG and LSTM.pdf
│   ├── knee_abnormality_report.pdf
│   ├── confusion matrix.png
│   ├── Block diagram.png
│   └── results.csv
│
├── data200.csv                     # Cleaned and merged dataset
├── Data_set.csv                    # Processed labeled dataset
├── References ieee.docx            # IEEE reference format
└── pone.0180526.s001.zip           # Supporting dataset file

````

---

## 📘 Research Highlights

### 🔬 Core Contributions
- Developed a **hybrid deep learning model** combining CNN + Transformer + Capsule architectures.
- Designed a **custom dataset pipeline** for biomedical signal processing.
- Conducted extensive **literature review and model benchmarking**.
- Validated across subjects for **real-world generalization**.

### 📈 Applications
- **Rehabilitation Monitoring** – Track patient recovery using EMG activity.
- **Prosthetic Leg Control** – Decode intent and improve robotic limb precision.
- **Human-Robot Interaction** – Enable natural control through neuromuscular signals.

---

## 🧪 Key Learnings

- Handling noisy **biomedical data** and ensuring proper normalization.
- Balancing **model depth vs. overfitting** in limited-subject datasets.
- Applying **attention-based networks** for physiological time-series.
- Understanding how **signal morphology changes** with muscle fatigue or abnormality.

---

## 🧭 Future Work

- Expand dataset with more subjects and real-time EMG recording.  
- Integrate IMU (Inertial Measurement Unit) data for gait fusion.  
- Optimize model for deployment on **embedded edge devices** (e.g., ESP32, Raspberry Pi).  
- Real-time **prosthetic leg prototype** using sEMG signals.

---

## 📚 References

Key research papers reviewed:
1. *Capsule Network for 1-D Biomedical Signals: A Review* (Elsevier, 2023)  
2. *Advancements in Knee Abnormality Diagnosis Leveraging sEMG and LSTM*  
3. *Vijayvargiya et al., Biomedical Signal Processing and Control, 2020*  
4. *Sensors Journal – Surface EMG-based Human Activity Recognition, 2021*  

All papers included under `/papers` and `/original_paper/`.

---

## 🧑‍💻 Author

**Sai Krishna Chowdary Chundru**  
🎓 B.Tech in Electronics and Communication Engineering — IIIT Nuzvid  
📍 India  

📧 **Email:** [cchsaikrishnachowdary@gmail.com](mailto:cchsaikrishnachowdary@gmail.com)  
🔗 **LinkedIn:** [linkedin.com/in/sai-krishna-chowdary-chundru](https://www.linkedin.com/in/sai-krishna-chowdary-chundru)  
💻 **GitHub:** [github.com/sAI-2025](https://github.com/sAI-2025)  
📰 **Medium:** [medium.com/@sai2025](https://medium.com/@sai2025)

---

## 🧩 Acknowledgments

Special thanks to my research mentors and teammates for their guidance in data acquisition, model experimentation, and validation.  
Grateful to open-access research platforms for enabling knowledge sharing in biomedical AI.

---

## 🪄 How to Run

1. Clone this repository  
   ```bash
   git clone https://github.com/sAI-2025/sEMG-Knee-Abnormality-Detection.git
   cd sEMG-Knee-Abnormality-Detection
````

2. Open Jupyter Notebook

   ```bash
   jupyter notebook Capasule_Network.ipynb
   ```

3. Install dependencies

   ```bash
   pip install -r requirements.txt
   ```

4. Run the notebook and visualize results.

---

## 💡 Quote

> “Signals from muscles are stories of motion — decoding them bridges biology and robotics.”
> — *Sai Krishna Chowdary Chundru*

---

⭐ **If this project inspires you, please give it a star — it helps support open biomedical AI research!**

  
