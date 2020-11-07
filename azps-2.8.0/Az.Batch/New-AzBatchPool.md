---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: C71C486E-34EB-42B5-B38A-D85B7DAA2F74
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchPool.md
ms.openlocfilehash: 255db3680707af4e3658ce8a526cfa7b4a4d6f1d
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/13/2020
ms.locfileid: "93847806"
---
# <span data-ttu-id="58adf-101">New-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="58adf-101">New-AzBatchPool</span></span>

## <span data-ttu-id="58adf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="58adf-102">SYNOPSIS</span></span>
<span data-ttu-id="58adf-103">Gyűjtőt hoz létre a köteg szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="58adf-103">Creates a pool in the Batch service.</span></span>

## <span data-ttu-id="58adf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="58adf-104">SYNTAX</span></span>

### <span data-ttu-id="58adf-105">CloudServiceAndTargetDedicated (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="58adf-105">CloudServiceAndTargetDedicated (Default)</span></span>
```
New-AzBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>] [-ResizeTimeout <TimeSpan>]
 [-TargetDedicatedComputeNodes <Int32>] [-TargetLowPriorityComputeNodes <Int32>]
 [-MaxTasksPerComputeNode <Int32>] [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-ApplicationLicenses <System.Collections.Generic.List`1[System.String]>]
 [-CloudServiceConfiguration <PSCloudServiceConfiguration>] [-NetworkConfiguration <PSNetworkConfiguration>]
 [-UserAccount <PSUserAccount[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58adf-106">VirtualMachineAndTargetDedicated</span><span class="sxs-lookup"><span data-stu-id="58adf-106">VirtualMachineAndTargetDedicated</span></span>
```
New-AzBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>] [-ResizeTimeout <TimeSpan>]
 [-TargetDedicatedComputeNodes <Int32>] [-TargetLowPriorityComputeNodes <Int32>]
 [-MaxTasksPerComputeNode <Int32>] [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-ApplicationLicenses <System.Collections.Generic.List`1[System.String]>]
 [-VirtualMachineConfiguration <PSVirtualMachineConfiguration>]
 [-NetworkConfiguration <PSNetworkConfiguration>] [-UserAccount <PSUserAccount[]>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="58adf-107">CloudServiceAndAutoScale</span><span class="sxs-lookup"><span data-stu-id="58adf-107">CloudServiceAndAutoScale</span></span>
```
New-AzBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-AutoScaleEvaluationInterval <TimeSpan>] [-AutoScaleFormula <String>] [-MaxTasksPerComputeNode <Int32>]
 [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-ApplicationLicenses <System.Collections.Generic.List`1[System.String]>]
 [-CloudServiceConfiguration <PSCloudServiceConfiguration>] [-NetworkConfiguration <PSNetworkConfiguration>]
 [-UserAccount <PSUserAccount[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58adf-108">VirtualMachineAndAutoScale</span><span class="sxs-lookup"><span data-stu-id="58adf-108">VirtualMachineAndAutoScale</span></span>
```
New-AzBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-AutoScaleEvaluationInterval <TimeSpan>] [-AutoScaleFormula <String>] [-MaxTasksPerComputeNode <Int32>]
 [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-ApplicationLicenses <System.Collections.Generic.List`1[System.String]>]
 [-VirtualMachineConfiguration <PSVirtualMachineConfiguration>]
 [-NetworkConfiguration <PSNetworkConfiguration>] [-UserAccount <PSUserAccount[]>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="58adf-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="58adf-109">DESCRIPTION</span></span>
<span data-ttu-id="58adf-110">A **New-AzBatchPool** parancsmag létrehoz egy készletet az Azure kötegelt szolgáltatásban a *BatchContext* paraméterrel megadott fiók alapján.</span><span class="sxs-lookup"><span data-stu-id="58adf-110">The **New-AzBatchPool** cmdlet creates a pool in the Azure Batch service under the account specified by the *BatchContext* parameter.</span></span>

## <span data-ttu-id="58adf-111">Példák</span><span class="sxs-lookup"><span data-stu-id="58adf-111">EXAMPLES</span></span>

### <span data-ttu-id="58adf-112">Példa 1: új készlet létrehozása a TargetDedicated paraméterrel az CloudServiceConfiguration használatával</span><span class="sxs-lookup"><span data-stu-id="58adf-112">Example 1: Create a new pool using the TargetDedicated parameter set using CloudServiceConfiguration</span></span>
```
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSCloudServiceConfiguration" -ArgumentList @(4,"*")
PS C:\>New-AzBatchPool -Id "MyPool" -VirtualMachineSize "Small" -CloudServiceConfiguration $configuration  -TargetDedicatedComputeNodes 3 -BatchContext $Context
```

### <span data-ttu-id="58adf-113">2. példa: új készlet létrehozása a TargetDedicated paraméterrel az VirtualMachineConfiguration használatával</span><span class="sxs-lookup"><span data-stu-id="58adf-113">Example 2: Create a new pool using the TargetDedicated parameter set using VirtualMachineConfiguration</span></span>
```
PS C:\$imageReference = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSImageReference" -ArgumentList @("WindowsServer", "MicrosoftWindowsServer", "2016-Datacenter", "*")
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.VirtualMachineConfiguration" -ArgumentList @($imageReference, "batch.node.windows amd64")
PS C:\>New-AzBatchPool -Id "MyPool" -VirtualMachineSize "Small" -VirtualMachineConfiguration $configuration -TargetDedicatedComputeNodes 3 -BatchContext $Context
```

<span data-ttu-id="58adf-114">Ezzel a paranccsal új készletet hoz létre a MyPool AZONOSÍTÓval az TargetDedicated paraméterrel.</span><span class="sxs-lookup"><span data-stu-id="58adf-114">This command creates a new pool with ID MyPool using the TargetDedicated parameter set.</span></span>
<span data-ttu-id="58adf-115">A cél kiosztása három csomópontból áll.</span><span class="sxs-lookup"><span data-stu-id="58adf-115">The target allocation is three compute nodes.</span></span>
<span data-ttu-id="58adf-116">A készlet úgy van konfigurálva, hogy a négy család legújabb verziójával ellátott kis virtuális gépeket használja.</span><span class="sxs-lookup"><span data-stu-id="58adf-116">The pool is configured to use small virtual machines imaged with the latest operating system version of family four.</span></span>

### <span data-ttu-id="58adf-117">3. példa: új készlet létrehozása az automéretarány paraméterérték használatával</span><span class="sxs-lookup"><span data-stu-id="58adf-117">Example 3: Create a new pool using the AutoScale parameter set</span></span>
```
PS C:\$imageReference = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSImageReference" -ArgumentList @("WindowsServer", "MicrosoftWindowsServer", "2016-Datacenter", "*")
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.VirtualMachineConfiguration" -ArgumentList @($imageReference, "batch.node.windows amd64")
PS C:\>New-AzBatchPool -Id "AutoScalePool" -VirtualMachineSize "Small" -VirtualMachineConfiguration $configuration -AutoScaleFormula '$TargetDedicated=2;' -BatchContext $Context
```

<span data-ttu-id="58adf-118">Ez a parancs létrehoz egy új készletet, az azonosító AutoScalePool az automéretarány paraméterrel.</span><span class="sxs-lookup"><span data-stu-id="58adf-118">This command creates a new pool with ID AutoScalePool using the AutoScale parameter set.</span></span>
<span data-ttu-id="58adf-119">A készlet úgy van konfigurálva, hogy a négy család legújabb verziójával ellátott kis virtuális gépeket használja, valamint a számítási csomópontok kitűzött számát az autoscale képlet határozza meg.</span><span class="sxs-lookup"><span data-stu-id="58adf-119">The pool is configured to use small virtual machines imaged with the latest operating system version of family four, and the target number of compute nodes are determined by the Autoscale formula.</span></span>

### <span data-ttu-id="58adf-120">Példa 4: egy alhálózatban csomópontokat tartalmazó Pool létrehozása</span><span class="sxs-lookup"><span data-stu-id="58adf-120">Example 4: Create a pool with nodes in a subnet</span></span>
```
PS C:\$imageReference = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSImageReference" -ArgumentList @("WindowsServer", "MicrosoftWindowsServer", "2016-Datacenter", "*")
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.VirtualMachineConfiguration" -ArgumentList @($imageReference, "batch.node.windows amd64")
PS C:\>$networkConfig = New-Object Microsoft.Azure.Commands.Batch.Models.PSNetworkConfiguration
PS C:\>$networkConfig.SubnetId = "/subscriptions/{subscription}/resourceGroups/{group}/providers/{provider}/virtualNetworks/{network}/subnets/{subnet}"
PS C:\>New-AzBatchPool -Id "AutoScalePool" -VirtualMachineSize "Small" -VirtualMachineConfiguration $configuration -TargetDedicatedComputeNodes 3 -NetworkConfiguration $networkConfig -BatchContext $Context
```

### <span data-ttu-id="58adf-121">Példa 5: egyéni felhasználói fiókokat tartalmazó készlet létrehozása</span><span class="sxs-lookup"><span data-stu-id="58adf-121">Example 5: Create a pool with custom user accounts</span></span>
```
PS C:\$imageReference = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSImageReference" -ArgumentList @("WindowsServer", "MicrosoftWindowsServer", "2016-Datacenter", "*")
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.VirtualMachineConfiguration" -ArgumentList @($imageReference, "batch.node.windows amd64")
PS C:\>$userAccount = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserAccount -ArgumentList @("myaccount", "mypassword")
PS C:\>New-AzBatchPool -Id "AutoScalePool" -VirtualMachineSize "Small" -VirtualMachineConfiguration $configuration -TargetDedicatedComputeNodes 3 -UserAccount $userAccount
```

## <span data-ttu-id="58adf-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="58adf-122">PARAMETERS</span></span>

### <span data-ttu-id="58adf-123">-ApplicationLicenses</span><span class="sxs-lookup"><span data-stu-id="58adf-123">-ApplicationLicenses</span></span>
<span data-ttu-id="58adf-124">Az alkalmazásspecifikus licencek listája, amelyet a kötegelt szolgáltatás a készlet minden számítási csomópontjára elérhetővé tesz.</span><span class="sxs-lookup"><span data-stu-id="58adf-124">The list of application licenses the Batch service will make available on each compute node in the pool.</span></span>

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

### <span data-ttu-id="58adf-125">-ApplicationPackageReferences</span><span class="sxs-lookup"><span data-stu-id="58adf-125">-ApplicationPackageReferences</span></span>
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

### <span data-ttu-id="58adf-126">-AutoScaleEvaluationInterval</span><span class="sxs-lookup"><span data-stu-id="58adf-126">-AutoScaleEvaluationInterval</span></span>
<span data-ttu-id="58adf-127">Azt adja meg, hogy hány perc múlva teljen el a program, mielőtt a program automatikusan kiigazítja a készlet méretét az automatikus méretezés képlete szerint.</span><span class="sxs-lookup"><span data-stu-id="58adf-127">Specifies the amount of time, in minutes, that elapses before the pool size is automatically adjusted according to the AutoScale formula.</span></span>
<span data-ttu-id="58adf-128">Az alapértelmezett érték 15 perc, és a minimális érték 5 perc.</span><span class="sxs-lookup"><span data-stu-id="58adf-128">The default value is 15 minutes, and the minimum value is 5 minutes.</span></span>

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

### <span data-ttu-id="58adf-129">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="58adf-129">-AutoScaleFormula</span></span>
<span data-ttu-id="58adf-130">Megadja a készlet automatikus méretezésének képletét.</span><span class="sxs-lookup"><span data-stu-id="58adf-130">Specifies the formula for automatically scaling the pool.</span></span>

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

### <span data-ttu-id="58adf-131">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="58adf-131">-BatchContext</span></span>
<span data-ttu-id="58adf-132">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="58adf-132">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="58adf-133">Ha a Get-AzBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="58adf-133">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="58adf-134">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzBatchAccountKeys parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="58adf-134">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="58adf-135">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="58adf-135">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="58adf-136">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="58adf-136">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="58adf-137">-CertificateReferences</span><span class="sxs-lookup"><span data-stu-id="58adf-137">-CertificateReferences</span></span>
<span data-ttu-id="58adf-138">A készlethez társított tanúsítványokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="58adf-138">Specifies certificates associated with the pool.</span></span>
<span data-ttu-id="58adf-139">A köteg szolgáltatás telepíti a hivatkozott tanúsítványokat a készlet minden egyes számítási csomópontjára.</span><span class="sxs-lookup"><span data-stu-id="58adf-139">The Batch service installs the referenced certificates on each compute node of the pool.</span></span>

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

### <span data-ttu-id="58adf-140">-CloudServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="58adf-140">-CloudServiceConfiguration</span></span>
<span data-ttu-id="58adf-141">Az Azure Cloud Service platformon alapuló alkalmazáskészlet konfigurációs beállításait adja meg.</span><span class="sxs-lookup"><span data-stu-id="58adf-141">Specifies configuration settings for a pool based on the Azure cloud service platform.</span></span>

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

### <span data-ttu-id="58adf-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58adf-142">-DefaultProfile</span></span>
<span data-ttu-id="58adf-143">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="58adf-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58adf-144">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="58adf-144">-DisplayName</span></span>
<span data-ttu-id="58adf-145">A készlet megjelenítendő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="58adf-145">Specifies the display name of the pool.</span></span>

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

### <span data-ttu-id="58adf-146">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="58adf-146">-Id</span></span>
<span data-ttu-id="58adf-147">A létrehozandó készlet AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="58adf-147">Specifies the ID of the pool to create.</span></span>

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

### <span data-ttu-id="58adf-148">-InterComputeNodeCommunicationEnabled</span><span class="sxs-lookup"><span data-stu-id="58adf-148">-InterComputeNodeCommunicationEnabled</span></span>
<span data-ttu-id="58adf-149">Jelzi, hogy ez a parancsmag a kijelölt számítási csomópontok közötti közvetlen kommunikációhoz a készletet állítja be.</span><span class="sxs-lookup"><span data-stu-id="58adf-149">Indicates that this cmdlet sets up the pool for direct communication between dedicated compute nodes.</span></span>

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

### <span data-ttu-id="58adf-150">-MaxTasksPerComputeNode</span><span class="sxs-lookup"><span data-stu-id="58adf-150">-MaxTasksPerComputeNode</span></span>
<span data-ttu-id="58adf-151">Az egyetlen számítási csomóponton futtatható feladatok maximális számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="58adf-151">Specifies the maximum number of tasks that can run on a single compute node.</span></span>

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

### <span data-ttu-id="58adf-152">-Metadata</span><span class="sxs-lookup"><span data-stu-id="58adf-152">-Metadata</span></span>
<span data-ttu-id="58adf-153">A metaadatokat adja meg kulcs/érték párokként az új készlethez való hozzáadáshoz.</span><span class="sxs-lookup"><span data-stu-id="58adf-153">Specifies the metadata, as key/value pairs, to add to the new pool.</span></span>
<span data-ttu-id="58adf-154">A kulcs a metaadat neve.</span><span class="sxs-lookup"><span data-stu-id="58adf-154">The key is the metadata name.</span></span>
<span data-ttu-id="58adf-155">Az érték a metaadat-érték.</span><span class="sxs-lookup"><span data-stu-id="58adf-155">The value is the metadata value.</span></span>

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

### <span data-ttu-id="58adf-156">-NetworkConfiguration</span><span class="sxs-lookup"><span data-stu-id="58adf-156">-NetworkConfiguration</span></span>
<span data-ttu-id="58adf-157">A készlet hálózati konfigurációja.</span><span class="sxs-lookup"><span data-stu-id="58adf-157">The network configuration for the pool.</span></span>

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

### <span data-ttu-id="58adf-158">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="58adf-158">-ResizeTimeout</span></span>
<span data-ttu-id="58adf-159">A számítási csomópontoknak a készlethez való hozzárendelésének időtúllépését adja meg.</span><span class="sxs-lookup"><span data-stu-id="58adf-159">Specifies the time-out for allocating compute nodes to the pool.</span></span>

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

### <span data-ttu-id="58adf-160">-StartTask</span><span class="sxs-lookup"><span data-stu-id="58adf-160">-StartTask</span></span>
<span data-ttu-id="58adf-161">A készlet kezdési tevékenységének specifikációját adja meg.</span><span class="sxs-lookup"><span data-stu-id="58adf-161">Specifies the start task specification for the pool.</span></span>
<span data-ttu-id="58adf-162">A kezdés tevékenység akkor fut, amikor egy számítási csomópont csatlakozik a készlethez, vagy ha a számítási csomópontot újraindítják vagy átvezetik.</span><span class="sxs-lookup"><span data-stu-id="58adf-162">The start task is run when a compute node joins the pool, or when the compute node is rebooted or reimaged.</span></span>

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

### <span data-ttu-id="58adf-163">-TargetDedicatedComputeNodes</span><span class="sxs-lookup"><span data-stu-id="58adf-163">-TargetDedicatedComputeNodes</span></span>
<span data-ttu-id="58adf-164">A kijelölt számítási csomópontok cél számát adja meg a készletre való kiosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="58adf-164">Specifies the target number of dedicated compute nodes to allocate to the pool.</span></span>

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

### <span data-ttu-id="58adf-165">-TargetLowPriorityComputeNodes</span><span class="sxs-lookup"><span data-stu-id="58adf-165">-TargetLowPriorityComputeNodes</span></span>
<span data-ttu-id="58adf-166">A minimális prioritású számítási csomópontok cél számát adja meg a készletre való kiosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="58adf-166">Specifies the target number of low-priority compute nodes to allocate to the pool.</span></span>

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

### <span data-ttu-id="58adf-167">-TaskSchedulingPolicy</span><span class="sxs-lookup"><span data-stu-id="58adf-167">-TaskSchedulingPolicy</span></span>
<span data-ttu-id="58adf-168">A tevékenység ütemezése házirendet adja meg, például a ComputeNodeFillType.</span><span class="sxs-lookup"><span data-stu-id="58adf-168">Specifies the task scheduling policy, such as the ComputeNodeFillType.</span></span>

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

### <span data-ttu-id="58adf-169">-Felhasználóifiók</span><span class="sxs-lookup"><span data-stu-id="58adf-169">-UserAccount</span></span>
<span data-ttu-id="58adf-170">A készlet minden csomópontján létrehozandó felhasználói fiókok listája.</span><span class="sxs-lookup"><span data-stu-id="58adf-170">The list of user accounts to be created on each node in the pool.</span></span>

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

### <span data-ttu-id="58adf-171">-VirtualMachineConfiguration</span><span class="sxs-lookup"><span data-stu-id="58adf-171">-VirtualMachineConfiguration</span></span>
<span data-ttu-id="58adf-172">A virtuális gépek infrastruktúrájában a készlet konfigurációs beállításait adja meg.</span><span class="sxs-lookup"><span data-stu-id="58adf-172">Specifies configuration settings for a pool on the virtual machines infrastructure.</span></span>

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

### <span data-ttu-id="58adf-173">-VirtualMachineSize</span><span class="sxs-lookup"><span data-stu-id="58adf-173">-VirtualMachineSize</span></span>
<span data-ttu-id="58adf-174">A készletben lévő virtuális gépek méretének meghatározása.</span><span class="sxs-lookup"><span data-stu-id="58adf-174">Specifies the size of the virtual machines in the pool.</span></span>
<span data-ttu-id="58adf-175">A virtuális gépek méretéről további információt a virtuális gépek méretei https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/ ( https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/) a Microsoft Azure webhelyén) című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="58adf-175">For more information about virtual machine sizes, see Sizes for virtual machineshttps://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/ (https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/) in the Microsoft Azure site.</span></span>

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

### <span data-ttu-id="58adf-176">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="58adf-176">-Confirm</span></span>
<span data-ttu-id="58adf-177">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="58adf-177">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58adf-178">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58adf-178">-WhatIf</span></span>
<span data-ttu-id="58adf-179">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="58adf-179">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58adf-180">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="58adf-180">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58adf-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58adf-181">CommonParameters</span></span>
<span data-ttu-id="58adf-182">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="58adf-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58adf-183">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58adf-183">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58adf-184">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="58adf-184">INPUTS</span></span>

### <span data-ttu-id="58adf-185">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="58adf-185">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="58adf-186">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="58adf-186">OUTPUTS</span></span>

### <span data-ttu-id="58adf-187">System. Void</span><span class="sxs-lookup"><span data-stu-id="58adf-187">System.Void</span></span>

## <span data-ttu-id="58adf-188">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="58adf-188">NOTES</span></span>

## <span data-ttu-id="58adf-189">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="58adf-189">RELATED LINKS</span></span>

[<span data-ttu-id="58adf-190">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="58adf-190">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="58adf-191">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="58adf-191">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="58adf-192">Remove-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="58adf-192">Remove-AzBatchPool</span></span>](./Remove-AzBatchPool.md)

[<span data-ttu-id="58adf-193">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="58adf-193">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


