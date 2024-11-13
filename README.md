# API Deployment Guide to Azure

## Introduction
This guide provides a step-by-step approach to deploying an API to Azure App Service using Terraform.
## Prerequisites
- An active **Azure account**
- **Azure CLI** installed or access to the **Azure Portal**
- The **API source code** prepared in advance


## Deployment Steps

### Step 1: Log In to Azure
Log into your Azure account using either the Azure CLI or the Azure Portal.

#### Using Azure CLI
1. Open a terminal or command prompt.
2. Run the following command to log in:
   
   ```bash
   az login
   ```   

### Step 2:  Go to root folder of main.tf

   ```bash
      cd ../TerraformScript/Private_ITS
   ```
### Step 3:  Terraform initiation

   ```bash
      terraform init -var-file="../variables.tf"
   ```

   If you have more than one API configuration, create additional tfvars files. You can use a naming convention like variables_<api>_<version>.tf to flexibly manage multiple APIs.
   
   

### Step 4: Terraform Plan

   ```bash
   terraform plan  -var-file="terraform.tfvars"
   ```
### Step 5: Apply

   ```bash
   terraform apply -v -var-file="terraform.tfvars"
   ```
