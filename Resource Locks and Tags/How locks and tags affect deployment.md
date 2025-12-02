# How Locks and Tagging Affects Deployments

This repository demonstrates how to:
1. Add a tag to a Resource Group.
2. Apply a **Read-Only lock** and attempt to deploy a VM to the locked resource group.
3. Apply a **Delete lock** and attempt to deploy a VM to the locked resource group.
4. Verify if tags have been inherited by resources within the locked resource group.

## Steps

### 1. Add a Tag to the Resource Group

Before applying any locks, we will add a tag to the resource group to test if it propagates to resources within it.

#### Instructions:
- Navigate to **Azure Portal** > **Resource Groups**.
- Select the resource group you want to work with.
- In the **Settings** section, click on **Tags**.
- Add a key-value pair for the tag (e.g., `Environment: Development`).
- Click **Save**.

### Screenshot:

<img width="1250" height="406" alt="image" src="https://github.com/user-attachments/assets/882f098f-c1af-40b5-b7ce-7267d573c64f" />


### 2. Apply a Read-Only Lock to the Resource Group

A **Read-Only lock** prevents modifications to resources, but allows read-only access.

#### Instructions:
- In the **Resource Group** overview, go to **Locks**.
- Click **+ Add**.
- Set **Lock Type** to **ReadOnly** and give it a name (e.g., `ReadOnlyLock`).
- Click **OK** to apply the lock.

#### Attempt to Deploy a Virtual Machine:
- Try to deploy a Virtual Machine (VM) to the resource group:
- 
### Screenshot:
<img width="955" height="595" alt="image" src="https://github.com/user-attachments/assets/4615b10b-2951-4dde-9221-fb2c019dd608" />


