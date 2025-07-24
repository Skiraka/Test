# Goal
- Ensure users are licensed and can access Microsoft 365 Collaboration services.

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
- Configured both groups to use Dynamic Membership rules for automatic user assignment based on the `Department` attribute.
  - Rule example: `(user.department -eq "Sales")`
  <img width="893" height="38" alt="image" src="https://github.com/user-attachments/assets/31decaf8-8637-4bf9-a9a4-b6b3858ee880" />
- Confirmed users were correctly dynamically assigned to their respective groups based on department.
---

## Microsoft Teams
-  Created a new Team from the `Sales_GRP` and `HR_GRP` Group.
-  Verified that group members were automatically added to their respective Teams.
-  Confirmed users could:
  - Send emails to one another
  - Send and receive messages from group mailboxes successfully
  
---

## Microsoft Outlook
- Verified that mailboxes were provisioned for both users and Microsoft 365 groups.
- Added group mailboxes to users' Outlook clients for visibility.
- Users could send email to each other and to group mailbox successfully.

---

## Microsoft Sharepoint
- Verified Sharepoint sites were created for the Sales and HR groups.
- Confirmed users could share files to their department through the site.

---

 ## Notes
 - This lab verifies that licenses were correctly assigned and that users can access core services.
