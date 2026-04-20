# Pay API Ansible Setup

Ansible playbook to configure web and database servers for the PayAPI application.

## Infrastructure
- 3 x Web servers (1 Ubuntu,2 Amazon Linux 2023) — pay-web01, pay-web02, pay-web03
- 1 x Database server (Amazon Linux 2023) — pay-db01

## What it does
- Installs required packages on web servers
- Installs and enables MariaDB on the database server
- Deploys a Jinja2 web template with environment variables
- Uses handlers to restart services only when needed

## Usage
bash
ansible-playbook pay-api.yaml
Variables
Located in group_vars/all:
db_name - Database name
db_port - Database port
app_version - Application version

Variables
Located in group_vars/all:
db_name - Database name
db_port - Database port
app_version - Application version
