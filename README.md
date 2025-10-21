# AWS CloudTrail CSPM Mini Project

### Course: CCS336 – Cloud Service Management  
**Student:** Nowshika Mirza R (814723104109)  
**Department:** CSE-B, Third Year  
**Dataset:** [AWS CloudTrails Dataset from flaws.cloud (Kaggle)](https://www.kaggle.com/datasets/nobukim/aws-cloudtrails-dataset-from-flaws-cloud)  
**SDG Alignment:** SDG 16 – Peace, Justice and Strong Institutions (Cyber Security & Governance)

---

## Overview
This project demonstrates **Cloud Security Posture Management (CSPM)** principles by analyzing AWS CloudTrail logs to simulate detection, scoring, and compliance monitoring.  
It automates **risk analysis, compliance evaluation, and anomaly detection** using Python and visualizes insights through interactive dashboards.

---

## Key Features
- Cleans and parses CloudTrail logs from CSV  
- Flags misconfigurations and suspicious activities (ConsoleLogins, S3 ACL changes, etc.)  
- Uses **Isolation Forest** to detect anomalous IP behavior  
- Computes a composite risk score for each event and classifies levels (Low → Critical)  
- Summarizes AWS region compliance percentages  
- Generates **five interactive visualizations** using Plotly

---

## Requirements
| Package | Purpose |
|---------|----------|
| pandas, numpy | Data wrangling |
| matplotlib, seaborn, plotly | Visualization |
| scikit-learn | Machine learning (Isolation Forest model) |
| tqdm | Progress feedback |

Install prerequisites once:

pip install pandas numpy matplotlib seaborn plotly scikit-learn tqdm


---

## Dataset Preparation
1. Download **`dec12_18features.csv`** from Kaggle.  
2. Place it in the project folder with the main notebook.  
3. First run automatically creates a sample file (`cloudtrail_logs_sample.csv`, ≈ 1 MB) safe for GitHub.

---

## How to Run
1. Launch **Jupyter Notebook** or Google Colab.  
2. Copy the Python code from the notebook `cspm_cloudtrail_analysis.ipynb` and run all cells in order.  
3. Outputs are generated in a folder named `cspm_outputs/`.  

You will see these visualizations:
1. Overall Risk Level Distribution (Pie Chart)  
2. Top Events by Risk (Bar Plot)  
3. Events Per Day (Timeline Line Chart)  
4. Compliance Percentage by Region (Bar Chart)  
5. Top IPs by Risk and Anomalous Flags (Bar Chart)

---

## Output Files (`cspm_outputs/`)
| File | Description |
|-------|--------------|
| **annotated_cloudtrail.csv** | Cleaned dataset with risk and compliance columns |
| **region_summary.csv** | Regional risk and compliance metrics |
| **risk_summary.csv** | Event risk distribution summary |
| **JSON summary** (optional) | Quick project statistics |

---

## Example Analysis Summary
{
"total_events": 800,
"unique_IPs": 45,
"high_risk_events": 67,
"non_compliant_events": 21
}


---

## Conceptual Mapping to CSPM
| CSPM Concept | Notebook Implementation |
|--------------|-------------------------|
| Asset Discovery | Extract unique IP sources |
| Misconfiguration Detection | Rule flags for IAM, S3 ACL, policy changes |
| Threat Detection | Isolation Forest anomaly detection |
| Compliance Monitoring | Region compliance and risk matrix |
| Security Reporting | Visual and CSV summaries |

---

## Improvement Ideas
- Integrate **GeoIP mapping** for location-based threat monitoring  
- Add **real-time dashboard** (Plotly Dash/Streamlit)  
- Incorporate **AWS Security Hub API** for live CSPM metrics  
- Expand anomaly detection across time windows and user identities  

---

## License
Educational use only. Dataset copyright remains with the original Kaggle source.

---

This README presents your AWS CloudTrail CSPM mini project professionally and is ready for GitHub.
