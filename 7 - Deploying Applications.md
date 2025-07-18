# Goal
- Set up a Micrisoft Endpoint Configuration Manager server and deploy an application to a client using the Configuration Manager.

---

## Configuration Steps
- Created a new Windows Server 2022 virtual machine and installed the Microsoft Endpoint Configuration Manager.
- Installed the prerequisites on the same server for simplicity.
- The Site Code was named 'LAB'.
- Created a new Windows 10 client virtual machine 'PC-10' for this lab to function as the client as PC-1 and PC-2 will be managed through Microsoft Intune in later labs.
- Joined PC-10 to the domain.

 ---

## Installing the Client
- Pushed the client install to PC-10 from the MECM Console.
- Confirmed PC-10 now has the Software Center installed and working.
<img width="477" height="263" alt="image" src="https://github.com/user-attachments/assets/89174210-2b55-4ec3-afe4-a301b474013a" />

---

## Creating and Deploying an Application
- Now that PC-10 has the ECM client installed I wanted to verify that I could actually push software through the Configuration Manager pipeline — from application creation, to distribution, to deployment, to client installation.
  <img width="854" height="46" alt="image" src="https://github.com/user-attachments/assets/0dbf5875-e8a0-47a6-a087-cac8f2f267ec" />
- Test
