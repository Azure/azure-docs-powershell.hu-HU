---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/new-azmigrateserverreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateServerReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateServerReplication.md
ms.openlocfilehash: cf6b87b8d03855ae79fc0cea62a3bd126f8342a0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930481"
---
# <span data-ttu-id="02319-101">New-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="02319-101">New-AzMigrateServerReplication</span></span>

## <span data-ttu-id="02319-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02319-102">SYNOPSIS</span></span>
<span data-ttu-id="02319-103">Replikáció indítása a megadott kiszolgálóhoz.</span><span class="sxs-lookup"><span data-stu-id="02319-103">Starts replication for the specified server.</span></span>

## <span data-ttu-id="02319-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="02319-104">SYNTAX</span></span>

### <span data-ttu-id="02319-105">ByIdDefaultUser (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="02319-105">ByIdDefaultUser (Default)</span></span>
```
New-AzMigrateServerReplication -DiskType <String> -LicenseType <String> -MachineId <String> -OSDiskID <String>
 -TargetNetworkId <String> -TargetResourceGroupId <String> -TargetSubnetName <String> -TargetVMName <String>
 [-DiskEncryptionSetID <String>] [-PerformAutoResync <String>] [-SubscriptionId <String>]
 [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetBootDiagnosticsStorageAccount <String>] [-TargetVMSize <String>] [-VMWarerunasaccountID <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="02319-106">ByIdPowerUser</span><span class="sxs-lookup"><span data-stu-id="02319-106">ByIdPowerUser</span></span>
```
New-AzMigrateServerReplication -DiskToInclude <IVMwareCbtDiskInput[]> -LicenseType <String>
 -MachineId <String> -TargetNetworkId <String> -TargetResourceGroupId <String> -TargetSubnetName <String>
 -TargetVMName <String> [-PerformAutoResync <String>] [-SubscriptionId <String>]
 [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetBootDiagnosticsStorageAccount <String>] [-TargetVMSize <String>] [-VMWarerunasaccountID <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="02319-107">ByInputObjectDefaultUser</span><span class="sxs-lookup"><span data-stu-id="02319-107">ByInputObjectDefaultUser</span></span>
```
New-AzMigrateServerReplication -DiskType <String> -InputObject <IVMwareMachine> -LicenseType <String>
 -OSDiskID <String> -TargetNetworkId <String> -TargetResourceGroupId <String> -TargetSubnetName <String>
 -TargetVMName <String> [-DiskEncryptionSetID <String>] [-PerformAutoResync <String>]
 [-SubscriptionId <String>] [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetBootDiagnosticsStorageAccount <String>] [-TargetVMSize <String>] [-VMWarerunasaccountID <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="02319-108">ByInputObjectPowerUser</span><span class="sxs-lookup"><span data-stu-id="02319-108">ByInputObjectPowerUser</span></span>
```
New-AzMigrateServerReplication -DiskToInclude <IVMwareCbtDiskInput[]> -InputObject <IVMwareMachine>
 -LicenseType <String> -TargetNetworkId <String> -TargetResourceGroupId <String> -TargetSubnetName <String>
 -TargetVMName <String> [-PerformAutoResync <String>] [-SubscriptionId <String>]
 [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetBootDiagnosticsStorageAccount <String>] [-TargetVMSize <String>] [-VMWarerunasaccountID <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="02319-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="02319-109">DESCRIPTION</span></span>
<span data-ttu-id="02319-110">A New-AzMigrateServerReplication parancsmag elindítja a replikációt az Azure-áttelepítési projekt egy bizonyos felderített kiszolgálója számára.</span><span class="sxs-lookup"><span data-stu-id="02319-110">The New-AzMigrateServerReplication cmdlet starts the replication for a particular discovered server in the Azure Migrate project.</span></span>

## <span data-ttu-id="02319-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="02319-111">EXAMPLES</span></span>

### <span data-ttu-id="02319-112">1. példa: Ha csak az operációs rendszer lemeze van</span><span class="sxs-lookup"><span data-stu-id="02319-112">Example 1: When there is only OS disk</span></span>
```powershell
PS C:\> New-AzMigrateServerReplication -MachineId "/subscriptions/xxx-xxx-xxx4/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.OffAzure/VMwareSites/AzMigratePWSHTc8d1site/machines/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f" -LicenseType NoLicenseType -TargetResourceGroupId "/subscriptions/xxx-xxx-xxx/resourceGroups/AzMigratePWSHtargetRG" -TargetNetworkId  "/subscriptions/xxx-xxx-xxx/resourceGroups/AzMigratePWSHtargetRG/providers/Microsoft.Network/virtualNetworks/AzMigrateTargetNetwork" -TargetSubnetName default -TargetVMName "prsadhu-TestVM" -DiskType "Standard_LRS" -OSDiskID "6000C299-343d-7bcd-c05e-a94bd63316dd"

ActivityId                       : 68af14b4-46ae-48d1-b3e9-cdcffb9e8a93 ActivityId: 74d1a396-1d37-4264-8a5b-b727aaef0171
AllowedAction                    : {}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          : 9/16/20 11:57:33 AM
Error                            : {}
FriendlyName                     : Enable
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/997e2a92-5afe-49c7-a81a-89660aec9b7b
Location                         :
Name                             : 997e2a92-5afe-49c7-a81a-89660aec9b7b
ScenarioName                     : Enable
StartTime                        : 9/16/20 11:57:32 AM
State                            : Succeeded
StateDescription                 : Completed
TargetInstanceType               : ProtectionProfile
TargetObjectId                   : 42752b89-5fad-52fd-bf93-679fbdb6fed9
TargetObjectName                 : migrateAzMigratePWSHTc8d1sitepolicy
Task                             : {CloudPairingPrerequisitesCheck, CloudPairingPrepareSite}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="02319-113">Ez olyan esetben van így, amikor csak egyetlen lemez van védve.</span><span class="sxs-lookup"><span data-stu-id="02319-113">This is for the scenario, when there is only one single disk that has to be protected.</span></span>

### <span data-ttu-id="02319-114">2. példa: Több lemez esetén</span><span class="sxs-lookup"><span data-stu-id="02319-114">Example 2: When there are multiple disks</span></span>
```powershell
PS C:\> $OSDisk = New-AzMigrateDiskMapping -DiskID '6000C299-343d-7bcd-c05e-a94bd63316dd' -DiskType 'Standard_LRS' -IsOSDisk 'true'
PS C:\> $DataDisk = New-AzMigrateDiskMapping -DiskID '7000C299-343d-7bcd-c05e-a94bd63316dd' -DiskType 'Standard_LRS' -IsOSDisk 'false'
PS C:\> $DisksToInclude += $OSDisk
PS C:\> $DisksToInclude += $DataDisk
PS C:\> New-AzMigrateServerReplication -MachineId "/subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.OffAzure/VMwareSites/AzMigratePWSHTc8d1site/machines/bcdr-vcenter-fareast-corp-micro-cfcc5a24-a40e-56b9-a6af-e206c9ca4f93_50063baa-9806-d6d6-7e09-c0ae87309b4f" -LicenseType NoLicenseType -TargetResourceGroupId "/subscriptions/xxx-xxx-xxx/resourceGroups/AzMigratePWSHtargetRG" -TargetNetworkId  "/subscriptions/xxx-xxx-xxx/resourceGroups/AzMigratePWSHtargetRG/providers/Microsoft.Network/virtualNetworks/AzMigrateTargetNetwork" -TargetSubnetName default -TargetVMName "prsadhu-TestVM" -DiskToInclude $DisksToInclude -PerformAutoResync true

ActivityId                       : 68af14b4-46ae-48d1-b3e9-cdcffb9e8a93 ActivityId: 74d1a396-1d37-4264-8a5b-b727aaef0171
AllowedAction                    : {}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          : 9/16/20 11:57:33 AM
Error                            : {}
FriendlyName                     : Enable
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/997e2a92-5afe-49c7-a81a-89660aec9b7b
Location                         :
Name                             : 997e2a92-5afe-49c7-a81a-89660aec9b7b
ScenarioName                     : Enable
StartTime                        : 9/16/20 11:57:32 AM
State                            : Succeeded
StateDescription                 : Completed
TargetInstanceType               : ProtectionProfile
TargetObjectId                   : 42752b89-5fad-52fd-bf93-679fbdb6fed9
TargetObjectName                 : migrateAzMigratePWSHTc8d1sitepolicy
Task                             : {CloudPairingPrerequisitesCheck, CloudPairingPrepareSite}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

<span data-ttu-id="02319-115">Ez akkor van így, ha több lemez van, amelyek védettek.</span><span class="sxs-lookup"><span data-stu-id="02319-115">This is for the scenario, when there are multiple disks that has to be protected.</span></span>

## <span data-ttu-id="02319-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="02319-116">PARAMETERS</span></span>

### <span data-ttu-id="02319-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02319-117">-DefaultProfile</span></span>
<span data-ttu-id="02319-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="02319-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02319-119">-DiskEncryptionSetID</span><span class="sxs-lookup"><span data-stu-id="02319-119">-DiskEncryptionSetID</span></span>
<span data-ttu-id="02319-120">A használni használt lemez-encyption-készletet adja meg.</span><span class="sxs-lookup"><span data-stu-id="02319-120">Specifies the disk encyption set to be used.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIdDefaultUser, ByInputObjectDefaultUser
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02319-121">-DiskToInclude</span><span class="sxs-lookup"><span data-stu-id="02319-121">-DiskToInclude</span></span>
<span data-ttu-id="02319-122">Megadja, hogy a forráskiszolgáló mely lemezeket tartalmazza a replikációhoz.</span><span class="sxs-lookup"><span data-stu-id="02319-122">Specifies the disks on the source server to be included for replication.</span></span>
<span data-ttu-id="02319-123">A felépítésről a DISKTOINCLUDE tulajdonságokat és a kivonattáblát a NOTES (MEGJEGYZÉSEK) című szakaszban láthatja.</span><span class="sxs-lookup"><span data-stu-id="02319-123">To construct, see NOTES section for DISKTOINCLUDE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtDiskInput[]
Parameter Sets: ByIdPowerUser, ByInputObjectPowerUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02319-124">-DiskType</span><span class="sxs-lookup"><span data-stu-id="02319-124">-DiskType</span></span>
<span data-ttu-id="02319-125">Az Azure VM-hez használt lemeztípust határozza meg.</span><span class="sxs-lookup"><span data-stu-id="02319-125">Specifies the type of disks to be used for the Azure VM.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIdDefaultUser, ByInputObjectDefaultUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02319-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="02319-126">-InputObject</span></span>
<span data-ttu-id="02319-127">Az áttelepíteni talált kiszolgálót határozza meg.</span><span class="sxs-lookup"><span data-stu-id="02319-127">Specifies the discovered server to be migrated.</span></span>
<span data-ttu-id="02319-128">A kiszolgálóobjektum a Get-AzMigrateServer le.</span><span class="sxs-lookup"><span data-stu-id="02319-128">The server object can be retrieved using the Get-AzMigrateServer cmdlet.</span></span>
<span data-ttu-id="02319-129">Ennek létrehozásáról az INPUTOBJECT tulajdonságokat és egy kivonattáblát a JEGYZETEK szakaszban talál.</span><span class="sxs-lookup"><span data-stu-id="02319-129">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVMwareMachine
Parameter Sets: ByInputObjectDefaultUser, ByInputObjectPowerUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02319-130">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="02319-130">-LicenseType</span></span>
<span data-ttu-id="02319-131">Azt adja meg, hogy az Azure Hibrid előny alkalmazható-e a forráskiszolgáló áttelepítésére.</span><span class="sxs-lookup"><span data-stu-id="02319-131">Specifies if Azure Hybrid benefit is applicable for the source server to be migrated.</span></span>

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

### <span data-ttu-id="02319-132">-MachineId</span><span class="sxs-lookup"><span data-stu-id="02319-132">-MachineId</span></span>
<span data-ttu-id="02319-133">Az áttelepíteni talált kiszolgáló számítógépazonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="02319-133">Specifies the machine ID of the discovered server to be migrated.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIdDefaultUser, ByIdPowerUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02319-134">-OSDiskID</span><span class="sxs-lookup"><span data-stu-id="02319-134">-OSDiskID</span></span>
<span data-ttu-id="02319-135">Annak az operációs rendszernek a lemeze, amelybe áttelepíti a forráskiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="02319-135">Specifies the Operating System disk for the source server to be migrated.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIdDefaultUser, ByInputObjectDefaultUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02319-136">-PerformAutoResync</span><span class="sxs-lookup"><span data-stu-id="02319-136">-PerformAutoResync</span></span>
<span data-ttu-id="02319-137">Azt adja meg, hogy a replikáció automatikus javítása történik-e abban az esetben, ha a replikáció alatt található forráskiszolgáló esetében a változások követése elveszik.</span><span class="sxs-lookup"><span data-stu-id="02319-137">Specifies if replication be auto-repaired in case change tracking is lost for the source server under replication.</span></span>

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

### <span data-ttu-id="02319-138">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="02319-138">-SubscriptionId</span></span>
<span data-ttu-id="02319-139">Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="02319-139">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="02319-140">-TargetAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="02319-140">-TargetAvailabilitySet</span></span>
<span data-ttu-id="02319-141">Megadja a VM-létrehozáshoz használható rendelkezésre állási halmazT, amely meghatározza a VM-létrehozáshoz használható rendelkezésre állási készletet.</span><span class="sxs-lookup"><span data-stu-id="02319-141">Specifies the Availability Set to be used for VM creationSpecifies the Availability Set to be used for VM creation.</span></span>

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

### <span data-ttu-id="02319-142">-TargetAvailabilityZone</span><span class="sxs-lookup"><span data-stu-id="02319-142">-TargetAvailabilityZone</span></span>
<span data-ttu-id="02319-143">Megadja a VIRTUÁLIS gép létrehozásához használt rendelkezésre állási zónát.</span><span class="sxs-lookup"><span data-stu-id="02319-143">Specifies the Availability Zone to be used for VM creation.</span></span>

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

### <span data-ttu-id="02319-144">-TargetBootDiagnosticsStorageAccount</span><span class="sxs-lookup"><span data-stu-id="02319-144">-TargetBootDiagnosticsStorageAccount</span></span>
<span data-ttu-id="02319-145">Megadja a rendszerindítási diagnosztikához használt tárfiókot.</span><span class="sxs-lookup"><span data-stu-id="02319-145">Specifies the storage account to be used for boot diagnostics.</span></span>

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

### <span data-ttu-id="02319-146">-TargetNetworkId</span><span class="sxs-lookup"><span data-stu-id="02319-146">-TargetNetworkId</span></span>
<span data-ttu-id="02319-147">Megadja a virtuális hálózat azonosítóját azon a cél Azure-előfizetésen belül, amelybe a kiszolgálót át kell migrálni.</span><span class="sxs-lookup"><span data-stu-id="02319-147">Specifies the Virtual Network id within the destination Azure subscription to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="02319-148">-TargetResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="02319-148">-TargetResourceGroupId</span></span>
<span data-ttu-id="02319-149">Azt az Erőforráscsoport-azonosítót adja meg azon a cél Azure-előfizetésen belül, amelybe át kell migrálni a kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="02319-149">Specifies the Resource Group id within the destination Azure subscription to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="02319-150">-TargetSubnetName</span><span class="sxs-lookup"><span data-stu-id="02319-150">-TargetSubnetName</span></span>
<span data-ttu-id="02319-151">Megadja annak az alhálózatnak a nevét a virtual netowk célhelyen belül, amelybe át kell migrálni a kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="02319-151">Specifies the Subnet name within the destination Virtual Netowk to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="02319-152">-TargetVMName</span><span class="sxs-lookup"><span data-stu-id="02319-152">-TargetVMName</span></span>
<span data-ttu-id="02319-153">A létrehozható Azure VM nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="02319-153">Specifies the name of the Azure VM to be created.</span></span>

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

### <span data-ttu-id="02319-154">-TargetVMSize</span><span class="sxs-lookup"><span data-stu-id="02319-154">-TargetVMSize</span></span>
<span data-ttu-id="02319-155">Megadja a létrehozható Azure VM termékváltozatát.</span><span class="sxs-lookup"><span data-stu-id="02319-155">Specifies the SKU of the Azure VM to be created.</span></span>

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

### <span data-ttu-id="02319-156">-VMWarerunasaccountID</span><span class="sxs-lookup"><span data-stu-id="02319-156">-VMWarerunasaccountID</span></span>
<span data-ttu-id="02319-157">Fiókazonosító.</span><span class="sxs-lookup"><span data-stu-id="02319-157">Account id.</span></span>

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

### <span data-ttu-id="02319-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02319-158">CommonParameters</span></span>
<span data-ttu-id="02319-159">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02319-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02319-160">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="02319-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02319-161">INPUTS</span><span class="sxs-lookup"><span data-stu-id="02319-161">INPUTS</span></span>

## <span data-ttu-id="02319-162">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="02319-162">OUTPUTS</span></span>

### <span data-ttu-id="02319-163">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span><span class="sxs-lookup"><span data-stu-id="02319-163">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="02319-164">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="02319-164">NOTES</span></span>

<span data-ttu-id="02319-165">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="02319-165">ALIASES</span></span>

<span data-ttu-id="02319-166">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="02319-166">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="02319-167">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="02319-167">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="02319-168">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="02319-168">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="02319-169">DISKTOINCLUDE <IVMwareCbtDiskInput[]>: A forráskiszolgálón a replikációhoz szükséges lemezeket adja meg.</span><span class="sxs-lookup"><span data-stu-id="02319-169">DISKTOINCLUDE <IVMwareCbtDiskInput[]>: Specifies the disks on the source server to be included for replication.</span></span>
  - <span data-ttu-id="02319-170">`DiskId <String>`: A lemezazonosító.</span><span class="sxs-lookup"><span data-stu-id="02319-170">`DiskId <String>`: The disk Id.</span></span>
  - <span data-ttu-id="02319-171">`IsOSDisk <String>`: Egy érték, amely azt jelzi, hogy a lemez az operációs rendszer lemeze-e.</span><span class="sxs-lookup"><span data-stu-id="02319-171">`IsOSDisk <String>`: A value indicating whether the disk is the OS disk.</span></span>
  - <span data-ttu-id="02319-172">`LogStorageAccountId <String>`: A naplótároló fiók ARM azonosító.</span><span class="sxs-lookup"><span data-stu-id="02319-172">`LogStorageAccountId <String>`: The log storage account ARM Id.</span></span>
  - <span data-ttu-id="02319-173">`LogStorageAccountSasSecretName <String>`: A naplótároló fiók kulcstárának titkos neve.</span><span class="sxs-lookup"><span data-stu-id="02319-173">`LogStorageAccountSasSecretName <String>`: The key vault secret name of the log storage account.</span></span>
  - <span data-ttu-id="02319-174">`[DiskEncryptionSetId <String>]`: The DiskEncryptionSet ARM Id.</span><span class="sxs-lookup"><span data-stu-id="02319-174">`[DiskEncryptionSetId <String>]`: The DiskEncryptionSet ARM Id.</span></span>
  - <span data-ttu-id="02319-175">`[DiskType <DiskAccountType?>]`: A lemez típusa.</span><span class="sxs-lookup"><span data-stu-id="02319-175">`[DiskType <DiskAccountType?>]`: The disk type.</span></span>

<span data-ttu-id="02319-176">INPUTOBJECT: Az áttelepíteni <IVMwareMachine> szükséges felderített kiszolgáló.</span><span class="sxs-lookup"><span data-stu-id="02319-176">INPUTOBJECT <IVMwareMachine>: Specifies the discovered server to be migrated.</span></span> <span data-ttu-id="02319-177">A kiszolgálóobjektum a Get-AzMigrateServer le.</span><span class="sxs-lookup"><span data-stu-id="02319-177">The server object can be retrieved using the Get-AzMigrateServer cmdlet.</span></span>
  - <span data-ttu-id="02319-178">`[GuestOSDetailOstype <String>]`: Az operációs rendszer típusa.</span><span class="sxs-lookup"><span data-stu-id="02319-178">`[GuestOSDetailOstype <String>]`: Type of the operating system.</span></span>

## <span data-ttu-id="02319-179">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="02319-179">RELATED LINKS</span></span>

