# install_can_tools

This Ansible role installs CAN tools including can-utils and peakcan driver, and configures kernel modules for CAN bus support.

## Requirements

- Ubuntu/Debian system
- Ansible 2.9+

## Role Variables

None

## Dependencies

None

## Example Playbook

```yaml
- hosts: servers
  roles:
    - install_can_tools
```

## License

BSD