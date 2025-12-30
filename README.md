# Manufacturing-Analytics-Dashboard
Looker Studio dashboard analyzing manufacturing sensor data


<img width="281" height="238" alt="1" src="https://github.com/user-attachments/assets/b4a36093-dda9-4541-b1c7-976674305372" />

<img width="1436" height="766" alt="image" src="https://github.com/user-attachments/assets/2b2cdb30-a2df-4135-aaca-40ed79720003" />

<img width="1866" height="892" alt="image" src="https://github.com/user-attachments/assets/a876636d-5f3d-4c00-87ec-d681c5acd04a" />

<img width="2166" height="1138" alt="image" src="https://github.com/user-attachments/assets/ad075745-4a62-401b-b6c5-46c8c6e0ef65" />

<img width="2160" height="1290" alt="image" src="https://github.com/user-attachments/assets/492da601-bb23-4ec5-bea1-644e2a9230ab" />

<img width="1832" height="842" alt="image" src="https://github.com/user-attachments/assets/be883fd1-d2e6-4e8f-8372-cf5200cff2cc" />


## 📊 Live Dashboard
https://lookerstudio.google.com/reporting/71bb4cee-ce7b-4f66-ad6a-033422dfb92c

## 🎯 Project Overview

Interactive analytics dashboard analyzing **44,000+ manufacturing sensor readings** from a Fortune 500 client's production facility. Built during my Data Analytics internship at **EY-Parthenon**.

**Context:** Manufacturing operations team spending 10+ hours weekly on manual Excel analysis with limited visibility into production bottlenecks.

## 💼 Business Problem

**Challenges:**
- ⏱️ 10+ hours weekly manual data analysis
- 📉 Limited real-time visibility into production efficiency
- ⚠️ Reactive maintenance approach (costly unplanned downtime)
- 🔍 No predictive insights for operational planning
- 📊 Difficult to identify bottlenecks across 9 production stages

**Impact:**
- High operational costs
- Suboptimal resource allocation
- Delayed decision-making

## 🛠️ Solution: Interactive BI Dashboard

**7-Chart Analytics Dashboard covering:**

### 1. Production Stage Distribution
- Pie chart showing time allocation across stages
- Identifies which stages consume most production time
- **Key Insight:** Reaction stage = 31.8% of total time

### 2. Stage Duration Analysis  
- Bar chart comparing time spent in each stage
- Highlights inefficiencies and optimization opportunities

### 3. Temperature Monitoring
- Multi-line chart tracking 3 temperature sensors
- Shows temperature patterns across production lifecycle
- **Key Insight:** Temp drops from 70°C (Reaction) to 12°C (cooldown)

### 4. Pressure Analysis by Stage
- Average pressure levels for each production stage
- **Key Insight:** Vacuum stage shows negative pressure (-0.7), Reaction shows high positive pressure (20)

### 5. Chemical Flow Rate Tracking
- Multi-line chart showing TFE, Initiator, Ethane, PPVE flows
- Identifies which chemicals are active during each stage
- **Key Insight:** TFE flow spikes to 10 during Reaction phase

### 6. RPM Stability Monitoring
- Scorecard + trend line for equipment RPM
- **Key Insight:** System maintains stable 23 RPM during production

### 7. Stage Performance Summary
- Table with average sensor values per stage
- Conditional formatting highlights anomalies
- Enables quick stage comparison

---
## 🔧 Technical Implementation

### Data Pipeline
```
Raw Historian Data (44,000+ rows, 19 parameters)
            ↓
Python ETL Pipeline (Pandas, NumPy)
  - Extract from manufacturing historian system
  - Transform: validation, formula application, stage classification
  - Load to Excel outputs
            ↓
Google Looker Studio / Power BI
  - Interactive dashboards
  - Real-time KPI monitoring
  - Predictive analytics
```

### Stage Classification Logic

Python automation applied conditional logic to classify production stages:

**Stages Identified:**
1. **Recovery** - System startup (Temp: 47-50°C, RPM: ~5, Pressure: low)
2. **Vacuum** - Vacuum phase (Pressure: negative -0.7, Temp: 65-66°C)
3. **PPVE** - PPVE addition (PPVE Flow: 1.1-1.7)
4. **Initiator** - Initiator dosing (Initiator Flow: 900-1380)
5. **TFE Pressurization** - TFE addition (TFE Flow: 3.3-3.6, Pressure rising)
6. **Reaction** - Main production (Temp: 71-73°C, Pressure: 19-20, TFE Flow: 5-10)
7. **Ethane Dosing** - Ethane injection (Ethane Flow spike: 1790-2018)
8. **Box-up** - Packaging phase (RPM: ~0.35, System cooling)

### Technologies Used
- **Data Processing:** Python (Pandas, NumPy)
- **ETL Pipeline:** Custom automation scripts
- **Visualization:** Google Looker Studio
- **Analysis:** Statistical modeling, time-series analysis

---

## 🎓 Skills Demonstrated
**ETL Pipeline Development** - Automated data extraction, transformation, loading  
**Business Intelligence** - Dashboard design, KPI tracking  
**Data Visualization** - Multi-chart analytics storytelling  
**Python Automation** - Pandas, NumPy for data processing  
**Manufacturing Analytics** - Domain knowledge, process understanding  
**Stakeholder Communication** - Executive-ready insights  
**Problem Solving** - Complex business problem → technical solution  

---
## 🚀 Key Learnings

**Technical:**
- Building ETL pipelines for time-series IoT data
- Applying business logic through conditional programming
- Designing executive-ready dashboards
- Handling large datasets (44K+ rows) efficiently

**Business:**
- Translating sensor data into actionable insights
- Understanding manufacturing process workflows
- Communicating complex analysis to non-technical stakeholders
- Identifying cost-saving opportunities through data

---

This project showcases my ability to:
- Work with real business data at scale
- Build end-to-end analytics solutions
- Deliver measurable business impact
- Bridge technical analysis and executive communication

**Client data has been anonymized to protect confidentiality.**
## 📫 Contact

**Khushi Lakhlani**  
MS Information Systems @ Northeastern University  
📧 lakhlani.k@northeastern.edu  
💼 [LinkedIn](https://www.linkedin.com/in/khushilakhlani/)  
