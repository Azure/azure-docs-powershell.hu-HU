---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/start-azmigratetestmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateTestMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateTestMigration.md
ms.openlocfilehash: 9a4414ca5b86ac9ebf1867cf6a58d3e495c5ea71
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194330"
---
# <span data-ttu-id="4488c-101">Start-AzMigrateTestMigration</span><span class="sxs-lookup"><span data-stu-id="4488c-101">Start-AzMigrateTestMigration</span></span>

## <span data-ttu-id="4488c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4488c-102">SYNOPSIS</span></span>
<span data-ttu-id="4488c-103">Elindítja a replikálási kiszolgáló áttelepítését.</span><span class="sxs-lookup"><span data-stu-id="4488c-103">Starts the test migration for the replicating server.</span></span>

## <span data-ttu-id="4488c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4488c-104">SYNTAX</span></span>

### <span data-ttu-id="4488c-105">ByIDVMwareCbt (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4488c-105">ByIDVMwareCbt (Default)</span></span>
```
Start-AzMigrateTestMigration -TargetObjectID <String> -TestNetworkID <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4488c-106">ByInputObjectVMwareCbt</span><span class="sxs-lookup"><span data-stu-id="4488c-106">ByInputObjectVMwareCbt</span></span>
```
Start-AzMigrateTestMigration -InputObject <IMigrationItem> -TestNetworkID <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="4488c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="4488c-107">DESCRIPTION</span></span>
<span data-ttu-id="4488c-108">A Start-AzMigrateTestMigration parancsmag kezdeményezi a replikálási kiszolgáló áttelepítését.</span><span class="sxs-lookup"><span data-stu-id="4488c-108">The Start-AzMigrateTestMigration cmdlet initiates the test migration for the replicating server.</span></span>

## <span data-ttu-id="4488c-109">Példák</span><span class="sxs-lookup"><span data-stu-id="4488c-109">EXAMPLES</span></span>

### <span data-ttu-id="4488c-110">1. példa: gépi azonosítóval</span><span class="sxs-lookup"><span data-stu-id="4488c-110">Example 1: By machine id.</span></span>
```powershell
PS C:\> Start-AzMigrateTestMigration -TargetObjectID '/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f' -TestNetworkId '/subscriptions/xxx-xxx-xxx/resourceGroups/AzMigratePWSHtargetRG/providers/Microsoft.Network/virtualNetworks/AzMigrateTargetNetwork


ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Test Migrate
Id                               : /Subscriptions/xxx-xxx-xxxresourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : TestMigrate
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs

```

<span data-ttu-id="4488c-111">Gépi azonosítóval.</span><span class="sxs-lookup"><span data-stu-id="4488c-111">By machine id.</span></span>

### <span data-ttu-id="4488c-112">2. példa: beviteli objektum szerint</span><span class="sxs-lookup"><span data-stu-id="4488c-112">Example 2: By input object</span></span>
```powershell
PS C:\> $obj = Get-AzMigrateServerReplication -TargetObjectID $env.srsMachineId -SubscriptionId $env.srsSubscriptionId
PS C:\> Start-AzMigrateTestMigration -InputObject $obj -TestNetworkId '/subscriptions/xxx-xxx-xxx/resourceGroups/AzMigratePWSHtargetRG/providers/Microsoft.Network/virtualNetworks/AzMigrateTargetNetwork


ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Test Migrate
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : TestMigrate
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs

```

<span data-ttu-id="4488c-113">Beviteli objektum alapján.</span><span class="sxs-lookup"><span data-stu-id="4488c-113">By input object.</span></span>

## <span data-ttu-id="4488c-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4488c-114">PARAMETERS</span></span>

### <span data-ttu-id="4488c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4488c-115">-DefaultProfile</span></span>
<span data-ttu-id="4488c-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4488c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4488c-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4488c-117">-InputObject</span></span>
<span data-ttu-id="4488c-118">Azt a replikálási kiszolgálót adja meg, amelyen a teszt áttelepítését kezdeményezni kell.</span><span class="sxs-lookup"><span data-stu-id="4488c-118">Specifies the replicating server for which the test migration needs to be initiated.</span></span>
<span data-ttu-id="4488c-119">A kiszolgálói objektum az Get-AzMigrateServerReplication parancsmag használatával is beolvasható.</span><span class="sxs-lookup"><span data-stu-id="4488c-119">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
<span data-ttu-id="4488c-120">A kivitelezéshez tekintse meg a INPUTOBJECT tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="4488c-120">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4488c-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4488c-121">-SubscriptionId</span></span>
<span data-ttu-id="4488c-122">Azure-előfizetési azonosító</span><span class="sxs-lookup"><span data-stu-id="4488c-122">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="4488c-123">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="4488c-123">-TargetObjectID</span></span>
<span data-ttu-id="4488c-124">Azt a replikálási kiszolgálót adja meg, amelyen a teszt áttelepítését kezdeményezni kell.</span><span class="sxs-lookup"><span data-stu-id="4488c-124">Specifies the replicating server for which the test migration needs to be initiated.</span></span>
<span data-ttu-id="4488c-125">Az azonosítót az Get-AzMigrateServerReplication parancsmag segítségével kell beolvasni.</span><span class="sxs-lookup"><span data-stu-id="4488c-125">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="4488c-126">-TestNetworkID</span><span class="sxs-lookup"><span data-stu-id="4488c-126">-TestNetworkID</span></span>
<span data-ttu-id="4488c-127">Frissíti a virtuális hálózati azonosítót a cél Azure-előfizetésben, amelyet az áttelepítés teszteléséhez kell használni.</span><span class="sxs-lookup"><span data-stu-id="4488c-127">Updates the Virtual Network id within the destination Azure subscription to be used for test migration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4488c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4488c-128">CommonParameters</span></span>
<span data-ttu-id="4488c-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4488c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4488c-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4488c-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4488c-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4488c-131">INPUTS</span></span>

## <span data-ttu-id="4488c-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4488c-132">OUTPUTS</span></span>

### <span data-ttu-id="4488c-133">Microsoft. Azure. PowerShell. parancsmagok. áttelepítés. models. Api20180110. IJob</span><span class="sxs-lookup"><span data-stu-id="4488c-133">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="4488c-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4488c-134">NOTES</span></span>

<span data-ttu-id="4488c-135">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="4488c-135">ALIASES</span></span>

<span data-ttu-id="4488c-136">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="4488c-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4488c-137">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="4488c-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4488c-138">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="4488c-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4488c-139">INPUTOBJECT <IMigrationItem> : azt a replikáló kiszolgálót adja meg, amelyre a teszt-áttelepítést be kell indítani.</span><span class="sxs-lookup"><span data-stu-id="4488c-139">INPUTOBJECT <IMigrationItem>: Specifies the replicating server for which the test migration needs to be initiated.</span></span> <span data-ttu-id="4488c-140">A kiszolgálói objektum az Get-AzMigrateServerReplication parancsmag használatával is beolvasható.</span><span class="sxs-lookup"><span data-stu-id="4488c-140">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
  - <span data-ttu-id="4488c-141">`[Location <String>]`: Erőforrás helye</span><span class="sxs-lookup"><span data-stu-id="4488c-141">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="4488c-142">`[CurrentJobId <String>]`: A végrehajtandó feladat ARM azonosítója.</span><span class="sxs-lookup"><span data-stu-id="4488c-142">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="4488c-143">`[CurrentJobName <String>]`: A feladat neve.</span><span class="sxs-lookup"><span data-stu-id="4488c-143">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="4488c-144">`[CurrentJobStartTime <DateTime?>]`: A feladat kezdési időpontja.</span><span class="sxs-lookup"><span data-stu-id="4488c-144">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="4488c-145">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: Az áttelepítési szolgáltató egyéni beállításai.</span><span class="sxs-lookup"><span data-stu-id="4488c-145">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

## <span data-ttu-id="4488c-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4488c-146">RELATED LINKS</span></span>
