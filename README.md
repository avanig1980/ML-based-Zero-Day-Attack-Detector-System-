# 🛡️ Zero-Day DDoS Attack Detection Using Syslog Data and Machine Learning

A machine learning-based detection system for identifying zero-day Distributed Denial of Service (DDoS) attacks using synthetic and real-time syslog data generated from a Cisco Packet Tracer simulated network.

## 📘 Project Overview

This project addresses the growing challenge of detecting zero-day DDoS attacks, which evade traditional signature-based Intrusion Detection Systems (IDS). By leveraging syslog data and ensemble machine learning models, this system aims to proactively detect anomalies and generate alerts in near-real-time environments.

## 🎯 Objectives

- Simulate a secure enterprise network using Cisco Packet Tracer
- Generate and label synthetic syslog data representing normal and malicious activity
- Engineer predictive features from raw syslog logs
- Train and evaluate ML classifiers: Decision Tree, Random Forest, and Gradient Boosting
- Compare performance using accuracy, precision, recall, and F1-score
- Deploy the best-performing model as an alerting engine for proactive DDoS detection

## 🧰 Tools & Technologies

- 🖥 Cisco Packet Tracer
- 🐍 Python (Jupyter Notebook)
- 📊 Scikit-learn, Pandas, NumPy, Matplotlib, Seaborn
- 🗂 Syslog protocol
- 📈 SMOTE (Synthetic Minority Oversampling Technique)

## 🧠 Machine Learning Models

| Model            | Accuracy | F1-Score (Attack Class) |
|------------------|----------|--------------------------|
| Decision Tree    | 70%      | 0.18                     |
| Random Forest    | 78%      | 0.13                     |
| Gradient Boosting| 82%      | 0.00                     |

> ⚠️ The Gradient Boosting model, despite its high accuracy, failed to detect attacks due to class imbalance. Random Forest demonstrated the best trade-off between overall performance and attack detection.

## 🗃️ Dataset

- **Source**: Syslog messages from the simulated enterprise network
- **Entries**: 10,000 logs
- **Class Balance**: ~18% attacks
- **Features**: Timestamps, Source IPs, Message Types, Labels

## 📊 Results Summary

- Random Forest outperformed other models in detecting attacks despite the imbalanced dataset.
- Temporal features (timestamps) were more predictive than source IPs.
- High model accuracy can mislead imbalanced datasets (accuracy paradox).

## 📁 Repository Structure
data/ # Sample synthetic syslog logs
├── notebooks/ # Jupyter notebooks for EDA and ML models
├── models/ # Trained model files (optional)
├── scripts/ # Data processing and utility scripts
├── README.md # Project documentation
└── requirements.txt # Python dependencies

## ✅ How to Run

1. Clone the repository
```bash
git clone https://github.com/yourusername/zero-day-ddos-detector.git
cd zero-day-ddos-detector
2. Installation
pip install -r requirements.txt
Run the notebooks in notebooks/ to explore the dataset and train models.

🧪 Future Enhancements
Integrate additional log types (NetFlow, PCAP)

Implement deep learning (LSTM, CNN) for temporal modeling

Develop a live monitoring dashboard

Improve class balancing via advanced oversampling/undersampling methods

Deploy the model in a containerized environment (Docker)

📄 License
This project is for academic and research purposes only. © 2025 Avani Gopakumar

🙋‍♀️ Author
Avani Gopakumar
MSc Computer Networks and System Security
University of Hertfordshire
GitHub: [avanig1980] | LinkedIn: [https://www.linkedin.com/in/g-avani/]
