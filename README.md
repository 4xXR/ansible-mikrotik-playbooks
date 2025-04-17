# MikroTik Automation Playbooks (Ansible)

These playbooks are designed to automate common MikroTik RouterOS tasks using Ansible.

## Playbooks Included

### 1. show_interfaces.yml
- Retrieves and displays all MikroTik interfaces.

### 2. backup_mikrotik.yml
- Exports the full MikroTik configuration and saves it locally in `.rsc` format.

### 3. set_interface_comment.yml
- Adds or updates the comment field for a specified interface.

### 4. secure_unused_ports.yml
- Disables all unused ethernet ports (`ether2` to `ether5`) that are not currently running.

## Inventory Example

```
[mikrotik]
192.168.88.1 ansible_user=admin ansible_password=yourpassword ansible_network_os=routeros ansible_connection=network_cli
```

## Requirements

- Ansible 2.13+
- community.routeros collection
- SSH access enabled on MikroTik device