## Play the playbook:

```sh
#pre-requisit: prepare server from lxc-create and add ip address to hosts
ansible-playbook prepare_ansible_target.yml -i hosts -u ubuntu -k --ask-sudo-pass
#SSH password: ubuntu
#SUDO password[defaults to SSH password]: ubuntu

#PLAY [all] *************************************************************************************************************

#TASK [Update Packages] *************************************************************************************************
#changed: [10.0.3.73]

#TASK [Install Python 2] ************************************************************************************************
#changed: [10.0.3.73]

#TASK [Fancy way of doing authorized_keys] ******************************************************************************
#changed: [10.0.3.73]

#PLAY RECAP *************************************************************************************************************
#10.0.3.73                  : ok=3    changed=3    unreachable=0    failed=0

```
