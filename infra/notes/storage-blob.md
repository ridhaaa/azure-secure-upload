# 📦 Azure Storage + Blob + Key Vault – Secure File Upload Project

This document covers the configuration of Azure Storage, Blob container, file upload/download, and securing access via Azure Key Vault.

---

## 🔐 1. Storage Account Overview

![Storage Overview](../screenshots/storage-overview.png)

---

## 📁 2. Blob Container Creation

- Container Name: `uploads`
- Public access level: **Private (no anonymous access)**

![Blob Container](../screenshots/blob-container-created.png)

---

## 📤 3. File Upload & Download

Uploaded a ![Test File](../screenshots/test_file.txt) inside the blob container.

![Blob Upload](../screenshots/blob-upload.png)

Verified the uploaded file by downloading it back.

![Blob Download](../screenshots/blob-download.png)


---

## 🔑 4. Azure Key Vault (Securing Access)

- **Key Vault Name**: `secure-upload-kv`
- **Secret Name**: `storage-access-key`
- 📝 **Note**: The secret currently stored is a **dummy placeholder** used to simulate secure access control.  
  
![Key Vault Secret](../screenshots/keyvault-secret.png)



