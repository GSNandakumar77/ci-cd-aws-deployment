CI/CD AWS Deployment – ML Project
📖 Overview

This project demonstrates an end-to-end Machine Learning pipeline deployed on AWS EC2 with Docker and GitHub Actions CI/CD.
The ML model predicts student math scores based on demographic and academic data.

Key features:

Automated data preprocessing, training, and evaluation

Flask web application for model inference

Dockerized deployment for portability

CI/CD pipeline with GitHub Actions to build, test, and deploy automatically

Integrated logging & exception handling for production readiness

📂 Project Structure
ci-cd-aws-deployment/
│
├── .github/workflows/        # CI/CD pipeline definitions
├── artifacts/                # Saved models, metrics, and artifacts
├── awsvenv/                  # Virtual environment (not needed in repo ideally)
├── notebook/                 # Jupyter notebooks for EDA & experiments
├── src/                      # Modular ML pipeline source code
├── templates/                # HTML templates for Flask app
│
├── app.py                    # Flask entry point
├── Dockerfile                # Docker image definition
├── requirements.txt          # Python dependencies
├── setup.py                  # Package setup script
├── README.md                 # Documentation (this file)
└── .gitignore                # Ignored files

⚙️ Tech Stack

Python 3.9+

Flask (Web Framework)

scikit-learn, pandas, numpy (ML & preprocessing)

Jupyter Notebook (EDA & experiments)

Docker (Containerization)

AWS EC2 + ECR (Deployment & registry)

GitHub Actions (CI/CD pipeline)

🚀 Workflow

Data Pipeline

Preprocessing of student demographic & academic data

Train-test split & feature engineering

Model Training

Regression models trained & evaluated

Best model saved as an artifact

Flask App

Exposes /predict endpoint

Simple HTML form via templates/

Containerization

Dockerized application

Pushed to AWS ECR

CI/CD with GitHub Actions

On push → run tests → build Docker image → push to ECR → deploy to EC2

🛠️ Setup & Installation
Clone Repo
git clone https://github.com/GSNandakumar77/ci-cd-aws-deployment.git
cd ci-cd-aws-deployment

Create Virtual Environment
python -m venv venv
source venv/bin/activate   # Linux/Mac
venv\Scripts\activate      # Windows

Install Dependencies
pip install -r requirements.txt

Run Locally
python app.py


App will run on http://127.0.0.1:5000/

🐳 Docker Deployment

Build Docker image:

docker build -t student-score-app .


Run container:

docker run -p 5000:5000 student-score-app

☁️ AWS Deployment (CI/CD)

ECR stores the Docker image

EC2 hosts the container

GitHub Actions automates build & deploy steps

📊 Results

Automated pipeline runs end-to-end

Regression model predicts student scores with good accuracy

Fully deployed on AWS with minimal manual steps

📌 Future Improvements

Add monitoring & alerts

Experiment with Deep Learning models

Extend CI/CD for multi-environment (dev, staging, prod)

👨‍💻 Author

Nandhakumar G S

LinkedIn

GitHub
