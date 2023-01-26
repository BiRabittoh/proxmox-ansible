# Proxmox server setup

## Instructions

First, install dependencies:
```
ansible-galaxy install -r requirements.yml
```

Then, create a `.vault_pass.txt` with the correct password. Now you can run:

```
ansible-playbook base.yml --vault-pass-file .vault_pass.txt
```

## Playbooks

* `base.yml` sets up a basic configuration and updates all packages;
* `reboot.yml` reboots all servers unconditionally;
* `python.yml` deploys my Python projects;
* `node.yml` deploys my NodeJS projects;
* `deploy.yml` runs, in order: `base.yml`, `python.yml`, `node.yml`.
