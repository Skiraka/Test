# Goal 
- Create and set up the Domain, Windows Server Domain Controller
<img width="137" height="178" alt="image" src="https://github.com/user-attachments/assets/b1b84dcd-5c8a-4343-b8c5-59358606ab73" />


## Configuration

| Item               | Configuration                  |
|--------------------|--------------------------------|
| VM Name            | DC-1|
| OS                 | Windows Server 2022|
| Hostname           | DC-1                           |
| Domain Name        | domainname.com                 |
| IP Address         | 192.168.100.50                 |
| Subnet Mask        | 255.255.255.0                  |
| Default Gateway    | 192.168.142.2                  |
| DNS Server         | 127.0.0.1                      |



## Configuration Steps

### Create and prepare the VM
- Created the VM with hostname DC-1.
- Installed Windows Server 2022 from ISO.
- Set the Server hostname to DC-1.
- Configured static network settings:
  - IP Address: 192.168.100.50
  - Subnet Mask: 255.255.255.0
  - Default Gateway: None, internet access handled by other virtual NIC.
  - DNS Server: 127.0.0.1

### Install AD DS and DNS Roles
- Installed the Active Directory Domain Services and DNS Server roles.

### Promote Server to Domain Controller
- Promoted Server to Domain Controller, creating a new forest with the domain name 'domainname.com'.
- Rebooted server upon completion.

### Verification
- Logged in as domain administrator 'domainname\Administrator'
- Opened Active Directory Users and Computers to confirm domain structure.
- Ran ipconfig /all to confirm static IP and DNS settings.

### Domain OU set up
- Created custom Organizational Units (OU) to reflect a basic lab structure:
  - <img width="193" height="199" alt="image" src="https://github.com/user-attachments/assets/1e76b192-44d8-4fd6-b323-f87206fbf3b2" />



