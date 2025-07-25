# Goal
- Set up a **Microsoft Endpoint Configuration Manager (MECM)** server and deploy an application to a domain-joined client.

---

## Configuration Steps
- Created a new **Windows Server 2022** virtual machine and installed **Microsoft Endpoint Configuration Manager**.
- Installed all **prerequisites** on the same server for simplicity.
- Site Code: `LAB`
- Created a new **Windows 10** client virtual machine named `PC-10` for this lab.  
  `PC-1` and `PC-2` will be managed through **Microsoft Intune** in later labs.
- Joined `PC-10` to the domain.

 ---

## Installing the Client
- Pushed the MECM client install to `PC-10` from the **MECM Console**.
- Confirmed `PC-10` now has **Software Center** installed and functioning.

 <img width="477" height="263" alt="image" src="https://github.com/user-attachments/assets/89174210-2b55-4ec3-afe4-a301b474013a" />

---

## Creating the Application

 <img width="854" height="46" alt="image" src="https://github.com/user-attachments/assets/0dbf5875-e8a0-47a6-a087-cac8f2f267ec" />

- Downloaded `7z2500-x64.msi` into the lab source share:  
  `\\CM-1\ECM_Sources\Applications\7Zip`
- In the **MECM console**:
  - Navigated to: `Software Library > Applications`
  - Created a new application using the **MSI wizard**
  - Application Name: `7-Zip 25.00 (x64 edition)`

 ---

## Deploying the Application
- Right-clicked `7-Zip` > `Deploy`
  - Target Collection: `All Systems`
  - Availability: **Immediate**

---

## Client Software Center Verification
- On `PC-10`:
  - Opened **Software Center**
  - Manually triggered Configuration Manager **client actions**
  - Verified `7-Zip` appeared under **Applications**
  - Clicked **Install** and the installation succeeded
  - Confirmed `7-Zip` in:
    - **Start Menu**
    - **Apps & Features**
  <img width="475" height="330" alt="image" src="https://github.com/user-attachments/assets/fba7b931-af8c-4f8b-9497-49ce590d1f1f" />

---

## Notes
- Successfully demonstrated core **Microsoft Endpoint Configuration Manager** functionality.
- Lab will now pivot to **Microsoft Intune** to explore **cloud-native management**.

 <img width="335" height="363" alt="image" src="https://github.com/user-attachments/assets/2a0a79c9-1a6e-4376-be8f-82698d6b808a" />
