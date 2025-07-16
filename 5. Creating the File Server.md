# Goal
- Set up FS-1 as the dedicated file server for department-based shared access (HR, Sales, IT, Public)

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

## Configuration Steps

### Create and Join VM to Domain
- Created new VM named `FS-1` using Windows Server 2022 ISO.
- Assigned static IP: `192.168.100.60`
- Set DNS to point to domain controller: `192.168.100.50`
- Renamed to `FS-1` and joined to domain `domainname.com`.
- Rebooted and logged in as domain admin to continue setup.

---

### Create Department Shared Folders

| Share Name    | NTFS Path              | Purpose              |
|---------------|------------------------|----------------------|
| HR            | C:\Shares\HR           | HR Dept files        |
| Sales         | C:\Shares\Sales        | Sales Dept files     |
| IT            | C:\Shares\IT           | IT Admin files       |
| Public        | C:\Shares\Public       | Shared among all     |


