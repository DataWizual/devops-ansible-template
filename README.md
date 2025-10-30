
# 🚀 DevOps Ansible Template

A **universal automation template** built with **Ansible** to set up and deploy Docker-based environments — locally or on remote Linux servers.  
It’s designed for developers, system administrators, and DevOps engineers who want a **fast and reproducible setup** for any project.

---

## 🧰 Features

- 🐧 Works on any Debian/Ubuntu-based Linux system  
- ⚙️ Installs and starts Docker automatically (if not installed)  
- 🔁 Clones and deploys any Git repository (configurable in `group_vars`)  
- 🧩 Uses a clean modular role structure (`roles/devops`)  
- 🧱 Supports local or remote targets (via SSH connection)  
- 🔒 Idempotent — safe to run multiple times

---

## ⚙️ Requirements

| Component | Recommended Version |
|------------|----------------------|
| OS | Linux (Ubuntu 22.04+ / Debian 11+) |
| Ansible | 2.9 or later |
| Docker | 20.10+ |
| Git | any recent version |

---

## 🚀 Quick Start

```bash
# Clone this repository
git clone https://github.com/DataWizual/devops-ansible-template.git
cd devops-ansible-template

# Run the playbook
ansible-playbook playbook.yml

🔧 Configuration
Edit the variables in group_vars/all.yml before running:

project_repo: "https://github.com/DataWizual/dev-environment-setup.git"
project_dest: "/opt/dev-environment-setup"
project_branch: "main"
project_port: 8080

You can change project_repo to any repository you want to deploy —
the rest of the process will run automatically.

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

🧠 How It Works

1. Checks if Docker is already installed
2. Installs Docker if missing
3. Starts the Docker service
4. Clones the project repository
5. Runs docker compose up -d automatically
Each step is idempotent — it will skip actions if already done.

🧩 Example Output

PLAY RECAP ******************************************************************
localhost : ok=5 changed=3 unreachable=0 failed=0 skipped=2 rescued=0 ignored=0

This means the setup was successful and the environment is ready.
Your app will usually be available at http://localhost:<project_port>.

📦 Versioning
Stable release: v1.0
To tag your own release:

git tag -a v1.0 -m "Initial release of DevOps Ansible Template"
git push origin v1.0

🧑‍💻 Author

Eldor Zufarov (DataWizual)
💼 DevOps Engineer · Automation Enthusiast
📍 GitHub Profile

⚖️ License
This project is licensed under the MIT License — free for personal and commercial use.

“Infrastructure is code. Automation is clarity.” — Eldorz Zufarov
