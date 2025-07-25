# Goal
- Manage devices enrolled in Intune by configuring Compliance Policies, Configuration Profiles, and deploying Applications.

---

## Create Compliance Policy
- Created a new policy via `Intune > Devices > Compliance`.
- Named policy `Require Firewall Enabled` with the setting `Required` for Firewall.
- Assigned the policy to all devices.
  
  <img width="809" height="64" alt="image" src="https://github.com/user-attachments/assets/41305bac-eebf-4631-9837-90d2fc2bc566" />

## Test Compliance Policy
- Manually turned off the firewall on `PC-2`.
- Forced Intune sync by:
  - Using `Intune Admin Center > Devices > PC-2 > Sync`
  - On `PC-2`, navigating to `Settings > Accounts > Access Work or School > Info > Sync`
- Verified compliance report marked `PC-2` as **Noncompliant**.
  
    <img width="746" height="96" alt="image" src="https://github.com/user-attachments/assets/b8045de8-fcaa-4746-bac6-d3a59c31c3fd" />

---

## Create Configuration Profile
- Created a new configuration profile via `Intune > Devices > Configuration`.
- Named the profile `Enforce Firewall On`, with settings requiring the firewall to be `Enabled`.
- Assigned the configuration profile to all devices.
  
  <img width="298" height="81" alt="image" src="https://github.com/user-attachments/assets/d2df3ef7-f253-475b-8c7a-105195e9dece" />

## Test Configuration Profile
- `PC-2` still had its firewall turned off from the compliance policy test.
- Triggered a forced sync on the device.
- Confirmed the configuration profile was applied successfully:
  - All firewall profiles (Domain, Private, Public) were enabled.
  
  <img width="564" height="64" alt="image" src="https://github.com/user-attachments/assets/cc2b2ed9-95b3-4aa2-bdad-ee795bf57775" />

- Compliance policy report now shows `PC-2` as **Compliant**.

  <img width="1056" height="59" alt="image" src="https://github.com/user-attachments/assets/0ea26ae4-3702-4dec-849a-5a2a0a2cbc88" />

---

## Deploying Applications
- Created a new application deployment via `Intune > Devices > Apps`.
  - Assigned the app deployment to **All Devices**.
  - Selected apps: Word, Excel, PowerPoint, Outlook, OneDrive, Teams.

    <img width="772" height="31" alt="image" src="https://github.com/user-attachments/assets/b0194fa6-4768-47ac-8362-505f21c6f172" />

- Monitored the installation process via **Device Install Status**:
  - Initially showed as `Pending Install`.
  - Forced sync of the device.
  - Status eventually updated to `Installed`.
    
      <img width="528" height="56" alt="image" src="https://github.com/user-attachments/assets/a0fcc6b4-ecc9-46b4-8e7f-243b14a62074" />

- Confirmed application installation on device via `Settings > Apps`.
  
  <img width="440" height="55" alt="image" src="https://github.com/user-attachments/assets/ee0c2eb3-aa45-4831-848e-ea5b55f39877" />

## Notes
- Devices are now fully managed by Intune and can:
  - Enforce compliance policies
  - Apply configuration profiles
  - Receive and install applications remotely



  
    

