# Homelab ansible playbook

Personal ansible playbook self-hosting services.

## Description

This playbook contains basic installs and configs to make sure to install services via podman and compose in rootless mode.

## Getting started

### Dependencies

On managed node:
- Ansible

Guest:
- Debian 12

### Installing

1. Clone this repository
1. Create a `hosts.ini` with at least one remote server in `[remote]` group
1. Optional: customize ssh port by setting the variable in `roles/firewall/vars`

#### Example

```ini
[remote]
127.0.0.1:1024 ansible_user=foo
```

### Run playbook

```
ansible-playbook -i hosts.ini site.yaml
```