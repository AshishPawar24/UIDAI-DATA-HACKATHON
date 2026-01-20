UIDAI Aadhaar Enrolment Volatility Analysis
Decision-Grade Metrics for Operational Risk Signalling

This repository contains the complete data analysis pipeline developed for the UIDAI National Data Hackathon. The project focuses on extracting decision-grade, operationally meaningful insights from aggregated Aadhaar enrolment and update data using transparent statistical methods.

The analysis is implemented in a single Google Colab notebook for reproducibility and ease of evaluation.

📌 Problem Context

Aadhaar enrolment and update activity varies across regions and time due to migration, administrative processes, and civic events. While aggregate statistics may appear stable, localized and short-term volatility can indicate regions or periods requiring closer administrative attention.

This project addresses two operational problems:

Border-region enrolment volatility as a migration-linked risk signal

Election-period enrolment stress as a time-bound operational signal

The goal is not to infer illegality or causality, but to demonstrate how aggregated Aadhaar data can be converted into actionable monitoring signals.

🔍 Problems Addressed
1. Border-Region Enrolment Volatility (Migration-Linked Risk)

Demonstrated using selected West Bengal border districts

Focuses on localized, recurring enrolment deviations

Highlights the need for PIN-level, distribution-aware monitoring

2. Election-Sensitive Enrolment Stress

Demonstrated using Bihar (2025 Legislative Election period)

Focuses on adult (18+) enrolment behaviour

Supports time-bound monitoring and capacity planning

📊 Datasets Used

The analysis uses only the anonymised, aggregated datasets provided by UIDAI:

Aadhaar Enrolment Data

District-wise CSV files

Fields used:

Date

State, District, PIN code

Age-wise enrolments (0–5, 5–17, 18+)

Aadhaar Demographic Update Data (optional validation)

Monthly update counts per PIN

Used to validate enrolment volatility through behavioural churn

🧠 Methodology Overview

The methodology is designed around decision-grade metrics, meaning each metric answers a specific administrative question.

Key Concepts

PIN × Month granularity to preserve locality and temporal sensitivity

Percentile-based baselines instead of global thresholds

Distribution-aware analysis (not average-based)

Domain constraints (e.g., 18+ population for elections)

Core Metrics

Monthly enrolments per PIN

PIN-level 95th percentile baseline

Enrolment anomaly flags

Anomaly rates by region type

Distributional variability (IQR)

Election window comparisons (pre vs non-election)

📈 Analysis & Visualisations

The notebook generates the following visual and tabular outputs:

Histogram of enrolments per PIN per month

Border vs non-border enrolment distribution (boxplot)

Spatial–temporal heatmap of enrolment anomalies

Summary tables of anomaly rates

Time-series plot of adult (18+) enrolments during election period

Event-window comparison tables

Each visual is accompanied by explicit interpretation, suitable for inclusion in the final PDF submission.


⚠️ Important Notes

This project does not claim fraud detection or illegal activity

All findings represent statistical risk signals, not conclusions

The analysis complements, not replaces, UIDAI’s existing safeguards

No machine learning or predictive modelling is used by design

<img width="859" height="390" alt="image" src="https://github.com/user-attachments/assets/1b6f6e8b-6be8-415e-80cd-b1e3ec00e7fd" />
