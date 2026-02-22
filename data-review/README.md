# Lab: Managing Variables and Facts

## Overview
This activity focused on configuring a web server (serverb) with basic authentication. 

## Key Tasks Completed:
* Installed `httpd`, `mod_ssl`, and `firewalld`.
* Used **Ansible Vault** to encrypt the `vars/secret.yml` file.
* Used **Ansible Facts** (`ansible_facts['fqdn']`) to customize the `index.html` file.
* Configured `.htaccess` and `htpasswd` for user authentication.

## How to Run
`ansible-navigator run playbook.yml -m stdout --ask-vault-pass`
