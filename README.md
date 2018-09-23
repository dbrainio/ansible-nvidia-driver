NVIDIA Driver Ansible Role
==========================

Install the NVIDIA GPU driver from the [Graphics Drivers PPA](https://launchpad.net/~graphics-drivers/+archive/ubuntu/ppa).

Requirements
------------

This role only works with Ubuntu 18.04.

Role Variables
--------------

- `nvidia_driver_version` - Which version of the driver to install.
- `nvidia_driver_headless` - Whether to install the headless version of the driver.


Dependencies
------------

None.

Example Playbook
----------------

```yml
- hosts: gpu_servers
  roles:
     - tangentspace.nvidia-driver
```

License
-------

MIT / BSD
