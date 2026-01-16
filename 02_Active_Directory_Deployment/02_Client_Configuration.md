# Project B: Active Directory - Client Integration

**Objective:** simulate an employee workstation and join it to the secure corporate domain.

## 1. Client Specifications (Client01)
* **Hostname:** `Client01`
* **OS:** Windows 11 Enterprise
* **Resources:** 2 vCPUs, 4GB RAM, 50GB storage

## 2. Configuration Steps
1.  **OS Installation:**
    * Windows 11 Enterprise
2.  **Network Configuration:**
    * IP: `10.0.2.100` (Static)
    * **Preferred DNS:** `10.0.2.10` (Crucial: Points to Domain Controller).
3.  **Domain Join:**
    * Joined `ad.lab` using Administrator credentials.
    * Restarted and verified login capability for user `bbanner`.
4.  **Security Validation:**
    * Confirmed "Force Password Change" policy triggered upon first login for `bbanner`.
