# Enterprise Ansible Automation Lab (AWS + RHEL-style Architecture)

## Overview
This project demonstrates a real-world infrastructure automation setup using Ansible Navigator and AWS EC2 instances. It simulates a production-like environment with multiple managed nodes and role-based automation.

---

## Architecture

- Ansible Control Node (Ubuntu EC2)
- Web Node (Apache automation via Galaxy role)
- NFS Node (shared storage automation)
- Security Node (Linux hardening & SSH policies)

---

## Key Features

- Role-based infrastructure automation using Ansible Galaxy
- Apache web server deployment using reusable roles
- NFS server/client configuration for shared storage
- Security hardening (SSH key-only authentication, root login disabled)
- Inventory-based multi-node orchestration
- Privilege escalation (become) implementation
- Execution using Ansible Navigator (modern AAP workflow)

---

## Technologies Used

- Ansible Automation Platform (Navigator)
- Ansible Galaxy Roles
- AWS EC2 (Ubuntu)
- Linux (Ubuntu / RHEL-style configuration concepts)
- SSH key-based authentication
- NFS (Network File System)
- Apache HTTP Server

---

## Security Implementation

- Disabled root SSH login
- Disabled password authentication
- Enforced key-based authentication
- Managed privileged access using sudo (become)
- Secrets excluded from Git tracking (.gitignore)

---

## How to Run

```bash
ansible-navigator run playbooks/site.yml --mode stdout
