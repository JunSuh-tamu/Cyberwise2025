# Network Traffic Analysis & Cybersecurity Threat Detection

A Python-based data analysis pipeline built to analyze network flow metrics, classify Denial of Service (DoS/DDoS) attack vectors, and visualize traffic distributions[cite: 3].

---

## Dataset Overview

The notebook analyzes the network dataset `StdizedMerged63.xlsx` containing over 428,000 recorded network traffic instances[cite: 3].

| Metric Category | Features Included |
| :--- | :--- |
| **Network Indicators** | `Header_Length`, `Protocol Type`, `Rate`, `IAT` (Inter-Arrival Time)[cite: 3] |
| **TCP Flags & Counts** | `fin_flag_number`, `syn_flag_number`, `rst_flag_number`, `psh_flag_number`, `ack_flag_number`, `ack_count`, `syn_count`[cite: 3] |
| **Application Layer** | `HTTP`, `HTTPS`, `DNS`, `SSH`, `TELNET`, `SMTP`[cite: 3] |
| **Traffic Statistics** | `Tot sum`, `Min`, `Max`, `AVG`, `Std`[cite: 3] |
| **Target Label** | `Label` (e.g., `DOS-UDP_FLOOD`, `DDOS-UDP_FLOOD`, `DDOS-ICMP_FLOOD`, `DDOS-PSHACK_FLOOD`, `DOS-TCP_FLOOD`)[cite: 3] |

---

## Key Features & Workflow

* **Data Ingestion & Cleaning**: Handles Google Drive mounting/file uploads, standardizes messy column string names, and checks feature data types and missing values[cite: 3].
* **Protocol & Flag Profiling**: Aggregates usage counts across layer 4 protocols (TCP = 6, UDP = 17, ICMP = 1, GRE = 47) and evaluates total TCP flag occurrences[cite: 3].
* **Attack Classification Breakdown**: Generates frequency counts and summary statistics across distinct DoS/DDoS categories[cite: 3].
* **Data Visualization**:
  * Bar charts for attack label distributions[cite: 3].
  * Correlation heatmaps across numerical traffic features[cite: 3].
  * Time-series/Inter-Arrival Time (`IAT`) trend plots for peak attack traffic[cite: 3].

---

## Prerequisites & Installation

**Environment**:
* Python 3[cite: 3]
* Google Colab or Jupyter Notebook[cite: 3]

**Required Libraries**:
* `pandas`[cite: 3]
* `matplotlib`[cite: 3]
* `seaborn`[cite: 3]
* `openpyxl` (for `.xlsx` reading capability)[cite: 3]

---

## Getting Started

1. **Open Notebook**: Load the `.ipynb` notebook file into Google Colab[cite: 3].
2. **Provide Dataset**: Ensure `StdizedMerged63.xlsx` is available[cite: 3]. Upload it via the `google.colab.files.upload()` prompt or mount Google Drive directly (`/content/drive/My Drive/`)[cite: 3].
3. **Run Pipeline**: Execute cells sequentially to inspect DataFrame outputs, perform summary statistical checks, and generate visualizations[cite: 3].
