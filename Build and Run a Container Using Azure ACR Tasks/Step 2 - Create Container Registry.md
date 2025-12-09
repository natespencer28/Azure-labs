# 🏗️ Create a New Container Registry

Follow these steps to create an Azure Container Registry and prepare your Cloud Shell environment.

---

## 1. Open Your Resource Group
1. In the Azure Portal, click the **resource group** name that is listed.
2. Copy the resource group name to your clipboard — you’ll need it shortly.

---

## 2. Create a Container Registry
Run the following command in **Cloud Shell**, replacing `<RESOURCE_GROUP_NAME>` with the value you copied:

```bash
az acr create --resource-group <RESOURCE_GROUP_NAME> \
  --name acrbuildcontainer111 --sku Basic --admin-enabled true
```

<img width="1246" height="667" alt="image" src="https://github.com/user-attachments/assets/40bfff17-1f4b-4758-b325-354538fab2a1" />

