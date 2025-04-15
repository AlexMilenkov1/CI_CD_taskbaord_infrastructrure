# ☁️ Azure Taskboard Infrastructure with Terraform & GitHub Actions

This repository automates the deployment of an Azure-based Taskboard application using **Terraform** and **GitHub Actions**. It provisions a complete infrastructure stack including App Service, SQL Database, Resource Group, and other components.

---

## 🚀 Features

- 🌐 Azure Linux Web App deployment  
- 🗃️ Azure SQL Server + Database with firewall rule  
- ⚙️ App Service Plan  
- 🔐 Connection strings configured  
- 🌀 Unique resource names using random integer  
- 🔁 CI/CD Pipeline with GitHub Actions: validate, plan, apply  
- ☁️ Remote Terraform state in Azure Blob Storage  

---

## 📁 Folder Structure
. ├── .github/workflows # GitHub Actions workflows │ └── terraform.yml ├── main.tf # Main Terraform resources ├── variables.tf # Variable definitions ├── values.tfvars # Custom values for variables ├── README.md # This file
