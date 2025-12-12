# Connect an Azure File Share to a Windows Virtual Machine

## 📌 Scenario Overview
To validate access and restore operations, you must **connect an Azure File Share to a Windows Virtual Machine (VM)**. This allows you to interact with files using standard Windows tools and confirms that the file share is accessible over SMB.

---

## 🎯 Objectives
- Connect to a Windows VM using Remote Desktop
- Prepare the VM for SMB connectivity
- Mount an Azure File Share using PowerShell
- Verify successful authentication and connection

---

## 🛠️ Prerequisites
- A deployed Windows Virtual Machine (`winVM`)
- A deployed Azure Storage Account with an Azure File Share (`fileshare1`)
- Public IP access to the VM
- Valid VM login credentials
- Permissions to access the storage account

---

## 🚀 Step-by-Step Instructions

### 1️⃣ Connect to the Windows VM
1. In the **Azure Portal**, click the **Home** breadcrumb at the top of the page.
2. Open the **Resource Group** containing your VM.
3. Select the **winVM** virtual machine.
4. Copy the **Public IP address** to your clipboard.
5. Open **Remote Desktop Connection** on your local machine.
6. Connect to the VM using the copied IP address.
7. Log in using the **winVM username and password** provided in the lab credentials.

---

### 3️⃣ Open PowerShell as Administrator
1. Search for **Windows PowerShell**.
2. Right-click **Windows PowerShell** and select **Run as administrator**.

---

### 4️⃣ Retrieve the File Share Connection Script
1. Return to the **Azure Portal**.
2. Click the **Resource Group** breadcrumb.
3. Open the **Storage Account**.
4. Select **File shares** from the left menu.
5. Click **fileshare1**.
6. Select **Connect**.
7. In the side pane, click **Show Script**.
8. Copy the **PowerShell script** to your clipboard.

---

### 5️⃣ Mount the File Share
1. Paste the copied PowerShell script into the **PowerShell session** on the Windows VM.
2. Press **Enter** to execute the script.
3. Wait a few moments for execution to complete.

<img width="1333" height="577" alt="image" src="https://github.com/user-attachments/assets/1c3c66b1-7a1c-4d3a-b6e5-b33aca533c5d" />

<img width="1647" height="607" alt="image" src="https://github.com/user-attachments/assets/d85da09a-7211-4cc3-8966-6d3c4d3c236b" />



---

## ✅ Validation Checklist
- [ ] Successfully connected to the Windows VM via RDP  
- [ ] PowerShell launched with administrative privileges  
- [ ] Azure File Share connection script executed successfully  
- [ ] Confirmation message displayed: **Credential added successfully**  
- [ ] File share is accessible as a mapped network drive  

---

## 💡 Business Value
- Enables users and applications to access Azure File Shares using standard SMB
- Validates storage connectivity for backup and restore scenarios
- Supports hybrid and cloud-based file access models
- Provides a foundation for testing snapshots and recovery

---

## 📚 Azure Services Used
- Azure Virtual Machines
- Azure Storage Account
- Azure File Shares
- SMB (Server Message Block)

---

## 🔜 Next Steps
- Upload test files to the file share
- Take a snapshot of the file share
- Modify or delete files to simulate data loss
- Restore files from a snapshot to the Windows VM

---

> This step confirms that Azure File Shares can be securely accessed from Windows systems, enabling real-world file operations and recovery testing.
`
