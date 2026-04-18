# 🚀 DevOps Bootstrap Environment (Ansible)

A **production-grade, portable DevOps environment setup** using Ansible.

This project automates the installation and configuration of essential DevOps tools across **macOS and Linux (Debian/WSL)** in a repeatable and idempotent way.

---

# 🧠 Purpose

To eliminate manual setup and ensure every machine has a **consistent development environment** for:

* DevOps workflows
* Cloud engineering
* Infrastructure as Code (IaC)
* CI/CD pipelines

---

# ⚙️ What gets installed

## 🖥️ Core Tools

* Git
* Curl / Wget
* Python 3
* Pip / Venv

## ☁️ Cloud & DevOps Tools

* AWS CLI
* Terraform (version-controlled)
* kubectl (Kubernetes CLI)
* Helm

## 🐳 Containers

* Docker (Linux only)

## 🟢 Node.js Environment

* NVM (Node Version Manager)
* Node.js LTS
* npm

---

# 🧩 Supported Systems

| OS                                | Status             |
| --------------------------------- | ------------------ |
| macOS (Apple Silicon / Intel)     | ✅                  |
| Ubuntu / Debian                   | ✅                  |
| WSL (Windows Subsystem for Linux) | ⚠️ partial support |

---

# 🚀 Quick Start

## 1. Clone repository

```bash
git clone <repo-url>
cd quick-dev-env-ansible
```

## 2. Run setup

```bash
ansible-playbook playbook.yml
```

---

# 🔍 Verify installation

After running the playbook:

```bash
git --version
node -v
npm -v
python3 --version
aws --version
terraform -version
kubectl version --client
helm version
```

---

# 🏗️ Design Principles

This project follows production DevOps principles:

### ✔ Idempotency

* Safe to run multiple times
* No duplicate installations

### ✔ Portability

* Works across macOS and Linux

### ✔ Version Control

* Terraform and Kubernetes tools are pinned

### ✔ Minimal manual setup

* No need for manual installs after first run

---

# ⚠️ Notes

* NVM requires shell reload (`source ~/.zshrc`) after installation
* AWS CLI and Docker may require system permissions on Linux
* Kubernetes cluster is not installed (kubectl only)

---

# 🧠 Known Limitations

* kubectl requires a running cluster to test fully
* Docker install is system-level (Linux only)
* macOS Homebrew path differences may exist on Intel Macs

---

# 📈 Future Improvements

* Role-based Ansible structure
* CI/CD validation (GitHub Actions)
* Version lock file for all tools
* Multi-machine provisioning support


