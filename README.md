# Exercise1 :  
### Provision 2 virtual machines in azure that can communicate with each other using terraform/ansible/arm template.  
### Output log below  
gopalakrishnan@Azure:~/clouddrive$ ansible-playbook two-vm-creation-file.yml
[WARNING]: No inventory was parsed, only implicit localhost is available
[WARNING]: provided hosts list is empty, only localhost is available. Note that the implicit localhost does not match 'all'

PLAY [localhost] *********************************************************************************************************************************************************
TASK [Gathering Facts] ***************************************************************************************************************************************************ok: [localhost]

TASK [Create resource group] *********************************************************************************************************************************************ok: [localhost]

TASK [debug] *************************************************************************************************************************************************************ok: [localhost] => {
    "rg": {
        "changed": false,
        "contains_resources": true,
        "failed": false,
        "state": {
            "id": "/subscriptions/45a9efd2-11e0-47b0-8303-b27e7fb50abd/resourceGroups/my-rg",
            "location": "eastus",
            "name": "my-rg",
            "provisioning_state": "Succeeded",
            "tags": {}
        }
    }
}

TASK [create virtual network] ********************************************************************************************************************************************ok: [localhost]

TASK [add subnet in vnet] ************************************************************************************************************************************************ok: [localhost]

TASK [Creating public IP address - 1] ************************************************************************************************************************************ok: [localhost]

TASK [Creating public IP address - 2] ************************************************************************************************************************************ok: [localhost]

TASK [Create a network security group] ***********************************************************************************************************************************ok: [localhost]

TASK [Create virtual network interface card - 1] *************************************************************************************************************************[DEPRECATION WARNING]: Setting ip_configuration flatten is deprecated and will be removed. Using ip_configurations list to define the ip configuration. This feature will
 be removed in version [2, 9]. Deprecation warnings can be disabled by setting deprecation_warnings=False in ansible.cfg.
ok: [localhost]

TASK [Create virtual network interface card - 2] *************************************************************************************************************************ok: [localhost]

TASK [Creating VM - 1] ***************************************************************************************************************************************************[WARNING]: Module did not set no_log for ssh_password_enabled
ok: [localhost]

TASK [Creating VM - 2] ***************************************************************************************************************************************************ok: [localhost]

PLAY RECAP ***************************************************************************************************************************************************************localhost                  : ok=12   changed=0    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0
