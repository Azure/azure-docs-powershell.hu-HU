---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: bde840903c53dae9ba47b9eb30634ce90f80ee9e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185918"
---
# <span data-ttu-id="e6ccb-101">New-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="e6ccb-101">New-AzRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="e6ccb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e6ccb-102">SYNOPSIS</span></span>
<span data-ttu-id="e6ccb-103">Az ASR-védelemmel ellátott elemek replikálásának engedélyezése replikációs védelemmel ellátott elem létrehozásával.</span><span class="sxs-lookup"><span data-stu-id="e6ccb-103">Enables replication for an ASR protectable item by creating a replication protected item.</span></span>

## <span data-ttu-id="e6ccb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e6ccb-104">SYNTAX</span></span>

### <span data-ttu-id="e6ccb-105">EnterpriseToEnterprise (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e6ccb-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-VmmToVmm] -ProtectableItem <ASRProtectableItem>
 -Name <String> -ProtectionContainerMapping <ASRProtectionContainerMapping> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6ccb-106">VMwareToAzureWithDiskType</span><span class="sxs-lookup"><span data-stu-id="e6ccb-106">VMwareToAzureWithDiskType</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-VMwareToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -Account <ASRRunAsAccount> [-LogStorageAccountId <String>] -ProcessServer <ASRProcessServer>
 [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String>
 [-ReplicationGroupName <String>] [-WaitForCompletion] -DiskType <String> [-DiskEncryptionSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6ccb-107">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="e6ccb-107">VMwareToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-VMwareToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -Account <ASRRunAsAccount> [-LogStorageAccountId <String>]
 [-InMageAzureV2DiskInput <AsrInMageAzureV2DiskInput[]>] -ProcessServer <ASRProcessServer>
 [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String>
 [-ReplicationGroupName <String>] [-WaitForCompletion] [-DiskEncryptionSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6ccb-108">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="e6ccb-108">EnterpriseToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-HyperVToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -RecoveryResourceGroupId <String> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6ccb-109">HyperVSiteToAzure</span><span class="sxs-lookup"><span data-stu-id="e6ccb-109">HyperVSiteToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-HyperVToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -OSDiskName <String> -OS <String> [-LogStorageAccountId <String>]
 [-IncludeDiskId <String[]>] [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>]
 -RecoveryResourceGroupId <String> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6ccb-110">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="e6ccb-110">AzureToAzure</span></span>
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

### <span data-ttu-id="e6ccb-111">AzureToAzureWithoutDiskDetails</span><span class="sxs-lookup"><span data-stu-id="e6ccb-111">AzureToAzureWithoutDiskDetails</span></span>
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

## <span data-ttu-id="e6ccb-112">Leírás</span><span class="sxs-lookup"><span data-stu-id="e6ccb-112">DESCRIPTION</span></span>
<span data-ttu-id="e6ccb-113">A **New-AzRecoveryServicesAsrReplicationProtectedItem** parancsmag új replikációs védelemmel ellátott elemet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="e6ccb-113">The **New-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet creates a new replication protected item.</span></span>
<span data-ttu-id="e6ccb-114">Ezzel a parancsmaggal engedélyezheti az ASR-védelemmel ellátott elemek replikálását.</span><span class="sxs-lookup"><span data-stu-id="e6ccb-114">Use this cmdlet to enable replication for an ASR protectable item.</span></span>

## <span data-ttu-id="e6ccb-115">Példák</span><span class="sxs-lookup"><span data-stu-id="e6ccb-115">EXAMPLES</span></span>

### <span data-ttu-id="e6ccb-116">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e6ccb-116">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrReplicationProtectedItem -ProtectableItem $VM -Name $VM.Name -ProtectionContainerMapping $ProtectionContainerMapping
```

<span data-ttu-id="e6ccb-117">Elindítja a védett ASR-elem replikációs védett elem létrehozásának műveletét, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="e6ccb-117">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="e6ccb-118">2. példa</span><span class="sxs-lookup"><span data-stu-id="e6ccb-118">Example 2</span></span>
```
PS C:\>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] `
-RecoveryResourceGroupId $RecoveryResourceGroupId -RecoveryAzureNetworkId $RecoveryAzureNetworkId  -name $name `
-ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem -ProtectionContainerMapping $pcm `
-RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName -LogStorageAccountId $LogStorageAccountId
```

<span data-ttu-id="e6ccb-119">Elindítja a védett ASR-elem replikációs védett elem létrehozásának műveletét, és visszaadja a művelet nyomon követéséhez használt ASR-feladatot (vmWare – Azure eset).</span><span class="sxs-lookup"><span data-stu-id="e6ccb-119">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation(vmWare to Azure scenario).</span></span>

### <span data-ttu-id="e6ccb-120">3. példa</span><span class="sxs-lookup"><span data-stu-id="e6ccb-120">Example 3</span></span>
```
PS C:>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureToAzureDiskReplicationConfig disk1,disk2 -AzVmId $vmId `
-Name "a2aprotectedItem" -RecoveryVmName "vmName" -ProtectionContainerMapping $pcmMapping -RecoveryResourceGroupId $recoveryResourceGroup
```

<span data-ttu-id="e6ccb-121">Elindítja a védett ASR-elem replikációs védett elem létrehozásának műveletét, és visszaadja a művelet nyomon követéséhez használt ASR-feladatot (Azure – Azure forgatókönyv).</span><span class="sxs-lookup"><span data-stu-id="e6ccb-121">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

### <span data-ttu-id="e6ccb-122">4. példa</span><span class="sxs-lookup"><span data-stu-id="e6ccb-122">Example 4</span></span>
```
PS C:\> $disk1 = New-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri1 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId `
-LogStorageAccountId $logStorageAccountId  
PS C:\> $disk2 = New-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri2 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId `
-LogStorageAccountId $logStorageAccountId  
PS C:\> $enableDRjob = New-AzRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureVmId $vmId -Name $rpiName `
-RecoveryCloudServiceId  $recoveryCloudServiceId -ProtectionContainerMapping $pcm -RecoveryResourceGroupId  $RecoveryResourceGroupId `
-AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -RecoveryAzureNetworkId $RecoveryAzureNetworkId -RecoveryAzureSubnetName $RecoveryAzureSubnetName
```

<span data-ttu-id="e6ccb-123">Elindítja a megadott VmId replikációs védett elem létrehozása műveletet, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül (Azure – Azure forgatókönyv).</span><span class="sxs-lookup"><span data-stu-id="e6ccb-123">Starts the replication protected item creation operation for the specified VmId and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

### <span data-ttu-id="e6ccb-124">Példa 5</span><span class="sxs-lookup"><span data-stu-id="e6ccb-124">Example 5</span></span>
```
PS C:\>$disk1 = New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId -LogStorageAccountId $logStorageAccountId -DiskType $diskType
PS C:\>$disk2 = New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId2 -LogStorageAccountId $logStorageAccountId -DiskType $diskType2

PS C:\>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryAzureNetworkId $RecoveryAzureNetworkId  -name $name -ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem  `
-ProtectionContainerMapping $pcm -RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName `
-LogStorageAccountId $LogStorageAccountId -InMageAzureV2DiskInput $disk1,$disk2
```

<span data-ttu-id="e6ccb-125">A megadott ASR-védett elem replikációs védett elem-készítési műveletének indítása a szelektív lemezekkel együtt, valamint a kijelölt lemezekkel végzett (vmWare – Azure) műveletek nyomon követésére szolgáló ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="e6ccb-125">Starts the replication protected item creation operation for the specified ASR protectable item including selective disks and returns the ASR job used to track the operation(vmWare to Azure scenario) with selected disks.</span></span>

### <span data-ttu-id="e6ccb-126">6. példa</span><span class="sxs-lookup"><span data-stu-id="e6ccb-126">Example 6</span></span>
```
PS C:\>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryAzureNetworkId $RecoveryAzureNetworkId  -name $name -ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem  `
-ProtectionContainerMapping $pcm -RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName `
-LogStorageAccountId $LogStorageAccountId -DiskType Standard_LRS

Starts the replication protected item creation operation for the specified ASR protectable item with default disk type and returns the ASR job used to track the operation(vmWare to Azure scenario).
```

### <span data-ttu-id="e6ccb-127">7. példa</span><span class="sxs-lookup"><span data-stu-id="e6ccb-127">Example 7</span></span>
```
PS C:\> $disk1 = New-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri1 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId -LogStorageAccountId $logStorageAccountId  
PS C:\> $disk2 = new-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri2 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId -LogStorageAccountId $logStorageAccountId  
PS C:\> $enableDRjob = New-AzRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzVmId $vmId -Name $rpiName `
-RecoveryCloudServiceId  $recoveryCloudServiceId -ProtectionContainerMapping $pcm -RecoveryResourceGroupId  $RecoveryResourceGroupId `
-AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -DiskEncryptionVaultId  $DiskEncryptionVaultId -DiskEncryptionSecertUrl $DiskEncryptionSecertUrl `
 -KeyEncryptionVaultId $KeyEncryptionVaultId  -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl
```

<span data-ttu-id="e6ccb-128">Elindítja a megadott VmId replikációs védett elem létrehozása műveletet, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül (Azure – Azure forgatókönyv). A feladatátvevő VM-ben a titkosítási parancsmagban kapott részleteket a rendszer használja.</span><span class="sxs-lookup"><span data-stu-id="e6ccb-128">Starts the replication protected item creation operation for the specified VmId and returns the ASR job used to track the operation (Azure to Azure scenario).For the failover VM details passed in cmdlet for encryption will be used .</span></span>

### <span data-ttu-id="e6ccb-129">8. példa</span><span class="sxs-lookup"><span data-stu-id="e6ccb-129">Example 8</span></span>
```
PS C:>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureToAzureDiskReplicationConfig disk1,disk2 -AzVmId $vmId `
-Name "a2aprotectedItem" -RecoveryVmName "vmName" -ProtectionContainerMapping $pcmMapping -RecoveryResourceGroupId $recoveryResourceGroup -RecoveryProximityPlacementGroupId $ppg
```

<span data-ttu-id="e6ccb-130">A replikációs szolgáltatással védett elem létrehozásának műveletét indítja el egy virtuális gép számára a közelségi hely csoportban, és a művelet nyomon követéséhez használt ASR-feladatot (Azure – Azure eset) jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="e6ccb-130">Starts the replication protected item creation operation for a Virtual Machine inside Proximity placement group and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

## <span data-ttu-id="e6ccb-131">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e6ccb-131">PARAMETERS</span></span>

### <span data-ttu-id="e6ccb-132">-Fiók</span><span class="sxs-lookup"><span data-stu-id="e6ccb-132">-Account</span></span>
<span data-ttu-id="e6ccb-133">A Futtatás mint fiók, amellyel szükség esetén lenyomhatja a mobil szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="e6ccb-133">The run as account to be used to push install the Mobility service if needed.</span></span> <span data-ttu-id="e6ccb-134">Az ASR-anyagban a Run as (futtatási) fiókból kell lennie.</span><span class="sxs-lookup"><span data-stu-id="e6ccb-134">Must be one from the list of run as accounts in the ASR fabric.</span></span>

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

### <span data-ttu-id="e6ccb-135">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="e6ccb-135">-AzureToAzure</span></span>
<span data-ttu-id="e6ccb-136">Kapcsoló paraméter: a replikált elem létrehozása az Azure-ról Azure-helyzetbe</span><span class="sxs-lookup"><span data-stu-id="e6ccb-136">Switch parameter specifies creating the replicated item in azure to azure scenario.</span></span>

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

### <span data-ttu-id="e6ccb-137">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="e6ccb-137">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="e6ccb-138">A VM-hez az Azure-hoz Azure katasztrófa-helyreállítási forgatókönyvhez használt merevlemez-konfigurációt adja meg.</span><span class="sxs-lookup"><span data-stu-id="e6ccb-138">Specifies the disk configuration to used Vm for Azure to Azure disaster recovery scenario.</span></span>

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

### <span data-ttu-id="e6ccb-139">-AzureVmId</span><span class="sxs-lookup"><span data-stu-id="e6ccb-139">-AzureVmId</span></span>
<span data-ttu-id="e6ccb-140">Az Azure VM azonosítóját adja meg a helyreállítási terület katasztrófa-helyreállítási védeleméhez.</span><span class="sxs-lookup"><span data-stu-id="e6ccb-140">Specifies the Azure VM id for disaster recovery protection in recovery region.</span></span>

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

### <span data-ttu-id="e6ccb-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6ccb-141">-DefaultProfile</span></span>
<span data-ttu-id="e6ccb-142">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e6ccb-142">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="e6ccb-143">-DiskEncryptionSecretUrl</span><span class="sxs-lookup"><span data-stu-id="e6ccb-143">-DiskEncryptionSecretUrl</span></span>
<span data-ttu-id="e6ccb-144">A (Azure Disk Encryption) titkosítással elvégezhető titkosítatlan URL-címet adja meg, amelyet a feladatátvétel után kell használni a helyreállítási VM-nek.</span><span class="sxs-lookup"><span data-stu-id="e6ccb-144">Specifies the disk encryption secret URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="e6ccb-145">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="e6ccb-145">-DiskEncryptionSetId</span></span>
<span data-ttu-id="e6ccb-146">A távtárolású lemezek titkosításához használt Lemezkezelés-készlet erőforrás-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e6ccb-146">Specifies the resource Id of the disk encryption set, to be used for the encryption of the managed disks.</span></span>

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

### <span data-ttu-id="e6ccb-147">-DiskEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="e6ccb-147">-DiskEncryptionVaultId</span></span>
<span data-ttu-id="e6ccb-148">A titkosítatlan virtuális merevlemez-azonosító (Azure Disk Encryption) azonosítóját adja meg, amelyet a feladatátvétel után kell használni a helyreállítási VM-nek.</span><span class="sxs-lookup"><span data-stu-id="e6ccb-148">Specifies the disk encryption secret vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="e6ccb-149">-DiskType</span><span class="sxs-lookup"><span data-stu-id="e6ccb-149">-DiskType</span></span>
<span data-ttu-id="e6ccb-150">A helyreállítási VM felügyelt típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e6ccb-150">Specifies the Recovery VM managed disk type.</span></span>

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

### <span data-ttu-id="e6ccb-151">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="e6ccb-151">-HyperVToAzure</span></span>
<span data-ttu-id="e6ccb-152">Váltson paramétert a replikált elem megadásához: egy olyan Hyper-V virtuális gép, amely az Azure-ra replikálódik.</span><span class="sxs-lookup"><span data-stu-id="e6ccb-152">Switch parameter to specify the replicated item is a Hyper-V virtual machine that is being replicated to Azure.</span></span>

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

### <span data-ttu-id="e6ccb-153">-IncludeDiskId</span><span class="sxs-lookup"><span data-stu-id="e6ccb-153">-IncludeDiskId</span></span>
<span data-ttu-id="e6ccb-154">A replikációra felvenni kívánt lemezek listája.</span><span class="sxs-lookup"><span data-stu-id="e6ccb-154">The list of disks to include for replication.</span></span> <span data-ttu-id="e6ccb-155">Alapértelmezés szerint az összes lemez megtalálható.</span><span class="sxs-lookup"><span data-stu-id="e6ccb-155">By default all disks are included.</span></span>

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

### <span data-ttu-id="e6ccb-156">-InMageAzureV2DiskInput</span><span class="sxs-lookup"><span data-stu-id="e6ccb-156">-InMageAzureV2DiskInput</span></span>
<span data-ttu-id="e6ccb-157">A vMWare Disk azonosító Disk Configuration bemenetét adja meg a megadott védett elemtől való védelem érdekében.</span><span class="sxs-lookup"><span data-stu-id="e6ccb-157">Specifies the disk configuration input for vMWare disk id to protect from specified protectable item.</span></span>

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

### <span data-ttu-id="e6ccb-158">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="e6ccb-158">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="e6ccb-159">Annak a lemez-titkosítási kulcsnak az URL-címe, amelynek verziószáma (Azure Disk Encryption) a feladatátvétel után használatos a helyreállítási VM.</span><span class="sxs-lookup"><span data-stu-id="e6ccb-159">Specifies the disk encryption key URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="e6ccb-160">-KeyEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="e6ccb-160">-KeyEncryptionVaultId</span></span>
<span data-ttu-id="e6ccb-161">Itt adhatja meg, hogy a rendszer a merevlemez-tároló (Azure Disk Encryption) kulcsát használja a helyreállítási VM után a feladatátvétel után.</span><span class="sxs-lookup"><span data-stu-id="e6ccb-161">Specifies the disk encryption key key-vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="e6ccb-162">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="e6ccb-162">-LogStorageAccountId</span></span>
<span data-ttu-id="e6ccb-163">A replikációs naplók tárolásához használható naplófájl-vagy gyorsítótár-tárolási fiók azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e6ccb-163">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

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

### <span data-ttu-id="e6ccb-164">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e6ccb-164">-Name</span></span>
<span data-ttu-id="e6ccb-165">Az ASR replikációs szolgáltatása által védett elem nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e6ccb-165">Specifies a name for the ASR replication protected item.</span></span> <span data-ttu-id="e6ccb-166">A névnek a boltozaton belül egyedinek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="e6ccb-166">The name must be unique within the vault.</span></span>

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

### <span data-ttu-id="e6ccb-167">-OS</span><span class="sxs-lookup"><span data-stu-id="e6ccb-167">-OS</span></span>
<span data-ttu-id="e6ccb-168">Az operációs rendszer családját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e6ccb-168">Specifies the operating system family.</span></span>
<span data-ttu-id="e6ccb-169">A paraméter elfogadható értékei a következők: Windows vagy Linux.</span><span class="sxs-lookup"><span data-stu-id="e6ccb-169">The acceptable values for this parameter are: Windows or Linux.</span></span>

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

### <span data-ttu-id="e6ccb-170">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="e6ccb-170">-OSDiskName</span></span>
<span data-ttu-id="e6ccb-171">Az operációs rendszer lemezének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e6ccb-171">Specifies the name of the operating system disk.</span></span>

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

### <span data-ttu-id="e6ccb-172">-ProcessServer</span><span class="sxs-lookup"><span data-stu-id="e6ccb-172">-ProcessServer</span></span>
<span data-ttu-id="e6ccb-173">A gép replikálásához használt folyamat kiszolgálója.</span><span class="sxs-lookup"><span data-stu-id="e6ccb-173">The Process Server to use to replicate this machine.</span></span> <span data-ttu-id="e6ccb-174">Adja meg az ASR-anyagnak megfelelő folyamat-kiszolgálók listáját az ASR-szövetben, amely a beállítási kiszolgálónak megfelelő.</span><span class="sxs-lookup"><span data-stu-id="e6ccb-174">Use the list of process servers in the ASR fabric corresponding to the Configuration server to specify one.</span></span>

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

### <span data-ttu-id="e6ccb-175">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="e6ccb-175">-ProtectableItem</span></span>
<span data-ttu-id="e6ccb-176">Annak az ASR-elemnek az objektumát adja meg, amelyhez a replikáció engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="e6ccb-176">Specifies the ASR protectable item object for which replication is being enabled.</span></span>

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

### <span data-ttu-id="e6ccb-177">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="e6ccb-177">-ProtectionContainerMapping</span></span>
<span data-ttu-id="e6ccb-178">Az ASR-védelmi tároló társítása objektum, amely megfelel a replikációhoz használandó replikációs házirendnek.</span><span class="sxs-lookup"><span data-stu-id="e6ccb-178">Specifies the ASR protection container mapping object corresponding to the replication policy to be used for replication.</span></span>

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

### <span data-ttu-id="e6ccb-179">-RecoveryAvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="e6ccb-179">-RecoveryAvailabilitySetId</span></span>
<span data-ttu-id="e6ccb-180">A AvailabilitySet azonosítója, amellyel visszaállíthatja a gépet feladatátvétel esetén.</span><span class="sxs-lookup"><span data-stu-id="e6ccb-180">The ID of the AvailabilitySet to recover the machine to in the event of a failover.</span></span>

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

### <span data-ttu-id="e6ccb-181">-RecoveryAvailabilityZone</span><span class="sxs-lookup"><span data-stu-id="e6ccb-181">-RecoveryAvailabilityZone</span></span>
<span data-ttu-id="e6ccb-182">A helyreállítási VM elérhetőségi zónáját a feladatátvétel után adja meg.</span><span class="sxs-lookup"><span data-stu-id="e6ccb-182">Specifies the recovery VM availability zone after failover.</span></span>


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

### <span data-ttu-id="e6ccb-183">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="e6ccb-183">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="e6ccb-184">Az Azure virtuális hálózat azonosítója, amellyel a gépet feladatátvétel esetén helyreállíthatja.</span><span class="sxs-lookup"><span data-stu-id="e6ccb-184">The ID of the Azure virtual network to recover the machine to in the event of a failover.</span></span>

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

### <span data-ttu-id="e6ccb-185">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="e6ccb-185">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="e6ccb-186">A replikálni kívánt Azure Storage-fiók AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e6ccb-186">Specifies the ID of the Azure storage account to replicate to.</span></span>

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

### <span data-ttu-id="e6ccb-187">-RecoveryAzureSubnetName</span><span class="sxs-lookup"><span data-stu-id="e6ccb-187">-RecoveryAzureSubnetName</span></span>
<span data-ttu-id="e6ccb-188">A helyreállítási Azure virtuális hálózaton belül az alhálózat, amelyre a sikertelen virtuális gépet csatolni kell a feladatátvétel esetén.</span><span class="sxs-lookup"><span data-stu-id="e6ccb-188">The subnet within the recovery Azure virtual network to which the failed over virtual machine should be attached in the event of a failover.</span></span>

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

### <span data-ttu-id="e6ccb-189">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="e6ccb-189">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="e6ccb-190">A helyreállítás Azure VM rendszerindítási diagnosztika tárolási fiókját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e6ccb-190">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

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

### <span data-ttu-id="e6ccb-191">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="e6ccb-191">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="e6ccb-192">A helyreállítási felhő szolgáltatás erőforrás-AZONOSÍTÓját adja meg a virtuális gép feladatátvételéhez.</span><span class="sxs-lookup"><span data-stu-id="e6ccb-192">Specifies the resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

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

### <span data-ttu-id="e6ccb-193">-RecoveryProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="e6ccb-193">-RecoveryProximityPlacementGroupId</span></span>
<span data-ttu-id="e6ccb-194">Adja meg a közelségi hely azonosítóját, amelyet a feladatátvevő VM a TARGET Recovery régióban használt.</span><span class="sxs-lookup"><span data-stu-id="e6ccb-194">Specify the proximity placement group Id to used by the failover Vm in target recovery region.</span></span>

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

### <span data-ttu-id="e6ccb-195">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="e6ccb-195">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="e6ccb-196">Meghatározza annak az erőforráscsoport-azonosítónak az azonosítóját, amelyben a virtuális gépet feladatátvétel esetén létrehozzák.</span><span class="sxs-lookup"><span data-stu-id="e6ccb-196">Specifies the ARM identifier of the resource group in which the virtual machine will be created in the event of a failover.</span></span>

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

### <span data-ttu-id="e6ccb-197">-RecoveryVmName</span><span class="sxs-lookup"><span data-stu-id="e6ccb-197">-RecoveryVmName</span></span>
<span data-ttu-id="e6ccb-198">A feladatátvétel után létrejövő helyreállítási VM-név.</span><span class="sxs-lookup"><span data-stu-id="e6ccb-198">Name of the recovery Vm created after failover.</span></span>

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

### <span data-ttu-id="e6ccb-199">-ReplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="e6ccb-199">-ReplicationGroupName</span></span>
<span data-ttu-id="e6ccb-200">Annak a replikációs csoportnak a nevét adja meg, amely a több VM egységes helyreállítási pontok létrehozására használható.</span><span class="sxs-lookup"><span data-stu-id="e6ccb-200">Specifies the replication group name to use to create multi-VM consistent recovery points.</span></span> <span data-ttu-id="e6ccb-201">Alapértelmezés szerint az egyes replikációs védelemmel ellátott elemek a saját és a több VM-es konzisztens helyreállítási pontok csoportjába jönnek létre.</span><span class="sxs-lookup"><span data-stu-id="e6ccb-201">By default each replication protected item is created in a group of its own and multi-VM consistent recovery points are not generated.</span></span> <span data-ttu-id="e6ccb-202">Ezt a lehetőséget csak akkor használja, ha több VM-es konzisztens helyreállítási pontot kell létrehoznia a számítógépeken, ha az összes gépet ugyanabba a replikációs csoportba kívánja védeni.</span><span class="sxs-lookup"><span data-stu-id="e6ccb-202">Use this option only if you need to create multi-VM consistent recovery points across a group of machines by protecting all machines to the same replication group.</span></span> 

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

### <span data-ttu-id="e6ccb-203">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="e6ccb-203">-VmmToVmm</span></span>
<span data-ttu-id="e6ccb-204">Kapcsoló paraméter a replikált elem megadásához: egy olyan Hyper-V virtuális gép, amely a VMM felügyelt Hyper-V-webhelyek között replikálódik.</span><span class="sxs-lookup"><span data-stu-id="e6ccb-204">Switch parameter to specify the replicated item is a Hyper-V virtual machine that is being replicated between VMM managed Hyper-V sites.</span></span>

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

### <span data-ttu-id="e6ccb-205">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="e6ccb-205">-VMwareToAzure</span></span>
<span data-ttu-id="e6ccb-206">Váltson paramétert a replikált elem megadásához egy olyan VMware Virtual Machine vagy fizikai kiszolgáló, amely az Azure-ra replikálódni fog.</span><span class="sxs-lookup"><span data-stu-id="e6ccb-206">Switch parameter to specify the replicated item is a VMware virtual machine or physical server that will be replicate to Azure.</span></span>

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

### <span data-ttu-id="e6ccb-207">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="e6ccb-207">-WaitForCompletion</span></span>
<span data-ttu-id="e6ccb-208">Azt adja meg, hogy a parancsmagnak a művelet befejezésekor várnia kell.</span><span class="sxs-lookup"><span data-stu-id="e6ccb-208">Specifies that the cmdlet should wait for completion of the operation before returning.</span></span>

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

### <span data-ttu-id="e6ccb-209">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e6ccb-209">-Confirm</span></span>
<span data-ttu-id="e6ccb-210">Megerősítés kérése a művelet megkezdése előtt.</span><span class="sxs-lookup"><span data-stu-id="e6ccb-210">Prompts  for confirmation before starting the operation.</span></span>

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

### <span data-ttu-id="e6ccb-211">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6ccb-211">-WhatIf</span></span>
<span data-ttu-id="e6ccb-212">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e6ccb-212">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6ccb-213">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e6ccb-213">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6ccb-214">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6ccb-214">CommonParameters</span></span>
<span data-ttu-id="e6ccb-215">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e6ccb-215">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6ccb-216">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e6ccb-216">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6ccb-217">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e6ccb-217">INPUTS</span></span>

### <span data-ttu-id="e6ccb-218">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="e6ccb-218">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="e6ccb-219">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e6ccb-219">OUTPUTS</span></span>

### <span data-ttu-id="e6ccb-220">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="e6ccb-220">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="e6ccb-221">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e6ccb-221">NOTES</span></span>

## <span data-ttu-id="e6ccb-222">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e6ccb-222">RELATED LINKS</span></span>

[<span data-ttu-id="e6ccb-223">Get-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="e6ccb-223">Get-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="e6ccb-224">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="e6ccb-224">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="e6ccb-225">Set-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="e6ccb-225">Set-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzRecoveryServicesAsrReplicationProtectedItem.md)
