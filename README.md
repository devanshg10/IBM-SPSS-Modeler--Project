# 📊 Telco Customer Churn Analysis

<p align="center">
  <strong>Predictive Analytics with IBM SPSS Modeler</strong><br>
  Customer churn classification using the CHAID decision-tree technique
</p>

<p align="center">
  <img src="https://img.shields.io/badge/IBM-SPSS%20Modeler-0F62FE?style=for-the-badge">
  <img src="https://img.shields.io/badge/Model-CHAID-FF832B?style=for-the-badge">
  <img src="https://img.shields.io/badge/Project-Predictive%20Analytics-198038?style=for-the-badge">
</p>

---

## 🔎 Project Snapshot

Customer churn is an important business problem for telecommunications companies.  
This project uses **IBM SPSS Modeler** to prepare customer data, construct a predictive model, evaluate churn-related records, and generate an output dataset for further analysis.

### What this project covers

- 📥 Importing customer data
- 🧹 Filtering relevant records
- 🏷️ Defining field roles and measurement levels
- 🌳 Building a CHAID model
- 🧪 Applying the model to deployment data
- 🎯 Selecting relevant churn predictions
- 📤 Exporting the final results

---

## 🎯 Aim

The primary aim is to develop a predictive workflow that can identify customers associated with **churn** using the available telecommunications customer attributes.

The workflow is implemented completely through **IBM SPSS Modeler nodes**, making the project suitable for demonstrating a practical predictive-analytics pipeline.

---

## 🧩 Model Pipeline

```text
┌───────────────┐
│  Input Data   │
└───────┬───────┘
        ↓
┌───────────────┐
│ Select /      │
│ Filter Data   │
└───────┬───────┘
        ↓
┌───────────────┐
│ Define Fields │
│ & Data Types  │
└───────┬───────┘
        ↓
┌───────────────┐
│ CHAID Model   │
│    Training   │
└───────┬───────┘
        ↓
┌───────────────┐
│ Deployment /  │
│    Testing    │
└───────┬───────┘
        ↓
┌───────────────┐
│ Select Churn  │
│   Results     │
└───────┬───────┘
        ↓
┌───────────────┐
│ Export Final  │
│    Output     │
└───────────────┘
```

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

## 🖥️ SPSS Modeler Implementation

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


### 05 — Complete Model Training Stream


![Output Export](Workflow%20Screenshots/5-Complete%20Model%20Training%20Workflow.png)

---

### 06 — Deployment Dataset

A separate deployment dataset is imported into the stream for applying and evaluating the trained model.

![Model Testing](Workflow%20Screenshots/6-Importing%20for%20Testing.png)

---

### 07 — Deployment Record Selection

The deployment data is filtered to retain records where data_known = "yes".

![Model Testing](Workflow%20Screenshots/7-Selecting%20Node.png)

---

### 08 — Apply Trained Model

The trained CHAID model is applied to the deployment dataset to generate churn predictions.

![Model Testing](Workflow%20Screenshots/8-Churn%20Node.png)

---

### 9 — Churn Selection

The predicted results are filtered to identify customers meeting the specified churn prediction criteria.

![Model Testing](Workflow%20Screenshots/9-Churn.png)

---

### 10 — Churn Accuracy Calculation

Using the **Derive node**, the predicted churn score is converted into a percentage for evaluating the model’s prediction results.

![Model Testing](Workflow%20Screenshots/10.png)

---

### 11 — Field Filtering

Only the relevant fields required for the final analysis are retained.

![Model Testing](Workflow%20Screenshots/11-Filter%20Node.png)

---

### 12 — Result Export

The final results are exported to a flat file for external use and further analysis.

![Model Testing](Workflow%20Screenshots/12-Exporting%20Data%20(2).png)

---

### 13 — FULL Stream

![Model Testing](Workflow%20Screenshots/13-Full%20Stream.png)

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

## 🛠️ Technology Stack

| Category | Technology |
|---|---|
| Analytics Platform | **IBM SPSS Modeler** |
| Predictive Technique | **CHAID** |
| Dataset | Telco Customer Data |
| Data Input | Excel |
| Data Output | Flat File |
| Analysis Type | Classification / Predictive Analytics |

---

## 📁 Repository Structure

```text
IBM-SPSS-Modeler--Project/
│
├── datasets/
│   └── Telco-Customer-Churn.csv
│
├── screenshots/
│   ├── data_import.png
│   ├── data_filter.png
│   ├── type_node.png
│   ├── model_training.png
│   ├── model_testing.png
│   └── export_output.png
│
├── output/
│   └── churn_predictions.csv
│
└── README.md
```

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

---

## 🔗 References

- [IBM SPSS Modeler Documentation](https://www.ibm.com/docs/en/spss-modeler/18.6.0)
- Predictive Analytics course material
- Telco customer churn dataset used for the analysis

---

## 👨‍💻 Project Information

**Student:** Devansh Gupta  
**Program:** BCA — Data Science & Artificial Intelligence  
**Institution:** Babu Banarasi Das University  
**Course:** Predictive Analytics  

---

<p align="center">
  <sub>Built as an academic predictive analytics project using IBM SPSS Modeler.</sub>
</p>
