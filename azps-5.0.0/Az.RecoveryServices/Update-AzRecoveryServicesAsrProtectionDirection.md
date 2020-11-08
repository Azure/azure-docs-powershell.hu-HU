---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrprotectiondirection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionDirection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionDirection.md
ms.openlocfilehash: 326f73e0a056c6d68d0bdd96ddca1aea7c1c6147
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194884"
---
# <span data-ttu-id="485f3-101">Update-AzRecoveryServicesAsrProtectionDirection</span><span class="sxs-lookup"><span data-stu-id="485f3-101">Update-AzRecoveryServicesAsrProtectionDirection</span></span>

## <span data-ttu-id="485f3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="485f3-102">SYNOPSIS</span></span>
<span data-ttu-id="485f3-103">Frissíti a megadott replikációs védett elem vagy helyreállítási terv replikációs irányát.</span><span class="sxs-lookup"><span data-stu-id="485f3-103">Updates the replication direction for the specified replication protected item or recovery plan.</span></span> <span data-ttu-id="485f3-104">A replikált elem vagy helyreállítási terv ismételt védelméhez/visszavonásához használható.</span><span class="sxs-lookup"><span data-stu-id="485f3-104">Used to re-protect/reverse replicate a failed over replicated item or recovery plan.</span></span>

## <span data-ttu-id="485f3-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="485f3-105">SYNTAX</span></span>

### <span data-ttu-id="485f3-106">ByRPIObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="485f3-106">ByRPIObject (Default)</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="485f3-107">AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="485f3-107">AzureToVMware</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-AzureToVMware] [-Account <ASRRunAsAccount>]
 -DataStore <ASRDataStore> [-MasterTarget <ASRMasterTargetServer>] -ProcessServer <ASRProcessServer>
 -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> -Direction <String>
 -RetentionVolume <ASRRetentionVolume> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="485f3-108">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="485f3-108">VMwareToAzure</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-VMwareToAzure] -Account <ASRRunAsAccount>
 [-MasterTarget <ASRMasterTargetServer>] -ProcessServer <ASRProcessServer>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> [-LogStorageAccountId <String>]
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="485f3-109">HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="485f3-109">HyperVToAzure</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-HyperVToAzure] [-LogStorageAccountId <String>]
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="485f3-110">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="485f3-110">EnterpriseToEnterprise</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-VmmToVmm]
 -ReplicationProtectedItem <ASRReplicationProtectedItem> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="485f3-111">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="485f3-111">AzureToAzure</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-AzureToAzure]
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -LogStorageAccountId <String>
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-RecoveryResourceGroupId <String>] [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilitySetId <String>]
 [-RecoveryProximityPlacementGroupId <String>] [-RecoveryBootDiagStorageAccountId <String>]
 [-DiskEncryptionVaultId <String>] [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionVaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="485f3-112">AzureToAzureWithMultipleStorageAccount</span><span class="sxs-lookup"><span data-stu-id="485f3-112">AzureToAzureWithMultipleStorageAccount</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-AzureToAzure]
 -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -AzureToAzureDiskReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-RecoveryResourceGroupId <String>]
 [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilitySetId <String>]
 [-RecoveryProximityPlacementGroupId <String>] [-RecoveryBootDiagStorageAccountId <String>]
 [-DiskEncryptionVaultId <String>] [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionVaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="485f3-113">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="485f3-113">ByRPObject</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="485f3-114">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="485f3-114">ByPEObject</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -Direction <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="485f3-115">Leírás</span><span class="sxs-lookup"><span data-stu-id="485f3-115">DESCRIPTION</span></span>
<span data-ttu-id="485f3-116">Az **Update-AzRecoveryServicesAsrProtectionDirection** parancsmag a megadott Azure-webhely helyreállítási objektumának replikációs irányát frissíti a véglegesítést követő feladatátvételi művelet befejezése után.</span><span class="sxs-lookup"><span data-stu-id="485f3-116">The **Update-AzRecoveryServicesAsrProtectionDirection** cmdlet updates the replication direction for the specified Azure Site Recovery object after the completion of a commit failover operation.</span></span>

## <span data-ttu-id="485f3-117">Példák</span><span class="sxs-lookup"><span data-stu-id="485f3-117">EXAMPLES</span></span>

### <span data-ttu-id="485f3-118">Példa 1</span><span class="sxs-lookup"><span data-stu-id="485f3-118">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="485f3-119">Indítsa el a megadott helyreállítási csomag frissítési irányát, és a művelet nyomon követéséhez használt ASR-objektum értékét adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="485f3-119">Start the update direction operation for the specified recovery plan and returns the ASR job object used to track the operation.</span></span>

### <span data-ttu-id="485f3-120">2. példa</span><span class="sxs-lookup"><span data-stu-id="485f3-120">Example 2</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping -LogStorageAccountId $cacheStorageId `
 -ReplicationProtectedItem $rpi
```

<span data-ttu-id="485f3-121">A megfelelő replikációs védelemmel ellátott elem frissítési irányának indítása a tároló Azure-területen, a tároló-tárolók megfeleltetése és a gyorsítótár-tároló használata (a VM-ben).</span><span class="sxs-lookup"><span data-stu-id="485f3-121">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and using cache storage (in same region as VM).</span></span>

### <span data-ttu-id="485f3-122">3. példa</span><span class="sxs-lookup"><span data-stu-id="485f3-122">Example 3</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping `
 -AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -ReplicationProtectedItem  $rpi
```

<span data-ttu-id="485f3-123">A megfelelő replikációs védett elem frissítési irányának indítása a tároló Azure régióban, a védett tárolók megfeleltetése és a lemezkvóta-konfiguráció megadása által meghatározva.</span><span class="sxs-lookup"><span data-stu-id="485f3-123">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and provided disk replication configuration.</span></span>

### <span data-ttu-id="485f3-124">4. példa</span><span class="sxs-lookup"><span data-stu-id="485f3-124">Example 4</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping `
 -AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -ReplicationProtectedItem  $rpi `
 -DiskEncryptionVaultId  $DiskEncryptionVaultId -DiskEncryptionSecertUrl $DiskEncryptionSecertUrl `
 -KeyEncryptionVaultId $KeyEncryptionVaultId  -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl
```

    
<span data-ttu-id="485f3-125">A védelmi tároló megfeleltetése által meghatározott, a megadott titkosított replikációval védett elemhez tartozó frissítési irányt indítsa el, és adja meg a lemez replikációs konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="485f3-125">Start the update direction operation for the specified encrypted replication protected item in target azure region defined by protection container mapping and provided disk replication configuration.</span></span>

### <span data-ttu-id="485f3-126">Példa 5</span><span class="sxs-lookup"><span data-stu-id="485f3-126">Example 5</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping -LogStorageAccountId $cacheStorageId `
 -ReplicationProtectedItem $rpi -RecoveryProximityPlacementGroupId $ppg
```

<span data-ttu-id="485f3-127">A védelmi tárolók megfeleltetése és a gyorsítótár-tároló (a VM-ben) és a közelségi terület használata esetén a megadott replikációs védett elem frissítési irányának indítása</span><span class="sxs-lookup"><span data-stu-id="485f3-127">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and using cache storage (in same region as VM) and proximity placement group.</span></span>


## <span data-ttu-id="485f3-128">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="485f3-128">PARAMETERS</span></span>

### <span data-ttu-id="485f3-129">-Fiók</span><span class="sxs-lookup"><span data-stu-id="485f3-129">-Account</span></span>
<span data-ttu-id="485f3-130">A Futtatás mint fiók, amellyel szükség esetén lenyomhatja a mobil szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="485f3-130">The run as account to be used to push install the Mobility service if needed.</span></span> <span data-ttu-id="485f3-131">Az ASR-anyagban a Run as (futtatási) fiókból kell lennie.</span><span class="sxs-lookup"><span data-stu-id="485f3-131">Must be one from the list of run as accounts in the ASR fabric.</span></span>

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

### <span data-ttu-id="485f3-132">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="485f3-132">-AzureToAzure</span></span>
<span data-ttu-id="485f3-133">Az Azure – Azure katasztrófa-helyreállítást adja meg.</span><span class="sxs-lookup"><span data-stu-id="485f3-133">Specifies the Azure to Azure disaster recovery.</span></span>

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

### <span data-ttu-id="485f3-134">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="485f3-134">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="485f3-135">A katasztrófa-helyreállítási merevlemezek konfigurációját adja meg.</span><span class="sxs-lookup"><span data-stu-id="485f3-135">Specifies the disk configuration for disaster recovery.</span></span>

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

### <span data-ttu-id="485f3-136">-AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="485f3-136">-AzureToVMware</span></span>
<span data-ttu-id="485f3-137">Az Azure-től a vMWare-re való váltást adja meg.</span><span class="sxs-lookup"><span data-stu-id="485f3-137">Specifies the switch azure to vMWare scenario.</span></span>

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

### <span data-ttu-id="485f3-138">-Adattár</span><span class="sxs-lookup"><span data-stu-id="485f3-138">-DataStore</span></span>
<span data-ttu-id="485f3-139">A vmdisk használt VMware Data-Store.</span><span class="sxs-lookup"><span data-stu-id="485f3-139">The VMware data-store to be used for the vmdisk's.</span></span>

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

### <span data-ttu-id="485f3-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="485f3-140">-DefaultProfile</span></span>
<span data-ttu-id="485f3-141">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="485f3-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="485f3-142">-Irány</span><span class="sxs-lookup"><span data-stu-id="485f3-142">-Direction</span></span>
<span data-ttu-id="485f3-143">Megadja, hogy milyen irányt kell használni a frissítési művelethez a feladatátvétel után.</span><span class="sxs-lookup"><span data-stu-id="485f3-143">Specifies the direction to be used for the update operation post a failover.</span></span>
<span data-ttu-id="485f3-144">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="485f3-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="485f3-145">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="485f3-145">PrimaryToRecovery</span></span>
- <span data-ttu-id="485f3-146">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="485f3-146">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="485f3-147">-DiskEncryptionSecretUrl</span><span class="sxs-lookup"><span data-stu-id="485f3-147">-DiskEncryptionSecretUrl</span></span>
<span data-ttu-id="485f3-148">A (Azure Disk Encryption) titkosítással elvégezhető titkosítatlan URL-címet adja meg, amelyet a feladatátvétel után kell használni a helyreállítási VM-nek.</span><span class="sxs-lookup"><span data-stu-id="485f3-148">Specifies the disk encryption secret URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="485f3-149">-DiskEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="485f3-149">-DiskEncryptionVaultId</span></span>
<span data-ttu-id="485f3-150">A titkosítatlan virtuális merevlemez-azonosító (Azure Disk Encryption) azonosítóját adja meg, amelyet a feladatátvétel után kell használni a helyreállítási VM-nek.</span><span class="sxs-lookup"><span data-stu-id="485f3-150">Specifies the disk encryption secret vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="485f3-151">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="485f3-151">-HyperVToAzure</span></span>
<span data-ttu-id="485f3-152">A Hyper-V virtuális gép újravédelme a visszaállás után.</span><span class="sxs-lookup"><span data-stu-id="485f3-152">Reprotect a Hyper-V virtual machine after failback.</span></span>

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

### <span data-ttu-id="485f3-153">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="485f3-153">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="485f3-154">A merevlemez-titkosítási kulcs URL-címe (Azure Disk Encryption) a következőre való használathoz: helyreállítási VM a feladatátvétel után.</span><span class="sxs-lookup"><span data-stu-id="485f3-154">Specifies the disk encryption key URL(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="485f3-155">-KeyEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="485f3-155">-KeyEncryptionVaultId</span></span>
<span data-ttu-id="485f3-156">A merevlemez-titkosítási kulcs (Azure Disk Encryption) AZONOSÍTÓját adja meg, amelyet a feladatátvétel után kell használni a helyreállítási VM-nek.</span><span class="sxs-lookup"><span data-stu-id="485f3-156">Specifies the disk encryption key keyVault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="485f3-157">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="485f3-157">-LogStorageAccountId</span></span>
<span data-ttu-id="485f3-158">Megadja a tárolási fiók AZONOSÍTÓját a VMs-alapú replikációs napló tárolásához.</span><span class="sxs-lookup"><span data-stu-id="485f3-158">Specifies the storage account ID to store the replication log of VMs.</span></span>

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

### <span data-ttu-id="485f3-159">-MasterTarget</span><span class="sxs-lookup"><span data-stu-id="485f3-159">-MasterTarget</span></span>
<span data-ttu-id="485f3-160">A fő célkiszolgáló adatai</span><span class="sxs-lookup"><span data-stu-id="485f3-160">Master Target Server Details.</span></span>

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

### <span data-ttu-id="485f3-161">-ProcessServer</span><span class="sxs-lookup"><span data-stu-id="485f3-161">-ProcessServer</span></span>
<span data-ttu-id="485f3-162">A replikációhoz használandó folyamat kiszolgálója.</span><span class="sxs-lookup"><span data-stu-id="485f3-162">Process Server to be used for replication.</span></span>

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

### <span data-ttu-id="485f3-163">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="485f3-163">-ProtectionContainerMapping</span></span>
<span data-ttu-id="485f3-164">A replikációhoz használni kívánt védelmi containerMapping.</span><span class="sxs-lookup"><span data-stu-id="485f3-164">Protection containerMapping to be used for replication.</span></span>

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

### <span data-ttu-id="485f3-165">-RecoveryAvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="485f3-165">-RecoveryAvailabilitySetId</span></span>
<span data-ttu-id="485f3-166">Az elérhetőségi készlet, amelyet a virtuális gép a feladatátvételkor hoz létre.</span><span class="sxs-lookup"><span data-stu-id="485f3-166">The availability set that the virtual machine should be created in upon failover</span></span>

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

### <span data-ttu-id="485f3-167">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="485f3-167">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="485f3-168">A replikálni kívánt Azure Storage-fiók AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="485f3-168">Specifies the ID of the Azure storage account to replicate to.</span></span>

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

### <span data-ttu-id="485f3-169">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="485f3-169">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="485f3-170">A helyreállítás Azure VM rendszerindítási diagnosztika tárolási fiókját adja meg.</span><span class="sxs-lookup"><span data-stu-id="485f3-170">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

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

### <span data-ttu-id="485f3-171">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="485f3-171">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="485f3-172">A helyreállítási felhő szolgáltatás erőforrás-azonosítója a virtuális gép feladatátvételéhez.</span><span class="sxs-lookup"><span data-stu-id="485f3-172">The resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

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

### <span data-ttu-id="485f3-173">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="485f3-173">-RecoveryPlan</span></span>
<span data-ttu-id="485f3-174">Az ASR-helyreállítási terv objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="485f3-174">Specifies an ASR recovery plan object.</span></span>

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

### <span data-ttu-id="485f3-175">-RecoveryProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="485f3-175">-RecoveryProximityPlacementGroupId</span></span>
<span data-ttu-id="485f3-176">A helyreállítási közelségi csoport erőforrás-azonosítója a virtuális gép feladatátvételéhez.</span><span class="sxs-lookup"><span data-stu-id="485f3-176">The resource ID of the recovery proximity placement group to failover this virtual machine to.</span></span>

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

### <span data-ttu-id="485f3-177">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="485f3-177">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="485f3-178">Helyreállítási resourceGroup-azonosító a védett VM-hez.</span><span class="sxs-lookup"><span data-stu-id="485f3-178">Recovery resourceGroup id for protected Vm.</span></span>

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

### <span data-ttu-id="485f3-179">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="485f3-179">-ReplicationProtectedItem</span></span>
<span data-ttu-id="485f3-180">Egy ASR-replikációs védelemmel ellátott elemet ad meg.</span><span class="sxs-lookup"><span data-stu-id="485f3-180">Specifies an ASR replication protected item.</span></span>

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

### <span data-ttu-id="485f3-181">-RetentionVolume</span><span class="sxs-lookup"><span data-stu-id="485f3-181">-RetentionVolume</span></span>
<span data-ttu-id="485f3-182">Az adatmegőrzési mennyiség a fő célként használt kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="485f3-182">Retention Volume on the master target server to be used.</span></span>

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

### <span data-ttu-id="485f3-183">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="485f3-183">-VmmToVmm</span></span>
<span data-ttu-id="485f3-184">A replikáció irányának frissítése nem sikerült a Hyper-V virtuális gépén, amely két VMM felügyelt Hyper-V-webhelytől védett.</span><span class="sxs-lookup"><span data-stu-id="485f3-184">Update replication direction for a failed over Hyper-V virtual machine that is protected between two VMM managed Hyper-V sites.</span></span>

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

### <span data-ttu-id="485f3-185">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="485f3-185">-VMwareToAzure</span></span>
<span data-ttu-id="485f3-186">Frissítse a replikációs irányt a VMware-től az Azure-ig.</span><span class="sxs-lookup"><span data-stu-id="485f3-186">Update replication direction from VMware to Azure.</span></span>

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

### <span data-ttu-id="485f3-187">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="485f3-187">-Confirm</span></span>
<span data-ttu-id="485f3-188">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="485f3-188">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="485f3-189">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="485f3-189">-WhatIf</span></span>
<span data-ttu-id="485f3-190">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="485f3-190">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="485f3-191">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="485f3-191">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="485f3-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="485f3-192">CommonParameters</span></span>
<span data-ttu-id="485f3-193">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="485f3-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="485f3-194">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="485f3-194">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="485f3-195">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="485f3-195">INPUTS</span></span>

### <span data-ttu-id="485f3-196">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="485f3-196">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="485f3-197">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="485f3-197">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="485f3-198">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="485f3-198">OUTPUTS</span></span>

### <span data-ttu-id="485f3-199">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="485f3-199">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="485f3-200">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="485f3-200">NOTES</span></span>

## <span data-ttu-id="485f3-201">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="485f3-201">RELATED LINKS</span></span>
