# Malicious DNS-over-HTTPS (DoH) Traffic Detection using Hybrid ML & GraphSAGE GNN

## Project Overview
This project implements a hybrid deep learning approach to detect malicious DNS-over-HTTPS (DoH) traffic based on the CIC-DoHBrw 2020 dataset. The dataset contains two levels:

- **L1:** Detecting DoH vs Non-DoH traffic.  
- **L2:** Detecting Benign vs Malicious DoH traffic.

The workflow starts with preprocessing, including label encoding, feature scaling, and handling class imbalance using SMOTE. Initial experiments use Logistic Regression for baseline classification and feature importance extraction through model coefficients and permutation importance.

For advanced modeling, traffic flows are represented as a graph where each node corresponds to a network flow and edges connect temporally neighboring flows. A **GraphSAGE GNN** is trained to leverage both node features and relational information, providing robust detection performance. The system outputs classification metrics, including accuracy, precision, recall, F1-score, ROC-AUC, and confusion matrices.

This implementation is based on the methodology described in the research paper:  
*“Implementing a Hybrid Deep Learning Technique for Detecting Malicious DNS over HTTPS (DoH) Traffic” by Mohemmed Sha1 & Adel Binbusayyis.*

## Installation
To run this project, first create a Python virtual environment and install the required libraries listed in `requirements.txt`:

```bash
pip install -r requirements.txt
