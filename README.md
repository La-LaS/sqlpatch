# SQLPatch Automation for Windows Systems

[![Ansible](https://img.shields.io/badge/Ansible-2.10+-green.svg)](https://www.ansible.com)
[![Compatibility](https://img.shields.io/badge/Compatible%20with-AAP%2FAWX-blue.svg)](https://www.redhat.com/en/technologies/management/ansible-automation-platform)

A lightweight Ansible-based automation for deploying SQL Server patches across **Windows environments**, including AlwaysOn Availability Groups.  
**No custom modules required** – uses native Ansible capabilities.

---

## Features
- 🛠️ **Automated SQL Patching**: Deploy updates to standalone SQL servers and AlwaysOn clusters.
- 🔄 **Cluster-Aware**: Automatically detects and patches **all nodes** in an AlwaysOn cluster.
- ☁️ **Cloud-Ready**: Compatible with Ansible Automation Platform (AAP) and AWX.
- 🔒 **Secure**: Uses WinRM over HTTPS (port 5986) with NTLM authentication.

---

## Prerequisites
1. **WinRM Configuration**  
   Ensure WinRM is properly configured on all target Windows systems.
2. **Ansible Setup**  
   - Ansible 2.10+ (tested with AAP/AWX)
   - `ansible.windows` collection installed:
     ```bash
     ansible-galaxy collection install ansible.windows
     ```

---

## Configuration

### Inventory Setup
```
      ansible_host: 192.168.1.20
      ansible_connection: winrm
      ansible_winrm_transport: ntlm
      ansible_port: '5986'
```


      
