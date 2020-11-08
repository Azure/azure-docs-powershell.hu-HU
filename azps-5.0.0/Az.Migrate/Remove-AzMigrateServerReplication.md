---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/remove-azmigrateserverreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Remove-AzMigrateServerReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Remove-AzMigrateServerReplication.md
ms.openlocfilehash: e9e6d3f9c045b9ff9cc2d5a4860b2c7fc5559f14
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194337"
---
# <span data-ttu-id="df846-101">Remove-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="df846-101">Remove-AzMigrateServerReplication</span></span>

## <span data-ttu-id="df846-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="df846-102">SYNOPSIS</span></span>
<span data-ttu-id="df846-103">Leállítja az áttelepített kiszolgáló replikálását.</span><span class="sxs-lookup"><span data-stu-id="df846-103">Stops replication for the migrated server.</span></span>

## <span data-ttu-id="df846-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="df846-104">SYNTAX</span></span>

### <span data-ttu-id="df846-105">ByIDVMwareCbt (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="df846-105">ByIDVMwareCbt (Default)</span></span>
```
Remove-AzMigrateServerReplication -TargetObjectID <String> [-SubscriptionId <String>] [-ForceRemove <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="df846-106">ByInputObjectVMwareCbt</span><span class="sxs-lookup"><span data-stu-id="df846-106">ByInputObjectVMwareCbt</span></span>
```
Remove-AzMigrateServerReplication -InputObject <IMigrationItem> [-SubscriptionId <String>]
 [-ForceRemove <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="df846-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="df846-107">DESCRIPTION</span></span>
<span data-ttu-id="df846-108">A Remove-AzMigrateServerReplication parancsmag leállítja az áttelepített kiszolgálók replikálását.</span><span class="sxs-lookup"><span data-stu-id="df846-108">The Remove-AzMigrateServerReplication cmdlet stops the replication for a migrated server.</span></span>

## <span data-ttu-id="df846-109">Példák</span><span class="sxs-lookup"><span data-stu-id="df846-109">EXAMPLES</span></span>

### <span data-ttu-id="df846-110">1. példa: eltávolítás azonosítóval</span><span class="sxs-lookup"><span data-stu-id="df846-110">Example 1: Remove by id.</span></span>
```powershell
PS C:\> Remove-AzMigrateServerReplication -TargetObjectID "/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f"

ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Disable
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : Disable
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs

```

<span data-ttu-id="df846-111">Újraszinkronizálás azonosítóval</span><span class="sxs-lookup"><span data-stu-id="df846-111">Resync by id.</span></span>

### <span data-ttu-id="df846-112">2. példa: beviteli objektum szerinti eltávolítás</span><span class="sxs-lookup"><span data-stu-id="df846-112">Example 2: Remove by Input Object</span></span>
```powershell
PS C:\> $obj = Get-AzMigrateServerReplication -TargetObjectID "/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f"
PS C:\> Remove-AzMigrateServerReplication -InputObject $obj


ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Disable
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : Disable
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="df846-113">Név szerint.</span><span class="sxs-lookup"><span data-stu-id="df846-113">By name.</span></span>

## <span data-ttu-id="df846-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="df846-114">PARAMETERS</span></span>

### <span data-ttu-id="df846-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df846-115">-DefaultProfile</span></span>
<span data-ttu-id="df846-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="df846-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df846-117">-ForceRemove</span><span class="sxs-lookup"><span data-stu-id="df846-117">-ForceRemove</span></span>
<span data-ttu-id="df846-118">Azt adja meg, hogy a replikációt kényszeríteni kell-e.</span><span class="sxs-lookup"><span data-stu-id="df846-118">Specifies whether the replication needs to be force removed.</span></span>

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

### <span data-ttu-id="df846-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="df846-119">-InputObject</span></span>
<span data-ttu-id="df846-120">A replikáló kiszolgáló Machine-objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="df846-120">Specifies the machine object of the replicating server.</span></span>
<span data-ttu-id="df846-121">A kivitelezéshez tekintse meg a INPUTOBJECT tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="df846-121">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="df846-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="df846-122">-SubscriptionId</span></span>
<span data-ttu-id="df846-123">Azure-előfizetési azonosító</span><span class="sxs-lookup"><span data-stu-id="df846-123">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="df846-124">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="df846-124">-TargetObjectID</span></span>
<span data-ttu-id="df846-125">Annak a replcating-kiszolgálónak a megadása, amelyhez a replicatio le kell tiltani.</span><span class="sxs-lookup"><span data-stu-id="df846-125">Specifies the replcating server for which the replicatio needs to be disabled.</span></span>
<span data-ttu-id="df846-126">Az azonosítót az Get-AzMigrateServerReplication parancsmag segítségével kell beolvasni.</span><span class="sxs-lookup"><span data-stu-id="df846-126">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="df846-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df846-127">CommonParameters</span></span>
<span data-ttu-id="df846-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="df846-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df846-129">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="df846-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df846-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="df846-130">INPUTS</span></span>

## <span data-ttu-id="df846-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="df846-131">OUTPUTS</span></span>

### <span data-ttu-id="df846-132">Microsoft. Azure. PowerShell. parancsmagok. áttelepítés. models. Api20180110. IJob</span><span class="sxs-lookup"><span data-stu-id="df846-132">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="df846-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="df846-133">NOTES</span></span>

<span data-ttu-id="df846-134">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="df846-134">ALIASES</span></span>

<span data-ttu-id="df846-135">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="df846-135">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="df846-136">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="df846-136">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="df846-137">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="df846-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="df846-138">INPUTOBJECT <IMigrationItem> : a replikáló kiszolgáló Machine-objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="df846-138">INPUTOBJECT <IMigrationItem>: Specifies the machine object of the replicating server.</span></span>
  - <span data-ttu-id="df846-139">`[Location <String>]`: Erőforrás helye</span><span class="sxs-lookup"><span data-stu-id="df846-139">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="df846-140">`[CurrentJobId <String>]`: A végrehajtandó feladat ARM azonosítója.</span><span class="sxs-lookup"><span data-stu-id="df846-140">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="df846-141">`[CurrentJobName <String>]`: A feladat neve.</span><span class="sxs-lookup"><span data-stu-id="df846-141">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="df846-142">`[CurrentJobStartTime <DateTime?>]`: A feladat kezdési időpontja.</span><span class="sxs-lookup"><span data-stu-id="df846-142">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="df846-143">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: Az áttelepítési szolgáltató egyéni beállításai.</span><span class="sxs-lookup"><span data-stu-id="df846-143">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

## <span data-ttu-id="df846-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="df846-144">RELATED LINKS</span></span>

