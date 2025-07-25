# Goal
- Apply foundational Group Policy settings to domain-joined computers and users, and verify that the policies have been successfully enforced by confirming their application from the domain controller.

---

## Login Banner
- Configured a login banner to display an acceptable use policy upon user logon to domain-joined computers.
- GPO Path: Computer Configuration > Policies > Windows Settings > Security Settings > Local Policies > Security Options
- Policy Settings:
  - Interactive logon: Message title for users = "Authorized Access Only"
  - Interactive logon: Message text for users = "This system is for authorized users only. Activity may be monitored."
- Linked GPO to the Computers OU to apply on domain computers.

  <img width="498" height="149" alt="image" src="https://github.com/user-attachments/assets/adbd6148-f6b1-4c7a-8410-a026fc8af64b" />

---

## Password Policy
- Enforced password complexity requirements through the Default Domain Policy.
- GPO Path: Computer Configuration > Policies > Windows Settings > Security Settings > Account Policies > Password Policy
- Settings applied:
  - Minimum password length: 8 characters
  - Enforce password history: Remember last 5 passwords
  - Maximum password age: 30 days
  - Password must meet complexity requirements: Enabled

---

## Mapped Network Drives
- Configured automatic mapping of network drives based on user group membership.
- GPO Path: User Configuration > Preferences > Windows Settings > Drive Maps
- Example drive mappings:
  - Drive letter H: mapped to `\\FS-1\HR` for users in `HR_FullAccess` or `HR_ReadOnly` groups
  - Drive letter S: mapped to `\\FS-1\Sales` for users in `Sales_FullAccess` or `Sales_ReadOnly` groups
- Applied security group filtering on the GPO to target appropriate users.
- Verified drives were successfully mapped upon user logon, including after reboot.

---

## Verification
- Logged in as users `jdoe` and `aray` (Sales), verified:
  - Login banner was displayed.
  - Drive S: (Sales share) was automatically mapped.
  <img width="253" height="68" alt="image" src="https://github.com/user-attachments/assets/c683c490-c901-4dd9-83ee-01c2cb1413ac" />
- Logged in as users `jsmith` and `mwhite` (HR), verified:
  - Login banner was displayed.
  - Drive H: (HR share) was automatically mapped.
- Changed user passwords to test enforcement of password complexity requirements.
- Ran `gpupdate /force` and `gpresult /r` on client machines to confirm all GPO settings were applied successfully.
  <img width="480" height="325" alt="image" src="https://github.com/user-attachments/assets/4b143b6e-b9b5-435f-8b57-d8626a4a4db5" />



