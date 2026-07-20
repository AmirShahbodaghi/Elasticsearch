# Elasticsearch Cluster & Kibana Deployment with Ansible

Automated Ansible playbook to deploy a multi-node **Elasticsearch cluster** and a **Kibana** instance using **Docker Compose**.

---

##  Project Structure

```text
ELASTISEARCH/
├── inventory/
│   ├── group_vars/
│   │   └── all/
│   │       └── vars.yml          # Global variables across hosts
│   └── hosts.yml                 # Inventory definition (hosts & cluster topology)
├── roles/
│   ├── elasticsearch/
│   │   ├── defaults/
│   │   │   └── main.yml          # Default role variables
│   │   ├── tasks/
│   │   │   └── main.yml          # Tasks to run Docker Compose for Elasticsearch
│   │   └── templates/
│   │       └── docker-compose.yml.j2  # Docker Compose template for Elasticsearch
│   └── kibana/                   # Role for setting up Kibana
├── elasticsearch.yml             # Main playbook
└── README.md

---

## Deploy the Stack

```
ansible-playbook -i inventory/hosts.yml elasticsearch.yml
```
