# Project B: Group Policy Automation

**Objective:** Automate the deployment of a standardized desktop background to all employees using Group Policy Objects (GPO).
<img width="1079" height="1208" alt="001-ticket" src="https://github.com/user-attachments/assets/ba3e990f-f0df-4440-9a6c-d5e340c344f9" />


## 1. Resources Created
* **File Share:** `C:\CorpData` on Server (`WIN-IEU4MPTUGPG`).
* **Asset:** `wallpaper.jpg` created via MS Paint.
* **Permissions:** `Everyone` set to **Read** (Share & NTFS Security).
<img width="1006" height="842" alt="002-file- sharing" src="https://github.com/user-attachments/assets/6956a8cf-4c7c-428f-94a5-0f3b55bae077" />



## 2. Policy Configuration
* **GPO Name:** `Corporate Wallpaper`
* **Linked To:** `Employees` OU
* **Path:** User Configuration > Administrative Templates > Desktop > Desktop Wallpaper.
* **Setting:** Enabled.
* **Target Path (UNC):** `\\WIN-IEU4MPTUGPG\CorpData\wallpaper.jpg`
<img width="1045" height="888" alt="005-gpo-link" src="https://github.com/user-attachments/assets/757b2fdc-1758-4e69-9bfd-7e4ebacad000" />


<img width="858" height="898" alt="Screenshot 2026-01-16 110252" src="https://github.com/user-attachments/assets/cf9088b3-3507-4db1-8cf8-e7552e248be7" />


## 3. Deployment Verification
* Executed `gpupdate /force` on Client01.
* Verified desktop background changed automatically for user `bbanner`.
<img width="564" height="258" alt="Screenshot 2026-01-16 105121" src="https://github.com/user-attachments/assets/cccc4a75-a35e-4684-916b-bf491b171cad" />
<img width="1016" height="846" alt="Screenshot 2026-01-16 110349" src="https://github.com/user-attachments/assets/0bc08ee9-b92d-434e-8573-24d2e65a70f6" />
