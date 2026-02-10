# Ansible STIGs

This repository contains Ansible roles and sites for applying STIG fixes to different Operating Systems.

- rhel8STIG
    - Downloaded and extrated from DoD Cyber Exchange. The official zip file that contains this role can be found at https://dl.dod.cyber.mil/wp-content/uploads/stigs/zip/U_RHEL_8_V2R6_STIG_Ansible.zip.
- rhel9STIG
    - Downloaded and extrated from DoD Cyber Exchange. The official zip file that contains this role can be found at https://dl.dod.cyber.mil/wp-content/uploads/stigs/zip/U_RHEL_9_V2R7_STIG_Ansible.zip.
- ubuntu2004STIG
    - Downloaded and extrated from DoD Cyber Exchange. The official zip file that contains this role can be found at https://dl.dod.cyber.mil/wp-content/uploads/stigs/zip/U_CAN_Ubuntu_20-04_LTS_V1R11_STIG_Ansible.zip.
- ubuntu2204STIG
    - Downloaded and extrated from DoD Cyber Exchange. The official zip file that contains this role can be found at https://dl.dod.cyber.mil/wp-content/uploads/stigs/zip/U_CAN_Ubuntu_22-04_LTS_V2R7_STIG_Ansible.zip.
- ubuntu2204STIG
    - Downloaded and extrated from DoD Cyber Exchange. The official zip file that contains this role can be found at https://dl.dod.cyber.mil/wp-content/uploads/stigs/zip/U_CAN_Ubuntu_24-04_LTS_V1R4_STIG_Ansible.zip.
- win2022STIG
    - Downloaded and extrated from DoD Cyber Exchange. The official zip file that contains this role can be found at https://dl.dod.cyber.mil/wp-content/uploads/stigs/zip/U_MS_Windows_Server_2022_V1R1_STIG_Ansible.zip.

**NOTICE:** These roles will be updated as soon as possible when new version are uploaded, however sometimes that may be outdated compared to what is currently on DoD Cyber Exchange.

## How To Use

Both site files target remote systems. Follow below for how to run the sites.

1. Clone repository

    ```bash
    git clone https://github.com/shanedell/ansible-stigs.git
    ```
2. Run ansible-playbook command from inside of `ansible-stigs` folder.

    - Using inventory file
        
        ```bash
        ansible-playbook -i <inventory-file-path> <site-file>
        ```

        - Replace `<inventory-file>` with the path to the desired inventory file.
        - Replace `<site-file>` with either `ubuntu2004.site.yml`, `ubuntu2204.site.yml` or `win2022.site.yml`.

    - Using IP address
        
        ```bash
        ansible-playbook -i <ip-address>, <site-file>
        ```

        - Replace `<ip-address>` with the desired IP address.
        - Replace `<site-file>` with either `ubuntu2004.site.yml`, `ubuntu2204.site.yml` or `win2022.site.yml`.

**NOTICE:** When using IP address, make sure that after the IP address a comma (`,`) is present, otherwise the command will fail or the playbook will not get ran properly.
