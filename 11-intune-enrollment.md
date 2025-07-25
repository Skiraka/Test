# Goal
- Enable on-premises domain-joined devices to be:
  - Hybrid Azure AD Joined (in Microsoft Entra ID).
  - Auto-enrolled into Intune MDM.

---

## Azure AD Connect Configuration
- Set **Device Options** in Microsoft Entra Connect Sync to `Configure Hybrid Microsoft Entra ID Join`.
- Confirmed domain-joined clients populating in **Microsoft Entra admin center > Devices**.
  
  <img width="670" height="76" alt="22fcb25e-1673-4f85-b57f-3b004cf4226d" src="https://github.com/user-attachments/assets/e6c75e81-2a2d-46a4-8bfe-f24ce81f6766" />

---

## Intune Enrollment
- Set `Intune > Devices > Enrollment > Automatic Enrollment > MDM User Scope` to `All`.
- Created a Group Policy Object enabling MDM enrollment and applied it to the `Computers` OU.
  - Restarted the computer and used `gpresult /r` to confirm the PC received the GPO.
  
  <img width="487" height="75" alt="image" src="https://github.com/user-attachments/assets/ba6a7282-7426-4968-b1e4-48eb25c65f09" />

- Confirmed device configuration showing joined.
  
  <img width="337" height="153" alt="image" src="https://github.com/user-attachments/assets/c27b8ae4-3a85-42fc-bda5-514835fceddd" />

- Confirmed devices enrolled in Intune.

  <img width="379" height="101" alt="image" src="https://github.com/user-attachments/assets/e3e4ca90-1dc4-40d7-bea4-da85b36871bc" />

## Notes
- `PC-1` and `PC-2` are now enrolled in Intune and can be managed via the Intune Console.
  
