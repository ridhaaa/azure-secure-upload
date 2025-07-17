# 🐧 Linux VM Deployment – Azure Secure Upload Project

This document covers the steps to deploy a secure Linux VM on Azure using the Portal and configure secure SSH access for later monitoring and Terraform use.

---

## 🧱 1. Resource Group

- **Name**: `secure-upload-rg`
- Created in **Central India** 

---

## 💻 2. Virtual Machine Configuration

| Property             | Value                    |
|----------------------|--------------------------|
| **VM Name**          | `secure-linux-vm`        |
| **Image**            | Ubuntu Server 24.04 LTS  |
| **Region**           | Central India            |
| **Size**             | Standard B1s             |
| **Auth**             | SSH Public Key (Ed25519) |
| **Username**         | `reedo`                  |
| **Key Name**         | `reedokey.pem`           |
| **Public IP**        | Assigned                 |

---

## 🌐 3. Network Configuration

| Component   | Name                |
|-------------|---------------------|
| VNet        | `secure-vnet`       |
| Subnet      | `web-subnet`        |
| NSG         | `secure-nsg`        |
| NSG Rule    | `Allow-SSH-MyIP`    |
| Source      | My Public IP (`x.x.x.x`) |
| Port        | TCP 22              |
| Priority    | 100                 |
| Action      | Allow               |

- NSG is associated with the `web-subnet`
- Inbound rule only allows SSH (port 22) from a **specific IP**
- Ensures the VM is **not open to the public**

![NSG Rule](../screenshots/nsg-ssh-rule.png)


---
## 🔐 SSH Key & Access

- SSH key generated locally in Ed25519 format (`reedokey.pem`)
- Key is stored securely on the local machine
- SSH command used:

```bash
ssh -i "path/to/reedokey.pem" reedo@<your-vm-public-ip>
```

Successfully logged into the VM:
![SSH Access](../screenshots/ssh-access.png)



