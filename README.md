# MCSA Windows Server Lab (Enterprise Infrastructure Project)

## 📌 Overview
This project demonstrates hands-on experience in Windows Server administration by building a complete enterprise-like environment using Active Directory, Group Policy, and core network services.

The lab simulates a real company setup with departments, security policies, file sharing, storage management, and OS deployment.

---

## 🛠️ Environment Details
- Server Name: DC-SG
- Domain Name: ohi.com
- OS: Windows Server 2016 Standard
- Virtualization: VMware
- Network: 192.168.2.0/24

---

## ⚙️ Project Implementation

### 1. Domain Controller Setup
- Installed Windows Server 2016
- Promoted server to Domain Controller
- Created a new forest: **ohi.com**
<img width="678" height="371" alt="1" src="https://github.com/user-attachments/assets/718848b0-9f82-4073-a263-19896528894c" />

---<


### 2. Active Directory (AD DS)
- Created Organizational Units (OUs):
  - HR
  - IT
  - Sales
- Added users and groups
- Managed permissions
- <img width="1918" height="972" alt="ou-users" src="https://github.com/user-attachments/assets/5c4a6db3-0acd-4759-b9af-ac164b6af620" />

---

### 3. DNS & DHCP
- Configured DNS for name resolution
- Installed and configured DHCP Server
- Created DHCP Scope:
  - IP Range: 192.168.2.2 – 192.168.2.100
  - Subnet: 192.168.2.0/24
- Configured Default Gateway and DNS Server
<img width="1911" height="975" alt="dhcp-scoop" src="https://github.com/user-attachments/assets/06e2aadf-7609-4cbb-b8e2-e83344c89cd4" />
- Implemented DHCP Reservation:
  - Reserved IP: 192.168.2.2
  - Assigned to: PC1
  - Based on MAC Address
  - 
<img width="1919" height="697" alt="dhcp" src="https://github.com/user-attachments/assets/4fb66c55-d7fc-4576-b866-a996793f1bcd" />

---

### 4. Group Policy (GPO)
- Applied department-based policies:

  🔹 HR:
  - Deny removable storage (USB restriction)

  🔹 IT:
  - Disable Control Panel

  🔹 Sales:
  - Remove "Run" option

- Linked GPOs to respective OUs
<img width="1918" height="915" alt="GPO" src="https://github.com/user-attachments/assets/36637c4e-a5d2-4353-92cf-47ef1d7500a9" />

---

### 5. User Restrictions
- Configured Logon Hours for users
- Restricted login access to specific times
<img width="1919" height="962" alt="logon-hours" src="https://github.com/user-attachments/assets/83543d80-2032-4ae5-91b0-657e5a1a1919" />

---

### 6. Windows Deployment Services (WDS)
- Installed and configured WDS
- Added Windows 10 images
- Enabled PXE boot
- Deployed Windows 10 over the network
<img width="1918" height="677" alt="wds" src="https://github.com/user-attachments/assets/8b8c67d1-c6fd-4d9b-a281-490f1b38cd5b" />

---

### 7. File Sharing & Access Control
- Created shared folders for:
  - HR
  - IT
  - Sales
- Applied NTFS permissions
- Restricted access between departments
- Managed access using security groups
<img width="1674" height="867" alt="file-sharing" src="https://github.com/user-attachments/assets/b0382cd3-5e29-4ada-b899-9cf88487f11b" />

---

### 8. Shadow Copies & Storage Management
- Enabled Shadow Copies on (D:)
  - Schedule: Daily at 7:00 PM
  - Storage limit: 1999 MB
- Enabled file recovery (Previous Versions)
<img width="1649" height="742" alt="shadow-copy" src="https://github.com/user-attachments/assets/209a5c61-01eb-4416-8356-0720a4bb4caa" />

---

### 9. Disk Quota Management
- Default quota: 1 GB for all users
- Custom quota: 5 GB for user (saleh)
- Controlled and monitored storage usage
<img width="1560" height="714" alt="qouta" src="https://github.com/user-attachments/assets/f2313196-4d9d-4f8d-952f-3f34945923d6" />
<img width="1458" height="546" alt="qouta2" src="https://github.com/user-attachments/assets/155c119e-b76f-402b-a587-17778540f37a" />

---


## 🎯 Skills Gained
- Active Directory Administration
- Group Policy Management (GPO)
- User Access Control & Security
- DHCP & DNS Configuration
- Windows Deployment Services (WDS)
- File Sharing & NTFS Permissions
- Shadow Copies & Backup
- Disk Quota Management
- Windows Server Administration

---

## 🚀 Conclusion
This project simulates a real-world enterprise IT environment where centralized management, security enforcement, and efficient resource control are implemented using Microsoft technologies.
