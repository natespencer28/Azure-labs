# 🚀 Standardized Windows Server VM Deployment with ARM Templates

## Scenario: Why This ARM Template Exists

As the organization grows, new internal teams and applications constantly request Windows servers.  
Manually deploying these through the Azure Portal is:

- Time-consuming (20–30 minutes per VM)
- Error-prone (NSG rules, tags, and settings are easy to miss)
- Inconsistent (no guarantee every VM follows the same standard)

To fix this, we moved to **Infrastructure as Code (IaC)** using an **Azure Resource Manager (ARM) template**.

This template deploys a **standardized Windows Server VM** (configurable for Windows Server 2025) along with:

- Virtual Network and subnet
- Network Security Group (NSG) with RDP access (demo only)
- Public IP with DNS label
- Tags for Environment and Owner

This allows us to deploy a fully configured VM in minutes, with **consistent security, naming, and tagging** every time.

---

## 🧩 What This Template Deploys

This ARM template (`main.json`) deploys:

- `Microsoft.Network/virtualNetworks`
  - 1 VNet (default: `10.10.0.0/16`)
  - 1 Subnet (default: `10.10.1.0/24`)
- `Microsoft.Network/networkSecurityGroups`
  - NSG with an **Allow RDP** rule on TCP/3389  
  > ⚠️ In production, you should lock this down to specific IP ranges or use Azure Bastion.
- `Microsoft.Network/publicIPAddresses`
  - Dynamic public IP with a DNS label (e.g. `win2025-demo-nate.eastus.cloudapp.azure.com`)
- `Microsoft.Network/networkInterfaces`
  - NIC with the NSG and public IP associated
- `Microsoft.Compute/virtualMachines`
  - Windows Server VM (image is parameterized for Windows Server 2022/2025)
  - Standard_B2ms size by default
  - Premium managed OS disk
  - Local admin account (username/password via parameters)

---

## 📁 Files

- `main.json` – ARM template (infrastructure as code)
- `main.parameters.json` – sample parameters file
- `README.md` – this documentation


