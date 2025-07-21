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
- Confirmed installation succeeded.
- Checked Entra ID and noted On-Premesis users, devices, and groups populating.
<img width="740" height="118" alt="ff8a3244-e2c6-4109-9136-97605c7e7003" src="https://github.com/user-attachments/assets/5947fedb-b04d-46a6-9e37-174369caf701" />

---

## Post-Sync Validation
- Opened Microsoft Entra Admin Center.
- Confirmed sync service status: **Healthy**
- Users from on-prem AD began appearing in the cloud.
- Verified user source shows as **Windows Server AD**.
- Confirmed new users created in AD sync to M365 after a delta sync.

---

## Notes
- No custom domain added — using `*.onmicrosoft.com`.
- No Hybrid Join or Intune settings enabled (planned later).
- Azure AD Connect installed only on DC-1 (single forest/domain).

---

## Summary

Successfully connected on-prem Active Directory to Microsoft 365 tenant using Azure AD Connect. Sync is operational and new users from AD are reflected in Entra ID.
