# Goal
- Setting up DHCP on DC-1 to automatically assign IP addresses on the internal lab network 192.168.100.0/24
<img width="192" height="178" alt="image" src="https://github.com/user-attachments/assets/4f68fcda-05ba-479f-b683-d286cbc0a1d8" />

---

## Install DHCP Role
- From Server Manager on DC-1 added the DHCP Server role.
- Completed post-install configuration
- Authorized the DHCP server with domain credentials.

---

## Create and configure DHCP Scope
- Opened DHCP Management Console>IPv4>New Scope.
- Defined scope for 192.168.100.1 to 192.168.100.254 with the subnet mask 255.255.255.0.
- Set 192.168.100.50 as a reserved IP address for DC-1.
  - <img width="295" height="77" alt="image" src="https://github.com/user-attachments/assets/b30384e6-d4b4-49f3-b8db-dfa86d957db1" />

---

## Notes
- DC-1 is now acting as the DHCP, DNS, and AD DS server for the isolated lab network.
- Clients will now be able to:
    - Automatically receive an dynamic IP address from the DHCP pool
    - Resolve DNS via DC-1
    - Join the domain
* DC-1 is hosting multiple services for simplicity in this lab. In production, these roles would typically be split across dedicated servers.

