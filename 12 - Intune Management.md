# Goal
- Manage devices enrolled in Intune by configuring Compliance Policies, Configuration Profiles, and deploying Applications.

---

## Create Compliance Policy
- Created a new policy via `Intune > Devices > Compliance`
- Named policy `Require Firewall Enabled` with the setting `Required` for Firewall.
- Assigned Policy to all devices.
  
  <img width="809" height="64" alt="image" src="https://github.com/user-attachments/assets/41305bac-eebf-4631-9837-90d2fc2bc566" />

## Test Compliance Policy
- Manually turned off the Firewall on `PC-2`.
- Forced Intune Sync by:
  - Intune Admin Center > Devices > PC-2 > Sync
  - On `PC-2` Synced device via `Settings > Accounts > Access Work or School > Info > Sync`.
- Checked Compliance Report for the policy and confirmed PC-2 was marked noncompliant.
  
    <img width="746" height="96" alt="image" src="https://github.com/user-attachments/assets/b8045de8-fcaa-4746-bac6-d3a59c31c3fd" />

---

## Create Configuration Profile
- Created new Configuration Profile via `Intune > Devices > Configuration'
- Named Configuration `Enforce Firewall On ` requiring Firewall `Enabled`.
- Assigned configuration to all devices.
  
  <img width="298" height="81" alt="image" src="https://github.com/user-attachments/assets/d2df3ef7-f253-475b-8c7a-105195e9dece" />

## Test Configuration Profile
- `PC-2` still has their Firewall off from the compliance policy test.
- Triggered forced syncing.
- Confirmed configuration profile applied with `PC-2` having all Firewalls on.
  
  <img width="564" height="64" alt="image" src="https://github.com/user-attachments/assets/cc2b2ed9-95b3-4aa2-bdad-ee795bf57775" />

- Compliance Policy report now showing `PC-2` to be in compliance.

  <img width="1056" height="59" alt="image" src="https://github.com/user-attachments/assets/0ea26ae4-3702-4dec-849a-5a2a0a2cbc88" />

---

## Deploying Applications
- Created new Application via Intune > Devices > Apps
  - Assigned app to all Devices
  - Selected apps: Word, Excel, PowerPoint, Outlook, OneDrive, Teams

    <img width="772" height="31" alt="image" src="https://github.com/user-attachments/assets/b0194fa6-4768-47ac-8362-505f21c6f172" />

- Monitored the Application installaion process through the Device Install Status.
  - Initially displayed as Pending Install.
  - Force Synced the device with Intune.
  - Eventually displayed with a Status of `Installed`.
    
      <img width="528" height="56" alt="image" src="https://github.com/user-attachments/assets/a0fcc6b4-ecc9-46b4-8e7f-243b14a62074" />

- Confirmed the Applications pushed to the device via Settings > Apps
  <img width="440" height="55" alt="image" src="https://github.com/user-attachments/assets/ee0c2eb3-aa45-4831-848e-ea5b55f39877" />





  
    

