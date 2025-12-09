# 📦 Build an Image and Push to Azure Container Registry (ACR)

Now that your Dockerfile and container registry are ready, build and push your image to ACR.

---

## 1. Build & Push the Image

Run the following command in **Cloud Shell**.  
This will build the image using your Dockerfile and push it to your Azure Container Registry.  
⚠️ *Note: This step may take a few minutes to complete.*

```bash
az acr build --image sample/hello-world:v1 --registry acrbuildcontainer11 \
  --file Dockerfile .
```
<img width="1201" height="291" alt="image" src="https://github.com/user-attachments/assets/5e52961a-9a2b-48a8-83d5-712235d70a88" />
