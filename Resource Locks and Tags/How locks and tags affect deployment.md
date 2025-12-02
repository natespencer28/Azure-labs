## 🔒💡 How Locks and Tagging Affect Deployments

This file demonstrates:

🏷️ Add a tag to a Resource Group
🔐 Apply a Read-Only lock and attempt to deploy a VM
🚫 Apply a Delete lock and attempt to deploy a VM
🧩 Verify if tags are inherited by deployed resources

## 1️⃣ Add a Tag to the Resource Group 🏷️

Before applying any locks, we will add a tag to the resource group to test if it propagates to resources within it.

🔧 Instructions:

- Navigate to Azure Portal → Resource Groups
- Select your resource group
- Go to Tags under Settings
- Add a key-value tag (e.g., Environment: Development)
- Click Save

🖼️ Screenshot:
<img width="1250" height="406" alt="image" src="https://github.com/user-attachments/assets/882f098f-c1af-40b5-b7ce-7267d573c64f" />

## 2️⃣ Apply a Read-Only Lock 🔐 (and attempt VM deployment)

A Read-Only lock prevents resource modification — including creating new resources.

🔧 Instructions:

- Open the Resource Group
- Go to Locks
- Click + Add
- Set Lock Type: ReadOnly
- Name it (e.g., ReadOnlyLock)
- Click OK

🖼️ Screenshot:
<img width="955" height="595" alt="image" src="https://github.com/user-attachments/assets/4615b10b-2951-4dde-9221-fb2c019dd608" />
🧪 Attempt to Deploy a VM:

Try deploying a VM into this locked resource group.

❗ Expected Behavior:

🚫 Deployment fails
Read-only locks do block new resource creation.

## 3️⃣ Apply a Delete Lock 🚫 (and attempt VM deployment)

A Delete lock prevents removal of the RG or its resources, but creation is still allowed.

🔧 Instructions:

- In the Resource Group, go to Locks
- Click + Add
- Set Lock Type: Delete
- Name it (e.g., DeleteLock)
- Click OK

🧪 Attempt to Deploy a VM:

- Go to Virtual Machines → + Add
- Select the locked resource group
- Complete the VM setup
- Click Create

🖼️ Screenshot:
<img width="861" height="445" alt="image" src="https://github.com/user-attachments/assets/348a655f-8b90-42b0-909f-fb26b0310fe7" />
✔ Expected Behavior:

✅ Deployment succeeds
Delete locks prevent deletion but do not block creating new resources.

## 4️⃣ Verify Tag Inheritance 🧩

After a successful deployment, check whether the VM inherited the Resource Group tags.

🔧 Instructions:

- Open Virtual Machines
- Select the VM deployed in the locked RG
- Go to the Tags section
- Check if the RG tag (Environment: Development) appears

🖼️ Screenshot:
<img width="1253" height="584" alt="image" src="https://github.com/user-attachments/assets/7ba0b873-fcbe-49f3-91b4-b164c805aa50" />

🚫 Resources do not inherit tags from their resource group by default—an Azure Policy must be applied for automatic tag inheritance


Azure Resource Locks Documentation
https://docs.microsoft.com/en-us/azure/azure-resource-manager/management/lock-resources

Azure Tags Documentation
https://docs.microsoft.com/en-us/azure/governance/policy/overview#tags
