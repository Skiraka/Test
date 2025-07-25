# Goal
- Build an Organizational Unit and Group structure in Active Directory to organize users, computers, and manage permissions across the lab.

---

## OU Structure
- Created a basic but scalable OU hierarchy to simulate department-based organization.
- This structure supports user/group delegation, GPO targeting, and file server integration later.
- Moved previously created users to their respective department OUs:
  - John Smith and Megan White were moved to the `HR` OU.
  - Jane Doe and Alex Ray were moved to the `Sales` OU.
  - Juan Bernard was moved to the `IT` OU.

<img width="169" height="142" alt="image" src="https://github.com/user-attachments/assets/24e49f66-91e4-4226-b0f4-5fbf28f19d6a" />

---

## Group Structure
- Created several Global Security Groups to manage access.

<img width="263" height="141" alt="image" src="https://github.com/user-attachments/assets/da25fc27-f1b3-4fee-9c30-36821e1653fd" />

---

## Group Assignment

| Full Name    | Username | Department | Role           | Group(s)                    |
|------------- |----------|------------|----------------|-----------------------------|
| Juan Bernard | jb       | IT         | IT Admin       | IT_Admins, All_Staff        |
| John Smith   | jsmith   | HR         | HR Staff       | HR_ReadOnly, All_Staff      |
| Jane Doe     | jdoe     | Sales      | Sales Rep      | Sales_ReadOnly, All_Staff   |
| Megan White  | mwhite   | HR         | HR Manager     | HR_FullAccess, All_Staff    |
| Alex Ray     | aray     | Sales      | Sales Manager  | Sales_FullAccess, All_Staff |

---

## Verification
- Verified group memberships via:
  - Active Directory Users and Computers.
  - The `whoami /groups` command from logged-in client VMs.

---

## Notes
- This structure is designed for clarity and reusability across future lab services (File Server, GPOs, SCCM).
- Groups are ready to be used for folder permissions and login restrictions.
- Kept the structure minimal to reflect a clean lab setup without unnecessary complexity.
