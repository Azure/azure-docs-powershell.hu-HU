---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: C71C486E-34EB-42B5-B38A-D85B7DAA2F74
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchPool.md
ms.openlocfilehash: 3a9534ea2fd0f1bcfc17f9eb5df63b25f7760f2f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497896"
---
# <span data-ttu-id="9db1a-101">New-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="9db1a-101">New-AzureBatchPool</span></span>

## <span data-ttu-id="9db1a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9db1a-102">SYNOPSIS</span></span>
<span data-ttu-id="9db1a-103">Gyűjtőt hoz létre a köteg szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="9db1a-103">Creates a pool in the Batch service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9db1a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9db1a-104">SYNTAX</span></span>

### <span data-ttu-id="9db1a-105">CloudServiceAndTargetDedicated (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9db1a-105">CloudServiceAndTargetDedicated (Default)</span></span>
```
New-AzureBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-ResizeTimeout <TimeSpan>] [-TargetDedicated <Int32>] [-MaxTasksPerComputeNode <Int32>]
 [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-CloudServiceConfiguration <PSCloudServiceConfiguration>] [-NetworkConfiguration <PSNetworkConfiguration>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9db1a-106">VirtualMachineAndTargetDedicated</span><span class="sxs-lookup"><span data-stu-id="9db1a-106">VirtualMachineAndTargetDedicated</span></span>
```
New-AzureBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-ResizeTimeout <TimeSpan>] [-TargetDedicated <Int32>] [-MaxTasksPerComputeNode <Int32>]
 [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-VirtualMachineConfiguration <PSVirtualMachineConfiguration>]
 [-NetworkConfiguration <PSNetworkConfiguration>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9db1a-107">CloudServiceAndAutoScale</span><span class="sxs-lookup"><span data-stu-id="9db1a-107">CloudServiceAndAutoScale</span></span>
```
New-AzureBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-AutoScaleEvaluationInterval <TimeSpan>] [-AutoScaleFormula <String>] [-MaxTasksPerComputeNode <Int32>]
 [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-CloudServiceConfiguration <PSCloudServiceConfiguration>] [-NetworkConfiguration <PSNetworkConfiguration>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9db1a-108">VirtualMachineAndAutoScale</span><span class="sxs-lookup"><span data-stu-id="9db1a-108">VirtualMachineAndAutoScale</span></span>
```
New-AzureBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-AutoScaleEvaluationInterval <TimeSpan>] [-AutoScaleFormula <String>] [-MaxTasksPerComputeNode <Int32>]
 [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-VirtualMachineConfiguration <PSVirtualMachineConfiguration>]
 [-NetworkConfiguration <PSNetworkConfiguration>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9db1a-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="9db1a-109">DESCRIPTION</span></span>
<span data-ttu-id="9db1a-110">A **New-AzureBatchPool** parancsmag létrehoz egy készletet az Azure kötegelt szolgáltatásban a *BatchContext* paraméterrel megadott fiók alapján.</span><span class="sxs-lookup"><span data-stu-id="9db1a-110">The **New-AzureBatchPool** cmdlet creates a pool in the Azure Batch service under the account specified by the *BatchContext* parameter.</span></span>

## <span data-ttu-id="9db1a-111">Példák</span><span class="sxs-lookup"><span data-stu-id="9db1a-111">EXAMPLES</span></span>

### <span data-ttu-id="9db1a-112">1. példa: új készlet létrehozása a TargetDedicated paraméterérték használatával</span><span class="sxs-lookup"><span data-stu-id="9db1a-112">Example 1: Create a new pool using the TargetDedicated parameter set</span></span>
```
PS C:\>New-AzureBatchPool -Id "MyPool" -VirtualMachineSize "Small" -OSFamily "4" -TargetOSVersion "*" -TargetDedicated 3 -BatchContext $Context
```

<span data-ttu-id="9db1a-113">Ezzel a paranccsal új készletet hoz létre a MyPool AZONOSÍTÓval az TargetDedicated paraméterrel.</span><span class="sxs-lookup"><span data-stu-id="9db1a-113">This command creates a new pool with ID MyPool using the TargetDedicated parameter set.</span></span>
<span data-ttu-id="9db1a-114">A cél kiosztása három csomópontból áll.</span><span class="sxs-lookup"><span data-stu-id="9db1a-114">The target allocation is three compute nodes.</span></span>
<span data-ttu-id="9db1a-115">A készlet úgy van konfigurálva, hogy a négy család legújabb verziójával ellátott kis virtuális gépeket használja.</span><span class="sxs-lookup"><span data-stu-id="9db1a-115">The pool is configured to use small virtual machines imaged with the latest operating system version of family four.</span></span>

### <span data-ttu-id="9db1a-116">2. példa: új készlet létrehozása az automéretarány paraméterérték használatával</span><span class="sxs-lookup"><span data-stu-id="9db1a-116">Example 2: Create a new pool using the AutoScale parameter set</span></span>
```
PS C:\>New-AzureBatchPool -Id "AutoScalePool" -VirtualMachineSize "Small" -OSFamily "4" -TargetOSVersion "*" -AutoScaleFormula '$TargetDedicated=2;' -BatchContext $Context
```

<span data-ttu-id="9db1a-117">Ez a parancs létrehoz egy új készletet, az azonosító AutoScalePool az automéretarány paraméterrel.</span><span class="sxs-lookup"><span data-stu-id="9db1a-117">This command creates a new pool with ID AutoScalePool using the AutoScale parameter set.</span></span>
<span data-ttu-id="9db1a-118">A készlet úgy van konfigurálva, hogy a négy család legújabb verziójával ellátott kis virtuális gépeket használja, valamint a számítási csomópontok kitűzött számát az autoscale képlet határozza meg.</span><span class="sxs-lookup"><span data-stu-id="9db1a-118">The pool is configured to use small virtual machines imaged with the latest operating system version of family four, and the target number of compute nodes are determined by the Autoscale formula.</span></span>

## <span data-ttu-id="9db1a-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9db1a-119">PARAMETERS</span></span>

### <span data-ttu-id="9db1a-120">-ApplicationPackageReferences</span><span class="sxs-lookup"><span data-stu-id="9db1a-120">-ApplicationPackageReferences</span></span>
```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSApplicationPackageReference[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9db1a-121">-AutoScaleEvaluationInterval</span><span class="sxs-lookup"><span data-stu-id="9db1a-121">-AutoScaleEvaluationInterval</span></span>
<span data-ttu-id="9db1a-122">Azt adja meg, hogy hány perc múlva teljen el a program, mielőtt a program automatikusan kiigazítja a készlet méretét az automatikus méretezés képlete szerint.</span><span class="sxs-lookup"><span data-stu-id="9db1a-122">Specifies the amount of time, in minutes, that elapses before the pool size is automatically adjusted according to the AutoScale formula.</span></span>
<span data-ttu-id="9db1a-123">Az alapértelmezett érték 15 perc, és a minimális érték 5 perc.</span><span class="sxs-lookup"><span data-stu-id="9db1a-123">The default value is 15 minutes, and the minimum value is 5 minutes.</span></span>

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

### <span data-ttu-id="9db1a-124">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="9db1a-124">-AutoScaleFormula</span></span>
<span data-ttu-id="9db1a-125">Megadja a készlet automatikus méretezésének képletét.</span><span class="sxs-lookup"><span data-stu-id="9db1a-125">Specifies the formula for automatically scaling the pool.</span></span>

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

### <span data-ttu-id="9db1a-126">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="9db1a-126">-BatchContext</span></span>
<span data-ttu-id="9db1a-127">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="9db1a-127">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="9db1a-128">Ha az előfizetéshez hozzáférési kulcsokat tartalmazó **BatchAccountContext** objektumot szeretne beolvasni, használja az Get-AzureRmBatchAccountKeys parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="9db1a-128">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="9db1a-129">-CertificateReferences</span><span class="sxs-lookup"><span data-stu-id="9db1a-129">-CertificateReferences</span></span>
<span data-ttu-id="9db1a-130">A készlethez társított tanúsítványokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="9db1a-130">Specifies certificates associated with the pool.</span></span>
<span data-ttu-id="9db1a-131">A köteg szolgáltatás telepíti a hivatkozott tanúsítványokat a készlet minden egyes számítási csomópontjára.</span><span class="sxs-lookup"><span data-stu-id="9db1a-131">The Batch service installs the referenced certificates on each compute node of the pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCertificateReference[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9db1a-132">-CloudServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="9db1a-132">-CloudServiceConfiguration</span></span>
<span data-ttu-id="9db1a-133">Az Azure Cloud Service platformon alapuló alkalmazáskészlet konfigurációs beállításait adja meg.</span><span class="sxs-lookup"><span data-stu-id="9db1a-133">Specifies configuration settings for a pool based on the Azure cloud service platform.</span></span>

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

### <span data-ttu-id="9db1a-134">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="9db1a-134">-DisplayName</span></span>
<span data-ttu-id="9db1a-135">A készlet megjelenítendő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9db1a-135">Specifies the display name of the pool.</span></span>

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

### <span data-ttu-id="9db1a-136">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="9db1a-136">-Id</span></span>
<span data-ttu-id="9db1a-137">A létrehozandó készlet AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="9db1a-137">Specifies the ID of the pool to create.</span></span>

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

### <span data-ttu-id="9db1a-138">-InterComputeNodeCommunicationEnabled</span><span class="sxs-lookup"><span data-stu-id="9db1a-138">-InterComputeNodeCommunicationEnabled</span></span>
<span data-ttu-id="9db1a-139">Jelzi, hogy ez a parancsmag a kijelölt számítási csomópontok közötti közvetlen kommunikációhoz a készletet állítja be.</span><span class="sxs-lookup"><span data-stu-id="9db1a-139">Indicates that this cmdlet sets up the pool for direct communication between dedicated compute nodes.</span></span>

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

### <span data-ttu-id="9db1a-140">-MaxTasksPerComputeNode</span><span class="sxs-lookup"><span data-stu-id="9db1a-140">-MaxTasksPerComputeNode</span></span>
<span data-ttu-id="9db1a-141">Az egyetlen számítási csomóponton futtatható feladatok maximális számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="9db1a-141">Specifies the maximum number of tasks that can run on a single compute node.</span></span>

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

### <span data-ttu-id="9db1a-142">-Metadata</span><span class="sxs-lookup"><span data-stu-id="9db1a-142">-Metadata</span></span>
<span data-ttu-id="9db1a-143">A metaadatokat adja meg kulcs/érték párokként az új készlethez való hozzáadáshoz.</span><span class="sxs-lookup"><span data-stu-id="9db1a-143">Specifies the metadata, as key/value pairs, to add to the new pool.</span></span>
<span data-ttu-id="9db1a-144">A kulcs a metaadat neve.</span><span class="sxs-lookup"><span data-stu-id="9db1a-144">The key is the metadata name.</span></span>
<span data-ttu-id="9db1a-145">Az érték a metaadat-érték.</span><span class="sxs-lookup"><span data-stu-id="9db1a-145">The value is the metadata value.</span></span>

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

### <span data-ttu-id="9db1a-146">-NetworkConfiguration</span><span class="sxs-lookup"><span data-stu-id="9db1a-146">-NetworkConfiguration</span></span>
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

### <span data-ttu-id="9db1a-147">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="9db1a-147">-ResizeTimeout</span></span>
<span data-ttu-id="9db1a-148">A számítási csomópontoknak a készlethez való hozzárendelésének időtúllépését adja meg.</span><span class="sxs-lookup"><span data-stu-id="9db1a-148">Specifies the time-out for allocating compute nodes to the pool.</span></span>

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

### <span data-ttu-id="9db1a-149">-StartTask</span><span class="sxs-lookup"><span data-stu-id="9db1a-149">-StartTask</span></span>
<span data-ttu-id="9db1a-150">A készlet kezdési tevékenységének specifikációját adja meg.</span><span class="sxs-lookup"><span data-stu-id="9db1a-150">Specifies the start task specification for the pool.</span></span>
<span data-ttu-id="9db1a-151">A kezdés tevékenység akkor fut, amikor egy számítási csomópont csatlakozik a készlethez, vagy ha a számítási csomópontot újraindítják vagy átvezetik.</span><span class="sxs-lookup"><span data-stu-id="9db1a-151">The start task is run when a compute node joins the pool, or when the compute node is rebooted or reimaged.</span></span>

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

### <span data-ttu-id="9db1a-152">-TargetDedicated</span><span class="sxs-lookup"><span data-stu-id="9db1a-152">-TargetDedicated</span></span>
<span data-ttu-id="9db1a-153">Megadja a készlethez kiosztani kívánt számítási csomópontok számát.</span><span class="sxs-lookup"><span data-stu-id="9db1a-153">Specifies the target number of compute nodes to allocate to the pool.</span></span>

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

### <span data-ttu-id="9db1a-154">-TaskSchedulingPolicy</span><span class="sxs-lookup"><span data-stu-id="9db1a-154">-TaskSchedulingPolicy</span></span>
<span data-ttu-id="9db1a-155">A tevékenység ütemezése házirendet adja meg, például a ComputeNodeFillType.</span><span class="sxs-lookup"><span data-stu-id="9db1a-155">Specifies the task scheduling policy, such as the ComputeNodeFillType.</span></span>

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

### <span data-ttu-id="9db1a-156">-VirtualMachineConfiguration</span><span class="sxs-lookup"><span data-stu-id="9db1a-156">-VirtualMachineConfiguration</span></span>
<span data-ttu-id="9db1a-157">A virtuális gépek infrastruktúrájában a készlet konfigurációs beállításait adja meg.</span><span class="sxs-lookup"><span data-stu-id="9db1a-157">Specifies configuration settings for a pool on the virtual machines infrastructure.</span></span>

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

### <span data-ttu-id="9db1a-158">-VirtualMachineSize</span><span class="sxs-lookup"><span data-stu-id="9db1a-158">-VirtualMachineSize</span></span>
<span data-ttu-id="9db1a-159">A készletben lévő virtuális gépek méretének meghatározása.</span><span class="sxs-lookup"><span data-stu-id="9db1a-159">Specifies the size of the virtual machines in the pool.</span></span>
<span data-ttu-id="9db1a-160">A virtuális gépek méretéről további információt a virtuális gépek méretei https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/ ( https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/) a Microsoft Azure webhelyén) című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="9db1a-160">For more information about virtual machine sizes, see Sizes for virtual machineshttps://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/ (https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/) in the Microsoft Azure site.</span></span>

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

### <span data-ttu-id="9db1a-161">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9db1a-161">-Confirm</span></span>
<span data-ttu-id="9db1a-162">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9db1a-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9db1a-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9db1a-163">-WhatIf</span></span>
<span data-ttu-id="9db1a-164">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9db1a-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9db1a-165">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9db1a-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9db1a-166">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9db1a-166">-DefaultProfile</span></span>
<span data-ttu-id="9db1a-167">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9db1a-167">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9db1a-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9db1a-168">CommonParameters</span></span>
<span data-ttu-id="9db1a-169">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9db1a-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9db1a-170">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9db1a-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9db1a-171">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9db1a-171">INPUTS</span></span>

### <span data-ttu-id="9db1a-172">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="9db1a-172">BatchAccountContext</span></span>
<span data-ttu-id="9db1a-173">A ' BatchContext ' paraméter az "BatchAccountContext" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="9db1a-173">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="9db1a-174">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9db1a-174">OUTPUTS</span></span>

## <span data-ttu-id="9db1a-175">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9db1a-175">NOTES</span></span>

## <span data-ttu-id="9db1a-176">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9db1a-176">RELATED LINKS</span></span>

[<span data-ttu-id="9db1a-177">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="9db1a-177">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="9db1a-178">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="9db1a-178">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="9db1a-179">Remove-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="9db1a-179">Remove-AzureBatchPool</span></span>](./Remove-AzureBatchPool.md)

[<span data-ttu-id="9db1a-180">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="9db1a-180">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


