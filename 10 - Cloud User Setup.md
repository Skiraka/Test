# Goal
- Ensure users are licensed and can access Microsoft 365 Services.

---

## Licensing Setup
- Created a Cloud-only security group in M365 Entra ID named `Lic_O365_AllUsers`.
  - Assigned the `Microsoft 365 Business Premium` license to the group.
  - Manually added synced users to the group to verify licensing.
  - Verified assigned licenses applied successfully via M365 Admin Center.

  <img width="825" height="116" alt="image" src="https://github.com/user-attachments/assets/81872b54-deb3-4b58-ab8f-0e5f814c3202" />

---

## Microsoft 365 Group
- Created a Microsoft 365 group for the Sales and HR Teams.
- Configured both groups to use Dynamic Membership rules for automatic user assignment based on Department.
  - `(user.department -eq "Sales")`

---

 ## Notes
 - This lab verifies that licenses were correctly assigned and that users can access core services.
 - Services will be configured in more depth in upcoming lab sections

