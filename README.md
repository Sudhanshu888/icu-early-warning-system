AI-Based ICU Patient Deterioration Early Warning System
A web-based clinical monitoring dashboard that provides real-time vital sign monitoring, automated AI risk assessment, and intelligent alert generation for ICU patients.
📋 Overview
Intensive Care Units (ICUs) require continuous monitoring of multiple vital signs, but healthcare staff cannot simultaneously track every patient with full attention. Traditional threshold-based alarm systems are reactive and prone to false positives, causing alarm fatigue among clinical staff.
This project implements an AI-assisted early warning system that continuously evaluates six key vital parameters, computes a composite risk score for each patient, and generates timely, explainable alerts — helping clinical staff identify and respond to patient deterioration before it becomes critical.
✨ Features

Real-Time Patient Monitoring — Live dashboard tracking 8 ICU patients simultaneously
AI Risk Assessment Engine — Rule-based scoring algorithm classifying patients as LOW / MEDIUM / HIGH risk
Automated Critical Alerts — Instant alert banners for HIGH risk patients with clinical recommendations
Explainable AI — Every risk score comes with a plain-language explanation of contributing factors
Interactive Vitals Entry — Manually input vital signs for instant AI analysis
Analysis Log — Timestamped record of every AI assessment for audit and review
Zero Setup — Single self-contained HTML file, runs in any modern browser

🩺 Monitored Vital Signs
ParameterNormal RangeUnitHeart Rate60–100bpmSpO2 (Oxygen Saturation)95–100%Respiratory Rate12–20/minSystolic Blood Pressure90–140mmHgBody Temperature36.1–37.2°CGlasgow Coma Scale (GCS)14–15/15
🧠 Risk Classification Algorithm
Each vital sign is scored 0 (normal), 1 (warning), or 2 (critical) against clinical reference ranges. The composite score (0–12) determines the risk level:
Risk LevelScore RangeAction🟢 LOW0–2Continue standard monitoring🟡 MEDIUM3–5Increase monitoring frequency🔴 HIGH6–12Immediate critical alert + clinical review
🛠️ Tech Stack

HTML5 — Structure
CSS3 — Styling, responsive layout, color-coded UI
JavaScript (ES6) — AI risk engine, alert system, analysis logging
Python + PyTorch (planned) — BiLSTM model training on MIMIC-IV dataset
MIMIC-IV / PhysioNet (planned) — Real-world ICU dataset for future model training

🚀 Getting Started
No installation required.

Clone or download this repository
Open ICU_Early_Warning_System.html directly in any modern web browser (Chrome, Edge, Firefox)
Select a patient from the sidebar to view their AI risk assessment
Use the manual vitals entry form to test custom values

bashgit clone https://github.com/Sudhanshu888/icu-early-warning-system.git
cd icu-early-warning-system
open ICU_Early_Warning_System.html
📊 Demonstration Results
Tested on 8 ICU patients covering diverse conditions (Septic Shock, COPD, Cardiac Arrest Recovery, Pneumonia, Renal Failure, Trauma, Respiratory Failure):

100% correct risk classification across all three risk levels
< 1 second alert generation latency
< 2 seconds dashboard load time

🔭 Future Scope

Train a Bidirectional LSTM model with attention on the MIMIC-IV dataset (target AUROC > 0.85)
Integrate LangGraph multi-agent reasoning with Pinecone vector database for explainable clinical alerts
Develop a Flask REST API backend with a React.js frontend
Deploy via Docker on cloud infrastructure (AWS/GCP) for hospital pilot testing
Extend monitoring to lab values, ventilator parameters, and medication data
Integrate with Hospital Information Systems (HIS) and EHR platforms

📁 Repository Structure
icu-early-warning-system/
├── ICU_Early_Warning_System.html   # Complete self-contained application
└── README.md                        # Project documentation
👥 Authors

VasuDev Singh (2023A1R186)
Sudhanshu (2023A1R158)
Mukund Bhandari (2023A1R162)

Mini Project (COM-612) — B.Tech CSE, Semester VI
Model Institute of Engineering and Technology (Autonomous), Jammu — 2026
📄 License
This project was developed for academic purposes as part of the Mini Project (COM-612) curriculum.
