# DevOps Ansible Template

A universal **Ansible playbook** to automate setup of Docker-based development environments.

## 🧰 Features
- Installs and starts Docker automatically
- Clones any Git repository (configurable)
- Builds and runs containers via Docker Compose
- Works locally or on remote Linux hosts
- Uses clean, modular role structure

## ⚙️ Usage
1. Edit variables in `group_vars/all.yml` to set your repo and paths.
2. Run the playbook:
   ```bash
   ansible-playbook playbook.yml

3. Access your app at http://localhost:<project_port>.

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
