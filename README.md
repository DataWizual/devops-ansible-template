# DevOps Environment Setup (Ansible Template)

This playbook automates the setup of a Docker-based development environment.

## Usage

1. Edit variables in `group_vars/all.yml`
2. Run the playbook:
   ```bash
   ansible-playbook playbook.yml

3. Access the project at http://localhost:<project_port>

Features
   - Installs Docker if missing
   - Clones any Git repository
   - Builds and runs containers automatically
