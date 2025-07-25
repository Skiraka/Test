# Goal
- Set up DHCP on DC-1 to automatically assign IP addresses on the internal lab network `192.168.100.0/24`.

<img width="192" height="178" alt="image" src="https://github.com/user-attachments/assets/4f68fcda-05ba-479f-b683-d286cbc0a1d8" />

---

## Install DHCP Role
- From **Server Manager** on **DC-1**, added the **DHCP Server** role.
- Completed the post-install configuration wizard.
- Authorized the DHCP server with domain credentials.

---

## Create and Configure DHCP Scope
- Opened **DHCP Management Console** > **IPv4** > **New Scope**.
- Defined a scope for `192.168.100.1` to `192.168.100.30` with a subnet mask of `255.255.255.0`.

<img width="295" height="77" alt="image" src="https://github.com/user-attachments/assets/b30384e6-d4b4-49f3-b8db-dfa86d957db1" />

---

## Notes
- DC-1 is now acting as the **DHCP**, **DNS**, and **AD DS** server for the isolated lab network.
- Clients will now be able to:
  - Automatically receive a dynamic IP address from the DHCP pool.
  - Resolve DNS via DC-1.
  - Join the domain.
- DC-1 is hosting multiple services for simplicity in this lab. In production, these roles would typically be split across dedicated servers.


