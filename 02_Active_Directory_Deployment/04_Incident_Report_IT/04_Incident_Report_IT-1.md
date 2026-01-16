# Incident Report: IT-1 (Wallpaper Deployment Failure)

**Status:** Resolved
**Date:** January 16, 2026
**System:** Jira Service Management

## Issue Description
**Ticket IT-1:** "Service Request: Deploy Corporate Wallpaper"
Upon initial application of the 'Corporate Wallpaper' GPO, the client workstation (`Client01`) displayed a black screen instead of the intended image.

## Root Cause Analysis (RCA)
* **Diagnosis:** The Group Policy setting was correctly enabled, but the file path syntax was invalid.
* **Specific Error:** The policy pointed to the directory root (`.../CorpData`) instead of the specific executable file.
* **Hidden Factor:** Windows File Explorer was hiding file extensions, causing confusion about the exact filename.

## Resolution Steps
1.  Enabled "Show File Extensions" on the client to verify the file name was `wallpaper.jpg`.
2.  Modified the GPO setting on the Domain Controller.
    * **Old Path:** `\\WIN-IEU4MPTUGPG\CorpData` (Incorrect)
      <img width="1227" height="997" alt="004-gpo-config" src="https://github.com/user-attachments/assets/55e83b1c-9c52-4120-aa2e-f72e67ab639e" />

    * **New Path:** `\\WIN-IEU4MPTUGPG\CorpData\wallpaper.jpg` (Correct)
      <img width="858" height="898" alt="Screenshot 2026-01-16 110252" src="https://github.com/user-attachments/assets/d9b5da27-39cc-4de8-9bec-a8dc159e501c" />

3.  Ran `gpupdate /force` on the client.
4.  Signed out/Signed in to verify the fix.
<img width="564" height="258" alt="Screenshot 2026-01-16 105121" src="https://github.com/user-attachments/assets/2a5906d2-f236-4c83-9723-01bc5a1427ee" />

## Outcome
Service restored. Ticket IT-1 closed with full documentation in Jira.
<img width="832" height="1127" alt="Screenshot 2026-01-16 111119" src="https://github.com/user-attachments/assets/eb9227f9-1954-44d5-93cb-f2b80f38d9a6" />
