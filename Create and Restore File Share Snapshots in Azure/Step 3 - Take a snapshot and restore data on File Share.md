# Take a Snapshot and Restore Data from an Azure File Share

## 📌 Scenario Overview
To validate file versioning and recovery capabilities, you are tasked with **creating a snapshot of an Azure File Share and restoring a file from that snapshot**. This test simulates a real-world scenario where a user accidentally modifies or overwrites a file and needs to recover a previous version.

---

## 🎯 Objectives
- Create and modify a file within an Azure File Share
- Take a snapshot of the file share
- Simulate accidental data modification
- Restore the original file from a snapshot
- Verify successful file recovery on a Windows VM

---

## 🛠️ Prerequisites
- A Windows Virtual Machine connected to an Azure File Share (`fileshare1`)
- An existing Azure Storage Account
- Permissions to manage file share snapshots
- Azure Portal access

---

## 🚀 Step-by-Step Instructions

### 1️⃣ Create a Test File
1. On the **Windows VM**, click **File Explorer** in the taskbar.
2. Select **This PC** and open **fileshare1**.
3. Right-click inside the **fileshare1** window and select **New > Text Document**.
4. Name the file `test.txt`.
5. Open the file and enter the following text:

6. Click **File > Save**, then close the file.
<img width="1656" height="421" alt="image" src="https://github.com/user-attachments/assets/c733b017-074b-43e5-9197-0020dcb05d84" />

  

---

### 2️⃣ Verify the File in Azure
1. Return to the **Azure Portal**.
2. Close the **Connect** side window if it is still open.
3. In the storage account, navigate to:
**File shares > fileshare1 > Browse**
4. Confirm that **test.txt** is visible.

<img width="1318" height="270" alt="image" src="https://github.com/user-attachments/assets/0b0be3e3-f2e6-4778-8c07-41aae92b4f4b" />


---

### 3️⃣ Create a File Share Snapshot
1. Within **fileshare1**, select **Snapshots**.
2. Click **+ Add Snapshot**.
3. In the **Comment** field, enter:

<img width="1396" height="210" alt="image" src="https://github.com/user-attachments/assets/f8a6f219-c54e-456a-b1eb-350a32ded2d1" />

4. Click **OK** to create the snapshot.

---

### 4️⃣ Modify the File (Simulate Data Loss)
1. Return to the **Windows VM**.
2. Open `test.txt`.
3. Add random or additional text to the file.
4. Click **File > Save** and close the file.

<img width="1061" height="222" alt="image" src="https://github.com/user-attachments/assets/6ab6f2d7-971d-4131-a3ce-7a44ccfbf196" />


---

### 5️⃣ Restore the File from Snapshot
1. Return to the **Azure Portal**.
2. Navigate back to **Snapshots** under `fileshare1`.
3. Locate and open **TestSnapshot**.
4. Find `test.txt`.
5. Click the **ellipsis (⋯)** on the right-hand side of the file.
6. Select **Restore**.
7. Choose **Overwrite original file**.
8. Click **OK**.

<img width="1434" height="527" alt="image" src="https://github.com/user-attachments/assets/a2b2b8f8-3d7a-4b2b-98a1-ec3b45877071" />

After restoring to orginal: 

<img width="999" height="264" alt="image" src="https://github.com/user-attachments/assets/afb11a24-effd-454b-9eca-6a583e802af9" />



---

## ✅ Validation Checklist
- [ ] Snapshot created successfully  
- [ ] File modified after snapshot creation  
- [ ] File restored from snapshot  
- [ ] Original file contents restored correctly  

---

## 🔍 Verification
1. Open `test.txt` on the Windows VM.
2. Confirm the file contents have reverted.



