# Ansible Network Automation

This project provides Ansible playbooks and roles to automate configurations for various network devices, including Cisco IOS, IOS-XE, ASA, NX-OS, Juniper, and F5 BIG-IP.

## Table of Contents

- [Requirements](#requirements)
- [Installation](#installation)
- [Project Structure](#project-structure)
- [Usage](#usage)
- [Roles](#roles)
- [Contributing](#contributing)

## Requirements

- Ansible (version 2.10 or higher)
- Python 3.6 or higher
- Required Ansible collections:
  - `cisco.ios`
  - `cisco.nxos`
  - `junipernetworks.juniper`
  - `f5networks.f5_modules`

## Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/yourusername/your-repo-name.git
   cd your-repo-name
2. **Install required Ansible collections:**
   ```bash
    ansible-galaxy collection install -r requirements.yml
3. **Verify the installation:**
   ```bash
    ansible-galaxy collection list  
## Project Structure
```css
ansible/
├── inventory
├── playbook.yml
└── roles/
    ├── ios/
    │   └── tasks/
    │       └── main.yml
    ├── iosxe/
    │   └── tasks/
    │       └── main.yml
    ├── asa/
    │   └── tasks/
    │       └── main.yml
    ├── nxos/
    │   └── tasks/
    │       └── main.yml
    ├── juniper/
    │   └── tasks/
    │       └── main.yml
    └── bigip/
        └── tasks/
            └── main.yml
```

## Usage
1.Edit the inventory file to specify the target devices and their connection details.

2.Run the playbook:
  ```bash
  ansible-playbook -i inventory playbook.yml 
  ```

## Roles
**ios**
- Manages Cisco IOS devices.
- Example task: Configure hostname.

**iosxe**
- Manages Cisco IOS-XE devices.
- Example task: Configure interfaces.

**asa**
- Manages Cisco ASA devices.
- Example task: Configure firewall settings.

**nxos**
* Manages Cisco NX-OS devices.
* Example task: Configure VLANs.

**juniper**
* Manages Juniper devices.
* Example task: Configure hostnames and interfaces.

**bigip**
* Manages F5 BIG-IP devices.
* Example task: Configure virtual servers.

## Contributing
Contributions are welcome! Please open an issue or submit a pull request for any enhancements or fixes.

