# 📦 Azure Storage + Blob + Key Vault – Secure File Upload Project

---

## 🔐 1. Storage Account Overview

![Storage Overview](../screenshots/storage-overview.png)

---

## 📁 2. Blob Container Creation

- Container Name: `secure-container`
- Public access level: **Private (no anonymous access)**

![Blob Container](../screenshots/blob-container-created.png)

---

## 📤 3. File Upload & Download

Uploaded a test `.txt` file inside the blob container:  
![Test File](../screenshots/test_file.txt)
![Blob Upload](../screenshots/blob-upload.png)

Downloaded back to verify data consistency.

![Blob Download](../screenshots/blob-download.png)


---

## 🔑 4. Azure Key Vault (Securing Access)

- Key Vault Name: `secure-upload-kv`
- Added secret: `storage-access-key`
![Key Vault Secret](../screenshots/keyvault-secret.png)



