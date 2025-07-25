# Goal
- Set up client virtual machines to join the domain.

  <img width="237" height="271" alt="image" src="https://github.com/user-attachments/assets/74448696-cbeb-4358-8e03-cba95c24cda9" />

## Prepare Client VMs
- Created two Windows 10 VMs named `PC-1` and `PC-2`.
- Configured each VM to use the internal lab virtual network (`192.168.100.0/24`), so they get IP addresses from DHCP on DC-1.
- Verified IP assignment via `ipconfig /all`.
- Confirmed DNS server IP points to DC-1 (`192.168.100.50`).

---

## Join PCs to Domain
- On each PC, logged in locally as `Administrator`.
- Manually joined each PC to the domain.
- When prompted, entered domain administrator credentials.
- Rebooted PCs after successful domain join.

---

## Verify Domain Join
- Logged in to each PC using domain credentials:
  - Username: `domainname\Administrator`
- Opened Command Prompt and ran the `whoami` command to verify logged-in user is domain user.
- Opened System Properties to confirm domain membership.
  
  <img width="592" height="243" alt="image" src="https://github.com/user-attachments/assets/e0d80206-2719-47d3-b140-9f70b6a5afa1" />
  
- Confirmed each PC was added to Active Directory Users and Computers.
- Moved each computer to the `Computers` OU for GPO assignment in later labs.

 ---
 
## Create User Accounts in AD DS
- On DC-1, logged in as domain administrator.
- Opened Active Directory Users and Computers, navigated to the `Users` OU, and created new users:

  <img width="220" height="100" alt="image" src="https://github.com/user-attachments/assets/0b9b817b-7dd0-405b-8724-f1c83991f78d" />

- Set passwords and configured `User must change password at next logon`.
- Filled out each user’s personal information, especially the Department attribute for later use with Dynamic Groups in Microsoft 365.

  ---
  
## Test User Login
- On PC-1 and PC-2:
  - Logged out domain admin.
  - Logged in as newly created users.
  - Confirmed successful login to domain profiles.

 ---
 
## Verified Central Management
- From Active Directory Users and Computers:
  - Verified ability to reset user passwords.
  - Verified ability to disable and enable user accounts.

---

## Installing Remote Server Administration Tools (RSAT)
- To manage the domain remotely, `PC-1` is configured as an admin workstation with RSAT tools installed.
- Installed the RSAT Active Directory optional features from Windows Settings.

  <img width="416" height="67" alt="image" src="https://github.com/user-attachments/assets/67f7097b-55b2-4580-9ff0-36c02b727f67" />

- Confirmed RSAT installation and verified `PC-1` could access Active Directory Domain Services remotely.

  <img width="255" height="209" alt="image" src="https://github.com/user-attachments/assets/28215ea8-9e72-4bac-bb27-5c0f1aff9e51" />




