---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/set-azmigrateserverreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Set-AzMigrateServerReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Set-AzMigrateServerReplication.md
ms.openlocfilehash: bb7f951403fd2298a2890f0b92f756c0417e94c9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194331"
---
# <span data-ttu-id="05df1-101">Set-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="05df1-101">Set-AzMigrateServerReplication</span></span>

## <span data-ttu-id="05df1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="05df1-102">SYNOPSIS</span></span>
<span data-ttu-id="05df1-103">Frissíti a replikált kiszolgáló megjelenítési tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="05df1-103">Updates the target properties for the replicating server.</span></span>

## <span data-ttu-id="05df1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="05df1-104">SYNTAX</span></span>

### <span data-ttu-id="05df1-105">ByIDVMwareCbt (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="05df1-105">ByIDVMwareCbt (Default)</span></span>
```
Set-AzMigrateServerReplication -TargetObjectID <String> [-NicToUpdate <IVMwareCbtNicInput[]>]
 [-SubscriptionId <String>] [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetNetworkId <String>] [-TargetResourceGroupID <String>] [-TargetVMName <String>]
 [-TargetVMSize <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="05df1-106">ByInputObjectVMwareCbt</span><span class="sxs-lookup"><span data-stu-id="05df1-106">ByInputObjectVMwareCbt</span></span>
```
Set-AzMigrateServerReplication -InputObject <IMigrationItem> [-NicToUpdate <IVMwareCbtNicInput[]>]
 [-SubscriptionId <String>] [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetNetworkId <String>] [-TargetResourceGroupID <String>] [-TargetVMName <String>]
 [-TargetVMSize <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="05df1-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="05df1-107">DESCRIPTION</span></span>
<span data-ttu-id="05df1-108">A Set-AzMigrateServerReplication parancsmag frissíti a replikált kiszolgáló megjelenítési tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="05df1-108">The Set-AzMigrateServerReplication cmdlet updates the target properties for the replicating server.</span></span>

## <span data-ttu-id="05df1-109">Példák</span><span class="sxs-lookup"><span data-stu-id="05df1-109">EXAMPLES</span></span>

### <span data-ttu-id="05df1-110">Példa 1: Update by id</span><span class="sxs-lookup"><span data-stu-id="05df1-110">Example 1: Update by id</span></span>
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

<span data-ttu-id="05df1-111">Azonosító alapján.</span><span class="sxs-lookup"><span data-stu-id="05df1-111">By id.</span></span>

## <span data-ttu-id="05df1-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="05df1-112">PARAMETERS</span></span>

### <span data-ttu-id="05df1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05df1-113">-DefaultProfile</span></span>
<span data-ttu-id="05df1-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="05df1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05df1-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="05df1-115">-InputObject</span></span>
<span data-ttu-id="05df1-116">Azt a replikáló kiszolgálót adja meg, amelyre a tulajdonságokat frissíteni kell.</span><span class="sxs-lookup"><span data-stu-id="05df1-116">Specifies the replicating server for which the properties need to be updated.</span></span>
<span data-ttu-id="05df1-117">A kiszolgálói objektum az Get-AzMigrateServerReplication parancsmag használatával is beolvasható.</span><span class="sxs-lookup"><span data-stu-id="05df1-117">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
<span data-ttu-id="05df1-118">A kivitelezéshez tekintse meg a INPUTOBJECT tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="05df1-118">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="05df1-119">-NicToUpdate</span><span class="sxs-lookup"><span data-stu-id="05df1-119">-NicToUpdate</span></span>
<span data-ttu-id="05df1-120">Frissíti az Azure VM-t létrehozó hálózati adaptert.</span><span class="sxs-lookup"><span data-stu-id="05df1-120">Updates the NIC for the Azure VM to be created.</span></span>
<span data-ttu-id="05df1-121">A kivitelezéshez tekintse meg a NICTOUPDATE tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="05df1-121">To construct, see NOTES section for NICTOUPDATE properties and create a hash table.</span></span>

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

### <span data-ttu-id="05df1-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="05df1-122">-SubscriptionId</span></span>
<span data-ttu-id="05df1-123">Az előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="05df1-123">The subscription Id.</span></span>

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

### <span data-ttu-id="05df1-124">-TargetAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="05df1-124">-TargetAvailabilitySet</span></span>
<span data-ttu-id="05df1-125">A VM-készítéshez használandó elérhetőségi készletet adja meg.</span><span class="sxs-lookup"><span data-stu-id="05df1-125">Specifies the Availability Set to be used for VM creation.</span></span>

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

### <span data-ttu-id="05df1-126">-TargetAvailabilityZone</span><span class="sxs-lookup"><span data-stu-id="05df1-126">-TargetAvailabilityZone</span></span>
<span data-ttu-id="05df1-127">A VM-készítéshez használandó elérhetőségi zóna meghatározása.</span><span class="sxs-lookup"><span data-stu-id="05df1-127">Specifies the Availability Zone to be used for VM creation.</span></span>

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

### <span data-ttu-id="05df1-128">-TargetNetworkId</span><span class="sxs-lookup"><span data-stu-id="05df1-128">-TargetNetworkId</span></span>
<span data-ttu-id="05df1-129">Frissíti a virtuális hálózati azonosítót a cél Azure-előfizetésén belül, amelyre a kiszolgálót át kell telepíteni.</span><span class="sxs-lookup"><span data-stu-id="05df1-129">Updates the Virtual Network id within the destination Azure subscription to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="05df1-130">-TargetObjectID</span><span class="sxs-lookup"><span data-stu-id="05df1-130">-TargetObjectID</span></span>
<span data-ttu-id="05df1-131">Azt a replcating-kiszolgálót adja meg, amelyhez frissíteni kell a tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="05df1-131">Specifies the replcating server for which the properties need to be updated.</span></span>
<span data-ttu-id="05df1-132">Az azonosítót az Get-AzMigrateServerReplication parancsmag segítségével kell beolvasni.</span><span class="sxs-lookup"><span data-stu-id="05df1-132">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="05df1-133">-TargetResourceGroupID</span><span class="sxs-lookup"><span data-stu-id="05df1-133">-TargetResourceGroupID</span></span>
<span data-ttu-id="05df1-134">Frissíti az erőforráscsoport-azonosítót a cél Azure-előfizetésen belül, amelyre a kiszolgálót át kell telepíteni.</span><span class="sxs-lookup"><span data-stu-id="05df1-134">Updates the Resource Group id within the destination Azure subscription to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="05df1-135">-TargetVMName</span><span class="sxs-lookup"><span data-stu-id="05df1-135">-TargetVMName</span></span>
<span data-ttu-id="05df1-136">Azt a replcating-kiszolgálót adja meg, amelyhez frissíteni kell a tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="05df1-136">Specifies the replcating server for which the properties need to be updated.</span></span>
<span data-ttu-id="05df1-137">Az azonosítót az Get-AzMigrateServerReplication parancsmag segítségével kell beolvasni.</span><span class="sxs-lookup"><span data-stu-id="05df1-137">The ID should be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>

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

### <span data-ttu-id="05df1-138">-TargetVMSize</span><span class="sxs-lookup"><span data-stu-id="05df1-138">-TargetVMSize</span></span>
<span data-ttu-id="05df1-139">Frissíti az Azure VM-t a létrehozandó SKU-ot.</span><span class="sxs-lookup"><span data-stu-id="05df1-139">Updates the SKU of the Azure VM to be created.</span></span>

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

### <span data-ttu-id="05df1-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05df1-140">CommonParameters</span></span>
<span data-ttu-id="05df1-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="05df1-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05df1-142">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="05df1-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05df1-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="05df1-143">INPUTS</span></span>

## <span data-ttu-id="05df1-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="05df1-144">OUTPUTS</span></span>

### <span data-ttu-id="05df1-145">Microsoft. Azure. PowerShell. parancsmagok. áttelepítés. models. Api20180110. IJob</span><span class="sxs-lookup"><span data-stu-id="05df1-145">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="05df1-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="05df1-146">NOTES</span></span>

<span data-ttu-id="05df1-147">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="05df1-147">ALIASES</span></span>

<span data-ttu-id="05df1-148">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="05df1-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="05df1-149">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="05df1-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="05df1-150">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="05df1-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="05df1-151">INPUTOBJECT <IMigrationItem> : azt a replikáló kiszolgálót adja meg, amelyhez a tulajdonságokat frissíteni kell.</span><span class="sxs-lookup"><span data-stu-id="05df1-151">INPUTOBJECT <IMigrationItem>: Specifies the replicating server for which the properties need to be updated.</span></span> <span data-ttu-id="05df1-152">A kiszolgálói objektum az Get-AzMigrateServerReplication parancsmag használatával is beolvasható.</span><span class="sxs-lookup"><span data-stu-id="05df1-152">The server object can be retrieved using the Get-AzMigrateServerReplication cmdlet.</span></span>
  - <span data-ttu-id="05df1-153">`[Location <String>]`: Erőforrás helye</span><span class="sxs-lookup"><span data-stu-id="05df1-153">`[Location <String>]`: Resource Location</span></span>
  - <span data-ttu-id="05df1-154">`[CurrentJobId <String>]`: A végrehajtandó feladat ARM azonosítója.</span><span class="sxs-lookup"><span data-stu-id="05df1-154">`[CurrentJobId <String>]`: The ARM Id of the job being executed.</span></span>
  - <span data-ttu-id="05df1-155">`[CurrentJobName <String>]`: A feladat neve.</span><span class="sxs-lookup"><span data-stu-id="05df1-155">`[CurrentJobName <String>]`: The job name.</span></span>
  - <span data-ttu-id="05df1-156">`[CurrentJobStartTime <DateTime?>]`: A feladat kezdési időpontja.</span><span class="sxs-lookup"><span data-stu-id="05df1-156">`[CurrentJobStartTime <DateTime?>]`: The start time of the job.</span></span>
  - <span data-ttu-id="05df1-157">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: Az áttelepítési szolgáltató egyéni beállításai.</span><span class="sxs-lookup"><span data-stu-id="05df1-157">`[ProviderSpecificDetail <IMigrationProviderSpecificSettings>]`: The migration provider custom settings.</span></span>

<span data-ttu-id="05df1-158">NICTOUPDATE <IVMwareCbtNicInput [] >: frissíti az Azure VM rendszerhez készült hálózati adaptert.</span><span class="sxs-lookup"><span data-stu-id="05df1-158">NICTOUPDATE <IVMwareCbtNicInput[]>: Updates the NIC for the Azure VM to be created.</span></span>
  - <span data-ttu-id="05df1-159">`IsPrimaryNic <String>`: Egy érték, amely azt jelzi, hogy az elsődleges NIC-e.</span><span class="sxs-lookup"><span data-stu-id="05df1-159">`IsPrimaryNic <String>`: A value indicating whether this is the primary NIC.</span></span>
  - <span data-ttu-id="05df1-160">`NicId <String>`: A NIC-azonosító.</span><span class="sxs-lookup"><span data-stu-id="05df1-160">`NicId <String>`: The NIC Id.</span></span>
  - <span data-ttu-id="05df1-161">`[IsSelectedForMigration <String>]`: Érték, amely azt jelzi, hogy be van-e jelölve az áttelepítéshez.</span><span class="sxs-lookup"><span data-stu-id="05df1-161">`[IsSelectedForMigration <String>]`: A value indicating whether this NIC is selected for migration.</span></span>
  - <span data-ttu-id="05df1-162">`[TargetStaticIPAddress <String>]`: A statikus IP-cím.</span><span class="sxs-lookup"><span data-stu-id="05df1-162">`[TargetStaticIPAddress <String>]`: The static IP address.</span></span>
  - <span data-ttu-id="05df1-163">`[TargetSubnetName <String>]`: Cél alhálózati név.</span><span class="sxs-lookup"><span data-stu-id="05df1-163">`[TargetSubnetName <String>]`: Target subnet name.</span></span>

## <span data-ttu-id="05df1-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="05df1-164">RELATED LINKS</span></span>

