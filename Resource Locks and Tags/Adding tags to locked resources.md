

## 🔐 Lock a VM Resource with a Read-Only Lock

### Instructions

* Navigate to **Azure Portal** → **Virtual Machines**.
* Select the VM you want to lock.
* In the **Settings** section, choose **Locks**.
* Click **+ Add** and set:

  * **Lock Type:** `ReadOnly`
  * **Name:** e.g., `VM-ReadOnly-Lock`
* Click **OK** to apply the lock.

### Expected Behavior

* This VM cannot be modified (including tag updates), but it can still be viewed.

### Screenshot

<img width="990" height="170" alt="image" src="https://github.com/user-attachments/assets/6e61e555-6b20-4ed3-9c8a-5c3f3872f80e" />


---

## 🚫 Lock a VM Resource with a Delete Lock

### Instructions

* Navigate to the specific **Virtual Machine**.
* Select **Locks** under **Settings**.
* Click **+ Add** and set:

  * **Lock Type:** `Delete`
  * **Name:** e.g., `VM-Delete-Lock`
* Click **OK** to apply.

### Expected Behavior

* The VM cannot be deleted, but normal modifications—including tags—are allowed.

### Screenshot

<img width="983" height="130" alt="image" src="https://github.com/user-attachments/assets/71de13af-6990-4aed-9c95-fa48f5ccae6a" />

---

## 🏷️ Attempt to Add Tags to All VM Resources at Once

### Instructions

* Navigate to the **Resource Group** containing your VMs.
* Select **Tags** from the left-hand menu.
* Add or update a tag key/value pair.
* Click **Save** to apply the tag update to all child resources.

### Expected Behavior

* Azure will attempt to apply the tag to each resource within the RG, including locked ones.

### Screenshot

<img width="820" height="193" alt="image" src="https://github.com/user-attachments/assets/b01334ec-e6ee-44b1-a0e4-d183f43db108" />


---

## 🔎 Verify if Locks Prevented Tags from Being Added

### Instructions

* Open each VM → **Tags**.
* Compare the applied tags against what was attempted.
* Note whether:

  * The **Read-Only locked VM** rejected the tag update.
  * The **Delete locked VM** successfully accepted the tag.

### Expected Behavior

* **Read-Only lock:** ❌ Tag update should fail
* **Delete lock:** ✅ Tag update should succeed



