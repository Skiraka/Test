# Goal
- Set up FS-1 as the dedicated file server for department-based shared access (HR, Sales, IT, Public)

<img width="253" height="262" alt="image" src="https://github.com/user-attachments/assets/4872550a-64da-475b-afa6-d7afb667f715" />

---

## Configuration

| Item               | Configuration                  |
|--------------------|--------------------------------|
| VM Name            | FS-1                           |
| OS                 | Windows Server 2022            |
| Hostname           | FS-1                           |
| IP Address         | 192.168.100.60                 |
| Subnet Mask        | 255.255.255.0                  |
| DNS Server         | 192.168.100.50 (DC-1)          |
| Domain             | domainname.com                 |

---

## Create and Join VM to Domain
- Created new VM named `FS-1` using Windows Server 2022 ISO.
- Assigned static IP: `192.168.100.60`
- Set DNS to point to domain controller: `192.168.100.50`
- Renamed to `FS-1` and joined to domain `domainname.com`.
- Rebooted and logged in as domain admin to continue setup.

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









