# ansible.role.provision-ubuntu-2404

Ansible role for baseline provisioning of Ubuntu 24.04 servers (packages, hardening, UFW, chrony, and optional GPU drivers).

## Usage

Example `requirements.yml` entry:

```yaml
roles:
  - name: ubuntu_2404_server
    src: git@github.com:khaosx/ansible.role.provision-ubuntu-2404.git
    version: main
```

Example playbook:

```yaml
- hosts: all
  become: true
  roles:
    - role: ubuntu_2404_server
```

## Notes

- Requires the `community.general` collection.
- Override environment-specific values via inventory/group/host vars as needed.
- See role defaults in `defaults/main.yml`.

## Raspberry Pi radios

Disable onboard Wi-Fi/Bluetooth using Device Tree overlays in `config.txt`. This is enabled by default for Raspberry Pi; opt out if needed.

```yaml
# opt out entirely:
# rpi_disable_radios: false
# or set individually:
# rpi_disable_wifi: true
# rpi_disable_bluetooth: true
# rpi_disable_bt_service: true
# rpi_config_txt_path: /boot/firmware/config.txt
```
