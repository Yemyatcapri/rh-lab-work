# Control Review Lab – Apache with SSL using Ansible

## Overview
This lab demonstrates how to deploy and secure an Apache web server using Ansible on Red Hat Enterprise Linux. The playbook automates package installation, SSL configuration, service management, and firewall setup.

The server is configured to support secure HTTPS connections using a self-signed SSL certificate.

## Objectives

- Install Apache and mod_ssl
- Configure HTTPS encryption
- Manage services using Ansible
- Implement conditionals, loops, and handlers
- Configure firewall for HTTP and HTTPS
- Handle configuration errors safely

## Files

- playbook.yml – Main Ansible playbook  
- vars.yml – Variables file  
- inventory – Host inventory  
- ansible.cfg – Ansible configuration  
- ssl.conf – SSL configuration  
- server.crt – SSL certificate  
- server.key – Private key  
- index.html – Test web page  

## Key Skills Demonstrated

- Ansible automation  
- Linux system administration  
- Apache deployment  
- SSL/TLS configuration  
- Firewall configuration  
- Infrastructure as Code (IaC)  

## Verification

The web server was successfully verified using HTTPS:
