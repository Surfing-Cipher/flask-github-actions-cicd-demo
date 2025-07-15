# 🚀 Flask CI/CD Demo with GitHub Actions & Docker

This project is a minimal but complete example of setting up **Continuous Integration and Continuous Deployment (CI/CD)** using **Flask**, **Docker**, and **GitHub Actions**. It’s designed to demonstrate how you can automate testing and Docker builds in a clean, reproducible workflow.

---

## 📌 Features

- ✅ Simple Flask web application
- ✅ Basic test suite with PyTest
- ✅ Dockerized application setup
- ✅ CI/CD pipeline via GitHub Actions
  - Runs tests on every push or PR to `main`
  - Builds Docker image after successful test run

---

## 🧱 Tech Stack

- **Python 3.9**
- **Flask**
- **PyTest**
- **Docker**
- **GitHub Actions**

---

## 🔁 CI/CD Lifecycle

This project implements the full CI/CD loop:

```

Plan → Code → Build → Test → Release → Deploy → Operate → Monitor

```

![CI/CD Lifecycle](assets/cicd-diagram.png)

---

## 📁 Project Structure

```

.
├── app.py                  # Flask web app
├── requirements.txt        # Python dependencies
├── Dockerfile              # Container definition
├── .dockerignore
├── tests/
│   └── test\_app.py         # Sample PyTest test
└── .github/
└── workflows/
└── cicd.yml        # GitHub Actions CI/CD config

````

---

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/Surfing-Cipher/flask-github-actions-cicd-demo.git
cd flask-github-actions-cicd-demo
````

### 2. Run Locally

```bash
pip install -r requirements.txt
python app.py
```

App will be available at: `http://localhost:5000`

---

## 🧪 Run Tests

```bash
pytest
```

---

## 🐳 Build Docker Image

```bash
docker build -t flask-ci-cd-demo .
```

---

## ⚙️ GitHub Actions: CI/CD Pipeline

This workflow is defined in `.github/workflows/cicd.yml`.

It does the following:

* On push to `main`:

  * Checks out code
  * Sets up Python
  * Installs dependencies
  * Runs tests with PyTest
  * Builds the Docker image if tests pass

---

## 📦 Future Improvements

* ✅ Add Docker image push to Docker Hub or GitHub Container Registry
* ✅ Auto-deploy to Heroku, Render, or EC2
* 🔒 Add security checks and linters
* 🔄 Add PR review automations

---

## 🙌 Acknowledgments

This project was built for learning and demonstrating modern DevOps practices using open-source tools. Inspired by the DevOps CI/CD lifecycle model.

---

## 📄 License

MIT License

```
