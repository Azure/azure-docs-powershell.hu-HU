---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: f27c9daa4e1d7df5b1feb3be42ccece780d66fb7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100151130"
---
# <span data-ttu-id="70582-101">New-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="70582-101">New-AzRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="70582-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70582-102">SYNOPSIS</span></span>
<span data-ttu-id="70582-103">Replikációt tesz lehetővé asr védett elemekhez a replikációval védett elem létrehozásával.</span><span class="sxs-lookup"><span data-stu-id="70582-103">Enables replication for an ASR protectable item by creating a replication protected item.</span></span>

## <span data-ttu-id="70582-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="70582-104">SYNTAX</span></span>

### <span data-ttu-id="70582-105">EnterpriseToEnterprise (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="70582-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-VmmToVmm] -ProtectableItem <ASRProtectableItem>
 -Name <String> -ProtectionContainerMapping <ASRProtectionContainerMapping> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70582-106">VMwareToAzureWithDiskType</span><span class="sxs-lookup"><span data-stu-id="70582-106">VMwareToAzureWithDiskType</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-VMwareToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -Account <ASRRunAsAccount> [-LogStorageAccountId <String>] -ProcessServer <ASRProcessServer>
 [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String>
 [-ReplicationGroupName <String>] [-RecoveryAvailabilityZone <String>]
 [-RecoveryProximityPlacementGroupId <String>] [-WaitForCompletion] -DiskType <String>
 [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="70582-107">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="70582-107">VMwareToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-VMwareToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -Account <ASRRunAsAccount> [-LogStorageAccountId <String>]
 [-InMageAzureV2DiskInput <AsrInMageAzureV2DiskInput[]>] -ProcessServer <ASRProcessServer>
 [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String>
 [-ReplicationGroupName <String>] [-RecoveryAvailabilityZone <String>]
 [-RecoveryProximityPlacementGroupId <String>] [-WaitForCompletion] [-DiskEncryptionSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70582-108">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="70582-108">EnterpriseToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-HyperVToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -RecoveryResourceGroupId <String> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70582-109">HyperVSiteToAzure</span><span class="sxs-lookup"><span data-stu-id="70582-109">HyperVSiteToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-HyperVToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -OSDiskName <String> -OS <String> [-LogStorageAccountId <String>]
 [-IncludeDiskId <String[]>] [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>]
 -RecoveryResourceGroupId <String> [-RecoveryAvailabilityZone <String>]
 [-RecoveryProximityPlacementGroupId <String>] [-UseManagedDisk <String>] [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70582-110">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="70582-110">AzureToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-AzureToAzure]
 -AzureToAzureDiskReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]> -AzureVmId <String>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String>
 [-ReplicationGroupName <String>] [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilityZone <String>]
 [-RecoveryProximityPlacementGroupId <String>] [-RecoveryAvailabilitySetId <String>]
 [-RecoveryBootDiagStorageAccountId <String>] [-DiskEncryptionVaultId <String>]
 [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>] [-KeyEncryptionVaultId <String>]
 [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70582-111">AzureToAzureWithoutDiskDetails</span><span class="sxs-lookup"><span data-stu-id="70582-111">AzureToAzureWithoutDiskDetails</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-AzureToAzure] -AzureVmId <String> -Name <String>
 [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 [-RecoveryAzureStorageAccountId <String>] -LogStorageAccountId <String> [-RecoveryAzureNetworkId <String>]
 [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String> [-ReplicationGroupName <String>]
 [-RecoveryAvailabilityZone <String>] [-RecoveryProximityPlacementGroupId <String>]
 [-RecoveryAvailabilitySetId <String>] [-RecoveryBootDiagStorageAccountId <String>]
 [-DiskEncryptionVaultId <String>] [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionVaultId <String>] [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70582-112">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="70582-112">DESCRIPTION</span></span>
<span data-ttu-id="70582-113">A **New-AzRecoveryServicesAsrReplicationProtectedItem** parancsmag új, replikációval védett elemet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="70582-113">The **New-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet creates a new replication protected item.</span></span>
<span data-ttu-id="70582-114">Ezzel a parancsmagot használva engedélyezze a replikációt egy ASR által védett elemhez.</span><span class="sxs-lookup"><span data-stu-id="70582-114">Use this cmdlet to enable replication for an ASR protectable item.</span></span>

## <span data-ttu-id="70582-115">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="70582-115">EXAMPLES</span></span>

### <span data-ttu-id="70582-116">1. példa</span><span class="sxs-lookup"><span data-stu-id="70582-116">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrReplicationProtectedItem -ProtectableItem $VM -Name $VM.Name -ProtectionContainerMapping $ProtectionContainerMapping
```

<span data-ttu-id="70582-117">Elindítja a replikációval védett elemek létrehozását a megadott ASR által védett elemhez, és visszaadja a művelet nyomon követéséhez használt ASR-feladatot.</span><span class="sxs-lookup"><span data-stu-id="70582-117">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="70582-118">2. példa</span><span class="sxs-lookup"><span data-stu-id="70582-118">Example 2</span></span>
```
PS C:\>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] `
-RecoveryResourceGroupId $RecoveryResourceGroupId -RecoveryAzureNetworkId $RecoveryAzureNetworkId  -name $name `
-ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem -ProtectionContainerMapping $pcm `
-RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName -LogStorageAccountId $LogStorageAccountId
```

<span data-ttu-id="70582-119">Elindítja a replikációval védett elemek létrehozását a megadott ASR által védett elemhez, és visszaadja a művelet nyomon követéséhez használt ASR-feladatot (vmWare – Azure eset).</span><span class="sxs-lookup"><span data-stu-id="70582-119">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation(vmWare to Azure scenario).</span></span>

### <span data-ttu-id="70582-120">3. példa</span><span class="sxs-lookup"><span data-stu-id="70582-120">Example 3</span></span>
```
PS C:>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureToAzureDiskReplicationConfig disk1,disk2 -AzVmId $vmId `
-Name "a2aprotectedItem" -RecoveryVmName "vmName" -ProtectionContainerMapping $pcmMapping -RecoveryResourceGroupId $recoveryResourceGroup
```

<span data-ttu-id="70582-121">Elindítja a replikációval védett elemek létrehozását a megadott ASR által védett elemhez, és visszaadja a művelet nyomon követéséhez használt ASR-feladatot (Azure–Azure eset).</span><span class="sxs-lookup"><span data-stu-id="70582-121">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

### <span data-ttu-id="70582-122">4. példa</span><span class="sxs-lookup"><span data-stu-id="70582-122">Example 4</span></span>
```
PS C:\> $disk1 = New-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri1 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId `
-LogStorageAccountId $logStorageAccountId  
PS C:\> $disk2 = New-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri2 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId `
-LogStorageAccountId $logStorageAccountId  
PS C:\> $enableDRjob = New-AzRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureVmId $vmId -Name $rpiName `
-RecoveryCloudServiceId  $recoveryCloudServiceId -ProtectionContainerMapping $pcm -RecoveryResourceGroupId  $RecoveryResourceGroupId `
-AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -RecoveryAzureNetworkId $RecoveryAzureNetworkId -RecoveryAzureSubnetName $RecoveryAzureSubnetName
```

<span data-ttu-id="70582-123">Elindítja a replikációval védett elemek létrehozását a megadott VmId-hez, és visszaadja a művelet nyomon követéséhez használt ASR-feladatot (Azure–Azure eset).</span><span class="sxs-lookup"><span data-stu-id="70582-123">Starts the replication protected item creation operation for the specified VmId and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

### <span data-ttu-id="70582-124">5. példa</span><span class="sxs-lookup"><span data-stu-id="70582-124">Example 5</span></span>
```
PS C:\>$disk1 = New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId -LogStorageAccountId $logStorageAccountId -DiskType $diskType
PS C:\>$disk2 = New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId2 -LogStorageAccountId $logStorageAccountId -DiskType $diskType2

PS C:\>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryAzureNetworkId $RecoveryAzureNetworkId  -name $name -ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem  `
-ProtectionContainerMapping $pcm -RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName `
-LogStorageAccountId $LogStorageAccountId -InMageAzureV2DiskInput $disk1,$disk2
```

<span data-ttu-id="70582-125">Elindítja a replikációval védett elemkészítési műveletet a megadott asr védelem alatt lévő elemhez, beleértve a szelektív lemezeket is, és visszaadja a kiválasztott lemezekkel végzett művelet (vmWare – Azure eset) nyomon követéséhez használt ASR-feladatot.</span><span class="sxs-lookup"><span data-stu-id="70582-125">Starts the replication protected item creation operation for the specified ASR protectable item including selective disks and returns the ASR job used to track the operation(vmWare to Azure scenario) with selected disks.</span></span>

### <span data-ttu-id="70582-126">6. példa</span><span class="sxs-lookup"><span data-stu-id="70582-126">Example 6</span></span>
```
PS C:\>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryAzureNetworkId $RecoveryAzureNetworkId  -name $name -ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem  `
-ProtectionContainerMapping $pcm -RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName `
-LogStorageAccountId $LogStorageAccountId -DiskType Standard_LRS

Starts the replication protected item creation operation for the specified ASR protectable item with default disk type and returns the ASR job used to track the operation(vmWare to Azure scenario).
```

### <span data-ttu-id="70582-127">7. példa</span><span class="sxs-lookup"><span data-stu-id="70582-127">Example 7</span></span>
```
PS C:\> $disk1 = New-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri1 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId -LogStorageAccountId $logStorageAccountId  
PS C:\> $disk2 = new-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri2 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId -LogStorageAccountId $logStorageAccountId  
PS C:\> $enableDRjob = New-AzRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzVmId $vmId -Name $rpiName `
-RecoveryCloudServiceId  $recoveryCloudServiceId -ProtectionContainerMapping $pcm -RecoveryResourceGroupId  $RecoveryResourceGroupId `
-AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -DiskEncryptionVaultId  $DiskEncryptionVaultId -DiskEncryptionSecertUrl $DiskEncryptionSecertUrl `
 -KeyEncryptionVaultId $KeyEncryptionVaultId  -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl
```

<span data-ttu-id="70582-128">Elindítja a replikációval védett elemek létrehozását a megadott VmId-hez, és visszaadja a művelet nyomon követéséhez használt ASR-feladatot (Azure–Azure eset). A rendszer a titkosítás parancsmagban átadott feladatátvételi VM-adatokat fogja használni.</span><span class="sxs-lookup"><span data-stu-id="70582-128">Starts the replication protected item creation operation for the specified VmId and returns the ASR job used to track the operation (Azure to Azure scenario).For the failover VM details passed in cmdlet for encryption will be used .</span></span>

### <span data-ttu-id="70582-129">8. példa</span><span class="sxs-lookup"><span data-stu-id="70582-129">Example 8</span></span>
```
PS C:>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureToAzureDiskReplicationConfig disk1,disk2 -AzVmId $vmId `
-Name "a2aprotectedItem" -RecoveryVmName "vmName" -ProtectionContainerMapping $pcmMapping -RecoveryResourceGroupId $recoveryResourceGroup -RecoveryProximityPlacementGroupId $ppg
```

<span data-ttu-id="70582-130">Elindítja a replikációval védett elemek létrehozását egy virtuális géphez a Közelítés elhelyezési csoporton belül, és visszaadja a művelet nyomon követéséhez használt ASR-feladatot (Azure–Azure eset).</span><span class="sxs-lookup"><span data-stu-id="70582-130">Starts the replication protected item creation operation for a Virtual Machine inside Proximity placement group and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

## <span data-ttu-id="70582-131">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="70582-131">PARAMETERS</span></span>

### <span data-ttu-id="70582-132">-Account</span><span class="sxs-lookup"><span data-stu-id="70582-132">-Account</span></span>
<span data-ttu-id="70582-133">A Futtatás fiókként, amely a Mobility szolgáltatás telepítéséhez szükséges.</span><span class="sxs-lookup"><span data-stu-id="70582-133">The run as account to be used to push install the Mobility service if needed.</span></span> <span data-ttu-id="70582-134">Az ASR-anyagban fiókként futtatott listában szerepelnie kell egynek.</span><span class="sxs-lookup"><span data-stu-id="70582-134">Must be one from the list of run as accounts in the ASR fabric.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRunAsAccount
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70582-135">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="70582-135">-AzureToAzure</span></span>
<span data-ttu-id="70582-136">A Kapcsoló paraméter a replikált elem azure-ba való létrehozását határozza meg az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="70582-136">Switch parameter specifies creating the replicated item in azure to azure scenario.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70582-137">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="70582-137">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="70582-138">Az Azure-hoz használt Azure-hoz használt lemezkonfiguráció az Azure-hoz– katasztrófa-helyreállítási forgatókönyv.</span><span class="sxs-lookup"><span data-stu-id="70582-138">Specifies the disk configuration to used Vm for Azure to Azure disaster recovery scenario.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig[]
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70582-139">-AzureVmId</span><span class="sxs-lookup"><span data-stu-id="70582-139">-AzureVmId</span></span>
<span data-ttu-id="70582-140">Megadja az Azure VM-azonosítót a helyreállítási régióban a katasztrófa-helyreállítás elleni védelemhez.</span><span class="sxs-lookup"><span data-stu-id="70582-140">Specifies the Azure VM id for disaster recovery protection in recovery region.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70582-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70582-141">-DefaultProfile</span></span>
<span data-ttu-id="70582-142">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="70582-142">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="70582-143">-DiskEncryptionSecretUrl</span><span class="sxs-lookup"><span data-stu-id="70582-143">-DiskEncryptionSecretUrl</span></span>
<span data-ttu-id="70582-144">Megadja azt a titkos lemeztitkosítási URL-címet, amely tartalmazza a feladatátvétel után helyreállítási VIRTUÁLIS GÉPként használni kívánt verzió(Azure lemeztitkosítás) címet.</span><span class="sxs-lookup"><span data-stu-id="70582-144">Specifies the disk encryption secret URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70582-145">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="70582-145">-DiskEncryptionSetId</span></span>
<span data-ttu-id="70582-146">A felügyelt lemez titkosítási készletének erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="70582-146">Specifies the resource Id of the disk encryption set, to be used for the encryption of the managed disks.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70582-147">-DiskEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="70582-147">-DiskEncryptionVaultId</span></span>
<span data-ttu-id="70582-148">Azt a lemeztitkosítási titkos tárolóazonosítót (Azure lemeztitkosítást) adja meg, amely helyreállítási VIRTUÁLIS GÉPként használható a feladatátvétel után.</span><span class="sxs-lookup"><span data-stu-id="70582-148">Specifies the disk encryption secret vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70582-149">-DiskType</span><span class="sxs-lookup"><span data-stu-id="70582-149">-DiskType</span></span>
<span data-ttu-id="70582-150">A helyreállítási virtuális gép felügyelt lemeztípusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="70582-150">Specifies the Recovery VM managed disk type.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70582-151">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="70582-151">-HyperVToAzure</span></span>
<span data-ttu-id="70582-152">A paraméter váltása a replikált elem megadásához egy Hyper-V virtuális gép, amely az Azure-ba replikálódik.</span><span class="sxs-lookup"><span data-stu-id="70582-152">Switch parameter to specify the replicated item is a Hyper-V virtual machine that is being replicated to Azure.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnterpriseToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70582-153">-IncludeDiskId</span><span class="sxs-lookup"><span data-stu-id="70582-153">-IncludeDiskId</span></span>
<span data-ttu-id="70582-154">A replikációhoz szükséges lemezlista.</span><span class="sxs-lookup"><span data-stu-id="70582-154">The list of disks to include for replication.</span></span> <span data-ttu-id="70582-155">Alapértelmezés szerint minden lemez megtalálható a csomagban.</span><span class="sxs-lookup"><span data-stu-id="70582-155">By default all disks are included.</span></span>

```yaml
Type: System.String[]
Parameter Sets: HyperVSiteToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70582-156">-InMageAzureV2DiskInput</span><span class="sxs-lookup"><span data-stu-id="70582-156">-InMageAzureV2DiskInput</span></span>
<span data-ttu-id="70582-157">Megadja a vMWare lemezazonosítójának lemezkonfigurációs bemenetét a megadott védett elemtől való védelemhez.</span><span class="sxs-lookup"><span data-stu-id="70582-157">Specifies the disk configuration input for vMWare disk id to protect from specified protectable item.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.AsrInMageAzureV2DiskInput[]
Parameter Sets: VMwareToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70582-158">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="70582-158">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="70582-159">Megadja a lemeztitkosítási kulcs URL-címét a feladatátvétel után helyreállítási VIRTUÁLIS GÉPként használni kívánt verzió(Azure lemeztitkosítás) mezőben.</span><span class="sxs-lookup"><span data-stu-id="70582-159">Specifies the disk encryption key URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70582-160">-KeyEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="70582-160">-KeyEncryptionVaultId</span></span>
<span data-ttu-id="70582-161">Megadja azt a lemeztitkosítási kulcs-tárolóazonosítót (Azure lemeztitkosítást), amely helyreállítási VIRTUÁLIS GÉPként használható a feladatátvétel után.</span><span class="sxs-lookup"><span data-stu-id="70582-161">Specifies the disk encryption key key-vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70582-162">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="70582-162">-LogStorageAccountId</span></span>
<span data-ttu-id="70582-163">A replikációs naplók tárolásához használt napló- vagy gyorsítótárfiók-azonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="70582-163">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AzureToAzureWithoutDiskDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70582-164">-Name</span><span class="sxs-lookup"><span data-stu-id="70582-164">-Name</span></span>
<span data-ttu-id="70582-165">Megadja a asr replikációs szolgáltatás által védett elem nevét.</span><span class="sxs-lookup"><span data-stu-id="70582-165">Specifies a name for the ASR replication protected item.</span></span> <span data-ttu-id="70582-166">A névnek egyedinek kell lennie a tárolóban.</span><span class="sxs-lookup"><span data-stu-id="70582-166">The name must be unique within the vault.</span></span>

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

### <span data-ttu-id="70582-167">-OS</span><span class="sxs-lookup"><span data-stu-id="70582-167">-OS</span></span>
<span data-ttu-id="70582-168">Az operációs rendszer családját határozza meg.</span><span class="sxs-lookup"><span data-stu-id="70582-168">Specifies the operating system family.</span></span>
<span data-ttu-id="70582-169">A paraméter elfogadható értékei: Windows vagy Linux.</span><span class="sxs-lookup"><span data-stu-id="70582-169">The acceptable values for this parameter are: Windows or Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVSiteToAzure
Aliases:
Accepted values: Windows, Linux

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70582-170">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="70582-170">-OSDiskName</span></span>
<span data-ttu-id="70582-171">Az operációs rendszer lemezének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="70582-171">Specifies the name of the operating system disk.</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVSiteToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70582-172">-ProcessServer</span><span class="sxs-lookup"><span data-stu-id="70582-172">-ProcessServer</span></span>
<span data-ttu-id="70582-173">A számítógép replikálása során használt folyamatkiszolgáló.</span><span class="sxs-lookup"><span data-stu-id="70582-173">The Process Server to use to replicate this machine.</span></span> <span data-ttu-id="70582-174">A Konfigurációs kiszolgálónak megfelelő ASR-anyagban található folyamatkiszolgálók listájával megadhat egyet.</span><span class="sxs-lookup"><span data-stu-id="70582-174">Use the list of process servers in the ASR fabric corresponding to the Configuration server to specify one.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProcessServer
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70582-175">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="70582-175">-ProtectableItem</span></span>
<span data-ttu-id="70582-176">Azt a asr védett elemobjektumot adja meg, amelyhez engedélyezve van a replikáció.</span><span class="sxs-lookup"><span data-stu-id="70582-176">Specifies the ASR protectable item object for which replication is being enabled.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem
Parameter Sets: EnterpriseToEnterprise, VMwareToAzureWithDiskType, VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="70582-177">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="70582-177">-ProtectionContainerMapping</span></span>
<span data-ttu-id="70582-178">A replikációhoz használt replikációs házirendnek megfelelő ASR védelmi tárolóleképezési objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="70582-178">Specifies the ASR protection container mapping object corresponding to the replication policy to be used for replication.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70582-179">-RecoveryAvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="70582-179">-RecoveryAvailabilitySetId</span></span>
<span data-ttu-id="70582-180">Annak az ElérhetőségiKészletnek az azonosítója, amely helyreállítja a gépet feladatátvétel esetén.</span><span class="sxs-lookup"><span data-stu-id="70582-180">The ID of the AvailabilitySet to recover the machine to in the event of a failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70582-181">-RecoveryAvailabilityZone</span><span class="sxs-lookup"><span data-stu-id="70582-181">-RecoveryAvailabilityZone</span></span>
<span data-ttu-id="70582-182">A helyreállítási virtuális gép rendelkezésre állási zónáját adja meg a feladatátvétel után.</span><span class="sxs-lookup"><span data-stu-id="70582-182">Specifies the recovery VM availability zone after failover.</span></span>


```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure, HyperVSiteToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70582-183">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="70582-183">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="70582-184">Annak az Azure virtuális hálózatnak az azonosítója, amely helyreállítja a gépet feladatátvétel esetén.</span><span class="sxs-lookup"><span data-stu-id="70582-184">The ID of the Azure virtual network to recover the machine to in the event of a failover.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure, HyperVSiteToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70582-185">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="70582-185">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="70582-186">Annak az Azure-tárfióknak az azonosítója, amelybe replikálni kell.</span><span class="sxs-lookup"><span data-stu-id="70582-186">Specifies the ID of the Azure storage account to replicate to.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToAzure, HyperVSiteToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70582-187">-RecoveryAzureSubnetName</span><span class="sxs-lookup"><span data-stu-id="70582-187">-RecoveryAzureSubnetName</span></span>
<span data-ttu-id="70582-188">A helyreállítási Azure virtuális hálózaton belüli alhálózatot, amelyhez feladatátvétel esetén csatolni kell a virtuális gépről áteső feladatátvételt.</span><span class="sxs-lookup"><span data-stu-id="70582-188">The subnet within the recovery Azure virtual network to which the failed over virtual machine should be attached in the event of a failover.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure, HyperVSiteToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70582-189">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="70582-189">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="70582-190">A helyreállítási azure VM rendszerindítási diagnosztikai eszközének tárfiókját adja meg.</span><span class="sxs-lookup"><span data-stu-id="70582-190">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70582-191">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="70582-191">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="70582-192">Annak a helyreállítási felhőszolgáltatásnak az erőforrás-azonosítója, amelybe a virtuális gép feladatátvétele szükséges.</span><span class="sxs-lookup"><span data-stu-id="70582-192">Specifies the resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70582-193">-RecoveryProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="70582-193">-RecoveryProximityPlacementGroupId</span></span>
<span data-ttu-id="70582-194">Adja meg a közvetlen közelítési csoport azonosítóját, amelyet a feladatátvételi virtuális gép használ a célhely-helyreállítási régióban.</span><span class="sxs-lookup"><span data-stu-id="70582-194">Specify the proximity placement group Id to used by the failover Vm in target recovery region.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure, HyperVSiteToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70582-195">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="70582-195">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="70582-196">Annak az ARM azonosítóját adja meg, amelyben a virtuális gép feladatátvétel esetén létre lesz hozva.</span><span class="sxs-lookup"><span data-stu-id="70582-196">Specifies the ARM identifier of the resource group in which the virtual machine will be created in the event of a failover.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70582-197">-RecoveryVmName</span><span class="sxs-lookup"><span data-stu-id="70582-197">-RecoveryVmName</span></span>
<span data-ttu-id="70582-198">A feladatátvétel után létrehozott helyreállítási virtuális gép neve.</span><span class="sxs-lookup"><span data-stu-id="70582-198">Name of the recovery Vm created after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70582-199">-ReplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="70582-199">-ReplicationGroupName</span></span>
<span data-ttu-id="70582-200">A több VM-konzisztens helyreállítási pontok létrehozásához használt replikációs csoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="70582-200">Specifies the replication group name to use to create multi-VM consistent recovery points.</span></span> <span data-ttu-id="70582-201">Alapértelmezés szerint minden replikációval védett elem egy csoportban jön létre, és nem jön létre több VM-konzisztens helyreállítási pont.</span><span class="sxs-lookup"><span data-stu-id="70582-201">By default each replication protected item is created in a group of its own and multi-VM consistent recovery points are not generated.</span></span> <span data-ttu-id="70582-202">Ezt a beállítást csak akkor használja, ha több virtuális gép konzisztens helyreállítási pontot kell létrehoznia több gépcsoportban úgy, hogy minden gépet ugyanazon replikációs csoportnak kell védenie.</span><span class="sxs-lookup"><span data-stu-id="70582-202">Use this option only if you need to create multi-VM consistent recovery points across a group of machines by protecting all machines to the same replication group.</span></span> 

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70582-203">-UseManagedDisk</span><span class="sxs-lookup"><span data-stu-id="70582-203">-UseManagedDisk</span></span>
<span data-ttu-id="70582-204">Azt adja meg, hogy a feladatátvételre létrehozott Azure virtuális gépnek felügyelt lemezeket kell-e használnia.</span><span class="sxs-lookup"><span data-stu-id="70582-204">Specifies if the Azure virtual machine that is created on failover should use managed disks.</span></span> <span data-ttu-id="70582-205">Igaz vagy Hamis értéket fogad el.</span><span class="sxs-lookup"><span data-stu-id="70582-205">It Accepts either True or False.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: True, False

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70582-206">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="70582-206">-VmmToVmm</span></span>
<span data-ttu-id="70582-207">A paraméter váltása a replikált elem megadásához egy hyper-V virtuális gép, amely a VMM által felügyelt Hyper-V webhelyek között replikálódik.</span><span class="sxs-lookup"><span data-stu-id="70582-207">Switch parameter to specify the replicated item is a Hyper-V virtual machine that is being replicated between VMM managed Hyper-V sites.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70582-208">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="70582-208">-VMwareToAzure</span></span>
<span data-ttu-id="70582-209">A paraméter váltása a replikált elem megadásához egy virtuális VMware-kiszolgáló vagy fizikai kiszolgáló, amely az Azure-ba replikálódik.</span><span class="sxs-lookup"><span data-stu-id="70582-209">Switch parameter to specify the replicated item is a VMware virtual machine or physical server that will be replicate to Azure.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70582-210">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="70582-210">-WaitForCompletion</span></span>
<span data-ttu-id="70582-211">Azt adja meg, hogy a parancsmagnak a visszatérés előtt várnia kell a művelet befejezésére.</span><span class="sxs-lookup"><span data-stu-id="70582-211">Specifies that the cmdlet should wait for completion of the operation before returning.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70582-212">-Confirm</span><span class="sxs-lookup"><span data-stu-id="70582-212">-Confirm</span></span>
<span data-ttu-id="70582-213">A művelet megkezdése előtt megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="70582-213">Prompts  for confirmation before starting the operation.</span></span>

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

### <span data-ttu-id="70582-214">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70582-214">-WhatIf</span></span>
<span data-ttu-id="70582-215">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="70582-215">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70582-216">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="70582-216">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70582-217">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70582-217">CommonParameters</span></span>
<span data-ttu-id="70582-218">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70582-218">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70582-219">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="70582-219">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70582-220">INPUTS</span><span class="sxs-lookup"><span data-stu-id="70582-220">INPUTS</span></span>

### <span data-ttu-id="70582-221">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="70582-221">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="70582-222">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="70582-222">OUTPUTS</span></span>

### <span data-ttu-id="70582-223">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRService</span><span class="sxs-lookup"><span data-stu-id="70582-223">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="70582-224">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="70582-224">NOTES</span></span>

## <span data-ttu-id="70582-225">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="70582-225">RELATED LINKS</span></span>

[<span data-ttu-id="70582-226">Get-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="70582-226">Get-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="70582-227">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="70582-227">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="70582-228">Set-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="70582-228">Set-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzRecoveryServicesAsrReplicationProtectedItem.md)
