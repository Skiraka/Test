# Goal
- Deploy a basic Veeam Backup & Replication server and successfully back up files from a test system

---

## Create and Join VM to Domain
- Created a new VM named `Veeam-1` using Windows Server 2022 ISO.
- Assigned static IP: `192.168.100.70`.
- Joined the VM to the domain.

---

## Install Veeam Backup & Replication
- Downloaded **Veeam Backup & Replication Community Edition**.
- Mounted ISO, ran the installer, and rebooted the server upon completion.

  ---

## Adding a Backup Repository
- In the Veeam console:
  - Navigated to **Backup Infrastructure > Backup Repositories**.
  - Added a new repository pointing to a local volume on `Veeam-1` named `FS1_FileShare_Backups`.

---

## Adding the File Server
- Navigated to **Inventory > Add Data Source**.
- Added a new managed server:
  - Selected **Microsoft Windows Server**.
  - Chose `FS-1` from the domain.
  - Verified credentials and connectivity.

  <img width="346" height="29" alt="image" src="https://github.com/user-attachments/assets/69fb7bf5-c29c-4c86-b3da-7779c6688f71" />

---

## Creating the Backup Job
- Navigated to **Home > Jobs**.
- Created a new **File Share Backup Job**:
  - Job Name: `FS-1 FileShare`.
  - Selected the `Share` folder from `FS-1`.
  - Targeted the local repository (`FS1-FileShare-Repo`).
  - Set the schedule to **daily**.

  <img width="1404" height="45" alt="image" src="https://github.com/user-attachments/assets/89ce0deb-011f-4354-aed5-d6e90b3bea7c" />

---

## Running the Backup
- Manually triggered the backup job.
- Monitored job progress under **History > Jobs**.
- Confirmed backup completion with a **successful status**.

  <img width="696" height="42" alt="image" src="https://github.com/user-attachments/assets/1a53b588-518c-46db-a2a2-1144ca70bf12" />

---

## Verifying Backup and Restore
- Navigated to **Home > Backups > Disk**.
- Performed a test restore of a deleted sample file from the backup to validate recovery.
- Confirmed multiple restore points were retained after rerunning the job.

  <img width="562" height="298" alt="image" src="https://github.com/user-attachments/assets/7f534f79-cda6-4fb2-a990-21a663c9ee32" />

---

## Notes
- Verified credentials and network connectivity between Veeam server and file server before backup configuration.
- Tested restore to ensure backup job effectiveness.





