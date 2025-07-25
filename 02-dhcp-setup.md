# Goal
- Set up DHCP on DC-1 to automatically assign IP addresses on the internal lab network.

<img width="192" height="178" alt="image" src="https://github.com/user-attachments/assets/4f68fcda-05ba-479f-b683-d286cbc0a1d8" />

---

## Install DHCP Role
- From **Server Manager** on **DC-1**, added the **DHCP Server** role.
- Completed the post-install configuration wizard.
- Authorized the DHCP server with domain credentials.

---

## Create and Configure DHCP Scope
- Opened **DHCP Management Console** > **IPv4** > **New Scope**.
- Defined a scope for `192.168.100.2` to `192.168.100.30` with a subnet mask of `255.255.255.0`.

<img width="464" height="51" alt="20d7cdbb-57aa-4205-b3b3-329eab1717bc" src="https://github.com/user-attachments/assets/e770ceed-d4f6-4f98-9bc5-b2bcd1e91912" />

---

## Notes
- DC-1 is now acting as the **DHCP**, **DNS**, and **AD DS** server for the isolated lab network.
- Clients will now be able to:
  - Automatically receive a dynamic IP address from the DHCP pool.
  - Resolve DNS via DC-1.
  - Join the domain.
- DC-1 is hosting multiple services for simplicity in this lab. In production, these roles would typically be split across dedicated servers.


