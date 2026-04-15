

# RHEL Automation with Ansible 9.0 — System Review Lab
 
Ansible playbooks for automating common Linux administration tasks on RHEL managed hosts.
 
## Setup
 
```bash
lab start system-review
cd ~/system-review
```
 
## Playbooks
 
| Playbook | What it does |
|----------|-------------|
| `repo_playbook.yml` | Configures internal Yum repo, imports GPG key, installs `rhelver` |
| `users.yml` | Creates `webadmin` group and users `ops1`, `ops2` |
| `storage.yml` | Sets up LVM volumes on `/dev/vdb` using `redhat.rhel_system_roles.storage` |
| `create_crontab_file.yml` | Schedules a disk usage cron job for the `devops` user |
| `network_playbook.yml` | Configures `eth1` with `172.25.250.40/24` using `redhat.rhel_system_roles.network` |
 
## Install Required Collection
 
```bash
ansible-galaxy collection install ./redhat-rhel_system_roles-1.19.3.tar.gz -p collections
```
 
## Running Playbooks
 
```bash
ansible-navigator run -m stdout <playbook>.yml
```
 
## Grade & Finish
 
```bash
lab grade system-review
lab finish system-review
```
 
> All playbooks target the `webservers` host group — `serverb.lab.example.com`.
