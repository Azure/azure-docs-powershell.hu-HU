---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/restart-azmigrateserverreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Restart-AzMigrateServerReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Restart-AzMigrateServerReplication.md
ms.openlocfilehash: 35bf416249f24d7158720e2a9c28230da3f4f291
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466318"
---
# <span data-ttu-id="5e7e0-101">Restart-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="5e7e0-101">Restart-AzMigrateServerReplication</span></span>

## <span data-ttu-id="5e7e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e7e0-102">SYNOPSIS</span></span>
<span data-ttu-id="5e7e0-103">A megadott kiszolgáló replikációjának újraindítása.</span><span class="sxs-lookup"><span data-stu-id="5e7e0-103">Restarts the replication for specified server.</span></span>

## <span data-ttu-id="5e7e0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5e7e0-104">SYNTAX</span></span>

### <span data-ttu-id="5e7e0-105">ByIDVMwareCbt (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5e7e0-105">ByIDVMwareCbt (Default)</span></span>
```
Restart-AzMigrateServerReplication -TargetObjectID <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5e7e0-106">ByInputObjectVMwareCbt</span><span class="sxs-lookup"><span data-stu-id="5e7e0-106">ByInputObjectVMwareCbt</span></span>
```
Restart-AzMigrateServerReplication -InputObject <IMigrationItem> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="5e7e0-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5e7e0-107">DESCRIPTION</span></span>
<span data-ttu-id="5e7e0-108">A Restart-AzMigrateServerReplication parancsmag kijavítja a replikációt a megadott kiszolgálóhoz.</span><span class="sxs-lookup"><span data-stu-id="5e7e0-108">The Restart-AzMigrateServerReplication cmdlet repairs the replication for the specified server.</span></span>

## <span data-ttu-id="5e7e0-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5e7e0-109">EXAMPLES</span></span>

### <span data-ttu-id="5e7e0-110">1. példa: Azonosító szerint.</span><span class="sxs-lookup"><span data-stu-id="5e7e0-110">Example 1: By id.</span></span>
```powershell
PS C:\> Restart-AzMigrateServerReplication -TargetObjectID "/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f"

ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Restart
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : Restart
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="5e7e0-111">Azonosító szerint.</span><span class="sxs-lookup"><span data-stu-id="5e7e0-111">By id.</span></span>

### <span data-ttu-id="5e7e0-112">2. példa: Bemeneti objektum alapján</span><span class="sxs-lookup"><span data-stu-id="5e7e0-112">Example 2: By Input Object</span></span>
```powershell
PS C:\> $obj = Get-AzMigrateServerReplication -TargetObjectID "/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f"
PS C:\> $output = Restart-AzMigrateServerReplication -InputObject $obj
ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Restart
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : Restart
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="5e7e0-113">Bemeneti objektum alapján.</span><span class="sxs-lookup"><span data-stu-id="5e7e0-113">By Input Object.</span></span>

## <span data-ttu-id="5e7e0-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5e7e0-114">PARAMETERS</span></span>

### <span data-ttu-id="5e7e0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e7e0-115">-DefaultProfile</span></span>
<span data-ttu-id="5e7e0-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5e7e0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e7e0-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5e7e0-117">-InputObject</span></span>
<span data-ttu-id="5e7e0-118">A replikáló kiszolgáló gépobjektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="5e7e0-118">Specifies the machine object of the replicating server.</span></span>
<span data-ttu-id="5e7e0-119">Ennek létrehozásáról az INPUTOBJECT tulajdonságokat és egy kivonattáblát a JEGYZETEK szakaszban talál.</span><span class="sxs-lookup"><span data-stu-id="5e7e0-119">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5e7e0-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5e7e0-120">-SubscriptionId</span></span>
<span data-ttu-id="5e7e0-121">Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="5e7e0-121">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="5e7e0-122">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="5e7e0-122">-TargetObjectID</span></span>
<span data-ttu-id="5e7e0-123">Megadja az újraszinkronizációs kiszolgálót, amelyre az újraszinkronizációt el kell indítani.</span><span class="sxs-lookup"><span data-stu-id="5e7e0-123">Specifies the replcating server for which the resync needs to be initiated.</span></span>
<span data-ttu-id="5e7e0-124">Az azonosítót a Get-AzMigrateServerReplication kell lekérdezni.</span><span class="sxs-lookup"><span data-stu-id="5e7e0-124">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="5e7e0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e7e0-125">CommonParameters</span></span>
<span data-ttu-id="5e7e0-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e7e0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e7e0-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5e7e0-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e7e0-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5e7e0-128">INPUTS</span></span>

## <span data-ttu-id="5e7e0-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5e7e0-129">OUTPUTS</span></span>

### <span data-ttu-id="5e7e0-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span><span class="sxs-lookup"><span data-stu-id="5e7e0-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="5e7e0-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5e7e0-131">NOTES</span></span>

<span data-ttu-id="5e7e0-132">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="5e7e0-132">ALIASES</span></span>

<span data-ttu-id="5e7e0-133">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="5e7e0-133">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5e7e0-134">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="5e7e0-134">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5e7e0-135">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5e7e0-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5e7e0-136">INPUTOBJECT: A replikáló <IMigrationItem> kiszolgáló gépobjektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="5e7e0-136">INPUTOBJECT <IMigrationItem>: Specifies the machine object of the replicating server.</span></span>
  - <span data-ttu-id="5e7e0-137">`[Location <String>]`: Erőforrás helye</span><span class="sxs-lookup"><span data-stu-id="5e7e0-137">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="5e7e0-138">`[CurrentJobId <String>]`: A ARM feladat ARM azonosítója.</span><span class="sxs-lookup"><span data-stu-id="5e7e0-138">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="5e7e0-139">`[CurrentJobName <String>]`: A feladat neve.</span><span class="sxs-lookup"><span data-stu-id="5e7e0-139">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="5e7e0-140">`[CurrentJobStartTime <DateTime?>]`: A feladat kezdési ideje.</span><span class="sxs-lookup"><span data-stu-id="5e7e0-140">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="5e7e0-141">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: Az áttelepítési szolgáltató egyéni beállításai.</span><span class="sxs-lookup"><span data-stu-id="5e7e0-141">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

## <span data-ttu-id="5e7e0-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5e7e0-142">RELATED LINKS</span></span>

