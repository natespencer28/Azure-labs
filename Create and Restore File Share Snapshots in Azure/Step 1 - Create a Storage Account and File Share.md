# Create an Azure Storage Account and File Share

## 📌 Scenario Overview
To support centralized file storage and future backup and recovery testing, you are tasked with **creating an Azure Storage Account and an Azure File Share**. This file share will later be used to validate snapshot, backup, and restore functionality.

---

## 🎯 Objectives
- Create a new Azure Storage Account
- Configure an Azure File Share
- Ensure resources align with existing subscription and resource group standards
- Prepare storage for backup and versioning scenarios

---

## 🛠️ Prerequisites
- Access to the Azure Portal
- An existing Azure subscription
- An existing Azure resource group
- Appropriate permissions to create storage resources

---

## 🚀 Deployment Steps

### 1️⃣ Create a Storage Account
1. In the **Azure Portal**, click the **hamburger menu (☰)** in the top-left corner.
2. Select **Storage accounts**.
3. Click **+ Create**.

#### Configure the following settings:
- **Subscription:** Use existing
- **Resource Group:** Use existing resource group
- **Storage account name:** Enter a **globally unique name**
- **Location:** Same location as the existing resource group
- **Performance:** Standard

> Leave all other settings as **default**.

4. Click **Review + create**.
5. Select **Create**.

<img width="992" height="344" alt="image" src="https://github.com/user-attachments/assets/18f9e19a-ce8a-4384-9407-1956c08f07f1" />



---

### 2️⃣ Access the Storage Account
1. After deployment completes, click **Go to resource**.
2. In the left-hand navigation menu, select **File shares**.

---

### 3️⃣ Create a File Share
1. Click **+ File share**.
2. Enter the following:
   - **Name:** `fileshare1`
3. Click **Review + create**.
4. Select **Create**.

<img width="1434" height="324" alt="image" src="https://github.com/user-attachments/assets/c68f47a2-90de-4316-8eae-e7758008c43e" />

---

## ✅ Validation Checklist
- [ ] Storage account deployed successfully  
- [ ] Storage account located in the correct resource group and region  
- [ ] Azure File Share (`fileshare1`) created  
- [ ] File share is visible under **File shares** in the storage account  

---

## 💡 Business Value
- Enables centralized and scalable file storage
- Supports backup, snapshot, and recovery use cases
- Provides a foundation for secure file access via SMB
- Aligns with cloud-first storage strategies

---

## 📚 Azure Services Used
- Azure Storage Account
- Azure File Shares
- Azure Portal

---

## 🔜 Next Steps
- Configure **Azure File Share snapshots**
- Enable **Azure Backup for file shares**
- Mount the file share to a **Windows mach**

