# Goal
- Set up FS-1 as the dedicated file server for department-based shared access (HR, Sales, IT, Public)

  <img width="253" height="262" alt="image" src="https://github.com/user-attachments/assets/4872550a-64da-475b-afa6-d7afb667f715" />

---

## Create and Join VM to Domain
- Deployed a new VM named `FS-1` using the Windows Server 2022 ISO.
- Configured a static IP: `192.168.100.60`
- Set the preferred DNS to the domain controller: `192.168.100.50`
- Renamed the server to `FS-1` and joined it to the domain `domainname.com`
- Rebooted and signed in as a domain administrator to continue configuration.

---

## Create Department Shared Folders
- Created directories to be used by each department.
<img width="78" height="146" alt="image" src="https://github.com/user-attachments/assets/87fc6485-7481-4e40-bc87-5762b7b3221b" />

---

## Share and Set Permissions
- HR_ReadOnly = Read on HR
- HR_FullAccess = Modify on HR
- Similar for Sales & IT groups
- Shared each folder via File Explorer

---

## Test Access from Clients
- Logged in as different users  on lab PCs
- Verified:
  - Correct network drive access
  - Read-only vs full access applied properly
  - Public share accessible by all users









