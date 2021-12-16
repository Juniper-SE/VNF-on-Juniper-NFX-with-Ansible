# Ansible commands to launch the VM:

`ansible-playbook -i ssh-hosts.ini generic_vm_image_add_on_nfx.yml`
`ansible-playbook -i junos-hosts.ini generic_vm_launch_action_on_nfx.yml`

(note: at the time of use, this was using NFX2 and then ssh commands were done to the linux system, then the ssh-hosts.ini, and then junos config was added to the JDM using junos-hosts.ini).


# Look on NFX for running VM:
`virsh list`
or 
`cli`
`show virtual-network-functions`


# Ansible command to stop/delete the VM:
`ansible-playbook -i junos-hosts.ini generic_vm_delete_action_on_nfx.yml`
 
