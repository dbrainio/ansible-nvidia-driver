NVIDIA Driver Ansible Role
==========================

Install the NVIDIA GPU driver from the [Graphics Drivers PPA](https://launchpad.net/~graphics-drivers/+archive/ubuntu/ppa).

Requirements
------------

Ubuntu 16.04 and 18.04

Role Variables
--------------

- `driver_version` - Which version of the driver to install.
- `nvidia_driver_headless` - Whether to install the headless version of the driver.


Tests
------------
Run
```
vagrant up
vagranty provision
```

Dependencies
------------

None.

Example Playbook
----------------

```yml
- hosts: gpu_servers
  roles:
     - tangentspace.nvidia_driver
```

License
-------

MIT / BSD
