# PackSure AI

### AI-Powered Packaged Commodity Compliance & Legal Metrology Platform

PackSure AI is an intelligent compliance platform designed to help inspect packaged commodities against applicable **Legal Metrology and Packaged Commodities requirements**.

The platform uses **OCR, image processing, AI-assisted information extraction, and a rule-based compliance engine** to analyze product labels and identify missing, incorrect, or potentially non-compliant declarations.

---

## 🚀 Features

### 📦 Product Label Scanning

Upload an image of a packaged product label and let PackSure AI analyze the visible declarations.

### 🔍 OCR & Information Extraction

The system extracts important information from product packaging, such as:

* Manufacturer / Packer details
* Generic product name
* Net quantity
* MRP
* Date-related declarations
* Consumer-care information
* PIN code
* Other relevant package declarations

### 🤖 AI-Assisted Analysis

PackSure AI combines OCR and AI-based interpretation to handle different packaging layouts and label formats.

### ⚖️ Compliance Rule Engine

Extracted information is checked against configured Legal Metrology / Packaged Commodities requirements.

The system produces results such as:

* **PASS**
* **FAIL**
* **NEEDS REVIEW**

### 📊 Compliance Dashboard

The dashboard provides an overview of:

* Total scans
* Passed scans
* Failed scans
* Items requiring review
* Compliance score
* Recent scan activity

### 📄 Compliance Reports

Generate structured reports containing:

* Scan information
* Extracted declarations
* Compliance results
* Failed checks
* Evidence / observations
* Overall result

### 🕘 Scan History

Previous inspections can be stored and reviewed for future reference.

### 🧪 Sandbox / Testing

The platform can be used to test different package images and evaluate the compliance workflow.

---

# 🧠 How PackSure AI Works

```text
        Product Package Image
                 │
                 ▼
        Image Quality Check
                 │
                 ▼
       Image Pre-processing
                 │
                 ▼
          OCR / AI Analysis
                 │
                 ▼
      Declaration Extraction
                 │
                 ▼
       Product Classification
                 │
                 ▼
        Applicable Rule Check
                 │
                 ▼
        Compliance Engine
                 │
        ┌────────┼─────────┐
        ▼        ▼         ▼
      PASS      FAIL    NEEDS REVIEW
        │        │         │
        └────────┼─────────┘
                 ▼
        Report & Dashboard
```

---

# 🏗️ System Architecture

```text
┌─────────────────────────────────────────┐
│              Frontend UI                │
│        HTML / CSS / JavaScript           │
└──────────────────┬──────────────────────┘
                   │
                   ▼
┌─────────────────────────────────────────┐
│              FastAPI Backend             │
│          REST API / Application Logic    │
└──────────────────┬──────────────────────┘
                   │
        ┌──────────┼───────────┐
        ▼          ▼           ▼
     OCR        AI Engine    Rules Engine
        │          │           │
        └──────────┼───────────┘
                   ▼
             Database
                   │
                   ▼
          Reports / History
```

---

# 🛠️ Technology Stack

## Frontend

* HTML5
* CSS3
* JavaScript
* Font Awesome
* Responsive UI

## Backend

* Python
* FastAPI
* Uvicorn

## AI / Image Processing

* OCR
* Tesseract OCR
* OpenCV
* AI-assisted text / label interpretation

## Database

* SQLite
* SQL-based data storage

## Reporting

* ReportLab
* PDF report generation

## Deployment

* Vercel — frontend / web interface
* Render — backend API

---

# 📁 Project Structure

```text
PackSure_AI_Project/
│
├── app/
│   ├── main.py
│   ├── routes/
│   ├── services/
│   ├── models/
│   └── ...
│
├── frontend/
│   ├── index.html
│   ├── dashboard.html
│   ├── style.css
│   ├── script.js
│   └── assets/
│
├── uploads/
├── reports/
├── output/
├── tests/
├── tmp/
│
├── .env
├── .env.example
├── .gitignore
├── requirements.txt
├── render.yaml
└── README.md
```

---

# ⚙️ Installation

## 1. Clone the Repository

```bash
git clone https://github.com/CodeWithRipun/PackSure-AI.git
cd PackSure-AI
```

## 2. Create a Virtual Environment

### Windows

```powershell
py -m venv .venv
```

Activate it:

```powershell
.\.venv\Scripts\Activate.ps1
```

### Linux / macOS

```bash
python3 -m venv .venv
source .venv/bin/activate
```

---

## 3. Install Dependencies

```bash
pip install -r requirements.txt
```

---

# 🔧 Environment Configuration

Create a `.env` file in the project root.

Example:

```env
APP_NAME=PackSure AI
DATABASE_URL=sqlite:///./packsure.db
MAX_UPLOAD_MB=10
TESSERACT_CMD=tesseract
CORS_ORIGINS=*
```

For production, configure environment variables according to your deployment environment.

---

# 🔤 Tesseract OCR

PackSure AI uses Tesseract OCR for text extraction.

Check whether Tesseract is installed:

```bash
tesseract --version
```

If the command works, the OCR engine is available to the application.

---

# ▶️ Run the Backend

From the project root:

```bash
py -m uvicorn app.main:app --reload
```

The backend will normally be available at:

```text
http://127.0.0.1:8000
```

FastAPI API documentation:

```text
http://127.0.0.1:8000/docs
```

---

# 🌐 Run the Frontend

Open the frontend entry page in your development environment.

If the frontend is served by the FastAPI application, open:

```text
http://127.0.0.1:8000/
```

The dashboard can then be accessed through the application's navigation.

---

# 🔎 Compliance Workflow

### Step 1 — Upload

Upload a clear image of the product package or label.

### Step 2 — Image Processing

The system evaluates and prepares the image for text extraction.

### Step 3 — OCR

Text is extracted from the package using OCR.

### Step 4 — AI Interpretation

The extracted information is structured into relevant product declarations.

### Step 5 — Rule Application

The compliance engine checks the extracted declarations against applicable configured rules.

### Step 6 — Result

The platform generates:

```text
PASS
FAIL
NEEDS REVIEW
```

### Step 7 — Report

The inspection result can be reviewed through the dashboard and report system.

---

# 📋 Example Compliance Fields

PackSure AI can evaluate fields such as:

| Declaration           | Example                   |
| --------------------- | ------------------------- |
| Manufacturer / Packer | ABC Foods Pvt. Ltd.       |
| Product Name          | Packaged Food             |
| Net Quantity          | 500 g                     |
| MRP                   | ₹120                      |
| Date Information      | Relevant date declaration |
| PIN Code              | 781001                    |
| Consumer Information  | Customer-care details     |

The exact requirements applied depend on the configured rules and applicable regulatory provisions.

---

# 📊 Dashboard

The PackSure AI dashboard provides a centralized view of inspection activity.

Typical dashboard information includes:

```text
Total Scans
     │
     ├── Passed
     ├── Failed
     └── Needs Review

Compliance Score
Recent Scans
Scan History
Reports
```

---

# 📄 Reports

Each inspection can produce a structured compliance report containing:

* Product information
* Extracted declarations
* Compliance checks
* Failed / missing declarations
* Review requirements
* Final inspection result

---

# 🔐 Security & Configuration

Do not commit sensitive information to GitHub.

The following files and data should remain private where appropriate:

```text
.env
Database files
Uploaded images
Generated reports
API keys
Authentication secrets
```

Use `.env.example` to document required environment variables without exposing secret values.

---

# 🧪 Testing

Run the project's test suite using:

```bash
pytest
```

For API testing, FastAPI's interactive documentation is available at:

```text
/docs
```

---

# 🚀 Deployment

## Frontend

The frontend can be deployed using a modern web hosting platform such as Vercel.

## Backend

The FastAPI backend can be deployed using a Python-compatible hosting platform such as Render.

Example backend start command:

```bash
uvicorn app.main:app --host 0.0.0.0 --port $PORT
```

Make sure all required environment variables are configured in the deployment dashboard.

---

# 🎯 Project Objective

The objective of PackSure AI is to provide a digital workflow for **faster, more consistent, and traceable inspection of packaged commodity declarations**.

Instead of manually checking every declaration on a package, the system assists the inspection process by:

```text
SCAN
  ↓
EXTRACT
  ↓
ANALYZE
  ↓
CHECK
  ↓
REPORT
```

---

# 💡 Key Innovation

PackSure AI combines:

**Computer Vision + OCR + AI + Rule-Based Compliance**

into a single inspection workflow.

This allows the system to transform an ordinary package image into structured compliance information and an actionable inspection result.

---

# 🏆 Hackathon Use Case

PackSure AI is designed as a technology prototype for **Smart India Hackathon-style problem solving** in the area of Legal Metrology and packaged commodity compliance.

The platform demonstrates how AI-assisted document and image analysis can support regulatory inspection workflows.

---

# ⚠️ Important Disclaimer

PackSure AI is a software prototype intended to assist compliance inspection.

Its automated results should not be treated as a substitute for official legal interpretation, regulatory authority decisions, or professional compliance review.

Applicable requirements should always be verified against the latest official rules, notifications, and regulatory guidance.

---

# 🔮 Future Improvements

Potential future enhancements include:

* Multilingual OCR
* Better curved-package recognition
* Improved handling of glossy packaging
* Advanced layout detection
* Barcode / QR analysis
* Automatic rule updates
* Evidence image highlighting
* Confidence scoring
* Mobile application
* Cloud database
* Role-based access control
* Advanced analytics
* API integrations
* Human-in-the-loop review
* More comprehensive regulatory rule coverage

---

# 👨‍💻 Project

**PackSure AI**

AI-Powered Packaged Commodity Compliance Platform

Developed as an innovative solution for automated Legal Metrology inspection assistance.

---

## 📜 License

This project is intended for educational, research, demonstration, and hackathon purposes unless otherwise specified by the project owner.
