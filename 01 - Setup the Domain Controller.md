# Goal 
- Create and set up a Windows Server Domain Controller and configure a new domain.
<img width="137" height="178" alt="image" src="https://github.com/user-attachments/assets/b1b84dcd-5c8a-4343-b8c5-59358606ab73" />

---

## Create and Prepare the VM
- Created a VM with hostname `DC-1` and installed Windows Server 2022 from ISO.
- Configured static network settings:
  - IP Address: `192.168.100.50`
  - Subnet Mask: `255.255.255.0`
  - Default Gateway: None (internet access handled via another virtual NIC)
  - DNS Server: `127.0.0.1`
  
---

## Install AD DS and DNS Roles
- Installed the Active Directory Domain Services and DNS Server roles.

---

## Promote Server to Domain Controller
- Promoted the server to a Domain Controller, creating a new forest with the domain name `domainname.com`.
- Rebooted the server upon completion.

---

## Verification
- Logged in as domain administrator `domainname\Administrator`.
- Opened **Active Directory Users and Computers** to confirm domain structure.
- Ran `ipconfig /all` to confirm static IP and DNS settings.

--- 

## Domain OU setup
- Created custom Organizational Units (OU) to reflect a basic lab structure:

<img width="193" height="199" alt="image" src="https://github.com/user-attachments/assets/1e76b192-44d8-4fd6-b323-f87206fbf3b2" />

---

## Notes
- This domain controller will serve as the main identity and authentication source for the lab environment.

