# Goal
- Ensure users are licensed and can access Microsoft 365 Collaboration services.

---

## Licensing Setup
- Created a Cloud-only security group in M365 Entra ID named `Lic_O365_AllUsers`.
  - Assigned the `Microsoft 365 Business Premium` license to the group.
  - Manually added synced users to the group to validate licensing.
  - Verified assigned licenses applied successfully via M365 Admin Center.

  <img width="825" height="116" alt="image" src="https://github.com/user-attachments/assets/81872b54-deb3-4b58-ab8f-0e5f814c3202" />

---

## Microsoft 365 Group
- Created a Microsoft 365 group for the Sales and HR Teams.
- Configured each group to use Dynamic Membership rules for automatic user assignment based on the `Department` attribute.
  - Rule example: `(user.department -eq "Sales")`
  <img width="893" height="38" alt="image" src="https://github.com/user-attachments/assets/31decaf8-8637-4bf9-a9a4-b6b3858ee880" />
- Verified users were automatically assigned to the correct group based on their department.
  
---

## Microsoft Teams
- Created new Teams from the `Sales_GRP` and `HR_GRP` Microsoft 365 Groups.
- Verified that group members were automatically added to the corresponding Teams.
- Confirmed users could:
  - Chat and collaborate in channels
  - Share files in the Teams Files tab
  - Schedule and participate in meetings
    
---

## Microsoft Outlook
- Verified that mailboxes were provisioned for both users and Microsoft 365 groups.
- Added group mailboxes to users' Outlook clients for accessibility.
- Confirmed users could:
  - Send emails to one another
  - Send and receive emails via group mailboxes

---

## Microsoft Sharepoint
- Verified that SharePoint team sites were automatically created for each Microsoft 365 Group.
- Uploaded test files to the Documents library.
- Confirmed users could access and edit department-specific documents and collaborate through SharePoint or via Teams file integration

---

 ## Notes
- This lab validates that:
  - Group-based licensing is functional
  - Users are dynamically grouped based on Entra ID attributes
  - Core Microsoft 365 collaboration services (Teams, Outlook, SharePoint) are available and working as expected
