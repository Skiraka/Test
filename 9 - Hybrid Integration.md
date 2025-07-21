# Goal
- Connect the on-prem Active Directory domain to the Microsoft 365 tenant using Azure AD Connect.

---

## Tenant 
- Logged into Microsoft 365 Admin Center and confirmed:
  - Tenant Name: HomeLab
  - Tenant ID: `06c7d7fd-c2dc-44d2-88cf-a8cf15007283`
  - Primary domain: `TestHomeLabx.onmicrosoft.com`
  - License: Microsoft Entra ID P1 (Trial)

---

## Install and Run Azure AD Connect
- On DC-1, downloaded Azure AD Connect and launched the installer.
- Entered Microsoft 365 Global Admin credentials.
- Selected the on-prem domain and continued through prompts.
- Selected valid OUs to be synced.
- Confirmed installation succeeded.

  <img width="457" height="133" alt="bcfaad1c-d562-4cc8-9cb2-e6649057987a" src="https://github.com/user-attachments/assets/ecfb9e75-bf92-43c9-9a32-e15f5911129d" />

---

## Post-Sync Validation
- Checked Entra ID and noted On-Premesis users, devices, and groups populating.
  
  <img width="740" height="118" alt="ff8a3244-e2c6-4109-9136-97605c7e7003" src="https://github.com/user-attachments/assets/5947fedb-b04d-46a6-9e37-174369caf701" />

- Confirmed user accounts can log in to Microsoft 365.
---

## Notes
- Azure AD Connect successfully established synchronization between the on-premises Domain Controller (`DC-1`) and Microsoft Entra ID.
- The environment is now ready for further hybrid cloud configuration and management.


