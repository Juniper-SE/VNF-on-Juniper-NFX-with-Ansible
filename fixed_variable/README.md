# These Ansible playbooks serve the same need as "static" but with few variable.


# Ansible commands to prepare the VM:
- `fixed_variable_new_vm_image.yml`: playbook to prepare the qcow2 image of the VM
- `fixed_variable_new_vm_config.yml`: playbook to prepare the config used for cloud-init of the VM
- `fixed_variable_prepare_jdm_set_config.yml`: playbook to add the VNF to NFX


# Ansible commands to launch the VM:
- `fixed_variable_launch_new_vm.yml`: playbook to launch the VM on NFX using the previous results


# Ansible command to stop/delete the VM:
- `fixed_variable_prepare_jdm_del_config.yml`: playbook to stop the VM
- `fixed_variable_stop_new_vm.yml`:  playbook to delete the VM config
- `fixed_variable_cleanup_all_files.yml`: cleanup the rest of the files
 

# OR LAUNCH THEM ALL WITH A SINGLE COMMAND:
`fixed_variable_launch_all_playbooks.yml`

