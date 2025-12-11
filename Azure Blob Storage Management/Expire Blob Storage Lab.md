## 📦 Upload Photos to Azure Blob Storage & Configure Lifecycle Management

This guide walks you through downloading sample images, uploading them to Azure Blob Storage, and configuring a lifecycle policy to automatically delete blobs older than 30 days.

## 🖼️ 1. Download the Photos

- Open this link in a new browser tab:
https://github.com/pluralsight-cloud/Microsoft-Certified-Azure-Administrator-Associate/tree/photos

- Click Code → Download ZIP
- When prompted, choose Save File → OK
- Click Save to download the ZIP file
- Extract the ZIP file and note where the images are saved

## ☁️ 2. Upload the Photos to Blob Storage

- In the Azure Portal, go to Storage accounts
- Open the account that begins with store
- In the left navigation pane, select Containers
- Click + Container
- Configure the new container:
- Name: holidaysale
- Click Create
- Open the new holidaysale container
- Select Upload
- In the Upload blob pane, click Browse for files
- Select the image files you downloaded earlier, then click Open
- Expand Advanced settings
- Under Upload to folder, enter: img
- Click Upload
