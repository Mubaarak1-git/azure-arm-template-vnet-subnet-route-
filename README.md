# Azure ARM Template: VNet, Subnet & Route Table 🚀

This repository contains my first complete **Azure Resource Manager (ARM) template** deployment.  
I successfully completed the lab **Deploying Your First ARM Template (60h, 2 XP)**.

## 📚 Contents
- `templates/vnet-subnet-route.json` → Full ARM template including parameters, variables, resources, and outputs
- `docs/lab-notes.md` → Notes and screenshots from the lab
- `scripts/deploy.sh` → Example deployment script using Azure CLI

## 🛠️ Skills Demonstrated
- Writing and validating ARM templates
- Parameterization for flexible deployments
- Linking resources (VNet, Subnet, Route Table)
- Using outputs for resource IDs

## 🚀 How to Deploy
```bash
az deployment group create \
  --resource-group myResourceGroup \
  --template-file templates/vnet-subnet-route.json
