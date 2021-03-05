---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/set-azmigrateserverreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Set-AzMigrateServerReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Set-AzMigrateServerReplication.md
ms.openlocfilehash: b87e541266c3ce555c0fc11910c9541914b14738
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009589"
---
# Set-AzMigrateServerReplication

## SYNOPSIS
Frissíti a replikáló kiszolgáló céltulajdonságokat.

## SZINTAXIS

### ByIDVMwareCbt (alapértelmezett)
```
Set-AzMigrateServerReplication -TargetObjectID <String> [-NicToUpdate <IVMwareCbtNicInput[]>]
 [-SubscriptionId <String>] [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetBootDiagnosticsStorageAccount <String>] [-TargetNetworkId <String>] [-TargetResourceGroupID <String>]
 [-TargetVMName <String>] [-TargetVMSize <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### ByInputObjectVMwareCbt
```
Set-AzMigrateServerReplication -InputObject <IMigrationItem> [-NicToUpdate <IVMwareCbtNicInput[]>]
 [-SubscriptionId <String>] [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetBootDiagnosticsStorageAccount <String>] [-TargetNetworkId <String>] [-TargetResourceGroupID <String>]
 [-TargetVMName <String>] [-TargetVMSize <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## LEÍRÁS
A Set-AzMigrateServerReplication parancsmag frissíti a replikáló kiszolgáló céltulajdonságokat.

## PÉLDÁK

### 1. példa: Frissítés azonosító szerint
```powershell
PS C:\> Set-AzMigrateServerReplication -TargetObjectID '/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_500f44f8-2aa3-587b-8958-ead358639629' -TargetVMName 'rb-w2k12r2-1'

ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Update
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : Update
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

Azonosító szerint.

## PARAMETERS

### -DefaultProfile
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Azt a replikáló kiszolgálót adja meg, amelynek a tulajdonságait frissíteni kell.
A kiszolgálóobjektum a Get-AzMigrateServerReplication le.
Ennek létrehozásáról az INPUTOBJECT tulajdonságokat és egy kivonattáblát a JEGYZETEK szakaszban talál.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IMigrationItem
Parameter Sets: ByInputObjectVMwareCbt
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NicToUpdate
Frissíti a nic for the Azure VM to be created.
Ennek létrehozásáról a NICTOUPDATE tulajdonságokAT és egy kivonattáblát hoz létre a MEGJEGYZÉSEK szakaszban található.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtNicInput[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
Az előfizetés azonosítója.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetAvailabilitySet
Megadja a VM-készítéshez használható rendelkezésre állási halmazt.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetAvailabilityZone
Megadja a VIRTUÁLIS gép létrehozásához használt rendelkezésre állási zónát.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetBootDiagnosticsStorageAccount
Megadja a rendszerindítási diagnosztikához használt tárfiókot.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetNetworkId
Frissíti a virtuális hálózat azonosítóját a cél Azure-előfizetésen belül, amelybe át kell telepíteni a kiszolgálót.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetObjectID
Megadja azt az újraplatkoló kiszolgálót, amelynek a tulajdonságait frissíteni kell.
Az azonosítót a Get-AzMigrateServerReplication kell lekérdezni.

```yaml
Type: System.String
Parameter Sets: ByIDVMwareCbt
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetResourceGroupID
Frissíti az erőforráscsoport azonosítóját a cél Azure-előfizetésen belül, amelybe át kell telepíteni a kiszolgálót.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetVMName
Megadja azt az újraplatkoló kiszolgálót, amelynek a tulajdonságait frissíteni kell.
Az azonosítót a Get-AzMigrateServerReplication kell lekérdezni.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetVMSize
Frissíti a létrehozni szükséges Azure VM termékváltozatát.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

## KIMENETEK

### Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob

## MEGJEGYZÉSEK

ALIASOK

COMPLEX PARAMETER PROPERTIES

Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat. A kivonattáblákról további információt a Get-Help about_Hash_Tables.


INPUTOBJECT: Azt a replikáló kiszolgálót adja meg, amelynek a tulajdonságait <IMigrationItem> frissíteni kell. A kiszolgálóobjektum a Get-AzMigrateServerReplication le.
  - `[Location <String>]`: Erőforrás helye
  - `[CurrentJobId <String>]`: A ARM feladat ARM azonosítója.
  - `[CurrentJobName <String>]`: A feladat neve.
  - `[CurrentJobStartTime <DateTime?>]`: A feladat kezdési ideje.
  - `[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: Az áttelepítési szolgáltató egyéni beállításai.

NICTOUPDATE <IVMwareCbtNicInput[]>: Frissíti a nic for the Azure VM to be created.
  - `IsPrimaryNic <String>`: Egy érték, amely azt jelzi, hogy ez az elsődleges NIC.
  - `NicId <String>`: A NIC-azonosító.
  - `[IsSelectedForMigration <String>]`: Egy érték, amely azt jelzi, hogy ez a NIC van-e kiválasztva az áttelepítéshez.
  - `[TargetStaticIPAddress <String>]`: A statikus IP-cím.
  - `[TargetSubnetName <String>]`: Cél alhálózat neve.

## KAPCSOLÓDÓ HIVATKOZÁSOK

