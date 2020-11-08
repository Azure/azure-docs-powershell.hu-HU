---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/start-azmigrateservermigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateServerMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateServerMigration.md
ms.openlocfilehash: 6a6eb5adb947793be1faf0d1d1921941e0d54065
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194333"
---
# <span data-ttu-id="eb39d-101">Start-AzMigrateServerMigration</span><span class="sxs-lookup"><span data-stu-id="eb39d-101">Start-AzMigrateServerMigration</span></span>

## <span data-ttu-id="eb39d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="eb39d-102">SYNOPSIS</span></span>
<span data-ttu-id="eb39d-103">Elindítja a replikált kiszolgáló áttelepítését.</span><span class="sxs-lookup"><span data-stu-id="eb39d-103">Starts the migration for the replicating server.</span></span>

## <span data-ttu-id="eb39d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="eb39d-104">SYNTAX</span></span>

### <span data-ttu-id="eb39d-105">ByIDVMwareCbt (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="eb39d-105">ByIDVMwareCbt (Default)</span></span>
```
Start-AzMigrateServerMigration -TargetObjectID <String> [-SubscriptionId <String>] [-TurnOffSourceServer]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="eb39d-106">ByInputObjectVMwareCbt</span><span class="sxs-lookup"><span data-stu-id="eb39d-106">ByInputObjectVMwareCbt</span></span>
```
Start-AzMigrateServerMigration -InputObject <IMigrationItem> [-SubscriptionId <String>] [-TurnOffSourceServer]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="eb39d-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="eb39d-107">DESCRIPTION</span></span>
<span data-ttu-id="eb39d-108">Elindítja a replikált kiszolgáló áttelepítését.</span><span class="sxs-lookup"><span data-stu-id="eb39d-108">Starts the migration for the replicating server.</span></span>

## <span data-ttu-id="eb39d-109">Példák</span><span class="sxs-lookup"><span data-stu-id="eb39d-109">EXAMPLES</span></span>

### <span data-ttu-id="eb39d-110">1. példa: azonosító szerint</span><span class="sxs-lookup"><span data-stu-id="eb39d-110">Example 1: By id</span></span>
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

<span data-ttu-id="eb39d-111">Azonosító szerint</span><span class="sxs-lookup"><span data-stu-id="eb39d-111">By id</span></span>

## <span data-ttu-id="eb39d-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="eb39d-112">PARAMETERS</span></span>

### <span data-ttu-id="eb39d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb39d-113">-DefaultProfile</span></span>
<span data-ttu-id="eb39d-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="eb39d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb39d-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eb39d-115">-InputObject</span></span>
<span data-ttu-id="eb39d-116">Azt a replikáló kiszolgálót adja meg, amelybe az áttelepítést be kell indítani.</span><span class="sxs-lookup"><span data-stu-id="eb39d-116">Specifies the replicating server for which migration needs to be initiated.</span></span>
<span data-ttu-id="eb39d-117">A kiszolgálói objektum az Get-AzMigrateServerReplication parancsmag használatával is beolvasható.</span><span class="sxs-lookup"><span data-stu-id="eb39d-117">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
<span data-ttu-id="eb39d-118">A kivitelezéshez tekintse meg a INPUTOBJECT tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="eb39d-118">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="eb39d-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="eb39d-119">-SubscriptionId</span></span>
<span data-ttu-id="eb39d-120">Azure-előfizetési azonosító</span><span class="sxs-lookup"><span data-stu-id="eb39d-120">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="eb39d-121">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="eb39d-121">-TargetObjectID</span></span>
<span data-ttu-id="eb39d-122">Azt a replcating-kiszolgálót adja meg, amelybe az áttelepítést be kell indítani.</span><span class="sxs-lookup"><span data-stu-id="eb39d-122">Specifies the replcating server for which migration needs to be initiated.</span></span>
<span data-ttu-id="eb39d-123">Az azonosítót az Get-AzMigrateServerReplication parancsmag segítségével kell beolvasni.</span><span class="sxs-lookup"><span data-stu-id="eb39d-123">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="eb39d-124">-TurnOffSourceServer</span><span class="sxs-lookup"><span data-stu-id="eb39d-124">-TurnOffSourceServer</span></span>
<span data-ttu-id="eb39d-125">Azt adja meg, hogy a forráskiszolgáló ki legyen-e kapcsolva az áttelepítés után.</span><span class="sxs-lookup"><span data-stu-id="eb39d-125">Specifies whether the source server should be turned off post migration.</span></span>

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

### <span data-ttu-id="eb39d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb39d-126">CommonParameters</span></span>
<span data-ttu-id="eb39d-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="eb39d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb39d-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="eb39d-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb39d-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="eb39d-129">INPUTS</span></span>

## <span data-ttu-id="eb39d-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="eb39d-130">OUTPUTS</span></span>

### <span data-ttu-id="eb39d-131">Microsoft. Azure. PowerShell. parancsmagok. áttelepítés. models. Api20180110. IJob</span><span class="sxs-lookup"><span data-stu-id="eb39d-131">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="eb39d-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="eb39d-132">NOTES</span></span>

<span data-ttu-id="eb39d-133">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="eb39d-133">ALIASES</span></span>

<span data-ttu-id="eb39d-134">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="eb39d-134">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="eb39d-135">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="eb39d-135">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="eb39d-136">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="eb39d-136">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="eb39d-137">INPUTOBJECT <IMigrationItem> : azt a replikáló kiszolgálót adja meg, amelybe az áttelepítést be kell indítani.</span><span class="sxs-lookup"><span data-stu-id="eb39d-137">INPUTOBJECT <IMigrationItem>: Specifies the replicating server for which migration needs to be initiated.</span></span> <span data-ttu-id="eb39d-138">A kiszolgálói objektum az Get-AzMigrateServerReplication parancsmag használatával is beolvasható.</span><span class="sxs-lookup"><span data-stu-id="eb39d-138">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
  - <span data-ttu-id="eb39d-139">`[Location <String>]`: Erőforrás helye</span><span class="sxs-lookup"><span data-stu-id="eb39d-139">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="eb39d-140">`[CurrentJobId <String>]`: A végrehajtandó feladat ARM azonosítója.</span><span class="sxs-lookup"><span data-stu-id="eb39d-140">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="eb39d-141">`[CurrentJobName <String>]`: A feladat neve.</span><span class="sxs-lookup"><span data-stu-id="eb39d-141">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="eb39d-142">`[CurrentJobStartTime <DateTime?>]`: A feladat kezdési időpontja.</span><span class="sxs-lookup"><span data-stu-id="eb39d-142">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="eb39d-143">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: Az áttelepítési szolgáltató egyéni beállításai.</span><span class="sxs-lookup"><span data-stu-id="eb39d-143">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

## <span data-ttu-id="eb39d-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="eb39d-144">RELATED LINKS</span></span>

