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
- Shared each folder via File Explorer → Advanced Sharing
- Configured **NTFS Permissions** as follows:

| Folder | Group Name         | NTFS Permissions |
|--------|--------------------|------------------|
| HR     | HR_ReadOnly        | Read             |
| HR     | HR_FullAccess      | Modify           |
| Sales  | Sales_ReadOnly     | Read             |
| Sales  | Sales_FullAccess   | Modify           |
| IT     | IT_ReadOnly        | Read             |
| IT     | IT_FullAccess      | Modify           |
| Public | Domain Users       | Modify           |

---

## Test Access from Clients
- Logged into test lab PCs as users from HR, Sales, and IT groups.
- Accessed shares via `\\FS-1\HR`.
- Verified the following:
  - Users with ReadOnly groups could access but not modify files.
  - Users with FullAccess groups could create, edit, and delete files.
  - The `Public` share was accessible and writable by all authenticated users.










