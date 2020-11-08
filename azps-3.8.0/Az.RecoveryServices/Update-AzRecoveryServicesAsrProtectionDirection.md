---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrprotectiondirection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionDirection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionDirection.md
ms.openlocfilehash: 32218fdb966a17cedcb51a2838acae1ae79d9f54
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013516"
---
# <span data-ttu-id="78777-101">Update-AzRecoveryServicesAsrProtectionDirection</span><span class="sxs-lookup"><span data-stu-id="78777-101">Update-AzRecoveryServicesAsrProtectionDirection</span></span>

## <span data-ttu-id="78777-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="78777-102">SYNOPSIS</span></span>
<span data-ttu-id="78777-103">Frissíti a megadott replikációs védett elem vagy helyreállítási terv replikációs irányát.</span><span class="sxs-lookup"><span data-stu-id="78777-103">Updates the replication direction for the specified replication protected item or recovery plan.</span></span> <span data-ttu-id="78777-104">A replikált elem vagy helyreállítási terv ismételt védelméhez/visszavonásához használható.</span><span class="sxs-lookup"><span data-stu-id="78777-104">Used to re-protect/reverse replicate a failed over replicated item or recovery plan.</span></span>

## <span data-ttu-id="78777-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="78777-105">SYNTAX</span></span>

### <span data-ttu-id="78777-106">ByRPIObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="78777-106">ByRPIObject (Default)</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78777-107">AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="78777-107">AzureToVMware</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-AzureToVMware] [-Account <ASRRunAsAccount>]
 -DataStore <ASRDataStore> [-MasterTarget <ASRMasterTargetServer>] -ProcessServer <ASRProcessServer>
 -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> -Direction <String>
 -RetentionVolume <ASRRetentionVolume> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="78777-108">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="78777-108">VMwareToAzure</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-VMwareToAzure] -Account <ASRRunAsAccount>
 [-MasterTarget <ASRMasterTargetServer>] -ProcessServer <ASRProcessServer>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> [-LogStorageAccountId <String>]
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78777-109">HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="78777-109">HyperVToAzure</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-HyperVToAzure] [-LogStorageAccountId <String>]
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78777-110">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="78777-110">EnterpriseToEnterprise</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-VmmToVmm]
 -ReplicationProtectedItem <ASRReplicationProtectedItem> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78777-111">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="78777-111">AzureToAzure</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-AzureToAzure]
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -LogStorageAccountId <String>
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-RecoveryResourceGroupId <String>] [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilitySetId <String>]
 [-RecoveryBootDiagStorageAccountId <String>] [-DiskEncryptionVaultId <String>]
 [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>] [-KeyEncryptionVaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78777-112">AzureToAzureWithMultipleStorageAccount</span><span class="sxs-lookup"><span data-stu-id="78777-112">AzureToAzureWithMultipleStorageAccount</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-AzureToAzure]
 -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -AzureToAzureDiskReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-RecoveryResourceGroupId <String>]
 [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilitySetId <String>]
 [-RecoveryBootDiagStorageAccountId <String>] [-DiskEncryptionVaultId <String>]
 [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>] [-KeyEncryptionVaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78777-113">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="78777-113">ByRPObject</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78777-114">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="78777-114">ByPEObject</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -Direction <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78777-115">Leírás</span><span class="sxs-lookup"><span data-stu-id="78777-115">DESCRIPTION</span></span>
<span data-ttu-id="78777-116">Az **Update-AzRecoveryServicesAsrProtectionDirection** parancsmag a megadott Azure-webhely helyreállítási objektumának replikációs irányát frissíti a véglegesítést követő feladatátvételi művelet befejezése után.</span><span class="sxs-lookup"><span data-stu-id="78777-116">The **Update-AzRecoveryServicesAsrProtectionDirection** cmdlet updates the replication direction for the specified Azure Site Recovery object after the completion of a commit failover operation.</span></span>

## <span data-ttu-id="78777-117">Példák</span><span class="sxs-lookup"><span data-stu-id="78777-117">EXAMPLES</span></span>

### <span data-ttu-id="78777-118">Példa 1</span><span class="sxs-lookup"><span data-stu-id="78777-118">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="78777-119">Indítsa el a megadott helyreállítási csomag frissítési irányát, és a művelet nyomon követéséhez használt ASR-objektum értékét adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="78777-119">Start the update direction operation for the specified recovery plan and returns the ASR job object used to track the operation.</span></span>

### <span data-ttu-id="78777-120">2. példa</span><span class="sxs-lookup"><span data-stu-id="78777-120">Example 2</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping -LogStorageAccountId $cacheStorageId `
 -ReplicationProtectedItem $rpi
```

<span data-ttu-id="78777-121">A megfelelő replikációs védelemmel ellátott elem frissítési irányának indítása a tároló Azure-területen, a tároló-tárolók megfeleltetése és a gyorsítótár-tároló használata (a VM-ben).</span><span class="sxs-lookup"><span data-stu-id="78777-121">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and using cache storage (in same region as VM).</span></span>

### <span data-ttu-id="78777-122">3. példa</span><span class="sxs-lookup"><span data-stu-id="78777-122">Example 3</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping `
 -AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -ReplicationProtectedItem  $rpi
```

<span data-ttu-id="78777-123">A megfelelő replikációs védett elem frissítési irányának indítása a tároló Azure régióban, a védett tárolók megfeleltetése és a lemezkvóta-konfiguráció megadása által meghatározva.</span><span class="sxs-lookup"><span data-stu-id="78777-123">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and provided disk replication configuration.</span></span>

### <span data-ttu-id="78777-124">4. példa</span><span class="sxs-lookup"><span data-stu-id="78777-124">Example 4</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping `
 -AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -ReplicationProtectedItem  $rpi `
 -DiskEncryptionVaultId  $DiskEncryptionVaultId -DiskEncryptionSecertUrl $DiskEncryptionSecertUrl `
 -KeyEncryptionVaultId $KeyEncryptionVaultId  -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl
```

    
<span data-ttu-id="78777-125">A védelmi tároló megfeleltetése által meghatározott, a megadott titkosított replikációval védett elemhez tartozó frissítési irányt indítsa el, és adja meg a lemez replikációs konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="78777-125">Start the update direction operation for the specified encrypted replication protected item in target azure region defined by protection container mapping and provided disk replication configuration.</span></span>

## <span data-ttu-id="78777-126">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="78777-126">PARAMETERS</span></span>

### <span data-ttu-id="78777-127">-Fiók</span><span class="sxs-lookup"><span data-stu-id="78777-127">-Account</span></span>
<span data-ttu-id="78777-128">A Futtatás mint fiók, amellyel szükség esetén lenyomhatja a mobil szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="78777-128">The run as account to be used to push install the Mobility service if needed.</span></span> <span data-ttu-id="78777-129">Az ASR-anyagban a Run as (futtatási) fiókból kell lennie.</span><span class="sxs-lookup"><span data-stu-id="78777-129">Must be one from the list of run as accounts in the ASR fabric.</span></span>

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

### <span data-ttu-id="78777-130">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="78777-130">-AzureToAzure</span></span>
<span data-ttu-id="78777-131">Az Azure – Azure katasztrófa-helyreállítást adja meg.</span><span class="sxs-lookup"><span data-stu-id="78777-131">Specifies the Azure to Azure disaster recovery.</span></span>

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

### <span data-ttu-id="78777-132">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="78777-132">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="78777-133">A katasztrófa-helyreállítási merevlemezek konfigurációját adja meg.</span><span class="sxs-lookup"><span data-stu-id="78777-133">Specifies the disk configuration for disaster recovery.</span></span>

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

### <span data-ttu-id="78777-134">-AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="78777-134">-AzureToVMware</span></span>
<span data-ttu-id="78777-135">Az Azure-től a vMWare-re való váltást adja meg.</span><span class="sxs-lookup"><span data-stu-id="78777-135">Specifies the switch azure to vMWare scenario.</span></span>

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

### <span data-ttu-id="78777-136">-Adattár</span><span class="sxs-lookup"><span data-stu-id="78777-136">-DataStore</span></span>
<span data-ttu-id="78777-137">A vmdisk használt VMware Data-Store.</span><span class="sxs-lookup"><span data-stu-id="78777-137">The VMware data-store to be used for the vmdisk's.</span></span>

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

### <span data-ttu-id="78777-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78777-138">-DefaultProfile</span></span>
<span data-ttu-id="78777-139">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="78777-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="78777-140">-Irány</span><span class="sxs-lookup"><span data-stu-id="78777-140">-Direction</span></span>
<span data-ttu-id="78777-141">Megadja, hogy milyen irányt kell használni a frissítési művelethez a feladatátvétel után.</span><span class="sxs-lookup"><span data-stu-id="78777-141">Specifies the direction to be used for the update operation post a failover.</span></span>
<span data-ttu-id="78777-142">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="78777-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="78777-143">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="78777-143">PrimaryToRecovery</span></span>
- <span data-ttu-id="78777-144">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="78777-144">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="78777-145">-DiskEncryptionSecretUrl</span><span class="sxs-lookup"><span data-stu-id="78777-145">-DiskEncryptionSecretUrl</span></span>
<span data-ttu-id="78777-146">A (Azure Disk Encryption) titkosítással elvégezhető titkosítatlan URL-címet adja meg, amelyet a feladatátvétel után kell használni a helyreállítási VM-nek.</span><span class="sxs-lookup"><span data-stu-id="78777-146">Specifies the disk encryption secret URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="78777-147">-DiskEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="78777-147">-DiskEncryptionVaultId</span></span>
<span data-ttu-id="78777-148">A titkosítatlan virtuális merevlemez-azonosító (Azure Disk Encryption) azonosítóját adja meg, amelyet a feladatátvétel után kell használni a helyreállítási VM-nek.</span><span class="sxs-lookup"><span data-stu-id="78777-148">Specifies the disk encryption secret vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="78777-149">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="78777-149">-HyperVToAzure</span></span>
<span data-ttu-id="78777-150">A Hyper-V virtuális gép újravédelme a visszaállás után.</span><span class="sxs-lookup"><span data-stu-id="78777-150">Reprotect a Hyper-V virtual machine after failback.</span></span>

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

### <span data-ttu-id="78777-151">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="78777-151">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="78777-152">A merevlemez-titkosítási kulcs URL-címe (Azure Disk Encryption) a következőre való használathoz: helyreállítási VM a feladatátvétel után.</span><span class="sxs-lookup"><span data-stu-id="78777-152">Specifies the disk encryption key URL(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="78777-153">-KeyEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="78777-153">-KeyEncryptionVaultId</span></span>
<span data-ttu-id="78777-154">A merevlemez-titkosítási kulcs (Azure Disk Encryption) AZONOSÍTÓját adja meg, amelyet a feladatátvétel után kell használni a helyreállítási VM-nek.</span><span class="sxs-lookup"><span data-stu-id="78777-154">Specifies the disk encryption key keyVault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="78777-155">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="78777-155">-LogStorageAccountId</span></span>
<span data-ttu-id="78777-156">Megadja a tárolási fiók AZONOSÍTÓját a VMs-alapú replikációs napló tárolásához.</span><span class="sxs-lookup"><span data-stu-id="78777-156">Specifies the storage account ID to store the replication log of VMs.</span></span>

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

### <span data-ttu-id="78777-157">-MasterTarget</span><span class="sxs-lookup"><span data-stu-id="78777-157">-MasterTarget</span></span>
<span data-ttu-id="78777-158">A fő célkiszolgáló adatai</span><span class="sxs-lookup"><span data-stu-id="78777-158">Master Target Server Details.</span></span>

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

### <span data-ttu-id="78777-159">-ProcessServer</span><span class="sxs-lookup"><span data-stu-id="78777-159">-ProcessServer</span></span>
<span data-ttu-id="78777-160">A replikációhoz használandó folyamat kiszolgálója.</span><span class="sxs-lookup"><span data-stu-id="78777-160">Process Server to be used for replication.</span></span>

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

### <span data-ttu-id="78777-161">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="78777-161">-ProtectionContainerMapping</span></span>
<span data-ttu-id="78777-162">A replikációhoz használni kívánt védelmi containerMapping.</span><span class="sxs-lookup"><span data-stu-id="78777-162">Protection containerMapping to be used for replication.</span></span>

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

### <span data-ttu-id="78777-163">-RecoveryAvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="78777-163">-RecoveryAvailabilitySetId</span></span>
<span data-ttu-id="78777-164">Az elérhetőségi készlet, amelyet a virtuális gép a feladatátvételkor hoz létre.</span><span class="sxs-lookup"><span data-stu-id="78777-164">The availability set that the virtual machine should be created in upon failover</span></span>

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

### <span data-ttu-id="78777-165">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="78777-165">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="78777-166">A replikálni kívánt Azure Storage-fiók AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="78777-166">Specifies the ID of the Azure storage account to replicate to.</span></span>

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

### <span data-ttu-id="78777-167">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="78777-167">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="78777-168">A helyreállítás Azure VM rendszerindítási diagnosztika tárolási fiókját adja meg.</span><span class="sxs-lookup"><span data-stu-id="78777-168">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

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

### <span data-ttu-id="78777-169">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="78777-169">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="78777-170">A helyreállítási felhő szolgáltatás erőforrás-azonosítója a virtuális gép feladatátvételéhez.</span><span class="sxs-lookup"><span data-stu-id="78777-170">The resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

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

### <span data-ttu-id="78777-171">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="78777-171">-RecoveryPlan</span></span>
<span data-ttu-id="78777-172">Az ASR-helyreállítási terv objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="78777-172">Specifies an ASR recovery plan object.</span></span>

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

### <span data-ttu-id="78777-173">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="78777-173">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="78777-174">Helyreállítási resourceGroup-azonosító a védett VM-hez.</span><span class="sxs-lookup"><span data-stu-id="78777-174">Recovery resourceGroup id for protected Vm.</span></span>

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

### <span data-ttu-id="78777-175">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="78777-175">-ReplicationProtectedItem</span></span>
<span data-ttu-id="78777-176">Egy ASR-replikációs védelemmel ellátott elemet ad meg.</span><span class="sxs-lookup"><span data-stu-id="78777-176">Specifies an ASR replication protected item.</span></span>

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

### <span data-ttu-id="78777-177">-RetentionVolume</span><span class="sxs-lookup"><span data-stu-id="78777-177">-RetentionVolume</span></span>
<span data-ttu-id="78777-178">Az adatmegőrzési mennyiség a fő célként használt kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="78777-178">Retention Volume on the master target server to be used.</span></span>

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

### <span data-ttu-id="78777-179">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="78777-179">-VmmToVmm</span></span>
<span data-ttu-id="78777-180">A replikáció irányának frissítése nem sikerült a Hyper-V virtuális gépén, amely két VMM felügyelt Hyper-V-webhelytől védett.</span><span class="sxs-lookup"><span data-stu-id="78777-180">Update replication direction for a failed over Hyper-V virtual machine that is protected between two VMM managed Hyper-V sites.</span></span>

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

### <span data-ttu-id="78777-181">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="78777-181">-VMwareToAzure</span></span>
<span data-ttu-id="78777-182">Frissítse a replikációs irányt a VMware-től az Azure-ig.</span><span class="sxs-lookup"><span data-stu-id="78777-182">Update replication direction from VMware to Azure.</span></span>

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

### <span data-ttu-id="78777-183">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="78777-183">-Confirm</span></span>
<span data-ttu-id="78777-184">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="78777-184">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78777-185">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78777-185">-WhatIf</span></span>
<span data-ttu-id="78777-186">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="78777-186">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="78777-187">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="78777-187">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78777-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78777-188">CommonParameters</span></span>
<span data-ttu-id="78777-189">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="78777-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78777-190">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="78777-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78777-191">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="78777-191">INPUTS</span></span>

### <span data-ttu-id="78777-192">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="78777-192">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="78777-193">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="78777-193">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="78777-194">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="78777-194">OUTPUTS</span></span>

### <span data-ttu-id="78777-195">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="78777-195">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="78777-196">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="78777-196">NOTES</span></span>

## <span data-ttu-id="78777-197">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="78777-197">RELATED LINKS</span></span>
