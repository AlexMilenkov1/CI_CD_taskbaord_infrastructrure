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

---

## 🔧 Prerequisites

- Azure subscription  
- Terraform Cloud API token  
- Azure CLI setup  
- GitHub repository secrets configured  

### Required GitHub Secrets

| Name | Description |
|------|-------------|
| `AZURE_CLIENT_ID` | Azure service principal client ID |
| `AZURE_CLIENT_SECRET` | Azure service principal secret |
| `AZURE_SUBSCRIPTION_ID` | Your Azure subscription ID |
| `AZURE_TENANT_ID` | Azure tenant ID |
| `AZURE_CREDENTIALS` | Full Azure credentials JSON for GitHub Action |
| `TF_API_TOKEN` | Terraform Cloud token |

---

## ⚙️ Usage

### 1. Clone the repo

```bash
git clone https://github.com/AlexMilenkov1/CI_CD_taskbaord_infrastructrure
cd CI_CD_taskbaord_infrastructrure

terraform init
terraform plan -var-file="values.tfvars"
terraform apply -var-file="values.tfvars"

🧪 Resources Created
- Resource Group

- App Service Plan (Linux)

- Azure Web App (.NET 6.0 stack)

- Azure SQL Server + Database

- SQL Firewall Rule (0.0.0.0 for all IPs)

- GitHub-integrated source control

