HealthGenomics – CVID & PID Diagnostic System

A Machine Learning–based Clinical Decision Support Tool for Primary Immunodeficiency Disease Classification

📌 Overview

This project presents a machine-learning-driven diagnostic system for identifying and classifying Primary Immunodeficiency Diseases (PIDs) with a focus on Common Variable Immunodeficiency (CVID).
It analyzes gene expression patterns and predicts the most probable PID category using a trained Multiclass Classification Model.

The system includes:

A Flask backend for handling predictions

A pre-trained ML model (multiclass_model.pkl)

A feature scaler (scaler.pkl)

An interactive HTML frontend

An augmented gene-expression dataset

A clean and extendable project structure

✨ Key Features
🔬 1. ML-Based PID Classification

Multiclass prediction: Classifies patient samples into major PID categories.

Trained on curated & augmented gene-expression data.

Uses a robust ML pipeline with scaling + classification.

🚀 2. Flask-Based Web Application

Simple, lightweight, and fast backend API.

Accepts user inputs for gene expression levels.

Returns real-time predictions via JSON.

🖥️ 3. User-Friendly Frontend

Clean HTML interface (front.html)

Easy input of gene values

Immediate display of classification results

📊 4. Dataset Included

PID_gene_expressions_augmented.csv

Contains cleaned, preprocessed, and augmented gene markers for machine learning.

🧠 5. Ready-to-Use Models

multiclass_model.pkl → Pretrained classifier

scaler.pkl → Normalization scaler for consistent preprocessing

📁 Project Structure
HealthGenomics-CVID-Diagnostic-main/
│
├── app.py                           # Flask server for prediction
├── front.html                       # UI for entering gene expression data
├── PID_gene_expressions_augmented.csv   # Gene expression dataset
├── multiclass_model.pkl             # Pretrained ML model
├── scaler.pkl                       # Feature scaling model
└── README.md                        # Documentation

🛠️ Tech Stack
Backend

Python 3.x

Flask

Scikit-learn

NumPy / Pandas

Frontend

HTML5

JavaScript (optional enhancements)

ML Pipeline

StandardScaler

Multiclass Classification (e.g., Random Forest / XGBoost / Logistic Regression depending on your model)

⚙️ Installation & Setup
1. Clone the Repository
git clone <repo-link>
cd HealthGenomics-CVID-Diagnostic-main

2. Create & Activate Virtual Environment
python -m venv env
source env/bin/activate     # Linux / macOS
env\Scripts\activate        # Windows

3. Install Dependencies
pip install -r requirements.txt


(If no requirements file exists, use this:)

pip install flask pandas numpy scikit-learn

4. Start the Flask Server
python app.py

5. Open the Frontend

Open front.html in your browser.

🧪 How the Prediction Works

User enters gene expression values.

Values are sent to the Flask backend API.

Backend:

Loads the saved scaler

Transforms input using StandardScaler

Loads the pretrained model

Returns the predicted PID class

Frontend displays the result instantly.

📈 Model Details

Model Type: Multiclass classifier

Input Features: Gene expression markers

Output: A PID category (e.g., CVID, SCID, XLA, etc.)

Preprocessing: StandardScaler normalization

📌 Future Enhancements

Add more PID classes from larger clinical datasets

Integrate visualization dashboards

Deploy on cloud (Azure/AWS/GCP)

Replace HTML with React/Next.js UI

Add SHAP-based explainability
