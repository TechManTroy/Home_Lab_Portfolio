# Project B: Active Directory - Network & Server Configuration

**Objective:** Establish the core infrastructure for the `ad.lab` domain.

## 1. Network Design
* **Hypervisor:** VirtualBox 7.0
* **Network Mode:** NAT Network (Isolated)
* **Network Name:** `AD-Lab-Net`
* **Subnet:** `10.0.2.0/24`
* **DHCP:** Disabled (VirtualBox DHCP off; Server managed).

<img width="771" height="876" alt="Screenshot 2026-01-16 133539" src="https://github.com/user-attachments/assets/d67bf732-1859-442d-b1b7-d9ad63a0877c" />



## 2. Server Specifications (DC01)
* **Hostname:** `WIN-IEU4MPTUGPG` (Role: Domain Controller)
* **OS:** Windows Server 2022 Standard Evaluation (Desktop Experience)
* **Resources:** 2 vCPUs, 4GB RAM, 50GB Storage
<img width="1052" height="554" alt="02-server-vm-name" src="https://github.com/user-attachments/assets/dbf44521-daa3-4b62-806e-2f3d987c8094" />
<img width="1054" height="545" alt="03-memory-cpu" src="https://github.com/user-attachments/assets/11a5aa87-febe-450a-b9e7-e7689056ebfc" />
<img width="1052" height="549" alt="04-storage" src="https://github.com/user-attachments/assets/8082806b-914d-4232-b890-cad95a140df7" />
<img width="775" height="509" alt="05-attached-network" src="https://github.com/user-attachments/assets/835d3dd9-5070-491f-ada0-8a707ba90c5c" />

## 3. Configuration Steps
1.  **Static IP Assignment:**
    * IP: `10.0.2.10`
    * Subnet: `255.255.255.0`
    * Gateway: `10.0.2.1`
    * DNS: `127.0.0.1` (Self-referencing for AD).
2.  **Role Installation:** Installed Active Directory Domain Services (AD DS).
3.  **Promotion:** Promoted server to Domain Controller for forest `ad.lab`.
4.  **User Management:** Created Organizational Unit (OU) `Employees` and provisioned user `bbanner` (Bruce Banner).
<img width="1031" height="849" alt="07-static-ip" src="https://github.com/user-attachments/assets/fc95c553-e8e8-4043-9832-4ed86d726865" />
<img width="1151" height="1021" alt="09-ping" src="https://github.com/user-attachments/assets/f2e67f6d-4fb6-40b0-b81c-997cfc61eab9" />

<img width="1025" height="852" alt="06-server-install" src="https://github.com/user-attachments/assets/4bcccc5a-3123-4516-8bb9-573f7031f7c7" />
<img width="1020" height="830" alt="08-adds" src="https://github.com/user-attachments/assets/90595224-5344-469a-9f9e-bc6df95ec4e8" />
<img width="743" height="554" alt="10-domain-name" src="https://github.com/user-attachments/assets/74cd2d66-9ba1-4790-83ec-f20f82790091" />
<img width="757" height="558" alt="11-controller-options" src="https://github.com/user-attachments/assets/7dd069a6-fcc2-4b6d-8073-bbf54781da76" />
<img width="1018" height="964" alt="12-ad-finish" src="https://github.com/user-attachments/assets/861a4a6d-79f9-40fc-906f-9431c0611d05" />
<img width="674" height="745" alt="13-creating-ou" src="https://github.com/user-attachments/assets/22c8de22-11d0-4a77-ae16-736013235c7a" />
<img width="451" height="379" alt="14-creating-new -user" src="https://github.com/user-attachments/assets/fcc5760c-77e6-4923-af97-6f70c496b551" />
<img width="435" height="377" alt="15-user-password" src="https://github.com/user-attachments/assets/5922a205-4b67-452e-8e3f-33130068e548" />

