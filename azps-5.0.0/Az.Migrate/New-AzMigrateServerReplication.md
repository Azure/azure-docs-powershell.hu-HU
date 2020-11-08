---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigrateserverreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateServerReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateServerReplication.md
ms.openlocfilehash: 0ef21777f5a7f22fff5d9352f667d8968ff843f3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187314"
---
# <span data-ttu-id="54306-101">New-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="54306-101">New-AzMigrateServerReplication</span></span>

## <span data-ttu-id="54306-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="54306-102">SYNOPSIS</span></span>
<span data-ttu-id="54306-103">A megadott kiszolgáló replikációjának indítása.</span><span class="sxs-lookup"><span data-stu-id="54306-103">Starts replication for the specified server.</span></span>

## <span data-ttu-id="54306-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="54306-104">SYNTAX</span></span>

### <span data-ttu-id="54306-105">ByIdDefaultUser (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="54306-105">ByIdDefaultUser (Default)</span></span>
```
New-AzMigrateServerReplication -DiskType <DiskAccountType> -LicenseType <LicenseType> -MachineId <String>
 -OSDiskID <String> -TargetNetworkId <String> -TargetResourceGroupId <String> -TargetSubnetName <String>
 -TargetVMName <String> [-DiskEncryptionSetID <String>] [-PerformAutoResync <String>]
 [-SubscriptionId <String>] [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetBootDiagnosticsStorageAccount <String>] [-TargetVMSize <String>] [-VMWarerunasaccountID <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="54306-106">ByIdPowerUser</span><span class="sxs-lookup"><span data-stu-id="54306-106">ByIdPowerUser</span></span>
```
New-AzMigrateServerReplication -DiskToInclude <IVMwareCbtDiskInput[]> -LicenseType <LicenseType>
 -MachineId <String> -TargetNetworkId <String> -TargetResourceGroupId <String> -TargetSubnetName <String>
 -TargetVMName <String> [-PerformAutoResync <String>] [-SubscriptionId <String>]
 [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetBootDiagnosticsStorageAccount <String>] [-TargetVMSize <String>] [-VMWarerunasaccountID <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="54306-107">ByInputObjectDefaultUser</span><span class="sxs-lookup"><span data-stu-id="54306-107">ByInputObjectDefaultUser</span></span>
```
New-AzMigrateServerReplication -DiskType <DiskAccountType> -InputObject <IVMwareMachine>
 -LicenseType <LicenseType> -OSDiskID <String> -TargetNetworkId <String> -TargetResourceGroupId <String>
 -TargetSubnetName <String> -TargetVMName <String> [-DiskEncryptionSetID <String>]
 [-PerformAutoResync <String>] [-SubscriptionId <String>] [-TargetAvailabilitySet <String>]
 [-TargetAvailabilityZone <String>] [-TargetBootDiagnosticsStorageAccount <String>] [-TargetVMSize <String>]
 [-VMWarerunasaccountID <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="54306-108">ByInputObjectPowerUser</span><span class="sxs-lookup"><span data-stu-id="54306-108">ByInputObjectPowerUser</span></span>
```
New-AzMigrateServerReplication -DiskToInclude <IVMwareCbtDiskInput[]> -InputObject <IVMwareMachine>
 -LicenseType <LicenseType> -TargetNetworkId <String> -TargetResourceGroupId <String>
 -TargetSubnetName <String> -TargetVMName <String> [-PerformAutoResync <String>] [-SubscriptionId <String>]
 [-TargetAvailabilitySet <String>] [-TargetAvailabilityZone <String>]
 [-TargetBootDiagnosticsStorageAccount <String>] [-TargetVMSize <String>] [-VMWarerunasaccountID <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="54306-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="54306-109">DESCRIPTION</span></span>
<span data-ttu-id="54306-110">A New-AzMigrateServerReplication parancsmag az Azure áttelepítési projektben egy bizonyos felfedezett kiszolgáló replikálását indítja el.</span><span class="sxs-lookup"><span data-stu-id="54306-110">The New-AzMigrateServerReplication cmdlet starts the replication for a particular discovered server in the Azure Migrate project.</span></span>

## <span data-ttu-id="54306-111">Példák</span><span class="sxs-lookup"><span data-stu-id="54306-111">EXAMPLES</span></span>

### <span data-ttu-id="54306-112">Példa 1: Ha csak az operációs rendszer lemeze van</span><span class="sxs-lookup"><span data-stu-id="54306-112">Example 1: When there is only OS disk</span></span>
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

<span data-ttu-id="54306-113">Ez a helyzet akkor jelenik meg, ha csak egyetlen, védett lemezről van-e szükség.</span><span class="sxs-lookup"><span data-stu-id="54306-113">This is for the scenario, when there is only one single disk that has to be protected.</span></span>

### <span data-ttu-id="54306-114">2. példa: több lemez esetén:</span><span class="sxs-lookup"><span data-stu-id="54306-114">Example 2: When there are multiple disks</span></span>
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

<span data-ttu-id="54306-115">Ez a helyzet akkor jelenik meg, ha több olyan lemez van, amelyet védeni kell.</span><span class="sxs-lookup"><span data-stu-id="54306-115">This is for the scenario, when there are multiple disks that has to be protected.</span></span>

## <span data-ttu-id="54306-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="54306-116">PARAMETERS</span></span>

### <span data-ttu-id="54306-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54306-117">-DefaultProfile</span></span>
<span data-ttu-id="54306-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="54306-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54306-119">-DiskEncryptionSetID</span><span class="sxs-lookup"><span data-stu-id="54306-119">-DiskEncryptionSetID</span></span>
<span data-ttu-id="54306-120">Adja meg a használni kívánt encyption.</span><span class="sxs-lookup"><span data-stu-id="54306-120">Specifies the disk encyption set to be used.</span></span>

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

### <span data-ttu-id="54306-121">-DiskToInclude</span><span class="sxs-lookup"><span data-stu-id="54306-121">-DiskToInclude</span></span>
<span data-ttu-id="54306-122">Itt adhatja meg, hogy a forráskiszolgálón mely lemezek kerüljenek a replikációba.</span><span class="sxs-lookup"><span data-stu-id="54306-122">Specifies the disks on the source server to be included for replication.</span></span>
<span data-ttu-id="54306-123">A kivitelezéshez tekintse meg a DISKTOINCLUDE tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="54306-123">To construct, see NOTES section for DISKTOINCLUDE properties and create a hash table.</span></span>

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

### <span data-ttu-id="54306-124">-DiskType</span><span class="sxs-lookup"><span data-stu-id="54306-124">-DiskType</span></span>
<span data-ttu-id="54306-125">Az Azure VM-hez használni kívánt lemezek típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="54306-125">Specifies the type of disks to be used for the Azure VM.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Support.DiskAccountType
Parameter Sets: ByIdDefaultUser, ByInputObjectDefaultUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54306-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="54306-126">-InputObject</span></span>
<span data-ttu-id="54306-127">Annak a felismert kiszolgálónak a meghatározása, amelyet át szeretne telepíteni.</span><span class="sxs-lookup"><span data-stu-id="54306-127">Specifies the discovered server to be migrated.</span></span>
<span data-ttu-id="54306-128">A kiszolgálói objektum az Get-AzMigrateServer parancsmag használatával is beolvasható.</span><span class="sxs-lookup"><span data-stu-id="54306-128">The server object can be retrieved using the Get-AzMigrateServer cmdlet.</span></span>
<span data-ttu-id="54306-129">A kivitelezéshez tekintse meg a INPUTOBJECT tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="54306-129">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="54306-130">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="54306-130">-LicenseType</span></span>
<span data-ttu-id="54306-131">Annak megadása, hogy az Azure hibrid előny a forráskiszolgáló áttelepítéséhez szükséges-e.</span><span class="sxs-lookup"><span data-stu-id="54306-131">Specifies if Azure Hybrid benefit is applicable for the source server to be migrated.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Support.LicenseType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54306-132">-MachineId</span><span class="sxs-lookup"><span data-stu-id="54306-132">-MachineId</span></span>
<span data-ttu-id="54306-133">Annak a felismert kiszolgálónak a gépi AZONOSÍTÓját adja meg, amelyet át szeretne telepíteni.</span><span class="sxs-lookup"><span data-stu-id="54306-133">Specifies the machine ID of the discovered server to be migrated.</span></span>

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

### <span data-ttu-id="54306-134">-OSDiskID</span><span class="sxs-lookup"><span data-stu-id="54306-134">-OSDiskID</span></span>
<span data-ttu-id="54306-135">Megadja az áttelepítendő forráskiszolgáló operációs rendszerének lemezét.</span><span class="sxs-lookup"><span data-stu-id="54306-135">Specifies the Operating System disk for the source server to be migrated.</span></span>

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

### <span data-ttu-id="54306-136">-PerformAutoResync</span><span class="sxs-lookup"><span data-stu-id="54306-136">-PerformAutoResync</span></span>
<span data-ttu-id="54306-137">Azt adja meg, hogy az automatikus javítás történik-e, ha a változtatások nyomon követése elvész a forráskiszolgálón a replikáció csoportban.</span><span class="sxs-lookup"><span data-stu-id="54306-137">Specifies if replication be auto-repaired in case change tracking is lost for the source server under replication.</span></span>

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

### <span data-ttu-id="54306-138">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="54306-138">-SubscriptionId</span></span>
<span data-ttu-id="54306-139">Azure-előfizetési azonosító</span><span class="sxs-lookup"><span data-stu-id="54306-139">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="54306-140">-TargetAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="54306-140">-TargetAvailabilitySet</span></span>
<span data-ttu-id="54306-141">Megadja a VM-creationSpecifies használandó elérhetőségi beállításokat a VM-készítéshez használt elérhetőségi érték esetén.</span><span class="sxs-lookup"><span data-stu-id="54306-141">Specifies the Availability Set to be used for VM creationSpecifies the Availability Set to be used for VM creation.</span></span>

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

### <span data-ttu-id="54306-142">-TargetAvailabilityZone</span><span class="sxs-lookup"><span data-stu-id="54306-142">-TargetAvailabilityZone</span></span>
<span data-ttu-id="54306-143">A VM-készítéshez használandó elérhetőségi zóna meghatározása.</span><span class="sxs-lookup"><span data-stu-id="54306-143">Specifies the Availability Zone to be used for VM creation.</span></span>

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

### <span data-ttu-id="54306-144">-TargetBootDiagnosticsStorageAccount</span><span class="sxs-lookup"><span data-stu-id="54306-144">-TargetBootDiagnosticsStorageAccount</span></span>
<span data-ttu-id="54306-145">Itt adhatja meg a boot Diagnostics rendszerhez használandó tárolási fiókot.</span><span class="sxs-lookup"><span data-stu-id="54306-145">Specifies the storage account to be used for boot diagnostics.</span></span>

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

### <span data-ttu-id="54306-146">-TargetNetworkId</span><span class="sxs-lookup"><span data-stu-id="54306-146">-TargetNetworkId</span></span>
<span data-ttu-id="54306-147">A cél Azure-előfizetéshez tartozó virtuális hálózati azonosítót adja meg, amelyre a kiszolgálót át kell telepíteni.</span><span class="sxs-lookup"><span data-stu-id="54306-147">Specifies the Virtual Network id within the destination Azure subscription to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="54306-148">-TargetResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="54306-148">-TargetResourceGroupId</span></span>
<span data-ttu-id="54306-149">A cél Azure-előfizetéshez tartozó erőforráscsoport azonosítóját adja meg, amelyre a kiszolgálót át kell telepíteni.</span><span class="sxs-lookup"><span data-stu-id="54306-149">Specifies the Resource Group id within the destination Azure subscription to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="54306-150">-TargetSubnetName</span><span class="sxs-lookup"><span data-stu-id="54306-150">-TargetSubnetName</span></span>
<span data-ttu-id="54306-151">Annak a virtuális netowk a neve, amelyhez a kiszolgálót át kell telepíteni.</span><span class="sxs-lookup"><span data-stu-id="54306-151">Specifies the Subnet name within the destination Virtual Netowk to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="54306-152">-TargetVMName</span><span class="sxs-lookup"><span data-stu-id="54306-152">-TargetVMName</span></span>
<span data-ttu-id="54306-153">A létrehozandó Azure VM-VM nevet adja meg.</span><span class="sxs-lookup"><span data-stu-id="54306-153">Specifies the name of the Azure VM to be created.</span></span>

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

### <span data-ttu-id="54306-154">-TargetVMSize</span><span class="sxs-lookup"><span data-stu-id="54306-154">-TargetVMSize</span></span>
<span data-ttu-id="54306-155">A létrehozandó Azure VM-SKU-t adja meg.</span><span class="sxs-lookup"><span data-stu-id="54306-155">Specifies the SKU of the Azure VM to be created.</span></span>

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

### <span data-ttu-id="54306-156">-VMWarerunasaccountID</span><span class="sxs-lookup"><span data-stu-id="54306-156">-VMWarerunasaccountID</span></span>
<span data-ttu-id="54306-157">Fiók azonosítója.</span><span class="sxs-lookup"><span data-stu-id="54306-157">Account id.</span></span>

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

### <span data-ttu-id="54306-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54306-158">CommonParameters</span></span>
<span data-ttu-id="54306-159">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="54306-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54306-160">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="54306-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54306-161">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="54306-161">INPUTS</span></span>

## <span data-ttu-id="54306-162">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="54306-162">OUTPUTS</span></span>

### <span data-ttu-id="54306-163">Microsoft. Azure. PowerShell. parancsmagok. áttelepítés. models. Api20180110. IJob</span><span class="sxs-lookup"><span data-stu-id="54306-163">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob</span></span>

## <span data-ttu-id="54306-164">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="54306-164">NOTES</span></span>

<span data-ttu-id="54306-165">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="54306-165">ALIASES</span></span>

<span data-ttu-id="54306-166">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="54306-166">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="54306-167">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="54306-167">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="54306-168">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="54306-168">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="54306-169">DISKTOINCLUDE <IVMwareCbtDiskInput [] >: Itt adhatja meg, hogy a forráskiszolgálón milyen lemezek szerepeljenek a replikációban.</span><span class="sxs-lookup"><span data-stu-id="54306-169">DISKTOINCLUDE <IVMwareCbtDiskInput[]>: Specifies the disks on the source server to be included for replication.</span></span>
  - <span data-ttu-id="54306-170">`DiskId <String>`: A lemezvezérlő-azonosító.</span><span class="sxs-lookup"><span data-stu-id="54306-170">`DiskId <String>`: The disk Id.</span></span>
  - <span data-ttu-id="54306-171">`IsOSDisk <String>`: Érték, amely azt jelzi, hogy a lemez az operációs rendszer lemeze-e.</span><span class="sxs-lookup"><span data-stu-id="54306-171">`IsOSDisk <String>`: A value indicating whether the disk is the OS disk.</span></span>
  - <span data-ttu-id="54306-172">`LogStorageAccountId <String>`: A log Storage Account ARM azonosítója.</span><span class="sxs-lookup"><span data-stu-id="54306-172">`LogStorageAccountId <String>`: The log storage account ARM Id.</span></span>
  - <span data-ttu-id="54306-173">`LogStorageAccountSasSecretName <String>`: A napló tárterületének titkos neve.</span><span class="sxs-lookup"><span data-stu-id="54306-173">`LogStorageAccountSasSecretName <String>`: The key vault secret name of the log storage account.</span></span>
  - <span data-ttu-id="54306-174">`[DiskEncryptionSetId <String>]`: A DiskEncryptionSet-kar azonosítója.</span><span class="sxs-lookup"><span data-stu-id="54306-174">`[DiskEncryptionSetId <String>]`: The DiskEncryptionSet ARM Id.</span></span>
  - <span data-ttu-id="54306-175">`[DiskType <DiskAccountType?>]`: A lemez típusa.</span><span class="sxs-lookup"><span data-stu-id="54306-175">`[DiskType <DiskAccountType?>]`: The disk type.</span></span>

<span data-ttu-id="54306-176">INPUTOBJECT <IVMwareMachine> : az áttelepítendő kiszolgálót adja meg.</span><span class="sxs-lookup"><span data-stu-id="54306-176">INPUTOBJECT <IVMwareMachine>: Specifies the discovered server to be migrated.</span></span> <span data-ttu-id="54306-177">A kiszolgálói objektum az Get-AzMigrateServer parancsmag használatával is beolvasható.</span><span class="sxs-lookup"><span data-stu-id="54306-177">The server object can be retrieved using the Get-AzMigrateServer cmdlet.</span></span>
  - <span data-ttu-id="54306-178">`[GuestOSDetailOstype <String>]`: Az operációs rendszer típusa.</span><span class="sxs-lookup"><span data-stu-id="54306-178">`[GuestOSDetailOstype <String>]`: Type of the operating system.</span></span>

## <span data-ttu-id="54306-179">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="54306-179">RELATED LINKS</span></span>

