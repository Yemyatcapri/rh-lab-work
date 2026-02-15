# Red Hat Lab: Implementing an Ansible Playbook

## Project Overview
This project demonstrates how to construct and run an Ansible Playbook to automate the installation and configuration of a web and database stack on a Red Hat Enterprise Linux (RHEL) environment.

## Lab Outcomes
* Developed a multi-play playbook (`internet.yml`).
* Automated package installation for `httpd`, `mariadb-server`, and `php`.
* Configured `firewalld` to allow HTTP traffic.
* Managed system services to ensure they are enabled and running.
* Performed post-deployment verification using the `uri` module.

## Files
* `internet.yml`: The main playbook containing the automation logic.
* `ansible.cfg`: Configuration file defining the inventory location and privilege escalation.
* `inventory`: Defines the managed hosts (`serverb.lab.example.com`).
* `index.php`: The PHP source file deployed to the web server.

## How to Run
To execute this playbook in a similar RHEL environment:
```bash
ansible-navigator run internet.yml -m stdout
