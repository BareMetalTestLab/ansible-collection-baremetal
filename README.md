# baremetal Ansible Collection

Collection for automating baremetal tasks.

## Roles
- install_eabi_arm_gcc: Installs the arm-none-eabi-gcc compiler
- install_jlink: Installs SEGGER J-Link tools
- install_can_tools: Installs can-utils and PEAK CAN driver

## Installation

You can install this collection in two ways:

### 1. From Ansible Galaxy (recommended)

```sh
ansible-galaxy collection install paulfirs.baremetal
```

### 2. Local installation

- Clone or download this repository
- `$ cd ansible-collection-baremetal/`
- `$ ansible-galaxy collection build`
- `$ ansible-galaxy collection install paulfirs-baremetal-<version>.tar.gz` (use -`-force` to overwrite existing version)

Then use the collection as shown below.

## Quick Start

1. Create a playbook file, for example, `site.yml` or use one of the `examples/` playbooks:

```yaml
- hosts: all
  become: yes  # Run tasks with root privileges (recommended)
  roles:
    - paulfirs.baremetal.install_eabi_arm_gcc
    - paulfirs.baremetal.install_jlink
    - paulfirs.baremetal.install_can_tools
```

2. Run the playbook with the command:

```sh
ansible-playbook -i "user@host," examples/site.yml --ask-pass --ask-become-pass
```

- `-i "user@host,"` — inline inventory (you can also use an inventory file)
- `--ask-pass` — prompt for SSH user password
- `--ask-become-pass` — prompt for sudo password

See the [Ansible documentation](https://docs.ansible.com/) for more details on syntax and configuration.
