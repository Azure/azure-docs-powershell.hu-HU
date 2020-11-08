---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/start-azmigratetestmigrationcleanup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateTestMigrationCleanup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateTestMigrationCleanup.md
ms.openlocfilehash: df4eac2c6380c36dcd07c906ccbbee4d2a93f27b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194329"
---
# <span data-ttu-id="7e4cd-101">Start-AzMigrateTestMigrationCleanup</span><span class="sxs-lookup"><span data-stu-id="7e4cd-101">Start-AzMigrateTestMigrationCleanup</span></span>

## <span data-ttu-id="7e4cd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7e4cd-102">SYNOPSIS</span></span>
<span data-ttu-id="7e4cd-103">Megtisztítja a replikálási kiszolgáló áttelepítését.</span><span class="sxs-lookup"><span data-stu-id="7e4cd-103">Cleans up the test migration for the replicating server.</span></span>

## <span data-ttu-id="7e4cd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7e4cd-104">SYNTAX</span></span>

### <span data-ttu-id="7e4cd-105">ByIDVMwareCbt (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7e4cd-105">ByIDVMwareCbt (Default)</span></span>
```
Start-AzMigrateTestMigrationCleanup -TargetObjectID <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7e4cd-106">ByInputObjectVMwareCbt</span><span class="sxs-lookup"><span data-stu-id="7e4cd-106">ByInputObjectVMwareCbt</span></span>
```
Start-AzMigrateTestMigrationCleanup -InputObject <IMigrationItem> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="7e4cd-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="7e4cd-107">DESCRIPTION</span></span>
<span data-ttu-id="7e4cd-108">A Start-AzMigrateTestMigrationCleanup parancsmag a replikálási kiszolgáló áttelepítésének megtisztítását kezdeményezi.</span><span class="sxs-lookup"><span data-stu-id="7e4cd-108">The Start-AzMigrateTestMigrationCleanup cmdlet initiates the clean up of the test migration for the replicating server.</span></span>

## <span data-ttu-id="7e4cd-109">Példák</span><span class="sxs-lookup"><span data-stu-id="7e4cd-109">EXAMPLES</span></span>

### <span data-ttu-id="7e4cd-110">1. példa: gépi azonosítóval</span><span class="sxs-lookup"><span data-stu-id="7e4cd-110">Example 1: By machine id.</span></span>
```powershell
PS C:\> Start-AzMigrateTestMigrationCleanup -TargetObjectID '/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f'


ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Test Migrate Cleanup
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : TestMigrateCleanup
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs

```

<span data-ttu-id="7e4cd-111">Gépi azonosítóval.</span><span class="sxs-lookup"><span data-stu-id="7e4cd-111">By machine id.</span></span>

### <span data-ttu-id="7e4cd-112">2. példa: beviteli objektum szerint</span><span class="sxs-lookup"><span data-stu-id="7e4cd-112">Example 2: By input object</span></span>
```powershell
PS C:\> $obj = Get-AzMigrateServerReplication -TargetObjectID $env.srsMachineId -SubscriptionId $env.srsSubscriptionId
PS C:\> Start-AzMigrateTestMigrationCleanup -InputObject $ob


AllowedOperation            : {DisableMigration, TestMigrate, Migrate}

ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Test Migrate Cleanup
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : TestMigrateCleanup
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs

```

<span data-ttu-id="7e4cd-113">Beviteli objektum alapján.</span><span class="sxs-lookup"><span data-stu-id="7e4cd-113">By input object.</span></span>

## <span data-ttu-id="7e4cd-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7e4cd-114">PARAMETERS</span></span>

### <span data-ttu-id="7e4cd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e4cd-115">-DefaultProfile</span></span>
<span data-ttu-id="7e4cd-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7e4cd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e4cd-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7e4cd-117">-InputObject</span></span>
<span data-ttu-id="7e4cd-118">Azt a replikálási kiszolgálót adja meg, amelynek a tesztelési áttelepítési folyamatot meg kell indítania.</span><span class="sxs-lookup"><span data-stu-id="7e4cd-118">Specifies the replicating server for which the test migration cleanup needs to be initiated.</span></span>
<span data-ttu-id="7e4cd-119">A kiszolgálói objektum a Get-AzMigrateServerReplication parancsmag használatával szerezhető be, lásd: a INPUTOBJECT tulajdonságainak megjegyzések szakasza, és hozzon létre egy kivonatoló táblázatot.</span><span class="sxs-lookup"><span data-stu-id="7e4cd-119">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="7e4cd-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7e4cd-120">-SubscriptionId</span></span>
<span data-ttu-id="7e4cd-121">Azure-előfizetési azonosító</span><span class="sxs-lookup"><span data-stu-id="7e4cd-121">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="7e4cd-122">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="7e4cd-122">-TargetObjectID</span></span>
<span data-ttu-id="7e4cd-123">Azt a replikálási kiszolgálót adja meg, amelynek a tesztelési áttelepítési folyamatot meg kell indítania.</span><span class="sxs-lookup"><span data-stu-id="7e4cd-123">Specifies the replicating server for which the test migration cleanup needs to be initiated.</span></span>
<span data-ttu-id="7e4cd-124">Az azonosítót az Get-AzMigrateServerReplication parancsmag segítségével kell beolvasni.</span><span class="sxs-lookup"><span data-stu-id="7e4cd-124">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="7e4cd-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e4cd-125">CommonParameters</span></span>
<span data-ttu-id="7e4cd-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7e4cd-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e4cd-127">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7e4cd-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e4cd-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7e4cd-128">INPUTS</span></span>

## <span data-ttu-id="7e4cd-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7e4cd-129">OUTPUTS</span></span>

### <span data-ttu-id="7e4cd-130">Microsoft. Azure. PowerShell. parancsmagok. áttelepítés. models. Api20180110. IJob</span><span class="sxs-lookup"><span data-stu-id="7e4cd-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="7e4cd-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7e4cd-131">NOTES</span></span>

<span data-ttu-id="7e4cd-132">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="7e4cd-132">ALIASES</span></span>

<span data-ttu-id="7e4cd-133">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="7e4cd-133">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7e4cd-134">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="7e4cd-134">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7e4cd-135">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="7e4cd-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7e4cd-136">INPUTOBJECT <IMigrationItem> : azt a replikáló kiszolgálót adja meg, amelynek a teszt-áttelepítési folyamatot meg kell indítania.</span><span class="sxs-lookup"><span data-stu-id="7e4cd-136">INPUTOBJECT <IMigrationItem>: Specifies the replicating server for which the test migration cleanup needs to be initiated.</span></span> <span data-ttu-id="7e4cd-137">A kiszolgálói objektum az Get-AzMigrateServerReplication parancsmag használatával is beolvasható.</span><span class="sxs-lookup"><span data-stu-id="7e4cd-137">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet</span></span>
  - <span data-ttu-id="7e4cd-138">`[Location <String>]`: Erőforrás helye</span><span class="sxs-lookup"><span data-stu-id="7e4cd-138">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="7e4cd-139">`[CurrentJobId <String>]`: A végrehajtandó feladat ARM azonosítója.</span><span class="sxs-lookup"><span data-stu-id="7e4cd-139">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="7e4cd-140">`[CurrentJobName <String>]`: A feladat neve.</span><span class="sxs-lookup"><span data-stu-id="7e4cd-140">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="7e4cd-141">`[CurrentJobStartTime <DateTime?>]`: A feladat kezdési időpontja.</span><span class="sxs-lookup"><span data-stu-id="7e4cd-141">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="7e4cd-142">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: Az áttelepítési szolgáltató egyéni beállításai.</span><span class="sxs-lookup"><span data-stu-id="7e4cd-142">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

## <span data-ttu-id="7e4cd-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7e4cd-143">RELATED LINKS</span></span>

