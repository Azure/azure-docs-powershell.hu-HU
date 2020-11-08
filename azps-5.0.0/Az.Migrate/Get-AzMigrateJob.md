---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateJob.md
ms.openlocfilehash: bb28550a0b23fa9032832873a78771d25d2a38bd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195783"
---
# Get-AzMigrateJob

## Áttekintés
Beolvassa az Azure áttelepítési feladat állapotát.

## SZINTAXISA

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

## Leírás
A Get-AzMigrateJob parancsmag az Azure áttelepítési feladat állapotát ismerteti.

## Példák

### Példa 1: Get by Job ID
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

Ezzel az azonosítóval beolvassa a feladatot.

### 2. példa: az erőforráscsoport és a projekt lista szerint
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

Ez a projekt minden feladatát bekapja.

### 3. példa: erőforrás csoport, projekt és feladat neve
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

Ez egy konkrét feladatot kap.

## PARAMÉTEREK

### -DefaultProfile
Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

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

### -Szűrő
OData-szűrési beállítások

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
A replikáló kiszolgáló projektfeladat-objektumát adja meg.
A kivitelezéshez tekintse meg a INPUTOBJECT tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.

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
Annak a projektnek az azonosítóját adja meg, amelyhez a részleteket vissza kell olvasni.

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

### -Feladatnév
Projekt azonosítója

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
Megadja az Azure áttelepítési projektet, amelyben a kiszolgálók replikálódnak.

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

### -Projektnév
Az áttelepítési projekt neve.

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
A jelenlegi előfizetésben az Azure áttelepítési projekt erőforrás csoportját adja meg.

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
Annak az erőforráscsoportnek a neve, amelyben a helyreállítási szolgáltatások boltozata található.

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
Azure-előfizetési azonosító

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
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.

## BEMENETEK

## KIMENETEK

### Microsoft. Azure. PowerShell. parancsmagok. áttelepítés. models. Api20180110. IJob

## MEGJEGYZI

ALIASOK

KOMPLEX PARAMÉTEREK TULAJDONSÁGAI

Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot. A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.


INPUTOBJECT <IJob> : a replikált kiszolgáló projektfeladat-objektumát adja meg.
  - `[Location <String>]`: Erőforrás helye
  - `[ActivityId <String>]`: A tevékenység azonosítója.
  - `[AllowedAction <String[]>]`: Az engedélyezett műveletek a feladatra.
  - `[CustomDetailAffectedObjectDetail <IJobDetailsAffectedObjectDetails>]`: A munkafolyamat-objektum részletei alapján az érintett objektum tulajdonságai, például a forráskiszolgáló, a forrás felhő, a célkiszolgáló, a cél felhő stb.
    - `[(Any) <String>]`: Ez azt jelzi, hogy az objektumhoz bármely tulajdonság hozzá lehet adni.
  - `[EndTime <DateTime?>]`: A befejezési idő.
  - `[Error <IJobErrorDetails[]>]`: A hibák.
    - `[CreationTime <DateTime?>]`: A munkahelyi hiba létrehozásának időpontja.
    - `[ErrorLevel <String>]`: Hiba szintje.
    - `[ProviderErrorDetailErrorCode <Int32?>]`: A hibakód.
    - `[ProviderErrorDetailErrorId <String>]`: A szolgáltató hibakezelő azonosítója.
    - `[ProviderErrorDetailErrorMessage <String>]`: A hibaüzenetet jeleníti meg.
    - `[ProviderErrorDetailPossibleCaus <String>]`: A hiba lehetséges okai.
    - `[ProviderErrorDetailRecommendedAction <String>]`: A hiba elhárításához javasolt teendő.
    - `[ServiceErrorDetailActivityId <String>]`: Tevékenység azonosítója.
    - `[ServiceErrorDetailCode <String>]`: Hibakód.
    - `[ServiceErrorDetailMessage <String>]`: Hibaüzenet.
    - `[ServiceErrorDetailPossibleCaus <String>]`: A hiba lehetséges okai.
    - `[ServiceErrorDetailRecommendedAction <String>]`: A hiba elhárításához javasolt műveletek.
    - `[TaskId <String>]`: A tevékenység azonosítója.
  - `[FriendlyName <String>]`: A DisplayName.
  - `[ScenarioName <String>]`: A ScenarioName.
  - `[StartTime <DateTime?>]`: A kezdés időpontja.
  - `[State <String>]`: A feladat állapota. Az alábbi értékek egyike: NotStarted, inelőrehaladás, sikeres, sikertelen, lemondott, felfüggesztett vagy egyéb.
  - `[StateDescription <String>]`: A feladat állapotának leírása. Például a sikeres állapot eléréséhez a Leírás elvégezhető, PartiallySucceeded, CompletedWithInformation vagy kihagyható.
  - `[TargetInstanceType <String>]`: Az érintett objektum típusa ({Microsoft.Azure.SiteRecovery.V2015_11_10. AffectedObjectType} osztály).
  - `[TargetObjectId <String>]`: Az érintett Object id.
  - `[TargetObjectName <String>]`: Az érintett objektum neve.
  - `[Task <IAsrTask[]>]`: A feladatok.
    - `[AllowedAction <String[]>]`: A feladatra vonatkozó állam/műveletek.
    - `[CustomDetailInstanceType <String>]`: A tevékenység részleteinek típusa.
    - `[EndTime <DateTime?>]`: A befejezési idő.
    - `[Error <IJobErrorDetails[]>]`: A tevékenység hibájának részletei.
    - `[FriendlyName <String>]`: A név.
    - `[GroupTaskCustomDetailChildTask <IAsrTask[]>]`: A Child Tasks.
    - `[GroupTaskCustomDetailInstanceType <String>]`: A tevékenység részleteinek típusa.
    - `[Name <String>]`: Az egyedi tevékenység neve.
    - `[StartTime <DateTime?>]`: A kezdés időpontja.
    - `[State <String>]`: Az állam. Az alábbi értékek egyike: NotStarted, inelőrehaladás, sikeres, sikertelen, lemondott, felfüggesztett vagy egyéb.
    - `[StateDescription <String>]`: A tevékenység állapotának leírása. A sikeres állapothoz például a Leírás elvégezhető, PartiallySucceeded, CompletedWithInformation vagy kihagyható.
    - `[TaskId <String>]`: Az azonosító.
    - `[TaskType <String>]`: A tevékenység típusa. Az CustomDetails tulajdonság részletei az adott típustól függnek.

## KAPCSOLÓDÓ HIVATKOZÁSOK

