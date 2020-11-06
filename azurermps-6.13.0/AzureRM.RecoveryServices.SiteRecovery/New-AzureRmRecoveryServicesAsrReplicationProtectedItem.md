---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 6a35620b7a4d8952b10973f181c2ab50f5d958b7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93491873"
---
# <span data-ttu-id="454cf-101">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="454cf-101">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="454cf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="454cf-102">SYNOPSIS</span></span>
<span data-ttu-id="454cf-103">Az ASR-védelemmel ellátott elemek replikálásának engedélyezése replikációs védelemmel ellátott elem létrehozásával.</span><span class="sxs-lookup"><span data-stu-id="454cf-103">Enables replication for an ASR protectable item by creating a replication protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="454cf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="454cf-104">SYNTAX</span></span>

### <span data-ttu-id="454cf-105">EnterpriseToEnterprise (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="454cf-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem [-VmmToVmm] -ProtectableItem <ASRProtectableItem>
 -Name <String> -ProtectionContainerMapping <ASRProtectionContainerMapping> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="454cf-106">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="454cf-106">VMwareToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem [-VMwareToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -Account <ASRRunAsAccount> [-LogStorageAccountId <String>]
 [-IncludeDiskId <String[]>] -ProcessServer <ASRProcessServer> [-RecoveryAzureNetworkId <String>]
 [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String> [-ReplicationGroupName <String>]
 [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="454cf-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="454cf-107">EnterpriseToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem [-HyperVToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -RecoveryResourceGroupId <String> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="454cf-108">HyperVSiteToAzure</span><span class="sxs-lookup"><span data-stu-id="454cf-108">HyperVSiteToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem [-HyperVToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -OSDiskName <String> -OS <String> [-LogStorageAccountId <String>]
 [-IncludeDiskId <String[]>] [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>]
 -RecoveryResourceGroupId <String> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="454cf-109">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="454cf-109">AzureToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem [-AzureToAzure]
 -AzureToAzureDiskReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]> -AzureVmId <String>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryResourceGroupId <String> [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilitySetId <String>]
 [-RecoveryBootDiagStorageAccountId <String>] [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="454cf-110">AzureToAzureWithoutDiskDetails</span><span class="sxs-lookup"><span data-stu-id="454cf-110">AzureToAzureWithoutDiskDetails</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem [-AzureToAzure] -AzureVmId <String> -Name <String>
 [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 [-RecoveryAzureStorageAccountId <String>] -LogStorageAccountId <String> -RecoveryResourceGroupId <String>
 [-RecoveryAvailabilitySetId <String>] [-RecoveryBootDiagStorageAccountId <String>] [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="454cf-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="454cf-111">DESCRIPTION</span></span>
<span data-ttu-id="454cf-112">A **New-AzureRmRecoveryServicesAsrReplicationProtectedItem** parancsmag új replikációs védelemmel ellátott elemet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="454cf-112">The **New-AzureRmRecoveryServicesAsrReplicationProtectedItem** cmdlet creates a new replication protected item.</span></span>
<span data-ttu-id="454cf-113">Ezzel a parancsmaggal engedélyezheti az ASR-védelemmel ellátott elemek replikálását.</span><span class="sxs-lookup"><span data-stu-id="454cf-113">Use this cmdlet to enable replication for an ASR protectable item.</span></span>

## <span data-ttu-id="454cf-114">Példák</span><span class="sxs-lookup"><span data-stu-id="454cf-114">EXAMPLES</span></span>

### <span data-ttu-id="454cf-115">Példa 1</span><span class="sxs-lookup"><span data-stu-id="454cf-115">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectableItem $VM -Name $VM.Name -ProtectionContainerMapping $ProtectionContainerMapping
```

<span data-ttu-id="454cf-116">Elindítja a védett ASR-elem replikációs védett elem létrehozásának műveletét, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="454cf-116">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="454cf-117">2. példa</span><span class="sxs-lookup"><span data-stu-id="454cf-117">Example 2</span></span>
```
PS C:\>$job = New-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectableItem $pi -Name $rpiName -ProtectionContainerMapping $pcm `
-RecoveryAzureStorageAccountId $RecoveryAzureStorageAccountId -RecoveryResourceGroupId  $RecoveryResourceGroupId `
-ProcessServer $fabric.fabricSpecificDetails.ProcessServers[0] -Account $fabric.fabricSpecificDetails.RunAsAccounts[0]
```

<span data-ttu-id="454cf-118">Elindítja a védett ASR-elem replikációs védett elem létrehozásának műveletét, és visszaadja a művelet nyomon követéséhez használt ASR-feladatot (vmWare – Azure eset).</span><span class="sxs-lookup"><span data-stu-id="454cf-118">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation(vmWare to Azure scenario).</span></span>

### <span data-ttu-id="454cf-119">3. példa</span><span class="sxs-lookup"><span data-stu-id="454cf-119">Example 3</span></span>
```
PS C:>$job = New-AzureRmRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureToAzureDiskReplicationConfig disk1,disk2 -AzureVmId $vmId `
-Name "a2aprotectedItem" -RecoveryVmName "vmName" -ProtectionContainerMapping $pcmMapping -RecoveryResourceGroupId $recoveryResourceGroup
```

<span data-ttu-id="454cf-120">Elindítja a védett ASR-elem replikációs védett elem létrehozásának műveletét, és visszaadja a művelet nyomon követéséhez használt ASR-feladatot (Azure – Azure forgatókönyv).</span><span class="sxs-lookup"><span data-stu-id="454cf-120">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

### <span data-ttu-id="454cf-121">4. példa</span><span class="sxs-lookup"><span data-stu-id="454cf-121">Example 4</span></span>
```
PS C:\> $disk1 = new-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri1 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId `
-LogStorageAccountId $logStorageAccountId  
PS C:\> $disk2 = new-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri2 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId `
-LogStorageAccountId $logStorageAccountId  
PS C:\> $enableDRjob = New-AzureRmRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureVmId $vmId -Name $rpiName `
-RecoveryCloudServiceId  $recoveryCloudServiceId -ProtectionContainerMapping $pcm -RecoveryResourceGroupId  $RecoveryResourceGroupId `
-AzureToAzureDiskReplicationConfiguration $disk1,$disk2
```

<span data-ttu-id="454cf-122">Elindítja a megadott VmId replikációs védett elem létrehozása műveletet, és a művelet nyomon követéséhez használt ASR-feladatot adja eredményül (Azure – Azure forgatókönyv).</span><span class="sxs-lookup"><span data-stu-id="454cf-122">Starts the replication protected item creation operation for the specified VmId and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

## <span data-ttu-id="454cf-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="454cf-123">PARAMETERS</span></span>

### <span data-ttu-id="454cf-124">-Fiók</span><span class="sxs-lookup"><span data-stu-id="454cf-124">-Account</span></span>
<span data-ttu-id="454cf-125">A Futtatás mint fiók, amellyel szükség esetén lenyomhatja a mobil szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="454cf-125">The run as account to be used to push install the Mobility service if needed.</span></span> <span data-ttu-id="454cf-126">Az ASR-anyagban a Run as (futtatási) fiókból kell lennie.</span><span class="sxs-lookup"><span data-stu-id="454cf-126">Must be one from the list of run as accounts in the ASR fabric.</span></span>

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

### <span data-ttu-id="454cf-127">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="454cf-127">-AzureToAzure</span></span>
<span data-ttu-id="454cf-128">A paramétert leválasztva megadhatja, hogy a replikált elem a helyreállítási Azure-területre replikált Azure virtuális gép.</span><span class="sxs-lookup"><span data-stu-id="454cf-128">Switch parameter to specify that the replicated item is an Azure virtual machine replicating to a recovery Azure region.</span></span>

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

### <span data-ttu-id="454cf-129">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="454cf-129">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="454cf-130">A replikálni kívánt virtuálisgép-lemezek listáját adja meg, valamint a gyorsítótár-tárolási fiókot és a helyreállítási tárterületet, amelyet a lemez replikálásához kell használni.</span><span class="sxs-lookup"><span data-stu-id="454cf-130">Specifies the list of virtual machine disks to replicated and the cache storage account and recovery storage account to be used to replicate the disk.</span></span>

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

### <span data-ttu-id="454cf-131">-AzureVmId</span><span class="sxs-lookup"><span data-stu-id="454cf-131">-AzureVmId</span></span>
<span data-ttu-id="454cf-132">A replikálni kívánt Azure VM-azonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="454cf-132">Specifies the azure vm id to be replicated.</span></span>

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

### <span data-ttu-id="454cf-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="454cf-133">-DefaultProfile</span></span>
<span data-ttu-id="454cf-134">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="454cf-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="454cf-135">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="454cf-135">-HyperVToAzure</span></span>
<span data-ttu-id="454cf-136">Váltson paramétert a replikált elem megadásához: egy olyan Hyper-V virtuális gép, amely az Azure-ra replikálódik.</span><span class="sxs-lookup"><span data-stu-id="454cf-136">Switch parameter to specify the replicated item is a Hyper-V virtual machine that is being replicated to Azure.</span></span>

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

### <span data-ttu-id="454cf-137">-IncludeDiskId</span><span class="sxs-lookup"><span data-stu-id="454cf-137">-IncludeDiskId</span></span>
<span data-ttu-id="454cf-138">A replikációra felvenni kívánt lemezek listája.</span><span class="sxs-lookup"><span data-stu-id="454cf-138">The list of disks to include for replication.</span></span> <span data-ttu-id="454cf-139">Alapértelmezés szerint az összes lemez megtalálható.</span><span class="sxs-lookup"><span data-stu-id="454cf-139">By default all disks are included.</span></span>

```yaml
Type: System.String[]
Parameter Sets: VMwareToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="454cf-140">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="454cf-140">-LogStorageAccountId</span></span>
<span data-ttu-id="454cf-141">A replikációs naplók tárolásához használható naplófájl-vagy gyorsítótár-tárolási fiók azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="454cf-141">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, HyperVSiteToAzure
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

### <span data-ttu-id="454cf-142">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="454cf-142">-Name</span></span>
<span data-ttu-id="454cf-143">Az ASR replikációs szolgáltatása által védett elem nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="454cf-143">Specifies a name for the ASR replication protected item.</span></span> <span data-ttu-id="454cf-144">A névnek a boltozaton belül egyedinek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="454cf-144">The name must be unique within the vault.</span></span>

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

### <span data-ttu-id="454cf-145">-OS</span><span class="sxs-lookup"><span data-stu-id="454cf-145">-OS</span></span>
<span data-ttu-id="454cf-146">Az operációs rendszer családját adja meg.</span><span class="sxs-lookup"><span data-stu-id="454cf-146">Specifies the operating system family.</span></span>
<span data-ttu-id="454cf-147">A paraméter elfogadható értékei a következők: Windows vagy Linux.</span><span class="sxs-lookup"><span data-stu-id="454cf-147">The acceptable values for this parameter are: Windows or Linux.</span></span>

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

### <span data-ttu-id="454cf-148">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="454cf-148">-OSDiskName</span></span>
<span data-ttu-id="454cf-149">Az operációs rendszer lemezének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="454cf-149">Specifies the name of the operating system disk.</span></span>

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

### <span data-ttu-id="454cf-150">-ProcessServer</span><span class="sxs-lookup"><span data-stu-id="454cf-150">-ProcessServer</span></span>
<span data-ttu-id="454cf-151">A gép replikálásához használt folyamat kiszolgálója.</span><span class="sxs-lookup"><span data-stu-id="454cf-151">The Process Server to use to replicate this machine.</span></span> <span data-ttu-id="454cf-152">Adja meg az ASR-anyagnak megfelelő folyamat-kiszolgálók listáját az ASR-szövetben, amely a beállítási kiszolgálónak megfelelő.</span><span class="sxs-lookup"><span data-stu-id="454cf-152">Use the list of process servers in the ASR fabric corresponding to the Configuration server to specify one.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProcessServer
Parameter Sets: VMwareToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="454cf-153">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="454cf-153">-ProtectableItem</span></span>
<span data-ttu-id="454cf-154">Annak az ASR-elemnek az objektumát adja meg, amelyhez a replikáció engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="454cf-154">Specifies the ASR protectable item object for which replication is being enabled.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem
Parameter Sets: EnterpriseToEnterprise, VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="454cf-155">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="454cf-155">-ProtectionContainerMapping</span></span>
<span data-ttu-id="454cf-156">Az ASR-védelmi tároló társítása objektum, amely megfelel a replikációhoz használandó replikációs házirendnek.</span><span class="sxs-lookup"><span data-stu-id="454cf-156">Specifies the ASR protection container mapping object corresponding to the replication policy to be used for replication.</span></span>

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

### <span data-ttu-id="454cf-157">-RecoveryAvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="454cf-157">-RecoveryAvailabilitySetId</span></span>
<span data-ttu-id="454cf-158">A AvailabilitySet azonosítója, amellyel visszaállíthatja a gépet feladatátvétel esetén.</span><span class="sxs-lookup"><span data-stu-id="454cf-158">The ID of the AvailabilitySet to recover the machine to in the event of a failover.</span></span>

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

### <span data-ttu-id="454cf-159">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="454cf-159">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="454cf-160">Az Azure virtuális hálózat azonosítója, amellyel a gépet feladatátvétel esetén helyreállíthatja.</span><span class="sxs-lookup"><span data-stu-id="454cf-160">The ID of the Azure virtual network to recover the machine to in the event of a failover.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="454cf-161">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="454cf-161">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="454cf-162">A replikálni kívánt Azure Storage-fiók AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="454cf-162">Specifies the ID of the Azure storage account to replicate to.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure
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

### <span data-ttu-id="454cf-163">-RecoveryAzureSubnetName</span><span class="sxs-lookup"><span data-stu-id="454cf-163">-RecoveryAzureSubnetName</span></span>
<span data-ttu-id="454cf-164">A helyreállítási Azure virtuális hálózaton belül az alhálózat, amelyre a sikertelen virtuális gépet csatolni kell a feladatátvétel esetén.</span><span class="sxs-lookup"><span data-stu-id="454cf-164">The subnet within the recovery Azure virtual network to which the failed over virtual machine should be attached in the event of a failover.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="454cf-165">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="454cf-165">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="454cf-166">A helyreállítás Azure VM rendszerindítási diagnosztika tárolási fiókját adja meg.</span><span class="sxs-lookup"><span data-stu-id="454cf-166">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

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

### <span data-ttu-id="454cf-167">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="454cf-167">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="454cf-168">A helyreállítási felhő szolgáltatás erőforrás-AZONOSÍTÓját adja meg a virtuális gép feladatátvételéhez.</span><span class="sxs-lookup"><span data-stu-id="454cf-168">Specifies the resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

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

### <span data-ttu-id="454cf-169">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="454cf-169">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="454cf-170">Meghatározza annak az erőforráscsoport-azonosítónak az azonosítóját, amelyben a virtuális gépet feladatátvétel esetén létrehozzák.</span><span class="sxs-lookup"><span data-stu-id="454cf-170">Specifies the ARM identifier of the resource group in which the virtual machine will be created in the event of a failover.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="454cf-171">-RecoveryVmName</span><span class="sxs-lookup"><span data-stu-id="454cf-171">-RecoveryVmName</span></span>
<span data-ttu-id="454cf-172">A feladatátvétel után létrejövő helyreállítási VM-név.</span><span class="sxs-lookup"><span data-stu-id="454cf-172">Name of the recovery Vm created after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="454cf-173">-ReplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="454cf-173">-ReplicationGroupName</span></span>
<span data-ttu-id="454cf-174">Annak a replikációs csoportnak a nevét adja meg, amely a több VM egységes helyreállítási pontok létrehozására használható.</span><span class="sxs-lookup"><span data-stu-id="454cf-174">Specifies the replication group name to use to create multi-VM consistent recovery points.</span></span> <span data-ttu-id="454cf-175">Alapértelmezés szerint az egyes replikációs védelemmel ellátott elemek a saját és a több VM-es konzisztens helyreállítási pontok csoportjába jönnek létre.</span><span class="sxs-lookup"><span data-stu-id="454cf-175">By default each replication protected item is created in a group of its own and multi-VM consistent recovery points are not generated.</span></span> <span data-ttu-id="454cf-176">Ezt a lehetőséget csak akkor használja, ha több VM-es konzisztens helyreállítási pontot kell létrehoznia a számítógépeken, ha az összes gépet ugyanabba a replikációs csoportba kívánja védeni.</span><span class="sxs-lookup"><span data-stu-id="454cf-176">Use this option only if you need to create multi-VM consistent recovery points across a group of machines by protecting all machines to the same replication group.</span></span> 

```yaml
Type: System.String
Parameter Sets: VMwareToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="454cf-177">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="454cf-177">-VmmToVmm</span></span>
<span data-ttu-id="454cf-178">Kapcsoló paraméter a replikált elem megadásához: egy olyan Hyper-V virtuális gép, amely a VMM felügyelt Hyper-V-webhelyek között replikálódik.</span><span class="sxs-lookup"><span data-stu-id="454cf-178">Switch parameter to specify the replicated item is a Hyper-V virtual machine that is being replicated between VMM managed Hyper-V sites.</span></span>

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

### <span data-ttu-id="454cf-179">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="454cf-179">-VMwareToAzure</span></span>
<span data-ttu-id="454cf-180">Váltson paramétert a replikált elem megadásához egy olyan VMware Virtual Machine vagy fizikai kiszolgáló, amely az Azure-ra replikálódni fog.</span><span class="sxs-lookup"><span data-stu-id="454cf-180">Switch parameter to specify the replicated item is a VMware virtual machine or physical server that will be replicate to Azure.</span></span>

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

### <span data-ttu-id="454cf-181">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="454cf-181">-WaitForCompletion</span></span>
<span data-ttu-id="454cf-182">Azt adja meg, hogy a parancsmagnak a művelet befejezésekor várnia kell.</span><span class="sxs-lookup"><span data-stu-id="454cf-182">Specifies that the cmdlet should wait for completion of the operation before returning.</span></span>

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

### <span data-ttu-id="454cf-183">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="454cf-183">-Confirm</span></span>
<span data-ttu-id="454cf-184">Megerősítés kérése a művelet megkezdése előtt.</span><span class="sxs-lookup"><span data-stu-id="454cf-184">Prompts  for confirmation before starting the operation.</span></span>

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

### <span data-ttu-id="454cf-185">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="454cf-185">-WhatIf</span></span>
<span data-ttu-id="454cf-186">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="454cf-186">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="454cf-187">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="454cf-187">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="454cf-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="454cf-188">CommonParameters</span></span>
<span data-ttu-id="454cf-189">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="454cf-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="454cf-190">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="454cf-190">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="454cf-191">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="454cf-191">INPUTS</span></span>

### <span data-ttu-id="454cf-192">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="454cf-192">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="454cf-193">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="454cf-193">OUTPUTS</span></span>

### <span data-ttu-id="454cf-194">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="454cf-194">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="454cf-195">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="454cf-195">NOTES</span></span>

## <span data-ttu-id="454cf-196">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="454cf-196">RELATED LINKS</span></span>

[<span data-ttu-id="454cf-197">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="454cf-197">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="454cf-198">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="454cf-198">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="454cf-199">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="454cf-199">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)
