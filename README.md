# Intrusion Detection Systems (IDS): State of the Art and ML Integration

## 📋 About This Project

This repository contains two Network Security reports developed for the *Network Security* course (Master in Network and Information Systems Engineering, U.Porto), covering both the **theoretical foundations** and a **practical Machine Learning-based IDS Proof of Concept**.

---

### 📖 Part 1 — Theoretical: *State of the Art and Tradeoffs*

A literature review covering the evolution and current landscape of Intrusion Detection Systems.

**What's inside:**
- **Traditional IDS Approaches** — Signature-based and Anomaly-based detection, their pros/cons.
- **IDS Types** — Network IDS (NIDS) vs. Host IDS (HIDS).
- **Modern & State-of-the-Art Approaches** — Machine Learning, Deep Learning, Hybrid/Ensemble methods (e.g., XCGAN), and AI-augmented IDS with SIEM integration.
- **Evaluation Metrics** — Accuracy, Detection Rate, Precision, Recall, F-Measure, derived from the confusion matrix.
- **Comparison & Tradeoffs** — Side-by-side comparison of all approaches across accuracy, false positives, adaptability, and cost/complexity.
- **Challenges & Future Trends** — High false alarm rates, zero-day detection, dataset limitations, explainable AI, and emerging Quantum Neural Network (QNN)-based IDS.



### 🛠 Part 2 — Practical: *A Study of Machine Learning Integration*

A hands-on implementation comparing ML models for intrusion detection and deploying a real-time Proof of Concept.

**What's inside:**
- **Dataset** — CIC-IDS2017 (`Wednesday-workingHours` subset), covering Benign traffic and multiple DoS attack types (Hulk, GoldenEye, Slowloris, Slowhttptest, Heartbleed).
- **Preprocessing** — Encoding, normalization, stratified train/test split, undersampling of the Benign class, and SMOTE oversampling to address severe class imbalance.
- **Model Comparison** — Decision Tree, Random Forest, and XGBoost, evaluated via Accuracy, Precision, Recall, F1-score, and confusion matrix analysis.
  - **Decision Tree** was selected for the PoC due to near-perfect accuracy (99.94%) and the lowest computational cost.
- **Proof of Concept** — A functional end-to-end MLIDS pipeline across two machines:
  - **Host (Windows):** Scapy + Npcap to replay attack traffic (`.pcap`) onto a virtual network interface.
  - **VM (Linux/Kali):** Tshark (capture) → CICFlowMeter (flow feature extraction) → trained Decision Tree model (classification).
- **Challenges & Future Work** — Validation limitations of the live simulation, and a roadmap for real-time monitoring, robust preprocessing, and model refinement.


*Reports developed for the Network Security course, Master in Network and Information Systems Engineering, Universidade do Porto — November/December 2025.*
