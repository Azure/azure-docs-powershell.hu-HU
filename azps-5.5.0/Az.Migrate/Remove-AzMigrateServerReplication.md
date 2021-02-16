---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/remove-azmigrateserverreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Remove-AzMigrateServerReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Remove-AzMigrateServerReplication.md
ms.openlocfilehash: e9e6d3f9c045b9ff9cc2d5a4860b2c7fc5559f14
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100152291"
---
# <span data-ttu-id="7cade-101">Remove-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="7cade-101">Remove-AzMigrateServerReplication</span></span>

## <span data-ttu-id="7cade-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7cade-102">SYNOPSIS</span></span>
<span data-ttu-id="7cade-103">Leállítja az áttelepített kiszolgáló replikációját.</span><span class="sxs-lookup"><span data-stu-id="7cade-103">Stops replication for the migrated server.</span></span>

## <span data-ttu-id="7cade-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7cade-104">SYNTAX</span></span>

### <span data-ttu-id="7cade-105">ByIDVMwareCbt (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7cade-105">ByIDVMwareCbt (Default)</span></span>
```
Remove-AzMigrateServerReplication -TargetObjectID <String> [-SubscriptionId <String>] [-ForceRemove <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7cade-106">ByInputObjectVMwareCbt</span><span class="sxs-lookup"><span data-stu-id="7cade-106">ByInputObjectVMwareCbt</span></span>
```
Remove-AzMigrateServerReplication -InputObject <IMigrationItem> [-SubscriptionId <String>]
 [-ForceRemove <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="7cade-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7cade-107">DESCRIPTION</span></span>
<span data-ttu-id="7cade-108">A Remove-AzMigrateServerReplication parancsmag leállítja az áttelepített kiszolgáló replikációját.</span><span class="sxs-lookup"><span data-stu-id="7cade-108">The Remove-AzMigrateServerReplication cmdlet stops the replication for a migrated server.</span></span>

## <span data-ttu-id="7cade-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7cade-109">EXAMPLES</span></span>

### <span data-ttu-id="7cade-110">1. példa: Eltávolítás azonosító szerint.</span><span class="sxs-lookup"><span data-stu-id="7cade-110">Example 1: Remove by id.</span></span>
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

<span data-ttu-id="7cade-111">Újraszinkronizáció azonosító alapján.</span><span class="sxs-lookup"><span data-stu-id="7cade-111">Resync by id.</span></span>

### <span data-ttu-id="7cade-112">2. példa: Eltávolítás bemeneti objektummal</span><span class="sxs-lookup"><span data-stu-id="7cade-112">Example 2: Remove by Input Object</span></span>
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

<span data-ttu-id="7cade-113">Név szerint.</span><span class="sxs-lookup"><span data-stu-id="7cade-113">By name.</span></span>

## <span data-ttu-id="7cade-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7cade-114">PARAMETERS</span></span>

### <span data-ttu-id="7cade-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cade-115">-DefaultProfile</span></span>
<span data-ttu-id="7cade-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7cade-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7cade-117">-ForceRemove</span><span class="sxs-lookup"><span data-stu-id="7cade-117">-ForceRemove</span></span>
<span data-ttu-id="7cade-118">Azt adja meg, hogy a replikációt kényszeríteni kell-e.</span><span class="sxs-lookup"><span data-stu-id="7cade-118">Specifies whether the replication needs to be force removed.</span></span>

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

### <span data-ttu-id="7cade-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7cade-119">-InputObject</span></span>
<span data-ttu-id="7cade-120">A replikáló kiszolgáló gépobjektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="7cade-120">Specifies the machine object of the replicating server.</span></span>
<span data-ttu-id="7cade-121">Ennek létrehozásáról az INPUTOBJECT tulajdonságokat és egy kivonattáblát a JEGYZETEK szakaszban talál.</span><span class="sxs-lookup"><span data-stu-id="7cade-121">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="7cade-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7cade-122">-SubscriptionId</span></span>
<span data-ttu-id="7cade-123">Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="7cade-123">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="7cade-124">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="7cade-124">-TargetObjectID</span></span>
<span data-ttu-id="7cade-125">Azt a replcating kiszolgálót adja meg, amelyen le kell tiltani a másodpéldányt.</span><span class="sxs-lookup"><span data-stu-id="7cade-125">Specifies the replcating server for which the replicatio needs to be disabled.</span></span>
<span data-ttu-id="7cade-126">Az azonosítót a Get-AzMigrateServerReplication kell lekérni.</span><span class="sxs-lookup"><span data-stu-id="7cade-126">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="7cade-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cade-127">CommonParameters</span></span>
<span data-ttu-id="7cade-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7cade-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cade-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7cade-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cade-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7cade-130">INPUTS</span></span>

## <span data-ttu-id="7cade-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7cade-131">OUTPUTS</span></span>

### <span data-ttu-id="7cade-132">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span><span class="sxs-lookup"><span data-stu-id="7cade-132">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="7cade-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7cade-133">NOTES</span></span>

<span data-ttu-id="7cade-134">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="7cade-134">ALIASES</span></span>

<span data-ttu-id="7cade-135">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="7cade-135">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7cade-136">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="7cade-136">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7cade-137">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7cade-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7cade-138">INPUTOBJECT: A replikáló <IMigrationItem> kiszolgáló gépobjektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="7cade-138">INPUTOBJECT <IMigrationItem>: Specifies the machine object of the replicating server.</span></span>
  - <span data-ttu-id="7cade-139">`[Location <String>]`: Erőforrás helye</span><span class="sxs-lookup"><span data-stu-id="7cade-139">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="7cade-140">`[CurrentJobId <String>]`: A ARM feladat ARM azonosítója.</span><span class="sxs-lookup"><span data-stu-id="7cade-140">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="7cade-141">`[CurrentJobName <String>]`: A feladat neve.</span><span class="sxs-lookup"><span data-stu-id="7cade-141">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="7cade-142">`[CurrentJobStartTime <DateTime?>]`: A feladat kezdési ideje.</span><span class="sxs-lookup"><span data-stu-id="7cade-142">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="7cade-143">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: Az áttelepítési szolgáltató egyéni beállításai.</span><span class="sxs-lookup"><span data-stu-id="7cade-143">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

## <span data-ttu-id="7cade-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7cade-144">RELATED LINKS</span></span>

