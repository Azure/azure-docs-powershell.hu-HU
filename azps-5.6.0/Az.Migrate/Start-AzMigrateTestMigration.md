---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/start-azmigratetestmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateTestMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Start-AzMigrateTestMigration.md
ms.openlocfilehash: 2c0582f8e91218679b9fbaeb3192e15f2848fd1e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009573"
---
# <span data-ttu-id="ca1e0-101">Start-AzMigrateTestMigration</span><span class="sxs-lookup"><span data-stu-id="ca1e0-101">Start-AzMigrateTestMigration</span></span>

## <span data-ttu-id="ca1e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca1e0-102">SYNOPSIS</span></span>
<span data-ttu-id="ca1e0-103">Elindítja a replikáló kiszolgáló tesztelését.</span><span class="sxs-lookup"><span data-stu-id="ca1e0-103">Starts the test migration for the replicating server.</span></span>

## <span data-ttu-id="ca1e0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ca1e0-104">SYNTAX</span></span>

### <span data-ttu-id="ca1e0-105">ByIDVMwareCbt (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ca1e0-105">ByIDVMwareCbt (Default)</span></span>
```
Start-AzMigrateTestMigration -TargetObjectID <String> -TestNetworkID <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ca1e0-106">ByInputObjectVMwareCbt</span><span class="sxs-lookup"><span data-stu-id="ca1e0-106">ByInputObjectVMwareCbt</span></span>
```
Start-AzMigrateTestMigration -InputObject <IMigrationItem> -TestNetworkID <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="ca1e0-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ca1e0-107">DESCRIPTION</span></span>
<span data-ttu-id="ca1e0-108">A Start-AzMigrateTestMigration parancsmag elindítja a teszt áttelepítését a replikáló kiszolgálóhoz.</span><span class="sxs-lookup"><span data-stu-id="ca1e0-108">The Start-AzMigrateTestMigration cmdlet initiates the test migration for the replicating server.</span></span>

## <span data-ttu-id="ca1e0-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ca1e0-109">EXAMPLES</span></span>

### <span data-ttu-id="ca1e0-110">1. példa: Gépazonosító szerint.</span><span class="sxs-lookup"><span data-stu-id="ca1e0-110">Example 1: By machine id.</span></span>
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

<span data-ttu-id="ca1e0-111">Gépazonosító szerint.</span><span class="sxs-lookup"><span data-stu-id="ca1e0-111">By machine id.</span></span>

### <span data-ttu-id="ca1e0-112">2. példa: Bemeneti objektum alapján</span><span class="sxs-lookup"><span data-stu-id="ca1e0-112">Example 2: By input object</span></span>
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

<span data-ttu-id="ca1e0-113">Bemeneti objektum alapján.</span><span class="sxs-lookup"><span data-stu-id="ca1e0-113">By input object.</span></span>

## <span data-ttu-id="ca1e0-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ca1e0-114">PARAMETERS</span></span>

### <span data-ttu-id="ca1e0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca1e0-115">-DefaultProfile</span></span>
<span data-ttu-id="ca1e0-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ca1e0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca1e0-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ca1e0-117">-InputObject</span></span>
<span data-ttu-id="ca1e0-118">Azt a replikáló kiszolgálót adja meg, amelyhez a tesztelési áttelepítést el kell indítani.</span><span class="sxs-lookup"><span data-stu-id="ca1e0-118">Specifies the replicating server for which the test migration needs to be initiated.</span></span>
<span data-ttu-id="ca1e0-119">A kiszolgálóobjektum a Get-AzMigrateServerReplication le.</span><span class="sxs-lookup"><span data-stu-id="ca1e0-119">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
<span data-ttu-id="ca1e0-120">Ennek létrehozásáról az INPUTOBJECT tulajdonságokat és egy kivonattáblát a JEGYZETEK szakaszban talál.</span><span class="sxs-lookup"><span data-stu-id="ca1e0-120">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ca1e0-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ca1e0-121">-SubscriptionId</span></span>
<span data-ttu-id="ca1e0-122">Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ca1e0-122">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="ca1e0-123">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="ca1e0-123">-TargetObjectID</span></span>
<span data-ttu-id="ca1e0-124">Azt a replikáló kiszolgálót adja meg, amelyhez a tesztelési áttelepítést el kell indítani.</span><span class="sxs-lookup"><span data-stu-id="ca1e0-124">Specifies the replicating server for which the test migration needs to be initiated.</span></span>
<span data-ttu-id="ca1e0-125">Az azonosítót a Get-AzMigrateServerReplication kell lekérdezni.</span><span class="sxs-lookup"><span data-stu-id="ca1e0-125">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="ca1e0-126">-TestNetworkID</span><span class="sxs-lookup"><span data-stu-id="ca1e0-126">-TestNetworkID</span></span>
<span data-ttu-id="ca1e0-127">Frissíti a virtuális hálózat azonosítóját a cél Azure-előfizetésen belül, hogy tesztelje az áttelepítést.</span><span class="sxs-lookup"><span data-stu-id="ca1e0-127">Updates the Virtual Network id within the destination Azure subscription to be used for test migration.</span></span>

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

### <span data-ttu-id="ca1e0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca1e0-128">CommonParameters</span></span>
<span data-ttu-id="ca1e0-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca1e0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca1e0-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ca1e0-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca1e0-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ca1e0-131">INPUTS</span></span>

## <span data-ttu-id="ca1e0-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ca1e0-132">OUTPUTS</span></span>

### <span data-ttu-id="ca1e0-133">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span><span class="sxs-lookup"><span data-stu-id="ca1e0-133">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="ca1e0-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ca1e0-134">NOTES</span></span>

<span data-ttu-id="ca1e0-135">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="ca1e0-135">ALIASES</span></span>

<span data-ttu-id="ca1e0-136">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="ca1e0-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ca1e0-137">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="ca1e0-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ca1e0-138">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ca1e0-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ca1e0-139">INPUTOBJECT: Azt a replikáló kiszolgálót adja meg, amelynek a tesztelését el kell <IMigrationItem> indítani.</span><span class="sxs-lookup"><span data-stu-id="ca1e0-139">INPUTOBJECT <IMigrationItem>: Specifies the replicating server for which the test migration needs to be initiated.</span></span> <span data-ttu-id="ca1e0-140">A kiszolgálóobjektum a Get-AzMigrateServerReplication le.</span><span class="sxs-lookup"><span data-stu-id="ca1e0-140">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
  - <span data-ttu-id="ca1e0-141">`[Location <String>]`: Erőforrás helye</span><span class="sxs-lookup"><span data-stu-id="ca1e0-141">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="ca1e0-142">`[CurrentJobId <String>]`: A ARM feladat ARM azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ca1e0-142">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="ca1e0-143">`[CurrentJobName <String>]`: A feladat neve.</span><span class="sxs-lookup"><span data-stu-id="ca1e0-143">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="ca1e0-144">`[CurrentJobStartTime <DateTime?>]`: A feladat kezdési ideje.</span><span class="sxs-lookup"><span data-stu-id="ca1e0-144">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="ca1e0-145">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: Az áttelepítési szolgáltató egyéni beállításai.</span><span class="sxs-lookup"><span data-stu-id="ca1e0-145">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

## <span data-ttu-id="ca1e0-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ca1e0-146">RELATED LINKS</span></span>

