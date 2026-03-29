# Ansible Role Review Lab (RHEL)

## 📌 Overview

This project demonstrates the use of **Ansible roles and system roles** to configure a development web server on Red Hat Enterprise Linux.

The setup replicates a production environment while allowing multiple developers to host their own web content on custom ports.

---

## ⚙️ Key Features

* Automated Apache HTTP server configuration using Ansible roles
* Role dependency management (`infra.apache`)
* Per-user web environments with custom ports (9081, 9082)
* SELinux configuration using `redhat.rhel_system_roles.selinux`
* Firewall and service management
* Idempotent and reusable playbook design

---

## 🏗️ Project Structure

```
role-review/
├── web_dev_server.yml        # Main playbook
├── ansible.cfg               # Ansible configuration
├── inventory                 # Inventory file
├── roles/
│   └── apache.developer_configs/
├── group_vars/
│   └── dev_webserver/
```

---

## 🚀 How It Works

1. Configures Apache using a dependency role
2. Creates user accounts for developers
3. Assigns each user a dedicated web directory
4. Maps each user to a unique port
5. Applies SELinux policies to allow non-standard HTTP ports
6. Ensures services and firewall rules are correctly set

---

## ▶️ Run the Playbook

```bash
ansible-navigator run web_dev_server.yml -m stdout
```

---

## 🌐 Example Output

```
curl servera
→ Production server page

curl servera:9081
→ John Doe (jdoe)

curl servera:9082
→ Jane Doe (jdoe2)
```

---

## 🛠️ Technologies Used

* Ansible
* Red Hat Enterprise Linux (RHEL)
* Apache HTTP Server
* SELinux
* YAML / Jinja2

---

## 🎯 Learning Outcomes

* Building and structuring Ansible roles
* Managing role dependencies
* Working with SELinux in automation
* Using group variables for scalable configurations
* Writing reusable and modular playbooks

---

## 📖 Notes

This project was completed as part of a Red Hat Ansible lab focused on role-based automation and system configuration.

---

## 👤 Author

Student User
