---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrprotectiondirection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionDirection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionDirection.md
ms.openlocfilehash: 326f73e0a056c6d68d0bdd96ddca1aea7c1c6147
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98343758"
---
# <span data-ttu-id="d477b-101">Update-AzRecoveryServicesAsrProtectionDirection</span><span class="sxs-lookup"><span data-stu-id="d477b-101">Update-AzRecoveryServicesAsrProtectionDirection</span></span>

## <span data-ttu-id="d477b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d477b-102">SYNOPSIS</span></span>
<span data-ttu-id="d477b-103">Frissíti a replikáció irányát a megadott replikációs védett elemhez vagy helyreállítási tervhez.</span><span class="sxs-lookup"><span data-stu-id="d477b-103">Updates the replication direction for the specified replication protected item or recovery plan.</span></span> <span data-ttu-id="d477b-104">A replikált elem vagy helyreállítási terv sikertelenül replikált replikálása ismételt védelmére/megfordítására használható.</span><span class="sxs-lookup"><span data-stu-id="d477b-104">Used to re-protect/reverse replicate a failed over replicated item or recovery plan.</span></span>

## <span data-ttu-id="d477b-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d477b-105">SYNTAX</span></span>

### <span data-ttu-id="d477b-106">ByRPIObject (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d477b-106">ByRPIObject (Default)</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d477b-107">AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="d477b-107">AzureToVMware</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-AzureToVMware] [-Account <ASRRunAsAccount>]
 -DataStore <ASRDataStore> [-MasterTarget <ASRMasterTargetServer>] -ProcessServer <ASRProcessServer>
 -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> -Direction <String>
 -RetentionVolume <ASRRetentionVolume> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d477b-108">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="d477b-108">VMwareToAzure</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-VMwareToAzure] -Account <ASRRunAsAccount>
 [-MasterTarget <ASRMasterTargetServer>] -ProcessServer <ASRProcessServer>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> [-LogStorageAccountId <String>]
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d477b-109">HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="d477b-109">HyperVToAzure</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-HyperVToAzure] [-LogStorageAccountId <String>]
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d477b-110">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="d477b-110">EnterpriseToEnterprise</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-VmmToVmm]
 -ReplicationProtectedItem <ASRReplicationProtectedItem> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d477b-111">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="d477b-111">AzureToAzure</span></span>
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

### <span data-ttu-id="d477b-112">AzureToAzureWithMultipleStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d477b-112">AzureToAzureWithMultipleStorageAccount</span></span>
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

### <span data-ttu-id="d477b-113">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="d477b-113">ByRPObject</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d477b-114">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="d477b-114">ByPEObject</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -Direction <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d477b-115">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d477b-115">DESCRIPTION</span></span>
<span data-ttu-id="d477b-116">Az **Update-AzRecoveryServicesAsrProtectionDirection parancsmag** a feladatátvételi művelet befejezése után frissíti a megadott Azure Site Recovery-objektum replikációs irányát.</span><span class="sxs-lookup"><span data-stu-id="d477b-116">The **Update-AzRecoveryServicesAsrProtectionDirection** cmdlet updates the replication direction for the specified Azure Site Recovery object after the completion of a commit failover operation.</span></span>

## <span data-ttu-id="d477b-117">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d477b-117">EXAMPLES</span></span>

### <span data-ttu-id="d477b-118">1. példa</span><span class="sxs-lookup"><span data-stu-id="d477b-118">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="d477b-119">Indítsa el a frissítési irányt a megadott helyreállítási tervhez, és adja vissza a művelet nyomon követéséhez használt ASR-feladatobjektumot.</span><span class="sxs-lookup"><span data-stu-id="d477b-119">Start the update direction operation for the specified recovery plan and returns the ASR job object used to track the operation.</span></span>

### <span data-ttu-id="d477b-120">2. példa</span><span class="sxs-lookup"><span data-stu-id="d477b-120">Example 2</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping -LogStorageAccountId $cacheStorageId `
 -ReplicationProtectedItem $rpi
```

<span data-ttu-id="d477b-121">Indítsa el a frissítési irányt a megadott replikációs védelemmel védett elemhez a védelmi tároló megfeleltetése által definiált cél azure-régióban, és használja a gyorsítótár-tárolót (a VM-hez hasonló régióban).</span><span class="sxs-lookup"><span data-stu-id="d477b-121">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and using cache storage (in same region as VM).</span></span>

### <span data-ttu-id="d477b-122">3. példa</span><span class="sxs-lookup"><span data-stu-id="d477b-122">Example 3</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping `
 -AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -ReplicationProtectedItem  $rpi
```

<span data-ttu-id="d477b-123">Indítsa el a frissítési irányt a megadott replikációs védelemmel védett elemhez a védelmi tároló megfeleltetése és a megadott lemezreplikációs konfiguráció által meghatározott cél azure-régióban.</span><span class="sxs-lookup"><span data-stu-id="d477b-123">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and provided disk replication configuration.</span></span>

### <span data-ttu-id="d477b-124">4. példa</span><span class="sxs-lookup"><span data-stu-id="d477b-124">Example 4</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping `
 -AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -ReplicationProtectedItem  $rpi `
 -DiskEncryptionVaultId  $DiskEncryptionVaultId -DiskEncryptionSecertUrl $DiskEncryptionSecertUrl `
 -KeyEncryptionVaultId $KeyEncryptionVaultId  -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl
```

    
<span data-ttu-id="d477b-125">Indítsa el a frissítési irányt a megadott titkosított replikációs védelemmel védett elemhez a cél azure-régióban, amelyet a védelmi tároló megfeleltetése és a lemez replikációs konfigurációja határoz meg.</span><span class="sxs-lookup"><span data-stu-id="d477b-125">Start the update direction operation for the specified encrypted replication protected item in target azure region defined by protection container mapping and provided disk replication configuration.</span></span>

### <span data-ttu-id="d477b-126">5. példa</span><span class="sxs-lookup"><span data-stu-id="d477b-126">Example 5</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping -LogStorageAccountId $cacheStorageId `
 -ReplicationProtectedItem $rpi -RecoveryProximityPlacementGroupId $ppg
```

<span data-ttu-id="d477b-127">Indítsa el a frissítési irányt a megadott replikációs védelemmel védett elemhez a védelmi tároló megfeleltetésével meghatározott cél azure-régióban, és használja a gyorsítótár -tárolót (a VM-hez hasonló régióban) és a közelség elhelyezési csoportját.</span><span class="sxs-lookup"><span data-stu-id="d477b-127">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and using cache storage (in same region as VM) and proximity placement group.</span></span>


## <span data-ttu-id="d477b-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d477b-128">PARAMETERS</span></span>

### <span data-ttu-id="d477b-129">-Account</span><span class="sxs-lookup"><span data-stu-id="d477b-129">-Account</span></span>
<span data-ttu-id="d477b-130">A Futtatás fiókként, amely a Mobility szolgáltatás telepítéséhez szükséges.</span><span class="sxs-lookup"><span data-stu-id="d477b-130">The run as account to be used to push install the Mobility service if needed.</span></span> <span data-ttu-id="d477b-131">Az ASR-anyagban fiókként futtatott listában szerepelnie kell egynek.</span><span class="sxs-lookup"><span data-stu-id="d477b-131">Must be one from the list of run as accounts in the ASR fabric.</span></span>

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

### <span data-ttu-id="d477b-132">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="d477b-132">-AzureToAzure</span></span>
<span data-ttu-id="d477b-133">Az Azure–Azure katasztrófa-helyreállítást határozza meg.</span><span class="sxs-lookup"><span data-stu-id="d477b-133">Specifies the Azure to Azure disaster recovery.</span></span>

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

### <span data-ttu-id="d477b-134">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="d477b-134">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="d477b-135">A katasztrófa-helyreállítás lemezkonfigurációját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d477b-135">Specifies the disk configuration for disaster recovery.</span></span>

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

### <span data-ttu-id="d477b-136">-AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="d477b-136">-AzureToVMware</span></span>
<span data-ttu-id="d477b-137">Az Azure-nak a vMWare-környezetre való váltását határozza meg.</span><span class="sxs-lookup"><span data-stu-id="d477b-137">Specifies the switch azure to vMWare scenario.</span></span>

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

### <span data-ttu-id="d477b-138">-DataStore</span><span class="sxs-lookup"><span data-stu-id="d477b-138">-DataStore</span></span>
<span data-ttu-id="d477b-139">A vmdisk-hez használt VMware adattár.</span><span class="sxs-lookup"><span data-stu-id="d477b-139">The VMware data-store to be used for the vmdisk's.</span></span>

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

### <span data-ttu-id="d477b-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d477b-140">-DefaultProfile</span></span>
<span data-ttu-id="d477b-141">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d477b-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="d477b-142">-Irány</span><span class="sxs-lookup"><span data-stu-id="d477b-142">-Direction</span></span>
<span data-ttu-id="d477b-143">Megadja a frissítési művelet feladatátvétel utáni irányát.</span><span class="sxs-lookup"><span data-stu-id="d477b-143">Specifies the direction to be used for the update operation post a failover.</span></span>
<span data-ttu-id="d477b-144">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="d477b-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d477b-145">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="d477b-145">PrimaryToRecovery</span></span>
- <span data-ttu-id="d477b-146">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="d477b-146">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="d477b-147">-DiskEncryptionSecretUrl</span><span class="sxs-lookup"><span data-stu-id="d477b-147">-DiskEncryptionSecretUrl</span></span>
<span data-ttu-id="d477b-148">Megadja a lemeztitkosítási titkos URL-címet verzióval (Azure lemeztitkosítás) a helyreállítási VM-hez a feladatátvétel után.</span><span class="sxs-lookup"><span data-stu-id="d477b-148">Specifies the disk encryption secret URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="d477b-149">-DiskEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="d477b-149">-DiskEncryptionVaultId</span></span>
<span data-ttu-id="d477b-150">Azt a lemeztitkosítási titkos tárolóazonosítót (Azure lemeztitkosítást) adja meg, amely helyreállítási VIRTUÁLIS GÉPként használható a feladatátvétel után.</span><span class="sxs-lookup"><span data-stu-id="d477b-150">Specifies the disk encryption secret vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="d477b-151">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="d477b-151">-HyperVToAzure</span></span>
<span data-ttu-id="d477b-152">A Hyper-V virtuális gép ismételt védelme a feladatátvétel után.</span><span class="sxs-lookup"><span data-stu-id="d477b-152">Reprotect a Hyper-V virtual machine after failback.</span></span>

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

### <span data-ttu-id="d477b-153">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="d477b-153">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="d477b-154">Megadja a helyreállítási VIRTUÁLIS GÉPként a feladatátvétel után használni kívánt lemeztitkosítási kulcs URL-címét (Azure lemeztitkosítás).</span><span class="sxs-lookup"><span data-stu-id="d477b-154">Specifies the disk encryption key URL(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="d477b-155">-KeyEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="d477b-155">-KeyEncryptionVaultId</span></span>
<span data-ttu-id="d477b-156">Azt a lemeztitkosítási kulcskulcsKulcsVault-azonosítót (Azure lemeztitkosítást) ad meg, amely helyreállítási VM-ként használható a feladatátvétel után.</span><span class="sxs-lookup"><span data-stu-id="d477b-156">Specifies the disk encryption key keyVault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="d477b-157">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="d477b-157">-LogStorageAccountId</span></span>
<span data-ttu-id="d477b-158">Megadja a tárfiók azonosítóját a virtuális gépek replikációs naplójának tárolásához.</span><span class="sxs-lookup"><span data-stu-id="d477b-158">Specifies the storage account ID to store the replication log of VMs.</span></span>

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

### <span data-ttu-id="d477b-159">-MasterTarget</span><span class="sxs-lookup"><span data-stu-id="d477b-159">-MasterTarget</span></span>
<span data-ttu-id="d477b-160">Fő célkiszolgáló adatai.</span><span class="sxs-lookup"><span data-stu-id="d477b-160">Master Target Server Details.</span></span>

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

### <span data-ttu-id="d477b-161">-ProcessServer</span><span class="sxs-lookup"><span data-stu-id="d477b-161">-ProcessServer</span></span>
<span data-ttu-id="d477b-162">A replikációhoz használt folyamatkiszolgáló.</span><span class="sxs-lookup"><span data-stu-id="d477b-162">Process Server to be used for replication.</span></span>

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

### <span data-ttu-id="d477b-163">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="d477b-163">-ProtectionContainerMapping</span></span>
<span data-ttu-id="d477b-164">Protection containerMapping to be used for replication.</span><span class="sxs-lookup"><span data-stu-id="d477b-164">Protection containerMapping to be used for replication.</span></span>

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

### <span data-ttu-id="d477b-165">-RecoveryAvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="d477b-165">-RecoveryAvailabilitySetId</span></span>
<span data-ttu-id="d477b-166">Az elérhetőségi készlet, amelybe a virtuális gépet feladatátvételkor létre kell hozatni</span><span class="sxs-lookup"><span data-stu-id="d477b-166">The availability set that the virtual machine should be created in upon failover</span></span>

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

### <span data-ttu-id="d477b-167">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="d477b-167">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="d477b-168">Annak az Azure-tárfióknak az azonosítója, amelybe replikálni kell.</span><span class="sxs-lookup"><span data-stu-id="d477b-168">Specifies the ID of the Azure storage account to replicate to.</span></span>

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

### <span data-ttu-id="d477b-169">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="d477b-169">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="d477b-170">A helyreállítási azure VM rendszerindítási diagnosztikai eszközének tárfiókját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d477b-170">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

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

### <span data-ttu-id="d477b-171">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="d477b-171">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="d477b-172">A helyreállítási felhőszolgáltatás erőforrás-azonosítója, amely feladatátvételt biztosít a virtuális gépnek.</span><span class="sxs-lookup"><span data-stu-id="d477b-172">The resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

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

### <span data-ttu-id="d477b-173">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d477b-173">-RecoveryPlan</span></span>
<span data-ttu-id="d477b-174">Egy ASR helyreállítási tervobjektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="d477b-174">Specifies an ASR recovery plan object.</span></span>

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

### <span data-ttu-id="d477b-175">-RecoveryProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="d477b-175">-RecoveryProximityPlacementGroupId</span></span>
<span data-ttu-id="d477b-176">A virtuális gép feladatátvétele a helyreállítási közelség elhelyezési csoportjának erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d477b-176">The resource ID of the recovery proximity placement group to failover this virtual machine to.</span></span>

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

### <span data-ttu-id="d477b-177">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="d477b-177">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="d477b-178">A védett virtuális gép helyreállítási erőforráscsoport-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d477b-178">Recovery resourceGroup id for protected Vm.</span></span>

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

### <span data-ttu-id="d477b-179">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="d477b-179">-ReplicationProtectedItem</span></span>
<span data-ttu-id="d477b-180">AsR-replikációval védett elemet ad meg.</span><span class="sxs-lookup"><span data-stu-id="d477b-180">Specifies an ASR replication protected item.</span></span>

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

### <span data-ttu-id="d477b-181">-RetentionVolume</span><span class="sxs-lookup"><span data-stu-id="d477b-181">-RetentionVolume</span></span>
<span data-ttu-id="d477b-182">Adatmegőrzési mennyiség a fő célkiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="d477b-182">Retention Volume on the master target server to be used.</span></span>

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

### <span data-ttu-id="d477b-183">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="d477b-183">-VmmToVmm</span></span>
<span data-ttu-id="d477b-184">Két VMM által felügyelt Hyper-V-webhely között védett, sikertelen hyper-V virtuális gép replikációs irányának frissítése.</span><span class="sxs-lookup"><span data-stu-id="d477b-184">Update replication direction for a failed over Hyper-V virtual machine that is protected between two VMM managed Hyper-V sites.</span></span>

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

### <span data-ttu-id="d477b-185">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="d477b-185">-VMwareToAzure</span></span>
<span data-ttu-id="d477b-186">Frissítse a replikáció irányát a VMware-ről az Azure-ba.</span><span class="sxs-lookup"><span data-stu-id="d477b-186">Update replication direction from VMware to Azure.</span></span>

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

### <span data-ttu-id="d477b-187">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d477b-187">-Confirm</span></span>
<span data-ttu-id="d477b-188">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d477b-188">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d477b-189">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d477b-189">-WhatIf</span></span>
<span data-ttu-id="d477b-190">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d477b-190">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d477b-191">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d477b-191">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d477b-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d477b-192">CommonParameters</span></span>
<span data-ttu-id="d477b-193">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d477b-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d477b-194">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d477b-194">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d477b-195">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d477b-195">INPUTS</span></span>

### <span data-ttu-id="d477b-196">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d477b-196">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="d477b-197">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="d477b-197">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="d477b-198">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d477b-198">OUTPUTS</span></span>

### <span data-ttu-id="d477b-199">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRService</span><span class="sxs-lookup"><span data-stu-id="d477b-199">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="d477b-200">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d477b-200">NOTES</span></span>

## <span data-ttu-id="d477b-201">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d477b-201">RELATED LINKS</span></span>
