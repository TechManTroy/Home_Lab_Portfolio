# Project B: Active Directory - Network & Server Configuration

**Objective:** Establish the core infrastructure for the `ad.lab` domain.

## 1. Network Design
* **Hypervisor:** VirtualBox 7.0
* **Network Mode:** NAT Network (Isolated)
* **Network Name:** `AD-Lab-Net`
* **Subnet:** `10.0.2.0/24`
* **DHCP:** Disabled (VirtualBox DHCP off; Server managed).

## 2. Server Specifications (DC01)
* **Hostname:** `WIN-IEU4MPTUGPG` (Role: Domain Controller)
* **OS:** Windows Server 2022 Standard Evaluation (Desktop Experience)
* **Resources:** 2 vCPUs, 4GB RAM, 50GB Storage

## 3. Configuration Steps
1.  **Static IP Assignment:**
    * IP: `10.0.2.10`
    * Subnet: `255.255.255.0`
    * Gateway: `10.0.2.1`
    * DNS: `127.0.0.1` (Self-referencing for AD).
2.  **Role Installation:** Installed Active Directory Domain Services (AD DS).
3.  **Promotion:** Promoted server to Domain Controller for forest `ad.lab`.
4.  **User Management:** Created Organizational Unit (OU) `Employees` and provisioned user `bbanner` (Bruce Banner).
