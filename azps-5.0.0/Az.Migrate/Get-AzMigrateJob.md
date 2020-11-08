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
# <span data-ttu-id="16c1e-101">Get-AzMigrateJob</span><span class="sxs-lookup"><span data-stu-id="16c1e-101">Get-AzMigrateJob</span></span>

## <span data-ttu-id="16c1e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="16c1e-102">SYNOPSIS</span></span>
<span data-ttu-id="16c1e-103">Beolvassa az Azure áttelepítési feladat állapotát.</span><span class="sxs-lookup"><span data-stu-id="16c1e-103">Retrieves the status of an Azure Migrate job.</span></span>

## <span data-ttu-id="16c1e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="16c1e-104">SYNTAX</span></span>

### <span data-ttu-id="16c1e-105">ListByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="16c1e-105">ListByName (Default)</span></span>
```
Get-AzMigrateJob -ProjectName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="16c1e-106">GetById</span><span class="sxs-lookup"><span data-stu-id="16c1e-106">GetById</span></span>
```
Get-AzMigrateJob -JobID <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="16c1e-107">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="16c1e-107">GetByInputObject</span></span>
```
Get-AzMigrateJob -InputObject <IJob> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="16c1e-108">GetByName</span><span class="sxs-lookup"><span data-stu-id="16c1e-108">GetByName</span></span>
```
Get-AzMigrateJob -JobName <String> -ProjectName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="16c1e-109">ListById</span><span class="sxs-lookup"><span data-stu-id="16c1e-109">ListById</span></span>
```
Get-AzMigrateJob -ProjectID <String> -ResourceGroupID <String> [-SubscriptionId <String>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="16c1e-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="16c1e-110">DESCRIPTION</span></span>
<span data-ttu-id="16c1e-111">A Get-AzMigrateJob parancsmag az Azure áttelepítési feladat állapotát ismerteti.</span><span class="sxs-lookup"><span data-stu-id="16c1e-111">The Get-AzMigrateJob cmdlet retrives the status of an Azure Migrate job.</span></span>

## <span data-ttu-id="16c1e-112">Példák</span><span class="sxs-lookup"><span data-stu-id="16c1e-112">EXAMPLES</span></span>

### <span data-ttu-id="16c1e-113">Példa 1: Get by Job ID</span><span class="sxs-lookup"><span data-stu-id="16c1e-113">Example 1: Get By Job Id</span></span>
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

<span data-ttu-id="16c1e-114">Ezzel az azonosítóval beolvassa a feladatot.</span><span class="sxs-lookup"><span data-stu-id="16c1e-114">This retrieves a job by it's Id.</span></span>

### <span data-ttu-id="16c1e-115">2. példa: az erőforráscsoport és a projekt lista szerint</span><span class="sxs-lookup"><span data-stu-id="16c1e-115">Example 2: List by resource group and project</span></span>
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

<span data-ttu-id="16c1e-116">Ez a projekt minden feladatát bekapja.</span><span class="sxs-lookup"><span data-stu-id="16c1e-116">This gets all jobs in a project.</span></span>

### <span data-ttu-id="16c1e-117">3. példa: erőforrás csoport, projekt és feladat neve</span><span class="sxs-lookup"><span data-stu-id="16c1e-117">Example 3: Get by resource group, project and job name</span></span>
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

<span data-ttu-id="16c1e-118">Ez egy konkrét feladatot kap.</span><span class="sxs-lookup"><span data-stu-id="16c1e-118">This gets a specific job.</span></span>

## <span data-ttu-id="16c1e-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="16c1e-119">PARAMETERS</span></span>

### <span data-ttu-id="16c1e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16c1e-120">-DefaultProfile</span></span>
<span data-ttu-id="16c1e-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="16c1e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16c1e-122">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="16c1e-122">-Filter</span></span>
<span data-ttu-id="16c1e-123">OData-szűrési beállítások</span><span class="sxs-lookup"><span data-stu-id="16c1e-123">OData filter options.</span></span>

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

### <span data-ttu-id="16c1e-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="16c1e-124">-InputObject</span></span>
<span data-ttu-id="16c1e-125">A replikáló kiszolgáló projektfeladat-objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="16c1e-125">Specifies the job object of the replicating server.</span></span>
<span data-ttu-id="16c1e-126">A kivitelezéshez tekintse meg a INPUTOBJECT tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="16c1e-126">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="16c1e-127">-JobID</span><span class="sxs-lookup"><span data-stu-id="16c1e-127">-JobID</span></span>
<span data-ttu-id="16c1e-128">Annak a projektnek az azonosítóját adja meg, amelyhez a részleteket vissza kell olvasni.</span><span class="sxs-lookup"><span data-stu-id="16c1e-128">Specifies the job id for which the details needs to be retrieved.</span></span>

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

### <span data-ttu-id="16c1e-129">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="16c1e-129">-JobName</span></span>
<span data-ttu-id="16c1e-130">Projekt azonosítója</span><span class="sxs-lookup"><span data-stu-id="16c1e-130">Job identifier</span></span>

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

### <span data-ttu-id="16c1e-131">-ProjectID</span><span class="sxs-lookup"><span data-stu-id="16c1e-131">-ProjectID</span></span>
<span data-ttu-id="16c1e-132">Megadja az Azure áttelepítési projektet, amelyben a kiszolgálók replikálódnak.</span><span class="sxs-lookup"><span data-stu-id="16c1e-132">Specifies the Azure Migrate Project in which servers are replicating.</span></span>

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

### <span data-ttu-id="16c1e-133">-Projektnév</span><span class="sxs-lookup"><span data-stu-id="16c1e-133">-ProjectName</span></span>
<span data-ttu-id="16c1e-134">Az áttelepítési projekt neve.</span><span class="sxs-lookup"><span data-stu-id="16c1e-134">The name of the migrate project.</span></span>

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

### <span data-ttu-id="16c1e-135">-ResourceGroupID</span><span class="sxs-lookup"><span data-stu-id="16c1e-135">-ResourceGroupID</span></span>
<span data-ttu-id="16c1e-136">A jelenlegi előfizetésben az Azure áttelepítési projekt erőforrás csoportját adja meg.</span><span class="sxs-lookup"><span data-stu-id="16c1e-136">Specifies the Resource Group of the Azure Migrate Project in the current subscription.</span></span>

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

### <span data-ttu-id="16c1e-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16c1e-137">-ResourceGroupName</span></span>
<span data-ttu-id="16c1e-138">Annak az erőforráscsoportnek a neve, amelyben a helyreállítási szolgáltatások boltozata található.</span><span class="sxs-lookup"><span data-stu-id="16c1e-138">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="16c1e-139">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="16c1e-139">-SubscriptionId</span></span>
<span data-ttu-id="16c1e-140">Azure-előfizetési azonosító</span><span class="sxs-lookup"><span data-stu-id="16c1e-140">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="16c1e-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16c1e-141">CommonParameters</span></span>
<span data-ttu-id="16c1e-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="16c1e-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16c1e-143">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="16c1e-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16c1e-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="16c1e-144">INPUTS</span></span>

## <span data-ttu-id="16c1e-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="16c1e-145">OUTPUTS</span></span>

### <span data-ttu-id="16c1e-146">Microsoft. Azure. PowerShell. parancsmagok. áttelepítés. models. Api20180110. IJob</span><span class="sxs-lookup"><span data-stu-id="16c1e-146">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="16c1e-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="16c1e-147">NOTES</span></span>

<span data-ttu-id="16c1e-148">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="16c1e-148">ALIASES</span></span>

<span data-ttu-id="16c1e-149">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="16c1e-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="16c1e-150">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="16c1e-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="16c1e-151">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="16c1e-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="16c1e-152">INPUTOBJECT <IJob> : a replikált kiszolgáló projektfeladat-objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="16c1e-152">INPUTOBJECT <IJob>: Specifies the job object of the replicating server.</span></span>
  - <span data-ttu-id="16c1e-153">`[Location <String>]`: Erőforrás helye</span><span class="sxs-lookup"><span data-stu-id="16c1e-153">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="16c1e-154">`[ActivityId <String>]`: A tevékenység azonosítója.</span><span class="sxs-lookup"><span data-stu-id="16c1e-154">`[ActivityId <String>]`: The activity id.</span></span>
  - <span data-ttu-id="16c1e-155">`[AllowedAction <String[]>]`: Az engedélyezett műveletek a feladatra.</span><span class="sxs-lookup"><span data-stu-id="16c1e-155">`[AllowedAction <String[]>]`: The Allowed action the job.</span></span>
  - <span data-ttu-id="16c1e-156">`[CustomDetailAffectedObjectDetail <IJobDetailsAffectedObjectDetails>]`: A munkafolyamat-objektum részletei alapján az érintett objektum tulajdonságai, például a forráskiszolgáló, a forrás felhő, a célkiszolgáló, a cél felhő stb.</span><span class="sxs-lookup"><span data-stu-id="16c1e-156">`[CustomDetailAffectedObjectDetail <IJobDetailsAffectedObjectDetails>]`: The affected object properties like source server, source cloud, target server, target cloud etc. based on the workflow object details.</span></span>
    - <span data-ttu-id="16c1e-157">`[(Any) <String>]`: Ez azt jelzi, hogy az objektumhoz bármely tulajdonság hozzá lehet adni.</span><span class="sxs-lookup"><span data-stu-id="16c1e-157">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="16c1e-158">`[EndTime <DateTime?>]`: A befejezési idő.</span><span class="sxs-lookup"><span data-stu-id="16c1e-158">`[EndTime <DateTime?>]`: The end time.</span></span>
  - <span data-ttu-id="16c1e-159">`[Error <IJobErrorDetails[]>]`: A hibák.</span><span class="sxs-lookup"><span data-stu-id="16c1e-159">`[Error <IJobErrorDetails[]>]`: The errors.</span></span>
    - <span data-ttu-id="16c1e-160">`[CreationTime <DateTime?>]`: A munkahelyi hiba létrehozásának időpontja.</span><span class="sxs-lookup"><span data-stu-id="16c1e-160">`[CreationTime <DateTime?>]`: The creation time of job error.</span></span>
    - <span data-ttu-id="16c1e-161">`[ErrorLevel <String>]`: Hiba szintje.</span><span class="sxs-lookup"><span data-stu-id="16c1e-161">`[ErrorLevel <String>]`: Error level of error.</span></span>
    - <span data-ttu-id="16c1e-162">`[ProviderErrorDetailErrorCode <Int32?>]`: A hibakód.</span><span class="sxs-lookup"><span data-stu-id="16c1e-162">`[ProviderErrorDetailErrorCode <Int32?>]`: The Error code.</span></span>
    - <span data-ttu-id="16c1e-163">`[ProviderErrorDetailErrorId <String>]`: A szolgáltató hibakezelő azonosítója.</span><span class="sxs-lookup"><span data-stu-id="16c1e-163">`[ProviderErrorDetailErrorId <String>]`: The Provider error Id.</span></span>
    - <span data-ttu-id="16c1e-164">`[ProviderErrorDetailErrorMessage <String>]`: A hibaüzenetet jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="16c1e-164">`[ProviderErrorDetailErrorMessage <String>]`: The Error message.</span></span>
    - <span data-ttu-id="16c1e-165">`[ProviderErrorDetailPossibleCaus <String>]`: A hiba lehetséges okai.</span><span class="sxs-lookup"><span data-stu-id="16c1e-165">`[ProviderErrorDetailPossibleCaus <String>]`: The possible causes for the error.</span></span>
    - <span data-ttu-id="16c1e-166">`[ProviderErrorDetailRecommendedAction <String>]`: A hiba elhárításához javasolt teendő.</span><span class="sxs-lookup"><span data-stu-id="16c1e-166">`[ProviderErrorDetailRecommendedAction <String>]`: The recommended action to resolve the error.</span></span>
    - <span data-ttu-id="16c1e-167">`[ServiceErrorDetailActivityId <String>]`: Tevékenység azonosítója.</span><span class="sxs-lookup"><span data-stu-id="16c1e-167">`[ServiceErrorDetailActivityId <String>]`: Activity Id.</span></span>
    - <span data-ttu-id="16c1e-168">`[ServiceErrorDetailCode <String>]`: Hibakód.</span><span class="sxs-lookup"><span data-stu-id="16c1e-168">`[ServiceErrorDetailCode <String>]`: Error code.</span></span>
    - <span data-ttu-id="16c1e-169">`[ServiceErrorDetailMessage <String>]`: Hibaüzenet.</span><span class="sxs-lookup"><span data-stu-id="16c1e-169">`[ServiceErrorDetailMessage <String>]`: Error message.</span></span>
    - <span data-ttu-id="16c1e-170">`[ServiceErrorDetailPossibleCaus <String>]`: A hiba lehetséges okai.</span><span class="sxs-lookup"><span data-stu-id="16c1e-170">`[ServiceErrorDetailPossibleCaus <String>]`: Possible causes of error.</span></span>
    - <span data-ttu-id="16c1e-171">`[ServiceErrorDetailRecommendedAction <String>]`: A hiba elhárításához javasolt műveletek.</span><span class="sxs-lookup"><span data-stu-id="16c1e-171">`[ServiceErrorDetailRecommendedAction <String>]`: Recommended action to resolve error.</span></span>
    - <span data-ttu-id="16c1e-172">`[TaskId <String>]`: A tevékenység azonosítója.</span><span class="sxs-lookup"><span data-stu-id="16c1e-172">`[TaskId <String>]`: The Id of the task.</span></span>
  - <span data-ttu-id="16c1e-173">`[FriendlyName <String>]`: A DisplayName.</span><span class="sxs-lookup"><span data-stu-id="16c1e-173">`[FriendlyName <String>]`: The DisplayName.</span></span>
  - <span data-ttu-id="16c1e-174">`[ScenarioName <String>]`: A ScenarioName.</span><span class="sxs-lookup"><span data-stu-id="16c1e-174">`[ScenarioName <String>]`: The ScenarioName.</span></span>
  - <span data-ttu-id="16c1e-175">`[StartTime <DateTime?>]`: A kezdés időpontja.</span><span class="sxs-lookup"><span data-stu-id="16c1e-175">`[StartTime <DateTime?>]`: The start time.</span></span>
  - <span data-ttu-id="16c1e-176">`[State <String>]`: A feladat állapota.</span><span class="sxs-lookup"><span data-stu-id="16c1e-176">`[State <String>]`: The status of the Job.</span></span> <span data-ttu-id="16c1e-177">Az alábbi értékek egyike: NotStarted, inelőrehaladás, sikeres, sikertelen, lemondott, felfüggesztett vagy egyéb.</span><span class="sxs-lookup"><span data-stu-id="16c1e-177">It is one of these values - NotStarted, InProgress, Succeeded, Failed, Cancelled, Suspended or Other.</span></span>
  - <span data-ttu-id="16c1e-178">`[StateDescription <String>]`: A feladat állapotának leírása.</span><span class="sxs-lookup"><span data-stu-id="16c1e-178">`[StateDescription <String>]`: The description of the state of the Job.</span></span> <span data-ttu-id="16c1e-179">Például a sikeres állapot eléréséhez a Leírás elvégezhető, PartiallySucceeded, CompletedWithInformation vagy kihagyható.</span><span class="sxs-lookup"><span data-stu-id="16c1e-179">For e.g. - For Succeeded state, description can be Completed, PartiallySucceeded, CompletedWithInformation or Skipped.</span></span>
  - <span data-ttu-id="16c1e-180">`[TargetInstanceType <String>]`: Az érintett objektum típusa ({Microsoft.Azure.SiteRecovery.V2015_11_10. AffectedObjectType} osztály).</span><span class="sxs-lookup"><span data-stu-id="16c1e-180">`[TargetInstanceType <String>]`: The type of the affected object which is of {Microsoft.Azure.SiteRecovery.V2015_11_10.AffectedObjectType} class.</span></span>
  - <span data-ttu-id="16c1e-181">`[TargetObjectId <String>]`: Az érintett Object id.</span><span class="sxs-lookup"><span data-stu-id="16c1e-181">`[TargetObjectId <String>]`: The affected Object Id.</span></span>
  - <span data-ttu-id="16c1e-182">`[TargetObjectName <String>]`: Az érintett objektum neve.</span><span class="sxs-lookup"><span data-stu-id="16c1e-182">`[TargetObjectName <String>]`: The name of the affected object.</span></span>
  - <span data-ttu-id="16c1e-183">`[Task <IAsrTask[]>]`: A feladatok.</span><span class="sxs-lookup"><span data-stu-id="16c1e-183">`[Task <IAsrTask[]>]`: The tasks.</span></span>
    - <span data-ttu-id="16c1e-184">`[AllowedAction <String[]>]`: A feladatra vonatkozó állam/műveletek.</span><span class="sxs-lookup"><span data-stu-id="16c1e-184">`[AllowedAction <String[]>]`: The state/actions applicable on this task.</span></span>
    - <span data-ttu-id="16c1e-185">`[CustomDetailInstanceType <String>]`: A tevékenység részleteinek típusa.</span><span class="sxs-lookup"><span data-stu-id="16c1e-185">`[CustomDetailInstanceType <String>]`: The type of task details.</span></span>
    - <span data-ttu-id="16c1e-186">`[EndTime <DateTime?>]`: A befejezési idő.</span><span class="sxs-lookup"><span data-stu-id="16c1e-186">`[EndTime <DateTime?>]`: The end time.</span></span>
    - <span data-ttu-id="16c1e-187">`[Error <IJobErrorDetails[]>]`: A tevékenység hibájának részletei.</span><span class="sxs-lookup"><span data-stu-id="16c1e-187">`[Error <IJobErrorDetails[]>]`: The task error details.</span></span>
    - <span data-ttu-id="16c1e-188">`[FriendlyName <String>]`: A név.</span><span class="sxs-lookup"><span data-stu-id="16c1e-188">`[FriendlyName <String>]`: The name.</span></span>
    - <span data-ttu-id="16c1e-189">`[GroupTaskCustomDetailChildTask <IAsrTask[]>]`: A Child Tasks.</span><span class="sxs-lookup"><span data-stu-id="16c1e-189">`[GroupTaskCustomDetailChildTask <IAsrTask[]>]`: The child tasks.</span></span>
    - <span data-ttu-id="16c1e-190">`[GroupTaskCustomDetailInstanceType <String>]`: A tevékenység részleteinek típusa.</span><span class="sxs-lookup"><span data-stu-id="16c1e-190">`[GroupTaskCustomDetailInstanceType <String>]`: The type of task details.</span></span>
    - <span data-ttu-id="16c1e-191">`[Name <String>]`: Az egyedi tevékenység neve.</span><span class="sxs-lookup"><span data-stu-id="16c1e-191">`[Name <String>]`: The unique Task name.</span></span>
    - <span data-ttu-id="16c1e-192">`[StartTime <DateTime?>]`: A kezdés időpontja.</span><span class="sxs-lookup"><span data-stu-id="16c1e-192">`[StartTime <DateTime?>]`: The start time.</span></span>
    - <span data-ttu-id="16c1e-193">`[State <String>]`: Az állam.</span><span class="sxs-lookup"><span data-stu-id="16c1e-193">`[State <String>]`: The State.</span></span> <span data-ttu-id="16c1e-194">Az alábbi értékek egyike: NotStarted, inelőrehaladás, sikeres, sikertelen, lemondott, felfüggesztett vagy egyéb.</span><span class="sxs-lookup"><span data-stu-id="16c1e-194">It is one of these values - NotStarted, InProgress, Succeeded, Failed, Cancelled, Suspended or Other.</span></span>
    - <span data-ttu-id="16c1e-195">`[StateDescription <String>]`: A tevékenység állapotának leírása.</span><span class="sxs-lookup"><span data-stu-id="16c1e-195">`[StateDescription <String>]`: The description of the task state.</span></span> <span data-ttu-id="16c1e-196">A sikeres állapothoz például a Leírás elvégezhető, PartiallySucceeded, CompletedWithInformation vagy kihagyható.</span><span class="sxs-lookup"><span data-stu-id="16c1e-196">For example - For Succeeded state, description can be Completed, PartiallySucceeded, CompletedWithInformation or Skipped.</span></span>
    - <span data-ttu-id="16c1e-197">`[TaskId <String>]`: Az azonosító.</span><span class="sxs-lookup"><span data-stu-id="16c1e-197">`[TaskId <String>]`: The Id.</span></span>
    - <span data-ttu-id="16c1e-198">`[TaskType <String>]`: A tevékenység típusa.</span><span class="sxs-lookup"><span data-stu-id="16c1e-198">`[TaskType <String>]`: The type of task.</span></span> <span data-ttu-id="16c1e-199">Az CustomDetails tulajdonság részletei az adott típustól függnek.</span><span class="sxs-lookup"><span data-stu-id="16c1e-199">Details in CustomDetails property depend on this type.</span></span>

## <span data-ttu-id="16c1e-200">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="16c1e-200">RELATED LINKS</span></span>

