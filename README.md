# Wazuh 4.5.x Installation on Ubuntu 22.04

Installation of Wazuh 4.5.x, a free and open-source security platform for unified XDR and SIEM capabilities, onto a single Ubuntu 22.04 server. This facilitates rapid deployment and allows you to experiment with Wazuh agents on your test systems.


## Prerequisites

- A freshly deployed Ubuntu 22.04 server with internet access
- Root or sudo privileges



## Plan is to set up Wazuh using a single server architecture, as illustrated in the following diagram.

![App Screenshot](https://github.com/Shwet-Kamal-Singh/wazuh/blob/main/Wazuh%20-all-in-one-deployment.png)


### Installation Steps

#### Install Dependencies
```bash
  sudo apt update && sudo apt install curl apt-transport-https unzip wget libcap2-bin software-properties-common lsb-release gnupg2
```

#### Download and Run Wazuh Installation Script

```bash
  curl -sO https://packages.wazuh.com/4.5/wazuh-install.sh && chmod 744 wazuh-install.sh && bash ./wazuh-install.sh -a
```
The -a flag indicates an all-in-one installation, deploying Wazuh's indexer, server, and dashboard on the same server.




#### Post-Installation

- Accessing the Wazuh dashboard: The URL, username, and password will be displayed on the terminal.
- Adding Wazuh agents: The Wazuh dashboard will provide commands to add agents to your test systems.

#### Additional Notes

- Refer to the official Wazuh documentation (https://documentation.wazuh.com/current/installation-guide/index.html) for more detailed configuration and customization options.
- Consider security best practices when setting passwords and access controls for your Wazuh deployment.
