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

## 🔒 Blob Access Control

- The storage container (`uploads`) is set to **Private – No anonymous access**.
- **Public access is disabled** at both the container and account level.
- **Access to upload/download blobs is restricted using Azure RBAC**, not shared keys.
- My user is assigned the `Storage Blob Data Contributor` role.
- This ensures only explicitly authorized users can interact with the container.

📸 [RBAC Assignment Screenshot](../screenshots/blob-iam.png)

---




