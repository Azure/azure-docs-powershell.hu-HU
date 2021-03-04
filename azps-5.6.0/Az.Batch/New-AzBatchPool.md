---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: C71C486E-34EB-42B5-B38A-D85B7DAA2F74
online version: https://docs.microsoft.com/powershell/module/az.batch/new-azbatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchPool.md
ms.openlocfilehash: 7fef035eda89d68d757658a512ca00369b69694a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939713"
---
# <span data-ttu-id="d21a7-101">New-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="d21a7-101">New-AzBatchPool</span></span>

## <span data-ttu-id="d21a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d21a7-102">SYNOPSIS</span></span>
<span data-ttu-id="d21a7-103">Létrehoz egy készletet a Batch szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="d21a7-103">Creates a pool in the Batch service.</span></span>

## <span data-ttu-id="d21a7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d21a7-104">SYNTAX</span></span>

### <span data-ttu-id="d21a7-105">CloudServiceAndTargetDedicated (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d21a7-105">CloudServiceAndTargetDedicated (Default)</span></span>
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

### <span data-ttu-id="d21a7-106">VirtualMachineAndTargetDedicated</span><span class="sxs-lookup"><span data-stu-id="d21a7-106">VirtualMachineAndTargetDedicated</span></span>
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

### <span data-ttu-id="d21a7-107">CloudServiceAndAutoScale</span><span class="sxs-lookup"><span data-stu-id="d21a7-107">CloudServiceAndAutoScale</span></span>
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

### <span data-ttu-id="d21a7-108">VirtualMachineAndAutoScale</span><span class="sxs-lookup"><span data-stu-id="d21a7-108">VirtualMachineAndAutoScale</span></span>
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

## <span data-ttu-id="d21a7-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d21a7-109">DESCRIPTION</span></span>
<span data-ttu-id="d21a7-110">A **New-AzBatchPool** parancsmag létrehoz egy készletet az Azure Batch szolgáltatásban a *BatchContext* paraméterrel megadott fiók alatt.</span><span class="sxs-lookup"><span data-stu-id="d21a7-110">The **New-AzBatchPool** cmdlet creates a pool in the Azure Batch service under the account specified by the *BatchContext* parameter.</span></span>

## <span data-ttu-id="d21a7-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d21a7-111">EXAMPLES</span></span>

### <span data-ttu-id="d21a7-112">1. példa: Új készlet létrehozása a TargetDedicated paraméterkészlet használatával a CloudServiceConfiguration segítségével</span><span class="sxs-lookup"><span data-stu-id="d21a7-112">Example 1: Create a new pool using the TargetDedicated parameter set using CloudServiceConfiguration</span></span>
```
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSCloudServiceConfiguration" -ArgumentList @(4,"*")
PS C:\>New-AzBatchPool -Id "MyPool" -VirtualMachineSize "STANDARD_D1_V2" -CloudServiceConfiguration $configuration  -TargetDedicatedComputeNodes 3 -BatchContext $Context
```

<span data-ttu-id="d21a7-113">A készlet úgy van konfigurálva, hogy STANDARD_D1_V2 virtuális gépeket használjon az operációs rendszer négyes verziójával.</span><span class="sxs-lookup"><span data-stu-id="d21a7-113">The pool is configured to use STANDARD_D1_V2 virtual machines with operating system version of family four.</span></span>

### <span data-ttu-id="d21a7-114">2. példa: Új készlet létrehozása a TargetDedicated paraméterkészlet használatával VirtualMachineConfiguration használatával</span><span class="sxs-lookup"><span data-stu-id="d21a7-114">Example 2: Create a new pool using the TargetDedicated parameter set using VirtualMachineConfiguration</span></span>
```
PS C:\>$imageReference = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSImageReference" -ArgumentList @("WindowsServer", "MicrosoftWindowsServer", "2016-Datacenter", "*")
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSVirtualMachineConfiguration" -ArgumentList @($imageReference, "batch.node.windows amd64")
PS C:\>New-AzBatchPool -Id "MyPool" -VirtualMachineSize "STANDARD_D1_V2" -VirtualMachineConfiguration $configuration -TargetDedicatedComputeNodes 3 -BatchContext $Context
```

<span data-ttu-id="d21a7-115">Ez a parancs létrehoz egy új készletet a MyPool azonosítóval a TargetDedicated paraméterkészlet használatával.</span><span class="sxs-lookup"><span data-stu-id="d21a7-115">This command creates a new pool with ID MyPool using the TargetDedicated parameter set.</span></span>
<span data-ttu-id="d21a7-116">A célfoglalás három számítási csomópont.</span><span class="sxs-lookup"><span data-stu-id="d21a7-116">The target allocation is three compute nodes.</span></span>
<span data-ttu-id="d21a7-117">A készlet úgy van konfigurálva, hogy STANDARD_D1_V2 virtuális gépeket használjon a Windows-2016-Datacenter operációs rendszerének képével.</span><span class="sxs-lookup"><span data-stu-id="d21a7-117">The pool is configured to use STANDARD_D1_V2 virtual machines with the Windows-2016-Datacenter operating system image.</span></span>

### <span data-ttu-id="d21a7-118">3. példa: Új készlet létrehozása az Automatikus méretezés paraméterkészlet használatával</span><span class="sxs-lookup"><span data-stu-id="d21a7-118">Example 3: Create a new pool using the AutoScale parameter set</span></span>
```
PS C:\>$imageReference = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSImageReference" -ArgumentList @("WindowsServer", "MicrosoftWindowsServer", "2016-Datacenter", "*")
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSVirtualMachineConfiguration" -ArgumentList @($imageReference, "batch.node.windows amd64")
PS C:\>New-AzBatchPool -Id "AutoScalePool" -VirtualMachineSize "STANDARD_D1_V2" -VirtualMachineConfiguration $configuration -AutoScaleFormula '$TargetDedicated=2;' -BatchContext $Context
```

<span data-ttu-id="d21a7-119">Ez a parancs létrehoz egy új készletet az Automatikus méretezési várólista azonosítóval, az Automatikus méretezés paraméterkészlet használatával.</span><span class="sxs-lookup"><span data-stu-id="d21a7-119">This command creates a new pool with ID AutoScalePool using the AutoScale parameter set.</span></span>
<span data-ttu-id="d21a7-120">A készlet úgy van konfigurálva, hogy virtuális gépeket használjon STANDARD_D1_V2 Windows-2016-Datacenter operációs rendszer képével, és a számítási csomópontok célszámát az automatikus skálázási képlet határozza meg.</span><span class="sxs-lookup"><span data-stu-id="d21a7-120">The pool is configured to use STANDARD_D1_V2 virtual machines with the Windows-2016-Datacenter operating system image, and the target number of compute nodes are determined by the Autoscale formula.</span></span>

### <span data-ttu-id="d21a7-121">4. példa: Alhálózat csomópontjaival létrehozott készlet</span><span class="sxs-lookup"><span data-stu-id="d21a7-121">Example 4: Create a pool with nodes in a subnet</span></span>
```
PS C:\>$imageReference = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSImageReference" -ArgumentList @("WindowsServer", "MicrosoftWindowsServer", "2016-Datacenter", "*")
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSVirtualMachineConfiguration" -ArgumentList @($imageReference, "batch.node.windows amd64")
PS C:\>$networkConfig = New-Object Microsoft.Azure.Commands.Batch.Models.PSNetworkConfiguration
PS C:\>$networkConfig.SubnetId = "/subscriptions/{subscription}/resourceGroups/{group}/providers/{provider}/virtualNetworks/{network}/subnets/{subnet}"
PS C:\>New-AzBatchPool -Id "AutoScalePool" -VirtualMachineSize "STANDARD_D1_V2" -VirtualMachineConfiguration $configuration -TargetDedicatedComputeNodes 3 -NetworkConfiguration $networkConfig -BatchContext $Context
```

### <span data-ttu-id="d21a7-122">5. példa: Egyéni felhasználói fiókokat használó készlet létrehozása</span><span class="sxs-lookup"><span data-stu-id="d21a7-122">Example 5: Create a pool with custom user accounts</span></span>
```
PS C:\>$imageReference = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSImageReference" -ArgumentList @("WindowsServer", "MicrosoftWindowsServer", "2016-Datacenter", "*")
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSVirtualMachineConfiguration" -ArgumentList @($imageReference, "batch.node.windows amd64")
PS C:\>$userAccount = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserAccount -ArgumentList @("myaccount", "mypassword")
PS C:\>New-AzBatchPool -Id "AutoScalePool" -VirtualMachineSize "STANDARD_D1_V2" -VirtualMachineConfiguration $configuration -TargetDedicatedComputeNodes 3 -UserAccount $userAccount
```

## <span data-ttu-id="d21a7-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d21a7-123">PARAMETERS</span></span>

### <span data-ttu-id="d21a7-124">-ApplicationLicenses</span><span class="sxs-lookup"><span data-stu-id="d21a7-124">-ApplicationLicenses</span></span>
<span data-ttu-id="d21a7-125">A Batch szolgáltatás által elérhetővé tenni szükséges alkalmazáslicencek listája a készlet minden egyes számítási csomópontján elérhetővé válik.</span><span class="sxs-lookup"><span data-stu-id="d21a7-125">The list of application licenses the Batch service will make available on each compute node in the pool.</span></span>

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

### <span data-ttu-id="d21a7-126">-ApplicationPackageReferences</span><span class="sxs-lookup"><span data-stu-id="d21a7-126">-ApplicationPackageReferences</span></span>
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

### <span data-ttu-id="d21a7-127">-AutoScaleEvaluationInterval</span><span class="sxs-lookup"><span data-stu-id="d21a7-127">-AutoScaleEvaluationInterval</span></span>
<span data-ttu-id="d21a7-128">Az automatikus méretezési képletnek megfelelően a készlet méretének automatikus beállítása előtt eltelt időt adja meg percben.</span><span class="sxs-lookup"><span data-stu-id="d21a7-128">Specifies the amount of time, in minutes, that elapses before the pool size is automatically adjusted according to the AutoScale formula.</span></span>
<span data-ttu-id="d21a7-129">Az alapértelmezett érték 15 perc, a minimális érték pedig 5 perc.</span><span class="sxs-lookup"><span data-stu-id="d21a7-129">The default value is 15 minutes, and the minimum value is 5 minutes.</span></span>

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

### <span data-ttu-id="d21a7-130">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="d21a7-130">-AutoScaleFormula</span></span>
<span data-ttu-id="d21a7-131">A készlet automatikus méretezésének képletét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d21a7-131">Specifies the formula for automatically scaling the pool.</span></span>

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

### <span data-ttu-id="d21a7-132">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="d21a7-132">-BatchContext</span></span>
<span data-ttu-id="d21a7-133">Azt a **BatchAccountContext példányt** adja meg, amely a parancsmagot használja a Batch szolgáltatáshoz való interakcióhoz.</span><span class="sxs-lookup"><span data-stu-id="d21a7-133">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="d21a7-134">Ha a Get-AzBatchAccount parancsmaggal szerezze be a BatchAccountContext parancsmagot, akkor a Batch szolgáltatás használata során az Azure Active Directory-hitelesítést fogja használni a rendszer.</span><span class="sxs-lookup"><span data-stu-id="d21a7-134">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="d21a7-135">Ha ehelyett megosztott kulcsú hitelesítést használ, a Get-AzBatchAccountKey parancsmaggal töltse le a BatchAccountContext objektumot a hozzáférési kulcsokkal.</span><span class="sxs-lookup"><span data-stu-id="d21a7-135">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="d21a7-136">Megosztott kulcs hitelesítése esetén a rendszer alapértelmezés szerint az elsődleges hozzáférési kulcsot használja.</span><span class="sxs-lookup"><span data-stu-id="d21a7-136">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="d21a7-137">A használni használt kulcs módosítása a BatchAccountContext.KeyInUse tulajdonsággal.</span><span class="sxs-lookup"><span data-stu-id="d21a7-137">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="d21a7-138">-CertificateReferences</span><span class="sxs-lookup"><span data-stu-id="d21a7-138">-CertificateReferences</span></span>
<span data-ttu-id="d21a7-139">A készlethez társított tanúsítványok megadása.</span><span class="sxs-lookup"><span data-stu-id="d21a7-139">Specifies certificates associated with the pool.</span></span>
<span data-ttu-id="d21a7-140">A Batch szolgáltatás a hivatkozott tanúsítványokat a készlet minden egyes számítási csomópontjára telepíti.</span><span class="sxs-lookup"><span data-stu-id="d21a7-140">The Batch service installs the referenced certificates on each compute node of the pool.</span></span>

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

### <span data-ttu-id="d21a7-141">-CloudServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="d21a7-141">-CloudServiceConfiguration</span></span>
<span data-ttu-id="d21a7-142">Egy készlet konfigurációs beállításait adja meg az Azure felhőbeli szolgáltatásplatform alapján.</span><span class="sxs-lookup"><span data-stu-id="d21a7-142">Specifies configuration settings for a pool based on the Azure cloud service platform.</span></span>

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

### <span data-ttu-id="d21a7-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d21a7-143">-DefaultProfile</span></span>
<span data-ttu-id="d21a7-144">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d21a7-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d21a7-145">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="d21a7-145">-DisplayName</span></span>
<span data-ttu-id="d21a7-146">A készlet megjelenítendő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d21a7-146">Specifies the display name of the pool.</span></span>

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

### <span data-ttu-id="d21a7-147">-Id</span><span class="sxs-lookup"><span data-stu-id="d21a7-147">-Id</span></span>
<span data-ttu-id="d21a7-148">A létrehozni szükséges készlet azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d21a7-148">Specifies the ID of the pool to create.</span></span>

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

### <span data-ttu-id="d21a7-149">-InterComputeNodeCommunicationEnabled</span><span class="sxs-lookup"><span data-stu-id="d21a7-149">-InterComputeNodeCommunicationEnabled</span></span>
<span data-ttu-id="d21a7-150">Azt jelzi, hogy ez a parancsmag beállítja a készletet a dedikált számítási csomópontok közötti közvetlen kommunikációhoz.</span><span class="sxs-lookup"><span data-stu-id="d21a7-150">Indicates that this cmdlet sets up the pool for direct communication between dedicated compute nodes.</span></span>

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

### <span data-ttu-id="d21a7-151">-MaxTasksPerComputeNode</span><span class="sxs-lookup"><span data-stu-id="d21a7-151">-MaxTasksPerComputeNode</span></span>
<span data-ttu-id="d21a7-152">Meghatározza, hogy legfeljebb hány feladat futtatható egyetlen számítási csomóponton.</span><span class="sxs-lookup"><span data-stu-id="d21a7-152">Specifies the maximum number of tasks that can run on a single compute node.</span></span>

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

### <span data-ttu-id="d21a7-153">-Metadata</span><span class="sxs-lookup"><span data-stu-id="d21a7-153">-Metadata</span></span>
<span data-ttu-id="d21a7-154">Meghatározza az új készlethez hozzáadni kulcs-érték párként hozzáadni a metaadatokat.</span><span class="sxs-lookup"><span data-stu-id="d21a7-154">Specifies the metadata, as key/value pairs, to add to the new pool.</span></span>
<span data-ttu-id="d21a7-155">A kulcs a metaadatok neve.</span><span class="sxs-lookup"><span data-stu-id="d21a7-155">The key is the metadata name.</span></span>
<span data-ttu-id="d21a7-156">Az érték a metaadatérték.</span><span class="sxs-lookup"><span data-stu-id="d21a7-156">The value is the metadata value.</span></span>

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

### <span data-ttu-id="d21a7-157">-MountConfiguration</span><span class="sxs-lookup"><span data-stu-id="d21a7-157">-MountConfiguration</span></span>
<span data-ttu-id="d21a7-158">A készlet egyes csomópontjaihoz csatlakoztatni kívánt fájlrendszerek listája.</span><span class="sxs-lookup"><span data-stu-id="d21a7-158">A list of file systems to mount on each node in the pool.</span></span> <span data-ttu-id="d21a7-159">Ez támogatja az Azure Files, AZ NFS, a CIFS/SMB és a Blobfuse fájlokat.</span><span class="sxs-lookup"><span data-stu-id="d21a7-159">This supports Azure Files, NFS, CIFS/SMB, and Blobfuse.</span></span>

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

### <span data-ttu-id="d21a7-160">-NetworkConfiguration</span><span class="sxs-lookup"><span data-stu-id="d21a7-160">-NetworkConfiguration</span></span>
<span data-ttu-id="d21a7-161">A készlet hálózati konfigurációja.</span><span class="sxs-lookup"><span data-stu-id="d21a7-161">The network configuration for the pool.</span></span>

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

### <span data-ttu-id="d21a7-162">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="d21a7-162">-ResizeTimeout</span></span>
<span data-ttu-id="d21a7-163">A számítási csomópontok készlethez való allocating időkorrának megadása.</span><span class="sxs-lookup"><span data-stu-id="d21a7-163">Specifies the time-out for allocating compute nodes to the pool.</span></span>

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

### <span data-ttu-id="d21a7-164">-StartTask</span><span class="sxs-lookup"><span data-stu-id="d21a7-164">-StartTask</span></span>
<span data-ttu-id="d21a7-165">A készlet kezdési tevékenységspecifikációját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d21a7-165">Specifies the start task specification for the pool.</span></span>
<span data-ttu-id="d21a7-166">A kezdési feladat akkor fut, amikor egy számítási csomópont csatlakozik a készlethez, vagy amikor a számítási csomópont újraindul vagy újra lesz iimagedve.</span><span class="sxs-lookup"><span data-stu-id="d21a7-166">The start task is run when a compute node joins the pool, or when the compute node is rebooted or reimaged.</span></span>

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

### <span data-ttu-id="d21a7-167">-TargetDedicatedComputeNodes</span><span class="sxs-lookup"><span data-stu-id="d21a7-167">-TargetDedicatedComputeNodes</span></span>
<span data-ttu-id="d21a7-168">A készlet számára lefoglalható dedikált számítási csomópontok célszámát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="d21a7-168">Specifies the target number of dedicated compute nodes to allocate to the pool.</span></span>

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

### <span data-ttu-id="d21a7-169">-TargetLowPriorityComputeNodes</span><span class="sxs-lookup"><span data-stu-id="d21a7-169">-TargetLowPriorityComputeNodes</span></span>
<span data-ttu-id="d21a7-170">Megadja a készlet számára kiosztható alacsony prioritású számítási csomópontok számát.</span><span class="sxs-lookup"><span data-stu-id="d21a7-170">Specifies the target number of low-priority compute nodes to allocate to the pool.</span></span>

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

### <span data-ttu-id="d21a7-171">-TaskSchedulingPolicy</span><span class="sxs-lookup"><span data-stu-id="d21a7-171">-TaskSchedulingPolicy</span></span>
<span data-ttu-id="d21a7-172">A tevékenység ütemezési házirendje, például a ComputeNodeFillType.</span><span class="sxs-lookup"><span data-stu-id="d21a7-172">Specifies the task scheduling policy, such as the ComputeNodeFillType.</span></span>

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

### <span data-ttu-id="d21a7-173">-UserAccount</span><span class="sxs-lookup"><span data-stu-id="d21a7-173">-UserAccount</span></span>
<span data-ttu-id="d21a7-174">A készlet minden egyes csomópontján létrehozható felhasználói fiókok listája.</span><span class="sxs-lookup"><span data-stu-id="d21a7-174">The list of user accounts to be created on each node in the pool.</span></span>

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

### <span data-ttu-id="d21a7-175">-VirtualMachineConfiguration</span><span class="sxs-lookup"><span data-stu-id="d21a7-175">-VirtualMachineConfiguration</span></span>
<span data-ttu-id="d21a7-176">A virtuális gépek infrastruktúrájában lévő készlet konfigurációs beállításait adja meg.</span><span class="sxs-lookup"><span data-stu-id="d21a7-176">Specifies configuration settings for a pool on the virtual machines infrastructure.</span></span>

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

### <span data-ttu-id="d21a7-177">-VirtualMachineSize</span><span class="sxs-lookup"><span data-stu-id="d21a7-177">-VirtualMachineSize</span></span>
<span data-ttu-id="d21a7-178">A készlet virtuális gépének mérete.</span><span class="sxs-lookup"><span data-stu-id="d21a7-178">Specifies the size of the virtual machines in the pool.</span></span>
<span data-ttu-id="d21a7-179">A virtuális gépek méretével kapcsolatos további információkért lásd: Méretek virtuális gépekhez https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/ ( a Microsoft Azure https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/) webhelyen.</span><span class="sxs-lookup"><span data-stu-id="d21a7-179">For more information about virtual machine sizes, see Sizes for virtual machineshttps://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/ (https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/) in the Microsoft Azure site.</span></span>

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

### <span data-ttu-id="d21a7-180">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d21a7-180">-Confirm</span></span>
<span data-ttu-id="d21a7-181">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d21a7-181">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d21a7-182">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d21a7-182">-WhatIf</span></span>
<span data-ttu-id="d21a7-183">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d21a7-183">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d21a7-184">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d21a7-184">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d21a7-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d21a7-185">CommonParameters</span></span>
<span data-ttu-id="d21a7-186">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d21a7-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d21a7-187">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d21a7-187">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d21a7-188">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d21a7-188">INPUTS</span></span>

### <span data-ttu-id="d21a7-189">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="d21a7-189">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="d21a7-190">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d21a7-190">OUTPUTS</span></span>

### <span data-ttu-id="d21a7-191">System.Void</span><span class="sxs-lookup"><span data-stu-id="d21a7-191">System.Void</span></span>

## <span data-ttu-id="d21a7-192">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d21a7-192">NOTES</span></span>

## <span data-ttu-id="d21a7-193">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d21a7-193">RELATED LINKS</span></span>

[<span data-ttu-id="d21a7-194">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="d21a7-194">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="d21a7-195">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="d21a7-195">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="d21a7-196">Remove-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="d21a7-196">Remove-AzBatchPool</span></span>](./Remove-AzBatchPool.md)

[<span data-ttu-id="d21a7-197">Azure Batch-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="d21a7-197">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
