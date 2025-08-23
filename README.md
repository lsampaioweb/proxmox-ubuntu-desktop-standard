# proxmox-ubuntu-desktop-standard
Project with Packer and Ansible scripts to create an Ubuntu Desktop template on Proxmox from a cloned virtual machine with the default packages and updates.

### Overview

This project can be used in two main scenarios:

1. **Proxmox VM (Recommended)**:

    If your VM is created via **Packer** (and optionally Terraform), most Ansible playbooks will be executed automatically as part of the provisioning process. You do not need to run them manually.

1. **Manual Setup (VirtualBox or Custom VM)**:

    If you created your VM manually (e.g., in VirtualBox), you need to run the Ansible playbooks yourself.

### Installation and Setup

### 1. Prepare the Environment

**For both VirtualBox and Proxmox VMs:**

Open a terminal and execute the following steps:

1. Update package lists and upgrade installed packages
    ```bash
    sudo apt update && sudo apt upgrade -y
    ```

1. Clone the repository and initialize submodules
    ```bash
    git clone --recurse-submodules https://github.com/lsampaioweb/proxmox-ubuntu-desktop-standard.git && cd proxmox-ubuntu-desktop-standard
    ```

1. If the repository is already cloned, update submodules
    ```bash
    git submodule update --init --recursive
    ```

### 2. Deploy the Template

Choose one of the following methods:

- **[Packer](packer/README.md "Packer")** (Recommended for Proxmox) – Automated deployment if your Proxmox cluster is operational.
- **[Ansible](ansible/README.md "Ansible")** – Manual configuration for both VirtualBox VMs and Proxmox VMs where Packer isn't suitable.

#
### Links:

[Links](links.md "Links")

### License:

[MIT](LICENSE "MIT License")

### Created by:

1. Luciano Sampaio.
