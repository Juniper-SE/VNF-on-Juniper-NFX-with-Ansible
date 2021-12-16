# Ansible commands to launch the VM:

- `dynamic_variable_prepare_new_vm_image.yml`: prepares the VM image 
- `dynamic_variable_prepare_new_vm_config.yml`: prepares the VM cloud-init config 


Uses jinja2 syntax from various variables to fill the fields in the jinja files.
For example here, values in `host_vars/ubuntu_server/generic-vm-vars.yml are used placed into dynamic_variable/dynamic_variable_prepare_jdm_set_config_with_jinja.yml following jinja2 rules dynamic_variable/dynamic_variable_prepare_jdm_set_config_with_jinja.j2.


- `dynamic_variable_prepare_jdm_set_config_with_jinja.yml`: the VM creation with multiple interface defined in vars, using Jinja2 below
- `dynamic_variable_prepare_jdm_set_config_with_jinja.j2`: the Jinja2 template looking at the variables to fill


# Ansible command to stop/delete the VM:
- `dynamic_variable_prepare_jdm_del_config.yml`: cleanup
 
