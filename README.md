
# Python CI Pipeline on AWS EC2 using GitHub Actions

## 📌 Project Overview

This project demonstrates Continuous Integration (CI) using GitHub Actions and a self-hosted runner hosted on an AWS EC2 Ubuntu instance.

Whenever code is pushed to the GitHub repository, GitHub Actions triggers a workflow that runs Python tests on the EC2 instance.

## 🏗️ Architecture

Developer → GitHub Repository → GitHub Actions → AWS EC2 Self-Hosted Runner → Python Tests

## 🛠️ Technologies Used

- **AWS EC2** – Ubuntu server hosting the self-hosted runner
- **GitHub Actions** – CI workflow automation
- **Python 3** – Application development
- **Pytest** – Automated testing
- **Git** – Version control

## 📂 Project Structure

```text
Github-Action-python-ci-aws/
├── .github/
│   └── workflows/
│       └── python-ci.yml
├── .gitignore
├── calculator.py
├── requirements.txt
└── test_calculator.py
```

## ⚙️ CI Workflow

The GitHub Actions workflow performs the following steps:

1. Trigger the workflow on push or pull request to the `main` branch.
2. Run the job on a self-hosted Ubuntu EC2 runner.
3. Check out the repository.
4. Check the Python version.
5. Create a Python virtual environment.
6. Install dependencies.
7. Run automated tests using Pytest.

## 🚀 Setup and Execution

### 1. Clone the repository

```bash
git clone https://github.com/Arunkrishna02/GitHub-Actions-python-ci-aws.git
cd GitHub-Actions-python-ci-aws
```

### 2. Install dependencies

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

### 3. Run tests locally

```bash
python -m pytest -v
```

## ☁️ AWS EC2 Self-Hosted Runner

The project uses an Ubuntu EC2 instance as a self-hosted GitHub Actions runner.

The runner is registered with the repository and executes CI jobs when GitHub Actions triggers the workflow.

## ✅ Expected Result

When the workflow runs successfully, GitHub Actions displays a green check mark, indicating that the Python tests have passed.

## 🎯 Learning Objectives

- Understand Continuous Integration using GitHub Actions.
- Configure a self-hosted runner on AWS EC2.
- Automate Python testing with Pytest.
- Connect GitHub repositories to AWS infrastructure.
- Monitor workflow execution through GitHub Actions logs.
