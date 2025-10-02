# This folder contains different command line or manifest that could be usefull using Ansible.


1. List Ansible collections inside an Execution Environment
    ```
    podman run --rm -it <execution-environment-image> ansible-galaxy collection list
    ```

1. List Python packages inside the EE
    ```
    podman run --rm -it <execution-environment-image> pip list
    ```
1. List system packages (RPM, DNF, APT depending on base)
    For RHEL-based EE (like ee-supported-rhel9):
    ```
    podman run --rm -it <execution-environment-image> rpm -qa
   ```
1. Explore interactively. You can also shell into the EE and explore:
    ```
    podman run --rm -it <execution-environment-image> /bin/bash
    ```