RG-Pharmasy (South Africa North)
┌───────────────┐     ┌───────────────┐     ┌───────────────┐
│    DC01       │     │   SEA-ADM1    │     │ VM-AZ104-01   │
│  (Win - Arrêté)│     │(Win - Arrêté)  │     │(Linux - Arrêté)│
└──────┬────────┘     └──────┬─────────┘     └──────┬─────────┘
       │ NSG                 │ NSG                   │ NSG
┌──────▼─────────────────────▼───────────────────────▼─────────┐
│                    SEA-DC1VNET 10.0.0.0/16                   │
│   default /24    DevSubnet /24    ProdSubnet /24            │
└──────────────────────────────┬───────────────────────────────┘
                               │
                    ┌──────────▼─────────────┐
                    │ staz104lab012          │
                    │ Storage Account (LRS)  │
                    └────────────────────────┘
Azure Monitor → Alerte CPU VM-AZ104-01: >80% Critique
RBAC → staz104lab012: 7 attributions Lecteur Blob
