---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/start-azmigrateservermigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateServerMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateServerMigration.md
ms.openlocfilehash: 6a6eb5adb947793be1faf0d1d1921941e0d54065
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98363577"
---
# <span data-ttu-id="6a137-101">Start-AzMigrateServerMigration</span><span class="sxs-lookup"><span data-stu-id="6a137-101">Start-AzMigrateServerMigration</span></span>

## <span data-ttu-id="6a137-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a137-102">SYNOPSIS</span></span>
<span data-ttu-id="6a137-103">Elindítja a replikáló kiszolgáló áttelepítését.</span><span class="sxs-lookup"><span data-stu-id="6a137-103">Starts the migration for the replicating server.</span></span>

## <span data-ttu-id="6a137-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6a137-104">SYNTAX</span></span>

### <span data-ttu-id="6a137-105">ByIDVMwareCbt (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6a137-105">ByIDVMwareCbt (Default)</span></span>
```
Start-AzMigrateServerMigration -TargetObjectID <String> [-SubscriptionId <String>] [-TurnOffSourceServer]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6a137-106">ByInputObjectVMwareCbt</span><span class="sxs-lookup"><span data-stu-id="6a137-106">ByInputObjectVMwareCbt</span></span>
```
Start-AzMigrateServerMigration -InputObject <IMigrationItem> [-SubscriptionId <String>] [-TurnOffSourceServer]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="6a137-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6a137-107">DESCRIPTION</span></span>
<span data-ttu-id="6a137-108">Elindítja a replikáló kiszolgáló áttelepítését.</span><span class="sxs-lookup"><span data-stu-id="6a137-108">Starts the migration for the replicating server.</span></span>

## <span data-ttu-id="6a137-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6a137-109">EXAMPLES</span></span>

### <span data-ttu-id="6a137-110">1. példa: Azonosító szerint</span><span class="sxs-lookup"><span data-stu-id="6a137-110">Example 1: By id</span></span>
```powershell
PS C:\> PS /src/Migrate [Az.Migrate]> Start-AzMigrateServerMigration -TargetObjectID "/Subscriptions/7xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_52f42ee7-8eb3-1aa4-e2d5-1ae83f86b085"

ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Migrate
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : Migrate
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="6a137-111">Azonosító szerint</span><span class="sxs-lookup"><span data-stu-id="6a137-111">By id</span></span>

## <span data-ttu-id="6a137-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6a137-112">PARAMETERS</span></span>

### <span data-ttu-id="6a137-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a137-113">-DefaultProfile</span></span>
<span data-ttu-id="6a137-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6a137-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a137-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6a137-115">-InputObject</span></span>
<span data-ttu-id="6a137-116">Azt a replikáló kiszolgálót adja meg, amelyhez áttelepítést kell kezdeményezni.</span><span class="sxs-lookup"><span data-stu-id="6a137-116">Specifies the replicating server for which migration needs to be initiated.</span></span>
<span data-ttu-id="6a137-117">A kiszolgálóobjektum a Get-AzMigrateServerReplication le.</span><span class="sxs-lookup"><span data-stu-id="6a137-117">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
<span data-ttu-id="6a137-118">Ennek létrehozásáról az INPUTOBJECT tulajdonságokat és egy kivonattáblát a JEGYZETEK szakaszban talál.</span><span class="sxs-lookup"><span data-stu-id="6a137-118">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="6a137-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6a137-119">-SubscriptionId</span></span>
<span data-ttu-id="6a137-120">Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="6a137-120">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="6a137-121">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="6a137-121">-TargetObjectID</span></span>
<span data-ttu-id="6a137-122">Megadja azt a újraplatkoló kiszolgálót, amelynek áttelepítését el kell indítani.</span><span class="sxs-lookup"><span data-stu-id="6a137-122">Specifies the replcating server for which migration needs to be initiated.</span></span>
<span data-ttu-id="6a137-123">Az azonosítót a Get-AzMigrateServerReplication kell lekérdezni.</span><span class="sxs-lookup"><span data-stu-id="6a137-123">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="6a137-124">-TurnOffSourceServer</span><span class="sxs-lookup"><span data-stu-id="6a137-124">-TurnOffSourceServer</span></span>
<span data-ttu-id="6a137-125">Azt adja meg, hogy a forráskiszolgálót ki kell-e kapcsolva az áttelepítés után.</span><span class="sxs-lookup"><span data-stu-id="6a137-125">Specifies whether the source server should be turned off post migration.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a137-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a137-126">CommonParameters</span></span>
<span data-ttu-id="6a137-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a137-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a137-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6a137-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a137-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6a137-129">INPUTS</span></span>

## <span data-ttu-id="6a137-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6a137-130">OUTPUTS</span></span>

### <span data-ttu-id="6a137-131">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span><span class="sxs-lookup"><span data-stu-id="6a137-131">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="6a137-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6a137-132">NOTES</span></span>

<span data-ttu-id="6a137-133">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="6a137-133">ALIASES</span></span>

<span data-ttu-id="6a137-134">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="6a137-134">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6a137-135">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="6a137-135">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6a137-136">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6a137-136">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6a137-137">INPUTOBJECT: Azt a replikáló kiszolgálót adja meg, amelyhez <IMigrationItem> áttelepítést kell kezdeményezni.</span><span class="sxs-lookup"><span data-stu-id="6a137-137">INPUTOBJECT <IMigrationItem>: Specifies the replicating server for which migration needs to be initiated.</span></span> <span data-ttu-id="6a137-138">A kiszolgálóobjektum a Get-AzMigrateServerReplication le.</span><span class="sxs-lookup"><span data-stu-id="6a137-138">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
  - <span data-ttu-id="6a137-139">`[Location <String>]`: Erőforrás helye</span><span class="sxs-lookup"><span data-stu-id="6a137-139">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="6a137-140">`[CurrentJobId <String>]`: A ARM feladat ARM azonosítója.</span><span class="sxs-lookup"><span data-stu-id="6a137-140">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="6a137-141">`[CurrentJobName <String>]`: A feladat neve.</span><span class="sxs-lookup"><span data-stu-id="6a137-141">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="6a137-142">`[CurrentJobStartTime <DateTime?>]`: A feladat kezdési ideje.</span><span class="sxs-lookup"><span data-stu-id="6a137-142">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="6a137-143">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: Az áttelepítési szolgáltató egyéni beállításai.</span><span class="sxs-lookup"><span data-stu-id="6a137-143">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

## <span data-ttu-id="6a137-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6a137-144">RELATED LINKS</span></span>

