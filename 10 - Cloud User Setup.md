# Goal
- Ensure users are licensed and can access basic Microsoft 365 Services.

---

## Licensing Setup
- Created a Cloud-only security group in M365 Entra ID named `Lic_O365_AllUsers`.
  - Assigned the `Microsoft 365 Business Premium` license to the group.
  - Manually added synced users to the group to verify licensing.
  - Verified assigned licenses applied successfully via M365 Admin Center.

  <img width="825" height="116" alt="image" src="https://github.com/user-attachments/assets/81872b54-deb3-4b58-ab8f-0e5f814c3202" />

---

## Exchange Online
- Confirmed mailboxes were provisioned in Exchange Admin Center.
  - Each user can successfully send and receive mail internally.

  <img width="297" height="65" alt="image" src="https://github.com/user-attachments/assets/5d9b4f68-be8c-43f2-ab2c-3294dd7dacca" />

## OneDrive for Business
- Confirmed each licensed user can launch OneDrive from the portal.
- Uploaded a sample file and tested sharing internally.

## Microsoft Teams
- Confirmed Teams is accessible for all users.
- Created a test Channel using Admin account, verifying chat, file uploading and channel posting.

## Business Apps
- Confirmed users can access business related apps:
    - Word
    - Excel
    - Sharepoint Online

---

 ## Notes
 - This lab verifies that licenses were correctly assigned and that users can access core services.
 - Services will be configured in more depth in upcoming lab sections

