---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: C71C486E-34EB-42B5-B38A-D85B7DAA2F74
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchPool.md
ms.openlocfilehash: 3c66893875dedd5e7298b9c6239c3da7ee86212e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182602"
---
# <span data-ttu-id="93f97-101">New-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="93f97-101">New-AzBatchPool</span></span>

## <span data-ttu-id="93f97-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="93f97-102">SYNOPSIS</span></span>
<span data-ttu-id="93f97-103">Gyűjtőt hoz létre a köteg szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="93f97-103">Creates a pool in the Batch service.</span></span>

## <span data-ttu-id="93f97-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="93f97-104">SYNTAX</span></span>

### <span data-ttu-id="93f97-105">CloudServiceAndTargetDedicated (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="93f97-105">CloudServiceAndTargetDedicated (Default)</span></span>
```
New-AzBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>] [-ResizeTimeout <TimeSpan>]
 [-TargetDedicatedComputeNodes <Int32>] [-TargetLowPriorityComputeNodes <Int32>]
 [-MaxTasksPerComputeNode <Int32>] [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-ApplicationLicenses <System.Collections.Generic.List`1[System.String]>]
 [-CloudServiceConfiguration <PSCloudServiceConfiguration>] [-NetworkConfiguration <PSNetworkConfiguration>]
 [-MountConfiguration <PSMountConfiguration[]>] [-UserAccount <PSUserAccount[]>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="93f97-106">VirtualMachineAndTargetDedicated</span><span class="sxs-lookup"><span data-stu-id="93f97-106">VirtualMachineAndTargetDedicated</span></span>
```
New-AzBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>] [-ResizeTimeout <TimeSpan>]
 [-TargetDedicatedComputeNodes <Int32>] [-TargetLowPriorityComputeNodes <Int32>]
 [-MaxTasksPerComputeNode <Int32>] [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-ApplicationLicenses <System.Collections.Generic.List`1[System.String]>]
 [-VirtualMachineConfiguration <PSVirtualMachineConfiguration>]
 [-NetworkConfiguration <PSNetworkConfiguration>] [-MountConfiguration <PSMountConfiguration[]>]
 [-UserAccount <PSUserAccount[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93f97-107">CloudServiceAndAutoScale</span><span class="sxs-lookup"><span data-stu-id="93f97-107">CloudServiceAndAutoScale</span></span>
```
New-AzBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-AutoScaleEvaluationInterval <TimeSpan>] [-AutoScaleFormula <String>] [-MaxTasksPerComputeNode <Int32>]
 [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-ApplicationLicenses <System.Collections.Generic.List`1[System.String]>]
 [-CloudServiceConfiguration <PSCloudServiceConfiguration>] [-NetworkConfiguration <PSNetworkConfiguration>]
 [-MountConfiguration <PSMountConfiguration[]>] [-UserAccount <PSUserAccount[]>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="93f97-108">VirtualMachineAndAutoScale</span><span class="sxs-lookup"><span data-stu-id="93f97-108">VirtualMachineAndAutoScale</span></span>
```
New-AzBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-AutoScaleEvaluationInterval <TimeSpan>] [-AutoScaleFormula <String>] [-MaxTasksPerComputeNode <Int32>]
 [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-ApplicationLicenses <System.Collections.Generic.List`1[System.String]>]
 [-VirtualMachineConfiguration <PSVirtualMachineConfiguration>]
 [-NetworkConfiguration <PSNetworkConfiguration>] [-MountConfiguration <PSMountConfiguration[]>]
 [-UserAccount <PSUserAccount[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93f97-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="93f97-109">DESCRIPTION</span></span>
<span data-ttu-id="93f97-110">A **New-AzBatchPool** parancsmag létrehoz egy készletet az Azure kötegelt szolgáltatásban a *BatchContext* paraméterrel megadott fiók alapján.</span><span class="sxs-lookup"><span data-stu-id="93f97-110">The **New-AzBatchPool** cmdlet creates a pool in the Azure Batch service under the account specified by the *BatchContext* parameter.</span></span>

## <span data-ttu-id="93f97-111">Példák</span><span class="sxs-lookup"><span data-stu-id="93f97-111">EXAMPLES</span></span>

### <span data-ttu-id="93f97-112">Példa 1: új készlet létrehozása a TargetDedicated paraméterrel az CloudServiceConfiguration használatával</span><span class="sxs-lookup"><span data-stu-id="93f97-112">Example 1: Create a new pool using the TargetDedicated parameter set using CloudServiceConfiguration</span></span>
```
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSCloudServiceConfiguration" -ArgumentList @(4,"*")
PS C:\>New-AzBatchPool -Id "MyPool" -VirtualMachineSize "STANDARD_D1_V2" -CloudServiceConfiguration $configuration  -TargetDedicatedComputeNodes 3 -BatchContext $Context
```

<span data-ttu-id="93f97-113">A medence úgy van konfigurálva, hogy a STANDARD_D1_V2 virtuális gépeket használja a négy család operációs rendszerének verziójával.</span><span class="sxs-lookup"><span data-stu-id="93f97-113">The pool is configured to use STANDARD_D1_V2 virtual machines with operating system version of family four.</span></span>

### <span data-ttu-id="93f97-114">2. példa: új készlet létrehozása a TargetDedicated paraméterrel az VirtualMachineConfiguration használatával</span><span class="sxs-lookup"><span data-stu-id="93f97-114">Example 2: Create a new pool using the TargetDedicated parameter set using VirtualMachineConfiguration</span></span>
```
PS C:\>$imageReference = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSImageReference" -ArgumentList @("WindowsServer", "MicrosoftWindowsServer", "2016-Datacenter", "*")
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSVirtualMachineConfiguration" -ArgumentList @($imageReference, "batch.node.windows amd64")
PS C:\>New-AzBatchPool -Id "MyPool" -VirtualMachineSize "STANDARD_D1_V2" -VirtualMachineConfiguration $configuration -TargetDedicatedComputeNodes 3 -BatchContext $Context
```

<span data-ttu-id="93f97-115">Ezzel a paranccsal új készletet hoz létre a MyPool AZONOSÍTÓval az TargetDedicated paraméterrel.</span><span class="sxs-lookup"><span data-stu-id="93f97-115">This command creates a new pool with ID MyPool using the TargetDedicated parameter set.</span></span>
<span data-ttu-id="93f97-116">A cél kiosztása három csomópontból áll.</span><span class="sxs-lookup"><span data-stu-id="93f97-116">The target allocation is three compute nodes.</span></span>
<span data-ttu-id="93f97-117">A készlet úgy van konfigurálva, hogy a Windows-2016-Datacenter operációs rendszerű virtuális gépeket STANDARD_D1_V2 használja.</span><span class="sxs-lookup"><span data-stu-id="93f97-117">The pool is configured to use STANDARD_D1_V2 virtual machines with the Windows-2016-Datacenter operating system image.</span></span>

### <span data-ttu-id="93f97-118">3. példa: új készlet létrehozása az automéretarány paraméterérték használatával</span><span class="sxs-lookup"><span data-stu-id="93f97-118">Example 3: Create a new pool using the AutoScale parameter set</span></span>
```
PS C:\>$imageReference = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSImageReference" -ArgumentList @("WindowsServer", "MicrosoftWindowsServer", "2016-Datacenter", "*")
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSVirtualMachineConfiguration" -ArgumentList @($imageReference, "batch.node.windows amd64")
PS C:\>New-AzBatchPool -Id "AutoScalePool" -VirtualMachineSize "STANDARD_D1_V2" -VirtualMachineConfiguration $configuration -AutoScaleFormula '$TargetDedicated=2;' -BatchContext $Context
```

<span data-ttu-id="93f97-119">Ez a parancs létrehoz egy új készletet, az azonosító AutoScalePool az automéretarány paraméterrel.</span><span class="sxs-lookup"><span data-stu-id="93f97-119">This command creates a new pool with ID AutoScalePool using the AutoScale parameter set.</span></span>
<span data-ttu-id="93f97-120">A készlet úgy van konfigurálva, hogy a Windows-2016-Datacenter operációs rendszerrel rendelkező virtuális gépeket STANDARD_D1_V2 használja, valamint a számítási csomópontok kitűzött számát az automéretarány képlet határozza meg.</span><span class="sxs-lookup"><span data-stu-id="93f97-120">The pool is configured to use STANDARD_D1_V2 virtual machines with the Windows-2016-Datacenter operating system image, and the target number of compute nodes are determined by the Autoscale formula.</span></span>

### <span data-ttu-id="93f97-121">Példa 4: egy alhálózatban csomópontokat tartalmazó Pool létrehozása</span><span class="sxs-lookup"><span data-stu-id="93f97-121">Example 4: Create a pool with nodes in a subnet</span></span>
```
PS C:\>$imageReference = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSImageReference" -ArgumentList @("WindowsServer", "MicrosoftWindowsServer", "2016-Datacenter", "*")
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSVirtualMachineConfiguration" -ArgumentList @($imageReference, "batch.node.windows amd64")
PS C:\>$networkConfig = New-Object Microsoft.Azure.Commands.Batch.Models.PSNetworkConfiguration
PS C:\>$networkConfig.SubnetId = "/subscriptions/{subscription}/resourceGroups/{group}/providers/{provider}/virtualNetworks/{network}/subnets/{subnet}"
PS C:\>New-AzBatchPool -Id "AutoScalePool" -VirtualMachineSize "STANDARD_D1_V2" -VirtualMachineConfiguration $configuration -TargetDedicatedComputeNodes 3 -NetworkConfiguration $networkConfig -BatchContext $Context
```

### <span data-ttu-id="93f97-122">Példa 5: egyéni felhasználói fiókokat tartalmazó készlet létrehozása</span><span class="sxs-lookup"><span data-stu-id="93f97-122">Example 5: Create a pool with custom user accounts</span></span>
```
PS C:\>$imageReference = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSImageReference" -ArgumentList @("WindowsServer", "MicrosoftWindowsServer", "2016-Datacenter", "*")
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSVirtualMachineConfiguration" -ArgumentList @($imageReference, "batch.node.windows amd64")
PS C:\>$userAccount = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserAccount -ArgumentList @("myaccount", "mypassword")
PS C:\>New-AzBatchPool -Id "AutoScalePool" -VirtualMachineSize "STANDARD_D1_V2" -VirtualMachineConfiguration $configuration -TargetDedicatedComputeNodes 3 -UserAccount $userAccount
```

## <span data-ttu-id="93f97-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="93f97-123">PARAMETERS</span></span>

### <span data-ttu-id="93f97-124">-ApplicationLicenses</span><span class="sxs-lookup"><span data-stu-id="93f97-124">-ApplicationLicenses</span></span>
<span data-ttu-id="93f97-125">Az alkalmazásspecifikus licencek listája, amelyet a kötegelt szolgáltatás a készlet minden számítási csomópontjára elérhetővé tesz.</span><span class="sxs-lookup"><span data-stu-id="93f97-125">The list of application licenses the Batch service will make available on each compute node in the pool.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: ApplicationLicense

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93f97-126">-ApplicationPackageReferences</span><span class="sxs-lookup"><span data-stu-id="93f97-126">-ApplicationPackageReferences</span></span>
```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSApplicationPackageReference[]
Parameter Sets: (All)
Aliases: ApplicationPackageReference

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93f97-127">-AutoScaleEvaluationInterval</span><span class="sxs-lookup"><span data-stu-id="93f97-127">-AutoScaleEvaluationInterval</span></span>
<span data-ttu-id="93f97-128">Azt adja meg, hogy hány perc múlva teljen el a program, mielőtt a program automatikusan kiigazítja a készlet méretét az automatikus méretezés képlete szerint.</span><span class="sxs-lookup"><span data-stu-id="93f97-128">Specifies the amount of time, in minutes, that elapses before the pool size is automatically adjusted according to the AutoScale formula.</span></span>
<span data-ttu-id="93f97-129">Az alapértelmezett érték 15 perc, és a minimális érték 5 perc.</span><span class="sxs-lookup"><span data-stu-id="93f97-129">The default value is 15 minutes, and the minimum value is 5 minutes.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: CloudServiceAndAutoScale, VirtualMachineAndAutoScale
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93f97-130">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="93f97-130">-AutoScaleFormula</span></span>
<span data-ttu-id="93f97-131">Megadja a készlet automatikus méretezésének képletét.</span><span class="sxs-lookup"><span data-stu-id="93f97-131">Specifies the formula for automatically scaling the pool.</span></span>

```yaml
Type: System.String
Parameter Sets: CloudServiceAndAutoScale, VirtualMachineAndAutoScale
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93f97-132">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="93f97-132">-BatchContext</span></span>
<span data-ttu-id="93f97-133">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="93f97-133">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="93f97-134">Ha a Get-AzBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="93f97-134">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="93f97-135">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzBatchAccountKey parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="93f97-135">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="93f97-136">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="93f97-136">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="93f97-137">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="93f97-137">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="93f97-138">-CertificateReferences</span><span class="sxs-lookup"><span data-stu-id="93f97-138">-CertificateReferences</span></span>
<span data-ttu-id="93f97-139">A készlethez társított tanúsítványokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="93f97-139">Specifies certificates associated with the pool.</span></span>
<span data-ttu-id="93f97-140">A köteg szolgáltatás telepíti a hivatkozott tanúsítványokat a készlet minden egyes számítási csomópontjára.</span><span class="sxs-lookup"><span data-stu-id="93f97-140">The Batch service installs the referenced certificates on each compute node of the pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCertificateReference[]
Parameter Sets: (All)
Aliases: CertificateReference

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93f97-141">-CloudServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="93f97-141">-CloudServiceConfiguration</span></span>
<span data-ttu-id="93f97-142">Az Azure Cloud Service platformon alapuló alkalmazáskészlet konfigurációs beállításait adja meg.</span><span class="sxs-lookup"><span data-stu-id="93f97-142">Specifies configuration settings for a pool based on the Azure cloud service platform.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudServiceConfiguration
Parameter Sets: CloudServiceAndTargetDedicated, CloudServiceAndAutoScale
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93f97-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93f97-143">-DefaultProfile</span></span>
<span data-ttu-id="93f97-144">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="93f97-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="93f97-145">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="93f97-145">-DisplayName</span></span>
<span data-ttu-id="93f97-146">A készlet megjelenítendő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="93f97-146">Specifies the display name of the pool.</span></span>

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

### <span data-ttu-id="93f97-147">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="93f97-147">-Id</span></span>
<span data-ttu-id="93f97-148">A létrehozandó készlet AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="93f97-148">Specifies the ID of the pool to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93f97-149">-InterComputeNodeCommunicationEnabled</span><span class="sxs-lookup"><span data-stu-id="93f97-149">-InterComputeNodeCommunicationEnabled</span></span>
<span data-ttu-id="93f97-150">Jelzi, hogy ez a parancsmag a kijelölt számítási csomópontok közötti közvetlen kommunikációhoz a készletet állítja be.</span><span class="sxs-lookup"><span data-stu-id="93f97-150">Indicates that this cmdlet sets up the pool for direct communication between dedicated compute nodes.</span></span>

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

### <span data-ttu-id="93f97-151">-MaxTasksPerComputeNode</span><span class="sxs-lookup"><span data-stu-id="93f97-151">-MaxTasksPerComputeNode</span></span>
<span data-ttu-id="93f97-152">Az egyetlen számítási csomóponton futtatható feladatok maximális számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="93f97-152">Specifies the maximum number of tasks that can run on a single compute node.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93f97-153">-Metadata</span><span class="sxs-lookup"><span data-stu-id="93f97-153">-Metadata</span></span>
<span data-ttu-id="93f97-154">A metaadatokat adja meg kulcs/érték párokként az új készlethez való hozzáadáshoz.</span><span class="sxs-lookup"><span data-stu-id="93f97-154">Specifies the metadata, as key/value pairs, to add to the new pool.</span></span>
<span data-ttu-id="93f97-155">A kulcs a metaadat neve.</span><span class="sxs-lookup"><span data-stu-id="93f97-155">The key is the metadata name.</span></span>
<span data-ttu-id="93f97-156">Az érték a metaadat-érték.</span><span class="sxs-lookup"><span data-stu-id="93f97-156">The value is the metadata value.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93f97-157">-MountConfiguration</span><span class="sxs-lookup"><span data-stu-id="93f97-157">-MountConfiguration</span></span>
<span data-ttu-id="93f97-158">A készlet minden csomópontján a csatlakoztatni kívánt fájlrendszerek listája.</span><span class="sxs-lookup"><span data-stu-id="93f97-158">A list of file systems to mount on each node in the pool.</span></span> <span data-ttu-id="93f97-159">Ez a funkció támogatja az Azure-fájlokat, az NFS-t, a CIFS/SMB-t és a Blobfuse.</span><span class="sxs-lookup"><span data-stu-id="93f97-159">This supports Azure Files, NFS, CIFS/SMB, and Blobfuse.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSMountConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93f97-160">-NetworkConfiguration</span><span class="sxs-lookup"><span data-stu-id="93f97-160">-NetworkConfiguration</span></span>
<span data-ttu-id="93f97-161">A készlet hálózati konfigurációja.</span><span class="sxs-lookup"><span data-stu-id="93f97-161">The network configuration for the pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSNetworkConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93f97-162">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="93f97-162">-ResizeTimeout</span></span>
<span data-ttu-id="93f97-163">A számítási csomópontoknak a készlethez való hozzárendelésének időtúllépését adja meg.</span><span class="sxs-lookup"><span data-stu-id="93f97-163">Specifies the time-out for allocating compute nodes to the pool.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: CloudServiceAndTargetDedicated, VirtualMachineAndTargetDedicated
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93f97-164">-StartTask</span><span class="sxs-lookup"><span data-stu-id="93f97-164">-StartTask</span></span>
<span data-ttu-id="93f97-165">A készlet kezdési tevékenységének specifikációját adja meg.</span><span class="sxs-lookup"><span data-stu-id="93f97-165">Specifies the start task specification for the pool.</span></span>
<span data-ttu-id="93f97-166">A kezdés tevékenység akkor fut, amikor egy számítási csomópont csatlakozik a készlethez, vagy ha a számítási csomópontot újraindítják vagy átvezetik.</span><span class="sxs-lookup"><span data-stu-id="93f97-166">The start task is run when a compute node joins the pool, or when the compute node is rebooted or reimaged.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSStartTask
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93f97-167">-TargetDedicatedComputeNodes</span><span class="sxs-lookup"><span data-stu-id="93f97-167">-TargetDedicatedComputeNodes</span></span>
<span data-ttu-id="93f97-168">A kijelölt számítási csomópontok cél számát adja meg a készletre való kiosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="93f97-168">Specifies the target number of dedicated compute nodes to allocate to the pool.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: CloudServiceAndTargetDedicated, VirtualMachineAndTargetDedicated
Aliases: TargetDedicated

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93f97-169">-TargetLowPriorityComputeNodes</span><span class="sxs-lookup"><span data-stu-id="93f97-169">-TargetLowPriorityComputeNodes</span></span>
<span data-ttu-id="93f97-170">A minimális prioritású számítási csomópontok cél számát adja meg a készletre való kiosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="93f97-170">Specifies the target number of low-priority compute nodes to allocate to the pool.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: CloudServiceAndTargetDedicated, VirtualMachineAndTargetDedicated
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93f97-171">-TaskSchedulingPolicy</span><span class="sxs-lookup"><span data-stu-id="93f97-171">-TaskSchedulingPolicy</span></span>
<span data-ttu-id="93f97-172">A tevékenység ütemezése házirendet adja meg, például a ComputeNodeFillType.</span><span class="sxs-lookup"><span data-stu-id="93f97-172">Specifies the task scheduling policy, such as the ComputeNodeFillType.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSTaskSchedulingPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93f97-173">-Felhasználóifiók</span><span class="sxs-lookup"><span data-stu-id="93f97-173">-UserAccount</span></span>
<span data-ttu-id="93f97-174">A készlet minden csomópontján létrehozandó felhasználói fiókok listája.</span><span class="sxs-lookup"><span data-stu-id="93f97-174">The list of user accounts to be created on each node in the pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSUserAccount[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93f97-175">-VirtualMachineConfiguration</span><span class="sxs-lookup"><span data-stu-id="93f97-175">-VirtualMachineConfiguration</span></span>
<span data-ttu-id="93f97-176">A virtuális gépek infrastruktúrájában a készlet konfigurációs beállításait adja meg.</span><span class="sxs-lookup"><span data-stu-id="93f97-176">Specifies configuration settings for a pool on the virtual machines infrastructure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSVirtualMachineConfiguration
Parameter Sets: VirtualMachineAndTargetDedicated, VirtualMachineAndAutoScale
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93f97-177">-VirtualMachineSize</span><span class="sxs-lookup"><span data-stu-id="93f97-177">-VirtualMachineSize</span></span>
<span data-ttu-id="93f97-178">A készletben lévő virtuális gépek méretének meghatározása.</span><span class="sxs-lookup"><span data-stu-id="93f97-178">Specifies the size of the virtual machines in the pool.</span></span>
<span data-ttu-id="93f97-179">A virtuális gépek méretéről további információt a virtuális gépek méretei https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/ ( https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/) a Microsoft Azure webhelyén) című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="93f97-179">For more information about virtual machine sizes, see Sizes for virtual machineshttps://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/ (https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/) in the Microsoft Azure site.</span></span>

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

### <span data-ttu-id="93f97-180">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="93f97-180">-Confirm</span></span>
<span data-ttu-id="93f97-181">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="93f97-181">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93f97-182">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93f97-182">-WhatIf</span></span>
<span data-ttu-id="93f97-183">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="93f97-183">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93f97-184">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="93f97-184">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93f97-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93f97-185">CommonParameters</span></span>
<span data-ttu-id="93f97-186">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="93f97-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93f97-187">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="93f97-187">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93f97-188">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="93f97-188">INPUTS</span></span>

### <span data-ttu-id="93f97-189">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="93f97-189">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="93f97-190">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="93f97-190">OUTPUTS</span></span>

### <span data-ttu-id="93f97-191">System. Void</span><span class="sxs-lookup"><span data-stu-id="93f97-191">System.Void</span></span>

## <span data-ttu-id="93f97-192">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="93f97-192">NOTES</span></span>

## <span data-ttu-id="93f97-193">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="93f97-193">RELATED LINKS</span></span>

[<span data-ttu-id="93f97-194">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="93f97-194">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="93f97-195">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="93f97-195">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="93f97-196">Remove-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="93f97-196">Remove-AzBatchPool</span></span>](./Remove-AzBatchPool.md)

[<span data-ttu-id="93f97-197">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="93f97-197">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
