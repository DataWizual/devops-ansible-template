# 🚀 DevOps Ansible Template

A **universal Ansible playbook** for automating the setup of Docker-based environments — locally or on remote Linux servers.

## 🧰 Features
- Installs and starts Docker automatically
- Clones any Git repository (configurable)
- Builds and runs containers using Docker Compose
- Fully modular role structure (`roles/devops`)
- Works both on localhost and remote servers via SSH

## ⚙️ Requirements
- Linux system (Ubuntu / Debian recommended)
- Ansible 2.9+
- Docker 20.10+
- Git installed

## 🚀 Quick Start

git clone https://github.com/DataWizual/devops-ansible-template.git
cd devops-ansible-template
ansible-playbook playbook.yml

To change repository or settings, edit:

group_vars/all.yml

📂 Project Structure

ansible/
├── ansible.cfg
├── playbook.yml
├── group_vars/
│   └── all.yml
├── inventory/
│   └── hosts
└── roles/
    └── devops/
        └── tasks/
            └── main.yml

🧠 About

Created as part of a personal DevOps learning roadmap — combining automation, containerization, and infrastructure as code.

Author: Eldorz Zufarov (DataWizual)
License: MIT
