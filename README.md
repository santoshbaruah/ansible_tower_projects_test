# ansible_tower_projects_test
Ansible Project
This project contains Ansible playbooks for configuring servers with various packages, services and tools.

# Project Structure


# ansible_project/
├── inventory.yml
├── roles/
│   ├── common/
│   │   └── tasks/
│   │       └── main.yml
│   ├── packages/
│   │   └── tasks/
│   │       └── main.yml
│   ├── services/
│   │   └── tasks/
│   │       └── main.yml
│   ├── mysql/
│   │   └── tasks/
│   │       └── main.yml
│   ├── clamav/
│   │   └── tasks/
│   │       └── main.yml
    ├── playbooks/
│   ├── setup_env.yml
│   ├── install_packages.yml
│   ├── manage_services.yml
│   ├── setup_mysql.yml
│   ├── install_clamav.yml
├── templates/
│   └── index.html.j2

roles contains the ansible roles to configure different components
playbooks contains the playbook files that invoke the roles
inventory.yml defines the hosts to run ansible against
templates contains any templates used by the roles

# Usage
These playbooks are designed to be run from Ansible Tower.

# Prerequisites
Ansible needs to be installed on the target nodes
Inventory needs to be imported into Tower
This project needs to be imported into Tower
Credentials like db password should be stored as Tower credentials

# Running
Create a job template that points to the site.yml playbook
Select inventory and credentials
Launch the job template to run on the hosts

The playbooks will install packages, configure nginx/apache, setup MySQL, and deploy a welcome page.
