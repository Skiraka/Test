# Goal
- Manage devices enrolled in Intune by configuring Compliance Policies, Configuration Profiles, and deploying Applications.

---

## Firewall Compliance Policy
- Created a new policy via `Intune > Devices > Compliance`
- Named policy `Require Firewall Enabled` with the setting `Required` for Firewall.
- Assigned Policy to all devices.
  
  <img width="809" height="64" alt="image" src="https://github.com/user-attachments/assets/41305bac-eebf-4631-9837-90d2fc2bc566" />

- To test the enforcement of the policy:
  - Manually turned off the Firewall on `PC-2`.
- Performed actions to Sync the device faster:
  - Selected `PC-2` on list of devices in Intune and selected the `Sync` option.
  - On `PC-2` Synced device via `Settings > Accounts > Access Work or School > Info > Sync`.
- Checked the `Require Firewall Enabled` policy report and confirmed `PC-2` was shown to be Noncompliant.
  
    <img width="746" height="96" alt="image" src="https://github.com/user-attachments/assets/b8045de8-fcaa-4746-bac6-d3a59c31c3fd" />

