---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: C71C486E-34EB-42B5-B38A-D85B7DAA2F74
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurebatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchPool.md
ms.openlocfilehash: 54a5d6dc737bc0bd6a7f1d236ce855b2a08dca6a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505528"
---
# <span data-ttu-id="9cd98-101">New-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="9cd98-101">New-AzureBatchPool</span></span>

## <span data-ttu-id="9cd98-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9cd98-102">SYNOPSIS</span></span>
<span data-ttu-id="9cd98-103">Gyűjtőt hoz létre a köteg szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="9cd98-103">Creates a pool in the Batch service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9cd98-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9cd98-104">SYNTAX</span></span>

### <span data-ttu-id="9cd98-105">CloudServiceAndTargetDedicated (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9cd98-105">CloudServiceAndTargetDedicated (Default)</span></span>
```
New-AzureBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-ResizeTimeout <TimeSpan>] [-TargetDedicatedComputeNodes <Int32>] [-TargetLowPriorityComputeNodes <Int32>]
 [-MaxTasksPerComputeNode <Int32>] [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-ApplicationLicenses <System.Collections.Generic.List`1[System.String]>]
 [-CloudServiceConfiguration <PSCloudServiceConfiguration>] [-NetworkConfiguration <PSNetworkConfiguration>]
 [-UserAccount <PSUserAccount[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cd98-106">VirtualMachineAndTargetDedicated</span><span class="sxs-lookup"><span data-stu-id="9cd98-106">VirtualMachineAndTargetDedicated</span></span>
```
New-AzureBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-ResizeTimeout <TimeSpan>] [-TargetDedicatedComputeNodes <Int32>] [-TargetLowPriorityComputeNodes <Int32>]
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

### <span data-ttu-id="9cd98-107">CloudServiceAndAutoScale</span><span class="sxs-lookup"><span data-stu-id="9cd98-107">CloudServiceAndAutoScale</span></span>
```
New-AzureBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
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

### <span data-ttu-id="9cd98-108">VirtualMachineAndAutoScale</span><span class="sxs-lookup"><span data-stu-id="9cd98-108">VirtualMachineAndAutoScale</span></span>
```
New-AzureBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
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

## <span data-ttu-id="9cd98-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="9cd98-109">DESCRIPTION</span></span>
<span data-ttu-id="9cd98-110">A **New-AzureBatchPool** parancsmag létrehoz egy készletet az Azure kötegelt szolgáltatásban a *BatchContext* paraméterrel megadott fiók alapján.</span><span class="sxs-lookup"><span data-stu-id="9cd98-110">The **New-AzureBatchPool** cmdlet creates a pool in the Azure Batch service under the account specified by the *BatchContext* parameter.</span></span>

## <span data-ttu-id="9cd98-111">Példák</span><span class="sxs-lookup"><span data-stu-id="9cd98-111">EXAMPLES</span></span>

### <span data-ttu-id="9cd98-112">1. példa: új készlet létrehozása a TargetDedicated paraméterérték használatával</span><span class="sxs-lookup"><span data-stu-id="9cd98-112">Example 1: Create a new pool using the TargetDedicated parameter set</span></span>
```
PS C:\>New-AzureBatchPool -Id "MyPool" -VirtualMachineSize "Small" -OSFamily "4" -TargetOSVersion "*" -TargetDedicatedComputeNodes 3 -BatchContext $Context
```

<span data-ttu-id="9cd98-113">Ezzel a paranccsal új készletet hoz létre a MyPool AZONOSÍTÓval az TargetDedicated paraméterrel.</span><span class="sxs-lookup"><span data-stu-id="9cd98-113">This command creates a new pool with ID MyPool using the TargetDedicated parameter set.</span></span>
<span data-ttu-id="9cd98-114">A cél kiosztása három csomópontból áll.</span><span class="sxs-lookup"><span data-stu-id="9cd98-114">The target allocation is three compute nodes.</span></span>
<span data-ttu-id="9cd98-115">A készlet úgy van konfigurálva, hogy a négy család legújabb verziójával ellátott kis virtuális gépeket használja.</span><span class="sxs-lookup"><span data-stu-id="9cd98-115">The pool is configured to use small virtual machines imaged with the latest operating system version of family four.</span></span>

### <span data-ttu-id="9cd98-116">2. példa: új készlet létrehozása az automéretarány paraméterérték használatával</span><span class="sxs-lookup"><span data-stu-id="9cd98-116">Example 2: Create a new pool using the AutoScale parameter set</span></span>
```
PS C:\>New-AzureBatchPool -Id "AutoScalePool" -VirtualMachineSize "Small" -OSFamily "4" -TargetOSVersion "*" -AutoScaleFormula '$TargetDedicated=2;' -BatchContext $Context
```

<span data-ttu-id="9cd98-117">Ez a parancs létrehoz egy új készletet, az azonosító AutoScalePool az automéretarány paraméterrel.</span><span class="sxs-lookup"><span data-stu-id="9cd98-117">This command creates a new pool with ID AutoScalePool using the AutoScale parameter set.</span></span>
<span data-ttu-id="9cd98-118">A készlet úgy van konfigurálva, hogy a négy család legújabb verziójával ellátott kis virtuális gépeket használja, valamint a számítási csomópontok kitűzött számát az autoscale képlet határozza meg.</span><span class="sxs-lookup"><span data-stu-id="9cd98-118">The pool is configured to use small virtual machines imaged with the latest operating system version of family four, and the target number of compute nodes are determined by the Autoscale formula.</span></span>

### <span data-ttu-id="9cd98-119">3. példa: az alhálózatban csomópontokat tartalmazó Pool létrehozása</span><span class="sxs-lookup"><span data-stu-id="9cd98-119">Example 3: Create a pool with nodes in a subnet</span></span>
```
PS C:\>$networkConfig = New-Object Microsoft.Azure.Commands.Batch.Models.PSNetworkConfiguration
PS C:\>$networkConfig.SubnetId = "/subscriptions/{subscription}/resourceGroups/{group}/providers/{provider}/virtualNetworks/{network}/subnets/{subnet}"
PS C:\>New-AzureBatchPool -Id "AutoScalePool" -VirtualMachineSize "Small" -OSFamily "4" -TargetDedicatedComputeNodes 3 -NetworkConfiguration $networkConfig -BatchContext $Context
```

### <span data-ttu-id="9cd98-120">Példa 4: egyéni felhasználói fiókokat tartalmazó készlet létrehozása</span><span class="sxs-lookup"><span data-stu-id="9cd98-120">Example 4: Create a pool with custom user accounts</span></span>
```
PS C:\>$userAccount = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserAccount -ArgumentList @("myaccount", "mypassword")
PS C:\>New-AzureBatchPool -Id "AutoScalePool" -VirtualMachineSize "Small" -OSFamily "4" -TargetDedicatedComputeNodes 3 -UserAccount $userAccount
```

## <span data-ttu-id="9cd98-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9cd98-121">PARAMETERS</span></span>

### <span data-ttu-id="9cd98-122">-ApplicationLicenses</span><span class="sxs-lookup"><span data-stu-id="9cd98-122">-ApplicationLicenses</span></span>
<span data-ttu-id="9cd98-123">Az alkalmazásspecifikus licencek listája, amelyet a kötegelt szolgáltatás a készlet minden számítási csomópontjára elérhetővé tesz.</span><span class="sxs-lookup"><span data-stu-id="9cd98-123">The list of application licenses the Batch service will make available on each compute node in the pool.</span></span>

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

### <span data-ttu-id="9cd98-124">-ApplicationPackageReferences</span><span class="sxs-lookup"><span data-stu-id="9cd98-124">-ApplicationPackageReferences</span></span>
```yaml
Type: PSApplicationPackageReference[]
Parameter Sets: (All)
Aliases: ApplicationPackageReference

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cd98-125">-AutoScaleEvaluationInterval</span><span class="sxs-lookup"><span data-stu-id="9cd98-125">-AutoScaleEvaluationInterval</span></span>
<span data-ttu-id="9cd98-126">Azt adja meg, hogy hány perc múlva teljen el a program, mielőtt a program automatikusan kiigazítja a készlet méretét az automatikus méretezés képlete szerint.</span><span class="sxs-lookup"><span data-stu-id="9cd98-126">Specifies the amount of time, in minutes, that elapses before the pool size is automatically adjusted according to the AutoScale formula.</span></span>
<span data-ttu-id="9cd98-127">Az alapértelmezett érték 15 perc, és a minimális érték 5 perc.</span><span class="sxs-lookup"><span data-stu-id="9cd98-127">The default value is 15 minutes, and the minimum value is 5 minutes.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: CloudServiceAndAutoScale, VirtualMachineAndAutoScale
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cd98-128">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="9cd98-128">-AutoScaleFormula</span></span>
<span data-ttu-id="9cd98-129">Megadja a készlet automatikus méretezésének képletét.</span><span class="sxs-lookup"><span data-stu-id="9cd98-129">Specifies the formula for automatically scaling the pool.</span></span>

```yaml
Type: String
Parameter Sets: CloudServiceAndAutoScale, VirtualMachineAndAutoScale
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cd98-130">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="9cd98-130">-BatchContext</span></span>
<span data-ttu-id="9cd98-131">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="9cd98-131">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="9cd98-132">Ha a Get-AzureRmBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="9cd98-132">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="9cd98-133">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzureRmBatchAccountKeys parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="9cd98-133">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="9cd98-134">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="9cd98-134">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="9cd98-135">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="9cd98-135">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9cd98-136">-CertificateReferences</span><span class="sxs-lookup"><span data-stu-id="9cd98-136">-CertificateReferences</span></span>
<span data-ttu-id="9cd98-137">A készlethez társított tanúsítványokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="9cd98-137">Specifies certificates associated with the pool.</span></span>
<span data-ttu-id="9cd98-138">A köteg szolgáltatás telepíti a hivatkozott tanúsítványokat a készlet minden egyes számítási csomópontjára.</span><span class="sxs-lookup"><span data-stu-id="9cd98-138">The Batch service installs the referenced certificates on each compute node of the pool.</span></span>

```yaml
Type: PSCertificateReference[]
Parameter Sets: (All)
Aliases: CertificateReference

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cd98-139">-CloudServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="9cd98-139">-CloudServiceConfiguration</span></span>
<span data-ttu-id="9cd98-140">Az Azure Cloud Service platformon alapuló alkalmazáskészlet konfigurációs beállításait adja meg.</span><span class="sxs-lookup"><span data-stu-id="9cd98-140">Specifies configuration settings for a pool based on the Azure cloud service platform.</span></span>

```yaml
Type: PSCloudServiceConfiguration
Parameter Sets: CloudServiceAndTargetDedicated, CloudServiceAndAutoScale
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cd98-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cd98-141">-DefaultProfile</span></span>
<span data-ttu-id="9cd98-142">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9cd98-142">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cd98-143">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="9cd98-143">-DisplayName</span></span>
<span data-ttu-id="9cd98-144">A készlet megjelenítendő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9cd98-144">Specifies the display name of the pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cd98-145">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="9cd98-145">-Id</span></span>
<span data-ttu-id="9cd98-146">A létrehozandó készlet AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="9cd98-146">Specifies the ID of the pool to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cd98-147">-InterComputeNodeCommunicationEnabled</span><span class="sxs-lookup"><span data-stu-id="9cd98-147">-InterComputeNodeCommunicationEnabled</span></span>
<span data-ttu-id="9cd98-148">Jelzi, hogy ez a parancsmag a kijelölt számítási csomópontok közötti közvetlen kommunikációhoz a készletet állítja be.</span><span class="sxs-lookup"><span data-stu-id="9cd98-148">Indicates that this cmdlet sets up the pool for direct communication between dedicated compute nodes.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cd98-149">-MaxTasksPerComputeNode</span><span class="sxs-lookup"><span data-stu-id="9cd98-149">-MaxTasksPerComputeNode</span></span>
<span data-ttu-id="9cd98-150">Az egyetlen számítási csomóponton futtatható feladatok maximális számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="9cd98-150">Specifies the maximum number of tasks that can run on a single compute node.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cd98-151">-Metadata</span><span class="sxs-lookup"><span data-stu-id="9cd98-151">-Metadata</span></span>
<span data-ttu-id="9cd98-152">A metaadatokat adja meg kulcs/érték párokként az új készlethez való hozzáadáshoz.</span><span class="sxs-lookup"><span data-stu-id="9cd98-152">Specifies the metadata, as key/value pairs, to add to the new pool.</span></span>
<span data-ttu-id="9cd98-153">A kulcs a metaadat neve.</span><span class="sxs-lookup"><span data-stu-id="9cd98-153">The key is the metadata name.</span></span>
<span data-ttu-id="9cd98-154">Az érték a metaadat-érték.</span><span class="sxs-lookup"><span data-stu-id="9cd98-154">The value is the metadata value.</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cd98-155">-NetworkConfiguration</span><span class="sxs-lookup"><span data-stu-id="9cd98-155">-NetworkConfiguration</span></span>
<span data-ttu-id="9cd98-156">A készlet hálózati konfigurációja.</span><span class="sxs-lookup"><span data-stu-id="9cd98-156">The network configuration for the pool.</span></span>

```yaml
Type: PSNetworkConfiguration
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cd98-157">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="9cd98-157">-ResizeTimeout</span></span>
<span data-ttu-id="9cd98-158">A számítási csomópontoknak a készlethez való hozzárendelésének időtúllépését adja meg.</span><span class="sxs-lookup"><span data-stu-id="9cd98-158">Specifies the time-out for allocating compute nodes to the pool.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: CloudServiceAndTargetDedicated, VirtualMachineAndTargetDedicated
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cd98-159">-StartTask</span><span class="sxs-lookup"><span data-stu-id="9cd98-159">-StartTask</span></span>
<span data-ttu-id="9cd98-160">A készlet kezdési tevékenységének specifikációját adja meg.</span><span class="sxs-lookup"><span data-stu-id="9cd98-160">Specifies the start task specification for the pool.</span></span>
<span data-ttu-id="9cd98-161">A kezdés tevékenység akkor fut, amikor egy számítási csomópont csatlakozik a készlethez, vagy ha a számítási csomópontot újraindítják vagy átvezetik.</span><span class="sxs-lookup"><span data-stu-id="9cd98-161">The start task is run when a compute node joins the pool, or when the compute node is rebooted or reimaged.</span></span>

```yaml
Type: PSStartTask
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cd98-162">-TargetDedicatedComputeNodes</span><span class="sxs-lookup"><span data-stu-id="9cd98-162">-TargetDedicatedComputeNodes</span></span>
<span data-ttu-id="9cd98-163">A kijelölt számítási csomópontok cél számát adja meg a készletre való kiosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="9cd98-163">Specifies the target number of dedicated compute nodes to allocate to the pool.</span></span>

```yaml
Type: Int32
Parameter Sets: CloudServiceAndTargetDedicated, VirtualMachineAndTargetDedicated
Aliases: TargetDedicated

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cd98-164">-TargetLowPriorityComputeNodes</span><span class="sxs-lookup"><span data-stu-id="9cd98-164">-TargetLowPriorityComputeNodes</span></span>
<span data-ttu-id="9cd98-165">A minimális prioritású számítási csomópontok cél számát adja meg a készletre való kiosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="9cd98-165">Specifies the target number of low-priority compute nodes to allocate to the pool.</span></span>

```yaml
Type: Int32
Parameter Sets: CloudServiceAndTargetDedicated, VirtualMachineAndTargetDedicated
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cd98-166">-TaskSchedulingPolicy</span><span class="sxs-lookup"><span data-stu-id="9cd98-166">-TaskSchedulingPolicy</span></span>
<span data-ttu-id="9cd98-167">A tevékenység ütemezése házirendet adja meg, például a ComputeNodeFillType.</span><span class="sxs-lookup"><span data-stu-id="9cd98-167">Specifies the task scheduling policy, such as the ComputeNodeFillType.</span></span>

```yaml
Type: PSTaskSchedulingPolicy
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cd98-168">-Felhasználóifiók</span><span class="sxs-lookup"><span data-stu-id="9cd98-168">-UserAccount</span></span>
<span data-ttu-id="9cd98-169">A készlet minden csomópontján létrehozandó felhasználói fiókok listája.</span><span class="sxs-lookup"><span data-stu-id="9cd98-169">The list of user accounts to be created on each node in the pool.</span></span>

```yaml
Type: PSUserAccount[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cd98-170">-VirtualMachineConfiguration</span><span class="sxs-lookup"><span data-stu-id="9cd98-170">-VirtualMachineConfiguration</span></span>
<span data-ttu-id="9cd98-171">A virtuális gépek infrastruktúrájában a készlet konfigurációs beállításait adja meg.</span><span class="sxs-lookup"><span data-stu-id="9cd98-171">Specifies configuration settings for a pool on the virtual machines infrastructure.</span></span>

```yaml
Type: PSVirtualMachineConfiguration
Parameter Sets: VirtualMachineAndTargetDedicated, VirtualMachineAndAutoScale
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cd98-172">-VirtualMachineSize</span><span class="sxs-lookup"><span data-stu-id="9cd98-172">-VirtualMachineSize</span></span>
<span data-ttu-id="9cd98-173">A készletben lévő virtuális gépek méretének meghatározása.</span><span class="sxs-lookup"><span data-stu-id="9cd98-173">Specifies the size of the virtual machines in the pool.</span></span>
<span data-ttu-id="9cd98-174">A virtuális gépek méretéről további információt a virtuális gépek méretei https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/ ( https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/) a Microsoft Azure webhelyén) című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="9cd98-174">For more information about virtual machine sizes, see Sizes for virtual machineshttps://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/ (https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/) in the Microsoft Azure site.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cd98-175">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9cd98-175">-Confirm</span></span>
<span data-ttu-id="9cd98-176">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9cd98-176">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cd98-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9cd98-177">-WhatIf</span></span>
<span data-ttu-id="9cd98-178">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9cd98-178">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9cd98-179">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9cd98-179">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cd98-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cd98-180">CommonParameters</span></span>
<span data-ttu-id="9cd98-181">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9cd98-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cd98-182">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9cd98-182">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cd98-183">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9cd98-183">INPUTS</span></span>

### <span data-ttu-id="9cd98-184">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="9cd98-184">BatchAccountContext</span></span>
<span data-ttu-id="9cd98-185">A ' BatchContext ' paraméter az "BatchAccountContext" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="9cd98-185">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="9cd98-186">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9cd98-186">OUTPUTS</span></span>

## <span data-ttu-id="9cd98-187">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9cd98-187">NOTES</span></span>

## <span data-ttu-id="9cd98-188">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9cd98-188">RELATED LINKS</span></span>

[<span data-ttu-id="9cd98-189">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="9cd98-189">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="9cd98-190">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="9cd98-190">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="9cd98-191">Remove-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="9cd98-191">Remove-AzureBatchPool</span></span>](./Remove-AzureBatchPool.md)

[<span data-ttu-id="9cd98-192">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="9cd98-192">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


