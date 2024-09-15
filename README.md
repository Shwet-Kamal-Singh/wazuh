# Wazuh 4.5.x Installation on Ubuntu 22.04

Streamlined installation script for Wazuh 4.5.x on Ubuntu 22.04. Deploy this free, open-source XDR and SIEM platform on a single server for rapid testing and experimentation. Ideal for security professionals and enthusiasts. Features one-click, all-in-one installation with detailed guidance.

## Table of Contents

- [Prerequisites](#prerequisites)
- [Architecture](#architecture)
- [Installation Steps](#installation-steps)
  - [Install Dependencies](#install-dependencies)
  - [Download and Run Wazuh Installation Script](#download-and-run-wazuh-installation-script)
- [Post-Installation](#post-installation)
- [Additional Notes](#additional-notes)

## Prerequisites

- A freshly deployed Ubuntu 22.04 server with internet access
- Root or sudo privileges

## Architecture

We'll set up Wazuh using a single server architecture, as illustrated in the following diagram:

![Wazuh All-in-One Deployment](https://github.com/Shwet-Kamal-Singh/wazuh/blob/main/Wazuh%20-all-in-one-deployment.png)

## Installation Steps

#### Install Dependencies
```bash
  sudo apt update && sudo apt install curl apt-transport-https unzip wget libcap2-bin software-properties-common lsb-release gnupg2
```

#### Download and Run Wazuh Installation Script

```bash
  curl -sO https://packages.wazuh.com/4.5/wazuh-install.sh && chmod 744 wazuh-install.sh && bash ./wazuh-install.sh -a
```
The -a flag indicates an all-in-one installation, deploying Wazuh's indexer, server, and dashboard on the same server.

## Post-Installation

After the installation is complete:

- **Accessing the Wazuh dashboard**: The URL, username, and password will be displayed on the terminal. Make sure to save this information securely.
- **Adding Wazuh agents**: The Wazuh dashboard will provide commands to add agents to your test systems. Follow these instructions to connect your devices to Wazuh.

## Additional Notes

- For more detailed configuration and customization options, refer to the [official Wazuh documentation](https://documentation.wazuh.com/current/installation-guide/index.html).
- It's crucial to follow security best practices when setting passwords and configuring access controls for your Wazuh deployment.
- Regularly update your Wazuh installation to ensure you have the latest security features and bug fixes.
