# VNF-on-Juniper-NFX-with-Ansible

These are different and simple ways to import, configure and launch a VNF on NFX using Ansible playbooks.

- playbook used to generate the config of the VNF if using config-drive (iso file): it works for Ubuntu and vSRX
- playbook used to load the image of the VNF on NFX
- playbook used to generate the VNF descriptor used on NFX: describe the VNF in NFW configuration
- playbook used to launch the VNF on NFX
- playbook used to stop the VNF on NFX
- playbook used to cleanup files on NFX: remove files from the import

# Static:
This uses static entries in the playbiooks (needs editing before launch if we want to change anything like VNF name or image).
The `commands` file contains the list of actions to perform.


# Fixed_variable:
Includes both fixed parts and few variables like the `{{ vm_name }}` where `vm_name: "newubuntu1"`
Same command order.


# Dynamic_variable:
Uses jinja2 syntax from various variables to fill the fields in the jinja files.
For example here, values in `host_vars/ubuntu_server/generic-vm-vars.yml` are used placed into `dynamic_variable/dynamic_variable_prepare_jdm_set_config_with_jinja.yml` following jinja2 rules `dynamic_variable/dynamic_variable_prepare_jdm_set_config_with_jinja.j2`.


Target VNF: vSRX, Ubuntu
