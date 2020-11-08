---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: F8418A93-8E6B-4A1C-B319-7CACE95AB600
online version: ''
schema: 2.0.0
ms.openlocfilehash: a1daf0cb8881beeb71f0b3fe68732d596c56ce12
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016240"
---
# Move-AzureService

## Áttekintés
Felhőalapú szolgáltatás áttelepítése az Azure Resource Manager-kötegbe.

## SZINTAXISA

### AbortMigrationParameterSet
```
Move-AzureService [-Abort] [-ServiceName] <String> [-DeploymentName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### CommitMigrationParameterSet
```
Move-AzureService [-Commit] [-ServiceName] <String> [-DeploymentName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### PrepareNewMigrationParameterSet
```
Move-AzureService [-Prepare] [-ServiceName] <String> [-DeploymentName] <String> [-CreateNewVirtualNetwork]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### PrepareExistingMigrationParameterSet
```
Move-AzureService [-Prepare] [-ServiceName] <String> [-DeploymentName] <String> [-UseExistingVirtualNetwork]
 [-VirtualNetworkResourceGroupName] <String> [-VirtualNetworkName] <String> [-SubnetName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### ValidateNewMigrationParameterSet
```
Move-AzureService [-Validate] [-ServiceName] <String> [-DeploymentName] <String> [-CreateNewVirtualNetwork]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### ValidateExistingMigrationParameterSet
```
Move-AzureService [-Validate] [-ServiceName] <String> [-DeploymentName] <String> [-UseExistingVirtualNetwork]
 [-VirtualNetworkResourceGroupName] <String> [-VirtualNetworkName] <String> [-SubnetName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## Leírás
A **Move-AzureService** parancsmag egy felhőalapú szolgáltatást és egy, a szolgáltatáson belüli központi üzembe helyezést áttelepít az Azure Resource Manager halom erőforrás csoportjába.

## Példák

### 1. példa: a szolgáltatás áttelepítésének előkészítése
```
PS C:\> Move-AzureService -Prepare -ServiceName "ContosoService" -DeploymentName "ContosoVM" -CreateNewVirtualNetwork
```

A parancs elkészíti a ContosoService nevű szolgáltatást az Azure Resource Manager-kötegbe való áttelepítéshez.
Az áttelepítés tartalmazza a ContosoVM nevű központi telepítőt.

### 2. példa: a szolgáltatás áttelepítésének megkezdése
```
PS C:\> Move-AzureService -Commit -ServiceName "ContosoService" -DeploymentName "ContosoVM"
```

Ez a parancs elindítja a ContosoService nevű szolgáltatás áttelepítését az Azure Resource Manager-kötegbe.
Az áttelepítés tartalmazza a ContosoVM nevű központi telepítőt.

### 3. példa: a szolgáltatás áttelepítésének visszavonása
```
PS C:\> Move-AzureService -Abort -ServiceName "ContosoService" -DeploymentName "ContosoVM"
```

Ez a parancs törli a ContosoService nevű szolgáltatás áttelepítését az Azure Resource Manager-kötegbe.

### 4. példa: a szolgáltatás áttelepítésének előkészítése meglévő virtuális hálózatra
```
PS C:\> Move-AzureService -Prepare -ServiceName "ContosoService" -DeploymentName "ContosoVM" -UseExistingVirtualNetwork -VirtualNetworkResourceGroupName "VnetRG" -VirtualNetworkName "ContosoVNET" -SubnetName "ContosoSubnet"
```

A parancs elkészíti a ContosoService nevű szolgáltatást az Azure Resource Manager-kötegbe való áttelepítéshez.
Az áttelepítés tartalmazza a ContosoVM nevű központi telepítőt.
Az áttelepítés a korábban létrehozott virtuális hálózatot használja.

### 5. példa: a szolgáltatás áttelepítésének ellenőrzése
```
PS C:\> Move-AzureService -Validate -ServiceName "ContosoService" -DeploymentName "ContosoVM" -CreateNewVirtualNetwork
```

Ez a parancs ellenőrzi a ContosoService nevű szolgáltatás áttelepítését az Azure Resource Manager-kötegbe.
Az áttelepítés tartalmazza a ContosoVM nevű központi telepítőt.

### Példa 6: a szolgáltatás áttelepítése meglévő virtuális hálózatba
```
PS C:\> Move-AzureService -Validate -ServiceName "contosoService" -DeploymentName "contosoVM" -UseExistingVirtualNetwork -VirtualNetworkResourceGroupName "vnetRG" -VirtualNetworkName "contosoVNET" -SubnetName "contosoSubnet"
```

Ez a parancs ellenőrzi a ContosoService nevű szolgáltatás áttelepítését az Azure Resource Manager-kötegbe.
Az áttelepítés tartalmazza a ContosoVM nevű központi telepítőt.
Az áttelepítés a korábban létrehozott virtuális hálózatot használja.

## PARAMÉTEREK

### -Megszakítás
Jelzi, hogy ez a parancsmag lemondja a szolgáltatás áttelepítését.

```yaml
Type: SwitchParameter
Parameter Sets: AbortMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Commit
Azt jelzi, hogy ez a parancsmag elindítja a szolgáltatás áttelepítését.

```yaml
Type: SwitchParameter
Parameter Sets: CommitMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CreateNewVirtualNetwork
Jelzi, hogy ez a parancsmag virtuális hálózatot hoz létre az Azure Resource Manager-kötegben.

```yaml
Type: SwitchParameter
Parameter Sets: PrepareNewMigrationParameterSet, ValidateNewMigrationParameterSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeploymentName
Annak a Felhőbeli szolgáltatásnak a nevét adja meg, amelyre a parancsmag át van telepítve.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationAction
Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.

A paraméter elfogadható értékei a következők:

- Folytassa
- Mellőzése
- Érdeklődni
- SilentlyContinue
- állj
- Felfüggesztheti

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Egy információs változót ad meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### – Előkészületek
Jelzi, hogy ez a parancsmag előkészíti a felhőalapú szolgáltatást az áttelepítésre.

```yaml
Type: SwitchParameter
Parameter Sets: PrepareNewMigrationParameterSet, PrepareExistingMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profil
Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.
Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Szolgáltatásnév
Annak a Felhőbeli szolgáltatásnak a nevét adja meg, amelyre a parancsmag át van telepítve.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SubnetName
A virtuális hálózaton belüli alhálózat nevét adja meg.

```yaml
Type: String
Parameter Sets: PrepareExistingMigrationParameterSet, ValidateExistingMigrationParameterSet
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseExistingVirtualNetwork
Jelzi, hogy ez a parancsmag áttelepíti a felhőalapú szolgáltatást egy meglévő virtuális hálózatra az Azure Resource Manager-kötegben.

```yaml
Type: SwitchParameter
Parameter Sets: PrepareExistingMigrationParameterSet, ValidateExistingMigrationParameterSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### – Érvényesítés
Azt adja meg, hogy ez a parancsmag ellenőrzi-e a felhőalapú szolgáltatást az áttelepítéshez.

```yaml
Type: SwitchParameter
Parameter Sets: ValidateNewMigrationParameterSet, ValidateExistingMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VirtualNetworkName
A virtuális hálózat nevét adja meg.

```yaml
Type: String
Parameter Sets: PrepareExistingMigrationParameterSet, ValidateExistingMigrationParameterSet
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VirtualNetworkResourceGroupName
Egy meglévő virtuális hálózat erőforráscsoport-csoportjának nevét adja meg.

```yaml
Type: String
Parameter Sets: PrepareExistingMigrationParameterSet, ValidateExistingMigrationParameterSet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Move-AzureNetworkSecurityGroup](./Move-AzureNetworkSecurityGroup.md)

[Move-AzureReservedIP](./Move-AzureReservedIP.md)

[Move-AzureRouteTable](./Move-AzureRouteTable.md)

[Move-AzureStorageAccount](./Move-AzureStorageAccount.md)

[Move-AzureVirtualNetwork](./Move-AzureVirtualNetwork.md)


