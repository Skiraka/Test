# Goal
- Build an OU and group structure in Active Directory to organize users, computers, and manage permissions across the lab.

## OU Structure
- Created a basic but scalable  OU hierarchy to simulate department-based organization.
- This structure supports user/group delegation, GPO targeting, and file server integration later.
- Moved previously created users to their respective department OUs:
  - John Smith was moved to the HR OU.
  - Jane Doe was moved to the Sales OU.
  <img width="169" height="142" alt="image" src="https://github.com/user-attachments/assets/24e49f66-91e4-4226-b0f4-5fbf28f19d6a" />



## Group Structure
- Created several Global Security Groups to manage access.
<img width="263" height="141" alt="image" src="https://github.com/user-attachments/assets/da25fc27-f1b3-4fee-9c30-36821e1653fd" />



Notes
This structure is designed for clarity and reusability across future lab services (File Server, GPOs, SCCM).
Groups are ready to be used for folder permissions and login restrictions.
Kept the structure minimal to reflect a clean lab setup without unnecessary complexity.


