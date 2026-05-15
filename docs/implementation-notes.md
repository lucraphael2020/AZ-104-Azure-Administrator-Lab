# AZ-104-Azure-Administrator-Lab
## Procédure de nettoyage (Cost Control)

### Arrêter la VM
Via le portail: Machines virtuelles > VM-AZ104-01 > Arrêter
ou via CLI: az vm deallocate --resource-group RG-Pharmasy --name VM-AZ104-01

### Supprimer le Storage Account (si plus requis)
Via le portail: Comptes de stockage > staz104lab012 > Supprimer
ou via CLI: az storage account delete --name staz104lab012 --resource-group RG-Pharmasy

### Supprimer l'alerte
VM > Supervision > Alertes > VM-AZ104-01-CPU-High > Supprimer

### Vérifier les coûts
Gestion des coûts + facturation > Vue d'ensemble

### Coût mensuel estimé (VM allouée): ~7,10 CAD/mois
### Coût avec VM arrêtée: ~2 CAD/mois

Note: Toutes les ressources sont taguées Project = AZ104-Lab
