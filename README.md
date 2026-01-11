# ansible.role.provision-ubuntu-2404

Ansible role for baseline provisioning of Ubuntu 24.04 servers (packages, hardening, UFW, chrony, and optional GPU drivers).

## Quick start

```bash
ansible-galaxy collection install -r requirements.yml
ansible-playbook -i ansible_inventory site.yml
```

## Notes

- Set environment-specific values in `group_vars/all.yml`.
- See role defaults in `roles/ubuntu_2404_server/defaults/main.yml`.
