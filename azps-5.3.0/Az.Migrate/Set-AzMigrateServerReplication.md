---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/set-azmigrateserverreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Set-AzMigrateServerReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Set-AzMigrateServerReplication.md
ms.openlocfilehash: bb7f951403fd2298a2890f0b92f756c0417e94c9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466317"
---
# <span data-ttu-id="517b4-101">Set-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="517b4-101">Set-AzMigrateServerReplication</span></span>

## <span data-ttu-id="517b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="517b4-102">SYNOPSIS</span></span>
<span data-ttu-id="517b4-103">Frissíti a replikáló kiszolgáló céltulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="517b4-103">Updates the target properties for the replicating server.</span></span>

## <span data-ttu-id="517b4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="517b4-104">SYNTAX</span></span>

### <span data-ttu-id="517b4-105">ByIDVMwareCbt (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="517b4-105">ByIDVMwareCbt (Default)</span></span>
```
Set-AzMigrateServerReplication -TargetObjectID <String> [-NicToUpdate <IVMwareCbtNicInput[]>]
 [-SubscriptionId <String>] [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetNetworkId <String>] [-TargetResourceGroupID <String>] [-TargetVMName <String>]
 [-TargetVMSize <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="517b4-106">ByInputObjectVMwareCbt</span><span class="sxs-lookup"><span data-stu-id="517b4-106">ByInputObjectVMwareCbt</span></span>
```
Set-AzMigrateServerReplication -InputObject <IMigrationItem> [-NicToUpdate <IVMwareCbtNicInput[]>]
 [-SubscriptionId <String>] [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetNetworkId <String>] [-TargetResourceGroupID <String>] [-TargetVMName <String>]
 [-TargetVMSize <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="517b4-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="517b4-107">DESCRIPTION</span></span>
<span data-ttu-id="517b4-108">A Set-AzMigrateServerReplication parancsmag frissíti a replikáló kiszolgáló céltulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="517b4-108">The Set-AzMigrateServerReplication cmdlet updates the target properties for the replicating server.</span></span>

## <span data-ttu-id="517b4-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="517b4-109">EXAMPLES</span></span>

### <span data-ttu-id="517b4-110">1. példa: Frissítés azonosító szerint</span><span class="sxs-lookup"><span data-stu-id="517b4-110">Example 1: Update by id</span></span>
```powershell
PS C:\> Set-AzMigrateServerReplication -TargetObjectID '/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabric/replicationProtectionContainers/AzMigratePWSHTc8d1replicationcontainer/replicationMigrationItems/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_500f44f8-2aa3-587b-8958-ead358639629' -TargetVMName 'rb-w2k12r2-1'

ActivityId                       : da958651-96b3-4e65-a41e-897d4b06f7dd ActivityId: 3a4c8d4d-920a-47cd-82c3-f3dcce90a588
AllowedAction                    : {Cancel}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          :
Error                            : {}
FriendlyName                     : Update
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/931dde9a-de67-4a30-a045-bb9d6162f8ab
Location                         :
Name                             : 931dde9a-de67-4a30-a045-bb9d6162f8ab
ScenarioName                     : Update
StartTime                        : 9/25/20 9:20:08 PM
State                            : InProgress
StateDescription                 : InProgress
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 101883a0-23f7-538a-bbd5-6d8b4fa900e2
TargetObjectName                 : prsadhu-TestVM
Task                             : {DisableProtectionOnPrimary, UpdateDraState}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="517b4-111">Azonosító szerint.</span><span class="sxs-lookup"><span data-stu-id="517b4-111">By id.</span></span>

## <span data-ttu-id="517b4-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="517b4-112">PARAMETERS</span></span>

### <span data-ttu-id="517b4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="517b4-113">-DefaultProfile</span></span>
<span data-ttu-id="517b4-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="517b4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="517b4-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="517b4-115">-InputObject</span></span>
<span data-ttu-id="517b4-116">Azt a replikáló kiszolgálót adja meg, amelynek a tulajdonságait frissíteni kell.</span><span class="sxs-lookup"><span data-stu-id="517b4-116">Specifies the replicating server for which the properties need to be updated.</span></span>
<span data-ttu-id="517b4-117">A kiszolgálóobjektum a Get-AzMigrateServerReplication le.</span><span class="sxs-lookup"><span data-stu-id="517b4-117">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
<span data-ttu-id="517b4-118">Ennek létrehozásáról az INPUTOBJECT tulajdonságokat és egy kivonattáblát a JEGYZETEK szakaszban talál.</span><span class="sxs-lookup"><span data-stu-id="517b4-118">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="517b4-119">-NicToUpdate</span><span class="sxs-lookup"><span data-stu-id="517b4-119">-NicToUpdate</span></span>
<span data-ttu-id="517b4-120">Frissíti a nic for the Azure VM to be created.</span><span class="sxs-lookup"><span data-stu-id="517b4-120">Updates the NIC for the Azure VM to be created.</span></span>
<span data-ttu-id="517b4-121">Ennek létrehozásáról a NICTOUPDATE tulajdonságokAT és egy kivonattáblát hoz létre a MEGJEGYZÉSEK szakaszban található.</span><span class="sxs-lookup"><span data-stu-id="517b4-121">To construct, see NOTES section for NICTOUPDATE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtNicInput[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="517b4-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="517b4-122">-SubscriptionId</span></span>
<span data-ttu-id="517b4-123">Az előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="517b4-123">The subscription Id.</span></span>

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

### <span data-ttu-id="517b4-124">-TargetAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="517b4-124">-TargetAvailabilitySet</span></span>
<span data-ttu-id="517b4-125">Megadja a VM-készítéshez használható rendelkezésre állási halmazt.</span><span class="sxs-lookup"><span data-stu-id="517b4-125">Specifies the Availability Set to be used for VM creation.</span></span>

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

### <span data-ttu-id="517b4-126">-TargetAvailabilityZone</span><span class="sxs-lookup"><span data-stu-id="517b4-126">-TargetAvailabilityZone</span></span>
<span data-ttu-id="517b4-127">Megadja a VIRTUÁLIS gép létrehozásához használt rendelkezésre állási zónát.</span><span class="sxs-lookup"><span data-stu-id="517b4-127">Specifies the Availability Zone to be used for VM creation.</span></span>

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

### <span data-ttu-id="517b4-128">-TargetNetworkId</span><span class="sxs-lookup"><span data-stu-id="517b4-128">-TargetNetworkId</span></span>
<span data-ttu-id="517b4-129">Frissíti a virtuális hálózat azonosítóját a cél Azure-előfizetésen belül, amelybe át kell telepíteni a kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="517b4-129">Updates the Virtual Network id within the destination Azure subscription to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="517b4-130">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="517b4-130">-TargetObjectID</span></span>
<span data-ttu-id="517b4-131">Megadja azt az újraplatkoló kiszolgálót, amelynek a tulajdonságait frissíteni kell.</span><span class="sxs-lookup"><span data-stu-id="517b4-131">Specifies the replcating server for which the properties need to be updated.</span></span>
<span data-ttu-id="517b4-132">Az azonosítót a Get-AzMigrateServerReplication kell lekérdezni.</span><span class="sxs-lookup"><span data-stu-id="517b4-132">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="517b4-133">-TargetResourceGroupID</span><span class="sxs-lookup"><span data-stu-id="517b4-133">-TargetResourceGroupID</span></span>
<span data-ttu-id="517b4-134">Frissíti az erőforráscsoport azonosítóját a cél Azure-előfizetésen belül, amelybe át kell telepíteni a kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="517b4-134">Updates the Resource Group id within the destination Azure subscription to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="517b4-135">-TargetVMName</span><span class="sxs-lookup"><span data-stu-id="517b4-135">-TargetVMName</span></span>
<span data-ttu-id="517b4-136">Megadja azt az újraplatkoló kiszolgálót, amelynek a tulajdonságait frissíteni kell.</span><span class="sxs-lookup"><span data-stu-id="517b4-136">Specifies the replcating server for which the properties need to be updated.</span></span>
<span data-ttu-id="517b4-137">Az azonosítót a Get-AzMigrateServerReplication kell lekérdezni.</span><span class="sxs-lookup"><span data-stu-id="517b4-137">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="517b4-138">-TargetVMSize</span><span class="sxs-lookup"><span data-stu-id="517b4-138">-TargetVMSize</span></span>
<span data-ttu-id="517b4-139">Frissíti a létrehozni szükséges Azure VM termékváltozatát.</span><span class="sxs-lookup"><span data-stu-id="517b4-139">Updates the SKU of the Azure VM to be created.</span></span>

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

### <span data-ttu-id="517b4-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="517b4-140">CommonParameters</span></span>
<span data-ttu-id="517b4-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="517b4-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="517b4-142">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="517b4-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="517b4-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="517b4-143">INPUTS</span></span>

## <span data-ttu-id="517b4-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="517b4-144">OUTPUTS</span></span>

### <span data-ttu-id="517b4-145">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span><span class="sxs-lookup"><span data-stu-id="517b4-145">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="517b4-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="517b4-146">NOTES</span></span>

<span data-ttu-id="517b4-147">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="517b4-147">ALIASES</span></span>

<span data-ttu-id="517b4-148">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="517b4-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="517b4-149">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="517b4-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="517b4-150">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="517b4-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="517b4-151">INPUTOBJECT: Azt a replikáló kiszolgálót adja meg, amelynek a tulajdonságait <IMigrationItem> frissíteni kell.</span><span class="sxs-lookup"><span data-stu-id="517b4-151">INPUTOBJECT <IMigrationItem>: Specifies the replicating server for which the properties need to be updated.</span></span> <span data-ttu-id="517b4-152">A kiszolgálóobjektum a Get-AzMigrateServerReplication le.</span><span class="sxs-lookup"><span data-stu-id="517b4-152">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
  - <span data-ttu-id="517b4-153">`[Location <String>]`: Erőforrás helye</span><span class="sxs-lookup"><span data-stu-id="517b4-153">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="517b4-154">`[CurrentJobId <String>]`: A ARM feladat ARM azonosítója.</span><span class="sxs-lookup"><span data-stu-id="517b4-154">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="517b4-155">`[CurrentJobName <String>]`: A feladat neve.</span><span class="sxs-lookup"><span data-stu-id="517b4-155">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="517b4-156">`[CurrentJobStartTime <DateTime?>]`: A feladat kezdési ideje.</span><span class="sxs-lookup"><span data-stu-id="517b4-156">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="517b4-157">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: Az áttelepítési szolgáltató egyéni beállításai.</span><span class="sxs-lookup"><span data-stu-id="517b4-157">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

<span data-ttu-id="517b4-158">NICTOUPDATE <IVMwareCbtNicInput[]>: Frissíti a nic for the Azure VM to be created.</span><span class="sxs-lookup"><span data-stu-id="517b4-158">NICTOUPDATE <IVMwareCbtNicInput[]>: Updates the NIC for the Azure VM to be created.</span></span>
  - <span data-ttu-id="517b4-159">`IsPrimaryNic <String>`: Egy érték, amely azt jelzi, hogy ez az elsődleges NIC.</span><span class="sxs-lookup"><span data-stu-id="517b4-159">`IsPrimaryNic <String>`: A value indicating whether this is the primary NIC.</span></span>
  - <span data-ttu-id="517b4-160">`NicId <String>`: A NIC-azonosító.</span><span class="sxs-lookup"><span data-stu-id="517b4-160">`NicId <String>`: The NIC Id.</span></span>
  - <span data-ttu-id="517b4-161">`[IsSelectedForMigration <String>]`: Egy érték, amely azt jelzi, hogy ez a NIC van-e kiválasztva az áttelepítéshez.</span><span class="sxs-lookup"><span data-stu-id="517b4-161">`[IsSelectedForMigration <String>]`: A value indicating whether this NIC is selected for migration.</span></span>
  - <span data-ttu-id="517b4-162">`[TargetStaticIPAddress <String>]`: A statikus IP-cím.</span><span class="sxs-lookup"><span data-stu-id="517b4-162">`[TargetStaticIPAddress <String>]`: The static IP address.</span></span>
  - <span data-ttu-id="517b4-163">`[TargetSubnetName <String>]`: Cél alhálózat neve.</span><span class="sxs-lookup"><span data-stu-id="517b4-163">`[TargetSubnetName <String>]`: Target subnet name.</span></span>

## <span data-ttu-id="517b4-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="517b4-164">RELATED LINKS</span></span>

