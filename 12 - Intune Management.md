# Goal
- Manage devices enrolled in Intune by configuring Compliance Policies, Configuration Profiles, and deploying Applications.

---

## Create Compliance Policy
- Created a new policy via `Intune > Devices > Compliance`
- Named policy `Require Firewall Enabled` with the setting `Required` for Firewall.
- Assigned Policy to all devices.
  
  <img width="809" height="64" alt="image" src="https://github.com/user-attachments/assets/41305bac-eebf-4631-9837-90d2fc2bc566" />

## Test Compliance Policy
- To test the policy:
  - Manually turned off the Firewall on `PC-2`.
- Forced Intune Sync by:
  - Intune Admin Center > Devices > PC-2 > Sync
  - On `PC-2` Synced device via `Settings > Accounts > Access Work or School > Info > Sync`.
- Checked Compliance Report for the policy and confirmed PC-2 was marked noncompliant.
  
    <img width="746" height="96" alt="image" src="https://github.com/user-attachments/assets/b8045de8-fcaa-4746-bac6-d3a59c31c3fd" />

---

## Create Configuration Profile
- Created new Configuration Profile via `Intune > Devices > Configuration'
- Named Configuration `Enforce Firewall On ` requiring Firewall `Enabled` on:
  
  <img width="298" height="81" alt="image" src="https://github.com/user-attachments/assets/d2df3ef7-f253-475b-8c7a-105195e9dece" />

  
    

