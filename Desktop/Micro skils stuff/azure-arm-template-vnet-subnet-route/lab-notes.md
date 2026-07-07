# Lab Notes: Deploying Your First ARM Template

This lab demonstrates how to deploy a **Virtual Network (VNet)**, a **Subnet**, and a **Route Table** in Azure using an ARM template.  
The template includes **parameters, variables, resources, and outputs** — making it a full example of Infrastructure as Code.

---

## 🔑 Parameters
- `vnetName` → Name of the Virtual Network (default: `myVNet`)
- `vnetAddressPrefix` → Address space for the VNet (default: `10.0.0.0/16`)
- `subnetName` → Name of the Subnet (default: `mySubnet`)
- `subnetPrefix` → Address space for the Subnet (default: `10.0.1.0/24`)
- `routeTableName` → Name of the Route Table (default: `myRouteTable`)

Parameters make the template **flexible** — you can reuse it with different names or address ranges.

---

## 📐 Variables
- `location` → Automatically uses the resource group’s location
- `subnetId` → Builds the resource ID for the Subnet

Variables simplify repeated values and keep the template clean.

---

## 🏗️ Resources
1. **Virtual Network (VNet)**  
   - Defines the overall network space.  
   - Contains the Subnet and links it to the Route Table.

2. **Subnet**  
   - A smaller segment inside the VNet.  
   - Configured with its own address prefix.  
   - Associated with the Route Table.

3. **Route Table**  
   - Contains a default route (`0.0.0.0/0`) pointing to the Internet.  
   - Ensures outbound traffic flows correctly.

---

## 📤 Outputs
- `vnetName` → Returns the name of the VNet
- `subnetId` → Returns the Subnet resource ID
- `routeTableName` → Returns the Route Table name

Outputs are useful for referencing deployed resources in other templates or scripts.

---

## 📸 Screenshots
- `deployment-success.png` → Proof of successful deployment via Azure CLI  
- `portal-view.png` → Visual confirmation in the Azure Portal

---

## 📝 Lessons Learned
- How to structure a full ARM template with parameters, variables, resources, and outputs.  
- Importance of linking resources (Subnet → Route Table).  
- Using outputs to make deployments reusable in larger projects.

---
