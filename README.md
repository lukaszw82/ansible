# Ansible Role: Install .NET SDK 10

This repository contains an Ansible playbook and role to install the .NET SDK 10 on Linux Mint (or Ubuntu-based distributions).

## Prerequisites

You need `ansible` installed on your machine to run this playbook.

```bash
sudo apt update
sudo apt install -y ansible
```

## Setup & Usage

1.  **Clone the repository** (if you haven't already):
    ```bash
    git clone https://github.com/lukaszw82/ansible.git
    cd ansible
    ```

2.  **Run the playbook**:
    This command runs the installation on your local machine (`localhost`) as defined in the `inventory` file. You will be prompted for your sudo password as the installation requires root privileges.
    
    ```bash
    ansible-playbook -i inventory install_dotnet.yml --ask-become-pass
    ```

## Files Overview

-   `install_dotnet.yml`: The main playbook entry point.
-   `inventory`: Hosts file defining the target (localhost).
-   `roles/dotnet_sdk/`: Contains the tasks and variables for the installation role.

## Verification

After the playbook finishes successfully, verify the installation by checking the dotnet version:

```bash
dotnet --version
```
