# AZ-104-Azure-Administrator-Lab
Hands-on Azure administration project aligned with AZ-104 domains such as identities and governance, storage, compute, virtual networking, monitoring, and backup.


## Objective

The goal of this project is to demonstrate practical Azure administration by deploying and managing a small but realistic Azure environment. This lab is designed to showcase core administrator responsibilities that map directly to AZ-104 skills.

## Lab Scope

This lab includes:

- Resource Group creation
- Virtual Network and Subnet configuration
- Network Security Group (NSG)
- Azure Virtual Machine deployment
- Storage Account deployment
- RBAC role assignment
- Basic monitoring using Azure Monitor
- Documentation of configuration and cost awareness

## Architecture

- **Resource Group:** central container for the lab
- **VNet/Subnet:** network segmentation for the workload
- **NSG:** traffic control
- **VM:** Windows or Linux Azure VM
- **Storage Account:** admin/storage service example
- **Azure Monitor:** metrics, logs, or alerts
- **RBAC:** least-privilege access demonstration

## Project Goals

- Create and manage Azure resources properly
- Configure virtual networking and secure access
- Deploy and validate a VM
- Implement basic governance with RBAC
- Deploy and validate Azure storage
- Monitor resource health and usage
- Document the setup clearly and professionally

## Technologies Used

- Microsoft Azure
- Azure Portal
- Azure Resource Groups
- Azure Virtual Network
- Network Security Group
- Azure Virtual Machines
- Azure Storage Account
- Azure Monitor
- RBAC / Entra ID
- Optional: Azure CLI or PowerShell

## Lab Steps

### 1. Create the resource group
- Create a dedicated resource group
- Apply a naming convention
- Add tags if possible

### 2. Configure networking
- Create a VNet
- Create at least one subnet
- Associate an NSG
- Define inbound rules carefully

### 3. Deploy the VM
- Create a Windows or Linux VM
- Place it in the correct subnet
- Test connectivity
- Review public/private IP configuration

### 4. Deploy storage
- Create a storage account
- Review performance and redundancy options
- Validate access controls or blob/container basics

### 5. Configure access and governance
- Assign a role using RBAC
- Document why that role was used
- Review least-privilege logic

### 6. Configure monitoring
- Enable Azure Monitor insights where possible
- Review VM metrics
- Add one basic alert if available
- Document what is being monitored

### 7. Cleanup and cost control
- Estimate the cost impact of resources
- Stop or deallocate the VM after testing
- Document cleanup steps

## Validation Checklist

- [ ] Resource group created
- [ ] VNet and subnet configured
- [ ] NSG created and associated
- [ ] VM deployed and reachable
- [ ] Storage account deployed
- [ ] RBAC role assigned
- [ ] Monitoring configured
- [ ] Screenshots captured
- [ ] README completed
- [ ] Cleanup documented

## Screenshots to Include

Store screenshots in `/screenshots` and reference them here:

- Resource group overview
- Virtual network and subnet
- NSG rules
- VM overview
- Storage account overview
- IAM / RBAC assignment
- Azure Monitor metrics or alert
- Cost/cleanup screen if possible

## Repository Structure

```text
.
├── README.md
├── screenshots/
├── docs/
│   ├── architecture-diagram.png
│   └── implementation-notes.md
└── scripts/
    ├── azure-cli/
    └── powershell/
```

## What I Learned

- How to deploy and manage core Azure infrastructure
- How network, compute, storage, and governance connect in Azure
- How RBAC and monitoring support operational administration
- How to present a lab as a professional portfolio project

## Improvements for Next Version

- Add backup and recovery configuration
- Add Azure Policy or tagging governance
- Add automation with Azure CLI, PowerShell, or Terraform
- Extend the project to a multi-VM or hub-spoke design

## Notes

This is a learning and portfolio lab built to demonstrate Azure administration skills aligned with AZ-104 objectives [web:88][web:85][web:86].
