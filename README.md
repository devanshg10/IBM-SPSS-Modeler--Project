<!-- Banner Section -->
<p align="center">
  <img src="assets/banner.png" alt="A Study of Churn" width="100%">
</p>

<h1 align="center">Customer Churn Prediction Pipeline</h1>

<p align="center">
  A CHAID-based predictive analytics workflow built with IBM SPSS Modeler
</p>

<p align="center">
  <img src="https://img.shields.io/badge/IBM-SPSS%20Modeler-0F62FE?style=for-the-badge">
  <img src="https://img.shields.io/badge/Model-CHAID-0F62FE?style=for-the-badge">
  <img src="https://img.shields.io/badge/Project-Predictive%20Analytics-0F62FE?style=for-the-badge">
</p>

---

## 🔎 Project Overview

Customer churn is an important business problem for telecommunications companies.  
This project uses **IBM SPSS Modeler** to prepare customer data, construct a predictive model, evaluate churn-related records, and generate an output dataset for further analysis.

### What this project covers

- Importing customer data
- Filtering relevant records
- Defining field roles and measurement levels
- Building a CHAID model
- Applying the model to deployment data
- Selecting relevant churn predictions
- Exporting the final results

---

## 🎯 Aim

The primary aim is to develop a predictive workflow that can identify customers associated with **churn** using the available telecommunications customer attributes.

The workflow is implemented completely through **IBM SPSS Modeler nodes**, making the project suitable for demonstrating a practical predictive-analytics pipeline.

---

## ⚙️ Processing Workflow

| Phase | SPSS Modeler Component | Purpose |
|---|---|---|
| **01** | Excel Node | Load the Telco customer dataset |
| **02** | Select Node | Keep records where `data_known = "yes"` |
| **03** | Type Node | Configure field roles and measurement levels |
| **04** | CHAID Node | Train the churn classification model |
| **05** | Deployment Data | Apply the trained model to new records |
| **06** | Selection | Extract relevant churn predictions |
| **07** | Filter Node | Retain required output fields |
| **08** | Flat File Node | Save the final prediction results |

---

## 🖥️ Workflow Walkthrough

The complete workflow consists of data preparation, model training, testing, prediction, filtering, and output stages.

### 01 — Dataset Import

The Telco customer churn dataset is imported into IBM SPSS Modeler through an Excel source node.

![Dataset Import](Workflow%20Screenshots/1-Importing.png)

---

### 02 — Record Selection

Records with **data_known = "yes"** are retained for further analysis.

![Data Filtering](Workflow%20Screenshots/2-Selecting%20Node.png)

---

### 03 — Field Configuration

The dataset fields are configured with their appropriate measurement levels and roles, including the churn target and predictor variables.

![Field Configuration](Workflow%20Screenshots/3-Type%20Node.png)

---

### 04 — CHAID Model Training

A **CHAID model** is trained using the prepared dataset to identify patterns associated with customer churn.

![CHAID Model](Workflow%20Screenshots/4-Churn.png)


---

### 05 — Applying Trained Model

The trained CHAID model is applied to the deployment dataset to generate churn predictions.

![Applying Trained Model](Workflow%20Screenshots/8-Churn%20Node.png)


---

### 06 — Result Export

The final results are exported to a flat file for external use and further analysis.

![Result Export](Workflow%20Screenshots/12-Exporting%20Data%20(2).png)

---

### 07 — Complete Stream

The complete SPSS Modeler stream brings together the training, testing, prediction, filtering, and output stages into a unified workflow.

![Complete Stream](Workflow%20Screenshots/13-Full%20Stream.png)

> 📄 **Detailed Documentation**  
> The complete 14-step IBM SPSS Modeler workflow, including detailed explanations and screenshots for each stage, is documented in the [**Project Report PDF**](Project%20Report.pdf).
---

## 📈 Analysis Highlights

The resulting model can be used to examine customer characteristics associated with churn.

Some of the customer attributes considered in the analysis include:

- **Contract type**
- **Customer tenure**
- **Monthly charges**
- Other available customer-level attributes

The final workflow produces a filtered set of prediction results that can be used for subsequent business analysis.

> **Note:** Model performance and predictor importance should be interpreted from the actual SPSS Modeler output generated for this project.

---

# 🚀 Project Extension — InsightAI

After developing the predictive analytics workflow using **IBM SPSS Modeler**, the project was extended to explore how data analysis can be made more interactive through modern web technologies and AI.

**InsightAI** is a web-based data analysis platform designed to allow users to upload datasets, explore their data, generate visual insights, and interact with the analysis through an LLM-powered interface.

The extension builds upon the analytical concepts explored in the SPSS project while introducing a more interactive approach to dataset analysis.

### What InsightAI covers

- Dataset uploading and processing
- Python-based data analysis using Pandas
- Interactive data exploration
- Data visualizations and statistical insights
- Conversational interaction with datasets
- LLM-powered analytical assistance
- Web-based analytics interface

---

## 🧩 InsightAI Architecture

```text
Dataset
   ↓
Python + Pandas
   ↓
FastAPI Backend
   ↓
Data Analysis & Processing
   ↓
React Frontend
   ↓
Interactive Visualizations
   ↓
LLM-powered Analysis & Chat
```

The platform combines a **React frontend** with a **FastAPI backend** for data processing and analysis. Python and Pandas handle dataset operations, while an LLM API is used to provide conversational analytical assistance.

---

## 🛠️ InsightAI Technology Stack

| Category | Technology |
|---|---|
| Frontend | **React** |
| Backend | **FastAPI** |
| Data Processing | **Python / Pandas** |
| Visualization | **Recharts** |
| AI / LLM | **OpenRouter API** |
| Analysis Type | Interactive Data Analytics |

---

## 🖥️ InsightAI Preview

### Interactive Data Analysis

![InsightAI Dashboard](assets/insightai-dashboard.png)

### Data Exploration & Visualizations

![InsightAI Analysis](assets/insightai-analysis.png)

### AI-Powered Data Interaction

![InsightAI Chat](assets/insightai-chat.png)

> Screenshots above represent the current development of the InsightAI extension.

---

## 🔗 From Predictive Analytics to AI-Powered Analytics

The project demonstrates a progression from a structured predictive analytics workflow to an interactive AI-powered analytics platform.

```text
IBM SPSS Modeler
       ↓
Data Preparation
       ↓
Predictive Modelling
       ↓
Customer Churn Analysis
       ↓
Project Extension
       ↓
InsightAI
       ↓
Interactive AI-Powered Data Analysis
```

The SPSS workflow focuses on building and applying a predictive model, while InsightAI extends the analytical experience through a web-based interface combining data processing, visualization, and AI-powered interaction.

---

## 📚 Learning Outcomes

Through this project, the following concepts were practiced:

- Data preparation in IBM SPSS Modeler
- Selecting records using conditions
- Defining field metadata
- Predictive model construction
- CHAID-based classification
- Model deployment
- Filtering prediction results
- Exporting analytical outputs
- Interpreting customer churn patterns
- Python-based data processing
- Building a FastAPI backend
- Developing an interactive React analytics interface
- Integrating LLM-powered analytical assistance

---

## 📄 Detailed Project Report

The accompanying **Project Report PDF** provides the complete documentation of the project, including:

- Detailed 14-step IBM SPSS Modeler workflow
- Complete workflow screenshots
- Dataset and methodology
- CHAID model development
- Testing and prediction process
- Output analysis
- InsightAI project extension
- System architecture
- Technologies used
- Project observations and outcomes

---

## 🔗 References

- [IBM SPSS Modeler Documentation](https://www.ibm.com/docs/en/spss-modeler/18.6.0)
- Predictive Analytics course material
- Telco customer churn dataset used for the analysis

---

## 👨‍💻 Built By:

| **Field** | **Details** |
|---|---|
| **Student** | Devansh Gupta |
| **Roll No** | 1240258159 |
| **Batch** | BCADS-33 |
| **University** | Babu Banarasi Das University |
| **Subject** | Predictive Analytics |

---

<p align="center">
  <sub>Built as an academic predictive analytics project using IBM SPSS Modeler and extended with an AI-powered data analytics platform.</sub>
</p>
