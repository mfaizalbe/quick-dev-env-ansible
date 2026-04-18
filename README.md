# quick-dev-env-ansible
Bootstrap a development environment on macOS, Linux, or WSL with a single Ansible command.

# 🚀 Quick Dev Environment (Ansible)

A simple Ansible playbook to bootstrap a ready-to-use DevOps development environment on Linux or WSL.

This project installs common DevOps tools in a consistent way for local development and onboarding.

---

## 🧰 What it installs

### 🐧 Linux / WSL
- Git  
- Curl / Wget  
- Python 3 + pip + venv  
- Build tools  
- Docker  
- Terraform  
- kubectl  
- Helm  
- AWS CLI  
- Node.js (via NVM)  

---

### 🍎 macOS
Uses Homebrew + Brewfile to install:

- Git  
- Python  
- Terraform  
- AWS CLI  
- kubectl  
- Helm  
- Docker Desktop  
- Node.js (NVM)  
- VS Code  

---

## ⚡ Quick Start

### 1️⃣ Install Ansible (if not installed)

**For macOS**

```bash
brew install ansible
```

**For Linux / WSL (Ubuntu / Debian)**

```bash
sudo apt update
sudo apt install ansible -y
```

### 2️⃣ Run the playbook
```bash
ansible-playbook playbook.yml
```

---

## 🧠 How it works
### macOS
  
  → Homebrew + Brewfile
  
  → Installs full dev toolchain



### Linux / WSL
  
  → Ansible playbook
  
  → Installs full dev toolchain



### WSL detection
  
  → Skips Docker engine install
  
  → Prompts Docker Desktop usage

---

## 🛠️ Tech Stack
Ansible (automation)

Homebrew (macOS)

Bash (Linux shell execution)

WSL (Windows Linux layer)

---

## 📌 Notes
Run with `sudo` when required (Linux)

Docker Desktop required on macOS/Windows

WSL must be enabled for Windows users

Designed for simplicity, not enterprise complexity
