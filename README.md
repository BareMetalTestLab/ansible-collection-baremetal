
# baremetal Ansible Collection

Collection for automating baremetal tasks, including installation of arm-none-eabi-gcc.

## Roles
- install_eabi_arm_gcc: Installs the arm-none-eabi-gcc compiler
- install_jlink: Installs SEGGER J-Link tools

## Installation

Copy the `baremetal` directory to your project's `ansible_collections` or use standard Ansible Galaxy publishing methods.

## Usage

Example: install both arm-none-eabi-gcc and J-Link tools

```yaml
- hosts: all
  roles:
    - baremetal.install_eabi_arm_gcc
    - baremetal.install_jlink
```
