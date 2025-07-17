# Goal
- Apply foundational policies to domain-joined computers and users to demonstrate management skills and enforce security best practices.

---

## Login Banner
- Displays simple acceptable use policy when users log in to a domain PC.
- Path: Computer Configuration > Policies > Windows Settings > Security Settings > Local Policies > Security Options
- Policy:
  - Interactive logon: Message title for users → "Authorized Access Only"
  - Interactive logon: Message text for users → "This system is for authorized users only. Activity may be monitored."
- GPO Scope: Linked to Computers OU
<img width="498" height="149" alt="image" src="https://github.com/user-attachments/assets/adbd6148-f6b1-4c7a-8410-a026fc8af64b" />

---

## Password Policy
- Enforce minimum password complexity.
- Path: Computer Configuration > Policies > Windows Settings > Security Settings > Account Policies > Password Policy
- Settings:
  - Minimum password length: 8
  - Enforce password history: 5 passwords remembered
  - Maximum password age: 30 days
  - Password must meet complexity requirements: Enabled
- GPO Scope: Default Domain Policy

---

## Mapped Network Drives
- Automatically mount department shares based on group membership.
- Path: User Configuration > Preferences > Windows Settings > Drive Maps
- Example Mappings:
  - H: \\FS-1\HR (Security Group: HR_FullAccess or HR_ReadOnly)
  - S: \\FS-1\Sales (Security Group: Sales_FullAccess or Sales_ReadOnly)
- GPO Scope: Filtered with Security Group Targeting
- Confirmed Drives are mounted after shutdown.

---

## Verification
Testing & Verification
- Logged in with jdoe and aray, verified:
  - Login banner displayed.
  - Drive S: (Sales) auto-mapped.
  <img width="253" height="68" alt="image" src="https://github.com/user-attachments/assets/c683c490-c901-4dd9-83ee-01c2cb1413ac" />
- Logged in with jsmith and mwhite, verified:
  - Login banner displayed.
  - Drive H: (HR) auto-mapped.
- Changed password and verified password complexity was enforced.
- Ran gpupdate /force and gpresult /r to ensure all GPO were applied successfully.
<img width="480" height="325" alt="image" src="https://github.com/user-attachments/assets/4b143b6e-b9b5-435f-8b57-d8626a4a4db5" />



