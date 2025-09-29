
---

# Python Project CI/CD Status

This repository contains a simple Python application managed via a robust **Continuous Integration (CI) pipeline** set up with **GitHub Actions**.

---

## 🛡️ Build and Security Status

![CI Build Status](https://github.com/Aamst258/progressAssignment-2/actions/workflows/python-ci.yml/badge.svg)
![CodeQL Security](https://github.com/Aamst258/progressAssignment-2/security/code-scanning/badge)

---

## 🚀 CI/CD Pipeline Summary

The GitHub Actions workflow executes the following steps automatically on every push and pull request to the `main` branch:

1. **Setup & Dependencies**

   * Checks out the code and installs Python 3.10, along with required packages from `requirements.txt`.

2. **Linting**

   * Runs `flake8` to enforce code style and catch simple errors.

3. **Testing**

   * Runs `pytest` to execute all unit and integration tests.

4. **Security Scanning (Bandit)**

   * Executes `bandit` to identify common security issues (e.g., use of `assert`, hardcoded passwords, unsafe imports) in Python code.

5. **Static Code Analysis (CodeQL)**

   * Performs deep security and bug hunting analysis, with results uploaded directly to the GitHub repository's **Security** tab.

---

## 🔧 How to Use

### 1. Clone the Repository

You need the repository URL from GitHub (usually ends with `.git`).

* Go to your repository on GitHub and click the **Code** button → copy the HTTPS URL.
* Open your terminal and run:

```bash
git clone https://github.com/YOUR_USERNAME/YOUR_REPOSITORY.git
cd YOUR_REPOSITORY
```

---

### 2. Required Project Files (Checklist)

| File/Directory                    | Purpose                                                                                |
| --------------------------------- | -------------------------------------------------------------------------------------- |
| `app.py`                          | Your main Flask application file.                                                      |
| `requirements.txt`                | Lists all dependencies (`flask`, `pytest`, `flake8`, `bandit`, etc.) for the pipeline. |
| `tests/` (Directory)              | Contains all test files.                                                               |
| `tests/__init__.py`               | Empty file that makes `tests` a Python package (prevents ModuleNotFoundError).         |
| `tests/test_app.py`               | Unit test file that imports and tests `app.py`.                                        |
| `.github/workflows/python-ci.yml` | GitHub Actions workflow defining CI/CD steps (lint, test, security scans).             |

> Make sure all required files exist, push to `main`, and the pipeline will automatically trigger.

---

### ✅ Notes

* Replace `YOUR_USERNAME/YOUR_REPOSITORY` in the badges and instructions with your actual GitHub repo path.
* You can view the CI/CD status and CodeQL security results directly in the **Actions** and **Security** tabs on GitHub.

---


