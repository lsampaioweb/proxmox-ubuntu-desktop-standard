# proxmox-ubuntu-desktop-standard
Project with Ansible scripts to create an Ubuntu Desktop template on Proxmox from a cloned virtual machine with the default packages and updates.

### Manual Usage:

1. Change to the ansible directory.
    ```bash
    cd ansible
    ```

1. Run the playbooks as needed:

    1. Proxmox VM:

        Install and setup application.
        ```bash
        ansible-playbook template.yml -e "hostname=ubuntu-24-04-desktop-standard"
        ```

        Setup VM settings on Proxmox.
        ```bash
        ansible-playbook kvm_setup.yml -e "node=edge-pve-01 vm_name=ubuntu-24-04-desktop-standard"
        ```

    1. Virtualbox VM:

        **Explanation of Flags:**
        - `-K` - Prompts for the **sudo password** to execute tasks as root.

        Install and setup application.
        ```bash
        ansible-playbook localhost.yml -K
        ```

#
### Created by:

1. Luciano Sampaio.
