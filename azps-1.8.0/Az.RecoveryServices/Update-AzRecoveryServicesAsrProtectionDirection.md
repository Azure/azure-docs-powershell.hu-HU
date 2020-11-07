---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrprotectiondirection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionDirection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionDirection.md
ms.openlocfilehash: 9dd28cd3a05db15cef64a1e6023b1684909fdc13
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669575"
---
# <span data-ttu-id="4fb08-101">Update-AzRecoveryServicesAsrProtectionDirection</span><span class="sxs-lookup"><span data-stu-id="4fb08-101">Update-AzRecoveryServicesAsrProtectionDirection</span></span>

## <span data-ttu-id="4fb08-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4fb08-102">SYNOPSIS</span></span>
<span data-ttu-id="4fb08-103">Frissíti a megadott replikációs védett elem vagy helyreállítási terv replikációs irányát.</span><span class="sxs-lookup"><span data-stu-id="4fb08-103">Updates the replication direction for the specified replication protected item or recovery plan.</span></span> <span data-ttu-id="4fb08-104">A replikált elem vagy helyreállítási terv ismételt védelméhez/visszavonásához használható.</span><span class="sxs-lookup"><span data-stu-id="4fb08-104">Used to re-protect/reverse replicate a failed over replicated item or recovery plan.</span></span>

## <span data-ttu-id="4fb08-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4fb08-105">SYNTAX</span></span>

### <span data-ttu-id="4fb08-106">ByRPIObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4fb08-106">ByRPIObject (Default)</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4fb08-107">AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="4fb08-107">AzureToVMware</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-AzureToVMware] [-Account <ASRRunAsAccount>]
 -DataStore <ASRDataStore> [-MasterTarget <ASRMasterTargetServer>] -ProcessServer <ASRProcessServer>
 -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> -Direction <String>
 -RetentionVolume <ASRRetentionVolume> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4fb08-108">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="4fb08-108">VMwareToAzure</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-VMwareToAzure] -Account <ASRRunAsAccount>
 [-MasterTarget <ASRMasterTargetServer>] -ProcessServer <ASRProcessServer>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> [-LogStorageAccountId <String>]
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4fb08-109">HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="4fb08-109">HyperVToAzure</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-HyperVToAzure] [-LogStorageAccountId <String>]
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4fb08-110">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="4fb08-110">EnterpriseToEnterprise</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-VmmToVmm]
 -ReplicationProtectedItem <ASRReplicationProtectedItem> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4fb08-111">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="4fb08-111">AzureToAzure</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-AzureToAzure]
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -LogStorageAccountId <String>
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-RecoveryResourceGroupId <String>] [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilitySetId <String>]
 [-RecoveryBootDiagStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4fb08-112">AzureToAzureWithMultipleStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4fb08-112">AzureToAzureWithMultipleStorageAccount</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-AzureToAzure]
 -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -AzureToAzureDiskReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-RecoveryResourceGroupId <String>]
 [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilitySetId <String>]
 [-RecoveryBootDiagStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4fb08-113">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="4fb08-113">ByRPObject</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4fb08-114">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="4fb08-114">ByPEObject</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -Direction <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4fb08-115">Leírás</span><span class="sxs-lookup"><span data-stu-id="4fb08-115">DESCRIPTION</span></span>
<span data-ttu-id="4fb08-116">Az **Update-AzRecoveryServicesAsrProtectionDirection** parancsmag a megadott Azure-webhely helyreállítási objektumának replikációs irányát frissíti a véglegesítést követő feladatátvételi művelet befejezése után.</span><span class="sxs-lookup"><span data-stu-id="4fb08-116">The **Update-AzRecoveryServicesAsrProtectionDirection** cmdlet updates the replication direction for the specified Azure Site Recovery object after the completion of a commit failover operation.</span></span>

## <span data-ttu-id="4fb08-117">Példák</span><span class="sxs-lookup"><span data-stu-id="4fb08-117">EXAMPLES</span></span>

### <span data-ttu-id="4fb08-118">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4fb08-118">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="4fb08-119">Indítsa el a megadott helyreállítási csomag frissítési irányát, és a művelet nyomon követéséhez használt ASR-objektum értékét adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="4fb08-119">Start the update direction operation for the specified recovery plan and returns the ASR job object used to track the operation.</span></span>

### <span data-ttu-id="4fb08-120">2. példa</span><span class="sxs-lookup"><span data-stu-id="4fb08-120">Example 2</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzToAzure -ProtectionContainerMapping $B2ApcmMapping -LogStorageAccountId $cacheStorageId `
 -ReplicationProtectedItem $rpi
```

<span data-ttu-id="4fb08-121">A megfelelő replikációs védelemmel ellátott elem frissítési irányának indítása a tároló Azure-területen, a tároló-tárolók megfeleltetése és a gyorsítótár-tároló használata (a VM-ben).</span><span class="sxs-lookup"><span data-stu-id="4fb08-121">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and using cache storage (in same region as VM).</span></span>

### <span data-ttu-id="4fb08-122">3. példa</span><span class="sxs-lookup"><span data-stu-id="4fb08-122">Example 3</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzToAzure -ProtectionContainerMapping $B2ApcmMapping `
 -AzToAzureDiskReplicationConfiguration $disk1,$disk2 -ReplicationProtectedItem  $rpi
```

<span data-ttu-id="4fb08-123">A megfelelő replikációs védett elem frissítési irányának indítása a tároló Azure régióban, a védett tárolók megfeleltetése és a lemezkvóta-konfiguráció megadása által meghatározva.</span><span class="sxs-lookup"><span data-stu-id="4fb08-123">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and provided disk replication configuration.</span></span>

## <span data-ttu-id="4fb08-124">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4fb08-124">PARAMETERS</span></span>

### <span data-ttu-id="4fb08-125">-Fiók</span><span class="sxs-lookup"><span data-stu-id="4fb08-125">-Account</span></span>
<span data-ttu-id="4fb08-126">A Futtatás mint fiók, amellyel szükség esetén lenyomhatja a mobil szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="4fb08-126">The run as account to be used to push install the Mobility service if needed.</span></span> <span data-ttu-id="4fb08-127">Az ASR-anyagban a Run as (futtatási) fiókból kell lennie.</span><span class="sxs-lookup"><span data-stu-id="4fb08-127">Must be one from the list of run as accounts in the ASR fabric.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRunAsAccount
Parameter Sets: AzureToVMware
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRunAsAccount
Parameter Sets: VMwareToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fb08-128">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="4fb08-128">-AzureToAzure</span></span>
<span data-ttu-id="4fb08-129">{{Fill AzureToAzure Description}}</span><span class="sxs-lookup"><span data-stu-id="4fb08-129">{{Fill AzureToAzure Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fb08-130">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="4fb08-130">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="4fb08-131">{{Fill AzureToAzureDiskReplicationConfiguration Description}}</span><span class="sxs-lookup"><span data-stu-id="4fb08-131">{{Fill AzureToAzureDiskReplicationConfiguration Description}}</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig[]
Parameter Sets: AzureToAzureWithMultipleStorageAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fb08-132">-AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="4fb08-132">-AzureToVMware</span></span>
<span data-ttu-id="4fb08-133">{{Fill AzureToVMware Description}}</span><span class="sxs-lookup"><span data-stu-id="4fb08-133">{{Fill AzureToVMware Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToVMware
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fb08-134">-Adattár</span><span class="sxs-lookup"><span data-stu-id="4fb08-134">-DataStore</span></span>
<span data-ttu-id="4fb08-135">A vmdisk használt VMware adattár.</span><span class="sxs-lookup"><span data-stu-id="4fb08-135">The VMware datastore to be used for the vmdisk's.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRDataStore
Parameter Sets: AzureToVMware
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fb08-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fb08-136">-DefaultProfile</span></span>
<span data-ttu-id="4fb08-137">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4fb08-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fb08-138">-Irány</span><span class="sxs-lookup"><span data-stu-id="4fb08-138">-Direction</span></span>
<span data-ttu-id="4fb08-139">Megadja, hogy milyen irányt kell használni a frissítési művelethez a feladatátvétel után.</span><span class="sxs-lookup"><span data-stu-id="4fb08-139">Specifies the direction to be used for the update operation post a failover.</span></span>
<span data-ttu-id="4fb08-140">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="4fb08-140">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4fb08-141">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="4fb08-141">PrimaryToRecovery</span></span>
- <span data-ttu-id="4fb08-142">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="4fb08-142">RecoveryToPrimary</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPIObject, AzureToVMware, VMwareToAzure, HyperVToAzure, EnterpriseToEnterprise, ByRPObject, ByPEObject
Aliases:
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fb08-143">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="4fb08-143">-HyperVToAzure</span></span>
<span data-ttu-id="4fb08-144">A Hyper-V virtuális gép újravédelme a visszaállás után.</span><span class="sxs-lookup"><span data-stu-id="4fb08-144">Reprotect a Hyper-V virtual machine after failback.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: HyperVToAzure
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fb08-145">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="4fb08-145">-LogStorageAccountId</span></span>
<span data-ttu-id="4fb08-146">Megadja a tárolási fiók AZONOSÍTÓját a VMs-alapú replikációs napló tárolásához.</span><span class="sxs-lookup"><span data-stu-id="4fb08-146">Specifies the storage account ID to store the replication log of VMs.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, HyperVToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fb08-147">-MasterTarget</span><span class="sxs-lookup"><span data-stu-id="4fb08-147">-MasterTarget</span></span>
<span data-ttu-id="4fb08-148">A fő célkiszolgáló adatai</span><span class="sxs-lookup"><span data-stu-id="4fb08-148">Master Target Server Details.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRMasterTargetServer
Parameter Sets: AzureToVMware, VMwareToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fb08-149">-ProcessServer</span><span class="sxs-lookup"><span data-stu-id="4fb08-149">-ProcessServer</span></span>
<span data-ttu-id="4fb08-150">A replikációhoz használandó folyamat kiszolgálója.</span><span class="sxs-lookup"><span data-stu-id="4fb08-150">Process Server to be used for replication.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProcessServer
Parameter Sets: AzureToVMware, VMwareToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fb08-151">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="4fb08-151">-ProtectionContainerMapping</span></span>
<span data-ttu-id="4fb08-152">A replikációhoz használni kívánt védelmi containerMapping.</span><span class="sxs-lookup"><span data-stu-id="4fb08-152">Protection containerMapping to be used for replication.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping
Parameter Sets: AzureToVMware, VMwareToAzure, AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fb08-153">-RecoveryAvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="4fb08-153">-RecoveryAvailabilitySetId</span></span>
<span data-ttu-id="4fb08-154">Az elérhetőségi készlet, amelyet a virtuális gép a feladatátvételkor hoz létre.</span><span class="sxs-lookup"><span data-stu-id="4fb08-154">The availability set that the virtual machine should be created in upon failover</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fb08-155">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="4fb08-155">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="4fb08-156">A replikálni kívánt Azure Storage-fiók AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="4fb08-156">Specifies the ID of the Azure storage account to replicate to.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, HyperVToAzure, AzureToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fb08-157">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="4fb08-157">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="4fb08-158">A helyreállítás Azure VM rendszerindítási diagnosztika tárolási fiókját adja meg.</span><span class="sxs-lookup"><span data-stu-id="4fb08-158">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fb08-159">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="4fb08-159">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="4fb08-160">A helyreállítási felhő szolgáltatás erőforrás-azonosítója a virtuális gép feladatátvételéhez.</span><span class="sxs-lookup"><span data-stu-id="4fb08-160">The resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fb08-161">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="4fb08-161">-RecoveryPlan</span></span>
<span data-ttu-id="4fb08-162">Az ASR-helyreállítási terv objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="4fb08-162">Specifies an ASR recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4fb08-163">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="4fb08-163">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="4fb08-164">Helyreállítási resourceGroup-azonosító a védett VM-hez.</span><span class="sxs-lookup"><span data-stu-id="4fb08-164">Recovery resourceGroup id for protected Vm.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fb08-165">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="4fb08-165">-ReplicationProtectedItem</span></span>
<span data-ttu-id="4fb08-166">Egy ASR-replikációs védelemmel ellátott elemet ad meg.</span><span class="sxs-lookup"><span data-stu-id="4fb08-166">Specifies an ASR replication protected item.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject, AzureToVMware, VMwareToAzure, HyperVToAzure, EnterpriseToEnterprise, AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4fb08-167">-RetentionVolume</span><span class="sxs-lookup"><span data-stu-id="4fb08-167">-RetentionVolume</span></span>
<span data-ttu-id="4fb08-168">Az adatmegőrzési mennyiség a fő célként használt kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="4fb08-168">Retention Volume on the master target server to be used.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRetentionVolume
Parameter Sets: AzureToVMware
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fb08-169">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="4fb08-169">-VmmToVmm</span></span>
<span data-ttu-id="4fb08-170">A replikáció irányának frissítése nem sikerült a Hyper-V virtuális gépén, amely két VMM felügyelt Hyper-V-webhelytől védett.</span><span class="sxs-lookup"><span data-stu-id="4fb08-170">Update replication direction for a failed over Hyper-V virtual machine that is protected between two VMM managed Hyper-V sites.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fb08-171">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="4fb08-171">-VMwareToAzure</span></span>
<span data-ttu-id="4fb08-172">Frissítse a replikációs irányt a VMware-től az Azure-ig.</span><span class="sxs-lookup"><span data-stu-id="4fb08-172">Update replication direction from VMware to Azure.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: VMwareToAzure
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fb08-173">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4fb08-173">-Confirm</span></span>
<span data-ttu-id="4fb08-174">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4fb08-174">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fb08-175">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4fb08-175">-WhatIf</span></span>
<span data-ttu-id="4fb08-176">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4fb08-176">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4fb08-177">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4fb08-177">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fb08-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fb08-178">CommonParameters</span></span>
<span data-ttu-id="4fb08-179">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4fb08-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fb08-180">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fb08-180">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fb08-181">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4fb08-181">INPUTS</span></span>

### <span data-ttu-id="4fb08-182">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="4fb08-182">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="4fb08-183">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="4fb08-183">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="4fb08-184">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4fb08-184">OUTPUTS</span></span>

### <span data-ttu-id="4fb08-185">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="4fb08-185">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="4fb08-186">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4fb08-186">NOTES</span></span>

## <span data-ttu-id="4fb08-187">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4fb08-187">RELATED LINKS</span></span>
