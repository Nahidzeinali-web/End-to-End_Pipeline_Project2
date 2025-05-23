# 🛡️ Network Security ML Pipeline

This project implements a complete machine learning pipeline for network security applications. It includes data ingestion, validation, transformation, model training, and deployment via a FastAPI web interface. The pipeline uses MongoDB for data storage and is containerized with Docker.

---

## 🚀 Features

- 📥 Data Ingestion from configured sources
- ✅ Data Validation checks
- 🔄 Data Transformation for ML readiness
- 🧠 Model Training using custom ML algorithms
- 🧪 Experiment tracking and logging
- 🌐 FastAPI app for model interaction
- 🐳 Docker support for containerized deployment

---

## 📁 Project Structure

```
.
├── app.py                 # FastAPI application entry
├── main.py                # Main training pipeline runner
├── Dockerfile             # Container setup
├── .gitignore             # Git exclusions
└── networksecurity/       # Core pipeline logic and utilities
```

---

## ⚙️ Installation

### 1. Clone the repository

```bash
git clone https://github.com/your-username/networksecurity-ml.git
cd networksecurity-ml
```

### 2. Create a virtual environment

```bash
python -m venv venv
source venv/bin/activate  # or `venv\Scripts\activate` on Windows
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

---

## 🧪 Running the ML Pipeline

```bash
python main.py
```

This will trigger the pipeline: ingestion → validation → transformation → training.

---

## 🌐 Running the FastAPI App

```bash
uvicorn app:app --reload
```

Open your browser and navigate to `http://127.0.0.1:8000`.

---

## 🐳 Docker Usage

### Build the Docker image

```bash
docker build -t networksecurity-app .
```

### Run the container

```bash
docker run -p 8000:8000 networksecurity-app
```

---

## 🧠 Tech Stack

- **Python**, **Pandas**, **Scikit-learn**
- **FastAPI** – for the web app
- **MongoDB** – data storage
- **Docker** – containerization
- **Uvicorn** – ASGI server
- **Certifi**, **dotenv** – secure and modular config


---

### 🧪 Network Security Project for Phishing Data

This project can be extended to phishing detection using structured network security data.

---

## 🔐 GitHub Secrets Configuration (for AWS ECR)

Ensure the following secrets are configured in your GitHub repository:

```env
AWS_ACCESS_KEY_ID=your_aws_access_key
AWS_SECRET_ACCESS_KEY=your_aws_secret_key
AWS_REGION=us-east-1
AWS_ECR_LOGIN_URI=788614365622.dkr.ecr.us-east-1.amazonaws.com/networkssecurity
ECR_REPOSITORY_NAME=networkssecurity
```

---

## 🐳 Docker Setup on AWS EC2

Use the following commands to set up Docker on a fresh EC2 Ubuntu instance:

### Optional (System update)

```bash
sudo apt-get update -y
sudo apt-get upgrade
```

### Required (Docker install & user permission)

```bash
curl -fsSL https://get.docker.com -o get-docker.sh
sudo sh get-docker.sh
sudo usermod -aG docker ubuntu
newgrp docker
```
