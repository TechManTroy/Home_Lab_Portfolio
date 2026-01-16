# Project B: Active Directory - Client Integration

**Objective:** simulate an employee workstation and join it to the secure corporate domain.

## 1. Client Specifications (Client01)
* **Hostname:** `Client01`
* **OS:** Windows 11 Enterprise
* **Resources:** 2 vCPUs, 4GB RAM, 50GB storage
<img width="780" height="897" alt="17-client" src="https://github.com/user-attachments/assets/5c35e888-3892-41f3-a7a4-68f9168c0915" />

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
<img width="1032" height="863" alt="18-install-finish" src="https://github.com/user-attachments/assets/3cf1c642-4f60-4f1d-ab39-34b564e425a7" />
<img width="1019" height="847" alt="19-client-ip" src="https://github.com/user-attachments/assets/772f35df-9a09-4fb7-be88-d361d899bfe9" />
<img width="1022" height="840" alt="20-client-ping" src="https://github.com/user-attachments/assets/2178ca66-94e6-415e-bcb5-47dbe708cb31" />
<img width="896" height="361" alt="21-ns-lookup" src="https://github.com/user-attachments/assets/101f2b86-6fc8-484a-824a-987fc3cd161c" />
<img width="1082" height="803" alt="22-ad-logon" src="https://github.com/user-attachments/assets/530fd4df-d1a6-4449-9954-8c5d5f27a244" />
<img width="722" height="630" alt="23-ad-logon-finish" src="https://github.com/user-attachments/assets/b4639d34-a3d3-450d-a921-7b9db10f5d9e" />
<img width="2165" height="800" alt="24-final" src="https://github.com/user-attachments/assets/301a36e4-24cb-4a20-b085-66eb4b39eea7" />
