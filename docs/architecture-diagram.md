# RG-Pharmasy Architecture Diagram - AZ-104 Lab

## Azure Resource Group: RG-Pharmasy

```mermaid
flowchart TB
    subgraph AZURE["Azure South Africa North"]
        direction TB
        
        subgraph RG["RG-Pharmasy"]
            direction TB
            
            subgraph VNET["SEA-DC1VNET 10.0.0.0/16"]
                direction LR
                
                subgraph SUB1["default /24"]
                    DC01["DC01"]
                end
                
                subgraph SUB2["DevSubnet /24"]
                    SEAA["SEA-ADM1"]
                end
                
                subgraph SUB3["ProdSubnet /24"]
                    VM["VM-AZ104-01"]
                end
            end
            
            VNET --- NSG1["NSG-DC01"]
            VNET --- NSG2["NSG-ADM1"]
            VNET --- NSG3["NSG-AZ104"]
            
            subgraph STORAGE["Storage"]
                STA["staz104lab012 LRS"]
            end
            
            subgraph MONITOR["Monitoring"]
                ALRT["Azure Monitor Alert CPU >80%"]
                RBAC["RBAC 7 Lecteur Blob"]
            end
        end
    end
    
    NSG1 --> DC01
    NSG2 --> SEAA
    NSG3 --> VM
    RBAC --> STA
    ALRT --> VM
```

## Resource Map

| Subgraph | Component | Type | Details |
|---|---|---|---|
| **RG-Pharmasy** | Resource Group | RG | Azure South Africa North |
| **SEA-DC1VNET** | Virtual Network | VNet | 10.0.0.0/16 |
| | default /24 | Subnet | DC01 host subnet |
| | DevSubnet /24 | Subnet | SEA-ADM1 dev subnet |
| | ProdSubnet /24 | Subnet | VM-AZ104-01 prod subnet |
| **Compute** | DC01 | VM | Windows Server - Stopped |
| | SEA-ADM1 | VM | Windows Server - Stopped |
| | VM-AZ104-01 | VM | Linux - Stopped |
| **Storage** | staz104lab012 | Storage Account | LRS Blob Storage |
| **Network** | NSG-DC01 | NSG | DC01 NSG |
| | NSG-ADM1 | NSG | SEA-ADM1 NSG |
| | NSG-AZ104 | NSG | VM-AZ104-01 NSG |
| **Monitor** | Azure Monitor | Monitor | CPU Alert > 80% |
| | RBAC | Access Control | 7 Lecteur Blob assignments |
