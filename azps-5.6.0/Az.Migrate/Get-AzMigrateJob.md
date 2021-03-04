---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/get-azmigratejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateJob.md
ms.openlocfilehash: 9521e069f0b472353403a16caffad86e1147c1fe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934090"
---
# Get-AzMigrateJob

## SYNOPSIS
Egy Azure-áttelepítési feladat állapotát olvassa be.

## SZINTAXIS

### ListByName (alapértelmezett)
```
Get-AzMigrateJob -ProjectName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetById
```
Get-AzMigrateJob -JobID <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetByInputObject
```
Get-AzMigrateJob -InputObject <IJob> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### GetByName
```
Get-AzMigrateJob -JobName <String> -ProjectName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### ListById
```
Get-AzMigrateJob -ProjectID <String> -ResourceGroupID <String> [-SubscriptionId <String>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## LEÍRÁS
A Get-AzMigrateJob parancsmag lekérte egy Azure-áttelepítési feladat állapotát.

## PÉLDÁK

### 1. példa: Get By Job Id
```powershell
PS C:\> Get-AzMigrateJob -JobID "/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/997e2a92-5afe-49c7-a81a-89660aec9b7b" 

ActivityId                       : 68af14b4-46ae-48d1-b3e9-cdcffb9e8a93 ActivityId: 74d1a396-1d37-4264-8a5b-b727aaef0171
AllowedAction                    : {}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          : 9/16/20 11:57:33 AM
Error                            : {}
FriendlyName                     : Associate replication policy
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/997e2a92-5afe-49c7-a81a-89660aec9b7b
Location                         :
Name                             : 997e2a92-5afe-49c7-a81a-89660aec9b7b
ScenarioName                     : AssociateProtectionProfile
StartTime                        : 9/16/20 11:57:32 AM
State                            : Succeeded
StateDescription                 : Completed
TargetInstanceType               : ProtectionProfile
TargetObjectId                   : 42752b89-5fad-52fd-bf93-679fbdb6fed9
TargetObjectName                 : migrateAzMigratePWSHTc8d1sitepolicy
Task                             : {CloudPairingPrerequisitesCheck, CloudPairingPrepareSite}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

Ez a feladat az azonosító alapján olvassa be a feladatot.

### 2. példa: Lista erőforráscsoportok és projektek szerint
```powershell
PS C:\> Get-AzMigrateJob -ResourceGroupName 'azmigratepwshtestasr13072020' -ProjectName 'AzMigrateTestProjectPWSH'

ActivityId                       :
AllowedAction                    : {}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         :
EndTime                          : 9/21/20 4:13:40 PM
Error                            : {}
FriendlyName                     : Update the virtual machine
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/1c89e38e-34ec-4903-aa7c-115201bf2de1
Location                         :
Name                             : 1c89e38e-34ec-4903-aa7c-115201bf2de1
ScenarioName                     : UpdateVmProperties
StartTime                        : 9/21/20 4:13:34 PM
State                            : Succeeded
StateDescription                 : Completed
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 593b735d-2a34-53b2-b8ed-e33da5650703
TargetObjectName                 : rb-w2k12r2-1
Task                             : {}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

Ez a projekt minden állását átveszi.

### 3. példa: Get by resource group, project and job name
```powershell
PS C:\> Get-AzMigrateJob -ResourceGroupName 'azmigratepwshtestasr13072020' -ProjectName 'AzMigrateTestProjectPWSH' -JobName 7ae1ee7c-442c-499d-8b0e-81d52a42b71e

ActivityId                       : 6986b7e5-0f1f-49d8-8b4b-77e6f66bcb92 ActivityId: eb73c6a1-7c66-469f-a853-d896aa38cc0f
AllowedAction                    : {}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          : 8/21/20 6:41:48 AM
Error                            : {}
FriendlyName                     : Create replication policy
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/7ae1ee7c-442c-499d-8b0e-81d52a42b71e
Location                         :
Name                             : 7ae1ee7c-442c-499d-8b0e-81d52a42b71e
ScenarioName                     : AddProtectionProfile
StartTime                        : 8/21/20 6:41:48 AM
State                            : Succeeded
StateDescription                 : Completed
TargetInstanceType               : ProtectionProfile
TargetObjectId                   : 18b2ccec-e39a-517b-ae5d-dd395e9f4f96
TargetObjectName                 : samplePolicy3
Task                             : {AddProtectionProfilePreflightsCheckTask, AddProtectionProfileTask}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

Ez egy adott feladatot kap.

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

### -Filter
OData-szűrési beállítások.

```yaml
Type: System.String
Parameter Sets: ListById, ListByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
A replikáló kiszolgáló feladatobjektumát adja meg.
Ennek létrehozásáról az INPUTOBJECT tulajdonságokat és egy kivonattáblát a JEGYZETEK szakaszban talál.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob
Parameter Sets: GetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobID
Megadja azt a feladatazonosítót, amelynek adatait le kellkérni.

```yaml
Type: System.String
Parameter Sets: GetById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobName
Feladat azonosítója

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProjectID
Azt az Azure-áttelepítési projektet adja meg, amelyben a kiszolgálók replikálnak.

```yaml
Type: System.String
Parameter Sets: ListById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProjectName
A projekt áttelepítésének neve.

```yaml
Type: System.String
Parameter Sets: GetByName, ListByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupID
Az aktuális előfizetés azure-áttelepítési projekt erőforráscsoportját határozza meg.

```yaml
Type: System.String
Parameter Sets: ListById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Annak az erőforráscsoportnak a neve, amelyben a helyreállítási szolgáltatások tárolója jelen van.

```yaml
Type: System.String
Parameter Sets: GetByName, ListByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
Azure-előfizetés azonosítója.

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

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

## KIMENETEK

### Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob

## MEGJEGYZÉSEK

ALIASOK

COMPLEX PARAMETER PROPERTIES

Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat. A kivonattáblákról további információt a Get-Help about_Hash_Tables.


INPUTOBJECT: A replikáló <IJob> kiszolgáló feladatobjektumát adja meg.
  - `[Location <String>]`: Erőforrás helye
  - `[ActivityId <String>]`: A tevékenységazonosító.
  - `[AllowedAction <String[]>]`: A feladat engedélyezett művelete.
  - `[CustomDetailAffectedObjectDetail <IJobDetailsAffectedObjectDetails>]`: Az érintett objektumtulajdonságok, például a forráskiszolgáló, a forrásfelhő, a célkiszolgáló, a célfelhő stb. a munkafolyamat-objektum adatai alapján.
    - `[(Any) <String>]`: Ez azt jelzi, hogy az objektumhoz bármilyen tulajdonság hozzáadható.
  - `[EndTime <DateTime?>]`: A záró időpont.
  - `[Error <IJobErrorDetails[]>]`: A hibák.
    - `[CreationTime <DateTime?>]`: A feladathiba létrehozási ideje.
    - `[ErrorLevel <String>]`: Hibaszint.
    - `[ProviderErrorDetailErrorCode <Int32?>]`: A hibakód.
    - `[ProviderErrorDetailErrorId <String>]`: A Szolgáltató hibaazonosítója.
    - `[ProviderErrorDetailErrorMessage <String>]`: A hibaüzenet.
    - `[ProviderErrorDetailPossibleCaus <String>]`: A hiba lehetséges okai.
    - `[ProviderErrorDetailRecommendedAction <String>]`: A hiba elhárításához javasolt művelet.
    - `[ServiceErrorDetailActivityId <String>]`: Tevékenységazonosító.
    - `[ServiceErrorDetailCode <String>]`: Hibakód.
    - `[ServiceErrorDetailMessage <String>]`: Hibaüzenet.
    - `[ServiceErrorDetailPossibleCaus <String>]`: A hiba lehetséges okai.
    - `[ServiceErrorDetailRecommendedAction <String>]`: Javasolt művelet a hiba elhárításához.
    - `[TaskId <String>]`: A tevékenység azonosítója.
  - `[FriendlyName <String>]`: A DisplayName.
  - `[ScenarioName <String>]`: A ScenarioName.
  - `[StartTime <DateTime?>]`: A kezdési időpont.
  - `[State <String>]`: A Feladat állapota. Ez az értékek egyike – NotStarted, InProgress, Succeeded, Failed, Cancelled, Suspended vagy Other.
  - `[StateDescription <String>]`: A feladat állapotának leírása. Például: - A sikeres állapothoz a leírás lehet Completed, PartiallySucceed, CompletedWithInformation vagy Skipped.
  - `[TargetInstanceType <String>]`: Az érintett objektum típusa, amely {Microsoft.Azure.SiteRecovery.V2015_11_10.AffectedObjectType} osztályba tartozik.
  - `[TargetObjectId <String>]`: Az érintett objektumazonosító.
  - `[TargetObjectName <String>]`: Az érintett objektum neve.
  - `[Task <IAsrTask[]>]`: A feladatok.
    - `[AllowedAction <String[]>]`: A tevékenységre vonatkozó állapot/műveletek.
    - `[CustomDetailInstanceType <String>]`: A tevékenység részleteinek típusa.
    - `[EndTime <DateTime?>]`: A záró időpont.
    - `[Error <IJobErrorDetails[]>]`: A feladathiba részletei.
    - `[FriendlyName <String>]`: A név.
    - `[GroupTaskCustomDetailChildTask <IAsrTask[]>]`: Gyermekfeladatok.
    - `[GroupTaskCustomDetailInstanceType <String>]`: A tevékenység részleteinek típusa.
    - `[Name <String>]`: Az egyedi tevékenység neve.
    - `[StartTime <DateTime?>]`: A kezdési időpont.
    - `[State <String>]`: Az állam. Ez az értékek egyike – NotStarted, InProgress, Succeeded, Failed, Cancelled, Suspended vagy Other.
    - `[StateDescription <String>]`: A tevékenységállapot leírása. A sikeres állapothoz például a leírás befejezve, részben sikeres, CompletedWithInformation vagy Kihagyva lehet.
    - `[TaskId <String>]`: Az azonosító.
    - `[TaskType <String>]`: A tevékenység típusa. A CustomDetails tulajdonság részletei ettől a típustól függnek.

## KAPCSOLÓDÓ HIVATKOZÁSOK

