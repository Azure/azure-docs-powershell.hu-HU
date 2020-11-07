---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearningCompute.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/new-azmlopcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlOpCluster.md
ms.openlocfilehash: 51c8beb396bb0795fa77431a256ddc38e4e8df38
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835294"
---
# <span data-ttu-id="f04d3-101">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="f04d3-101">New-AzMlOpCluster</span></span>

## <span data-ttu-id="f04d3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f04d3-102">SYNOPSIS</span></span>
<span data-ttu-id="f04d3-103">Új operationalization-fürtöt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="f04d3-103">Creates a new operationalization cluster.</span></span>

## <span data-ttu-id="f04d3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f04d3-104">SYNTAX</span></span>

### <span data-ttu-id="f04d3-105">CreateWithInputObject</span><span class="sxs-lookup"><span data-stu-id="f04d3-105">CreateWithInputObject</span></span>
```
New-AzMlOpCluster -ResourceGroupName <String> -Name <String> -InputObject <PSOperationalizationCluster>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f04d3-106">CreateWithParameters</span><span class="sxs-lookup"><span data-stu-id="f04d3-106">CreateWithParameters</span></span>
```
New-AzMlOpCluster -ResourceGroupName <String> -Name <String> -Location <String> -ClusterType <String>
 [-OrchestratorType <String>] [-ClientId <String>] [-Secret <String>] [-Description <String>]
 [-MasterCount <Int32>] [-AgentCount <Int32>] [-AgentVmSize <String>]
 [-GlobalServiceConfigurationETag <String>] [-SslStatus <String>] [-SslCertificate <String>] [-SslKey <String>]
 [-SslCName <String>] [-StorageAccount <String>] [-AzureContainerRegistry <String>]
 [-DefaultProfile <IAzureContextContainer>] [-GlobalServiceConfigurationAdditionalProperties <Hashtable>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f04d3-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="f04d3-107">DESCRIPTION</span></span>
<span data-ttu-id="f04d3-108">Új operationalization-fürtöt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="f04d3-108">Creates a new operationalization cluster.</span></span> <span data-ttu-id="f04d3-109">Ezzel létrehoz egy cluster objektumot, egy tároló szolgáltatást, ha szükséges, az alkalmazások és az Azure Container beállításjegyzéke.</span><span class="sxs-lookup"><span data-stu-id="f04d3-109">This will create a cluster object, a container service if needed, application insights, and an azure container registry.</span></span>

## <span data-ttu-id="f04d3-110">Példák</span><span class="sxs-lookup"><span data-stu-id="f04d3-110">EXAMPLES</span></span>

### <span data-ttu-id="f04d3-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f04d3-111">Example 1</span></span>
```
PS C:\> New-AzMlOpCluster -ResourceGroupName my-group -Name my-cluster -Location "East US 2" -ClusterType "ACS" -OrchestratorType "Kubernetes" -ClientId "abc" -Secret "xyz"
```

<span data-ttu-id="f04d3-112">Új operationalization-fürtöt hoz létre az Azure Container Service és a Kubernetes Orchestrator.</span><span class="sxs-lookup"><span data-stu-id="f04d3-112">Creates a new operationalization cluster with azure container service and Kubernetes as the orchestrator.</span></span>

### <span data-ttu-id="f04d3-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="f04d3-113">Example 2</span></span>
```
PS C:\> New-AzMlOpCluster -ResourceGroupName my-group -Name my-cluster -Location "East US 2" -ClusterType "Local"
```

<span data-ttu-id="f04d3-114">Új operationalization-fürtöt hoz létre helyben.</span><span class="sxs-lookup"><span data-stu-id="f04d3-114">Creates a new operationalization cluster locally.</span></span> <span data-ttu-id="f04d3-115">Ezzel létrehoz egy Azure Container-nyilvántartót, az alkalmazások elemzését és a tárolási fiókot, de nem hoz létre tároló szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="f04d3-115">This creates an azure container registry, application insights, and storage account, but does not create a container service.</span></span>

## <span data-ttu-id="f04d3-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f04d3-116">PARAMETERS</span></span>

### <span data-ttu-id="f04d3-117">-AgentCount</span><span class="sxs-lookup"><span data-stu-id="f04d3-117">-AgentCount</span></span>
<span data-ttu-id="f04d3-118">Az ügynök csomópontjainak száma az ACS-fürtben.</span><span class="sxs-lookup"><span data-stu-id="f04d3-118">The number of agent nodes in the ACS cluster.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f04d3-119">-AgentVmSize</span><span class="sxs-lookup"><span data-stu-id="f04d3-119">-AgentVmSize</span></span>
<span data-ttu-id="f04d3-120">Az ügynök csomópontjainak száma az ACS-fürtben.</span><span class="sxs-lookup"><span data-stu-id="f04d3-120">The number of agent nodes in the ACS cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f04d3-121">-AzureContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f04d3-121">-AzureContainerRegistry</span></span>
<span data-ttu-id="f04d3-122">A létrehozása helyett az Azure Container beállításjegyzékének URI-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f04d3-122">The URI to the azure container registry to use instead of creating one.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f04d3-123">-ClientId</span><span class="sxs-lookup"><span data-stu-id="f04d3-123">-ClientId</span></span>
<span data-ttu-id="f04d3-124">Az ACS-fürt Orchestrator-szolgáltatásának fő azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f04d3-124">The ACS cluster's orchestrator service principal id.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f04d3-125">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="f04d3-125">-ClusterType</span></span>
<span data-ttu-id="f04d3-126">A operationalization típusa.</span><span class="sxs-lookup"><span data-stu-id="f04d3-126">The operationalization cluster type.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f04d3-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f04d3-127">-DefaultProfile</span></span>
<span data-ttu-id="f04d3-128">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f04d3-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f04d3-129">-Leírás</span><span class="sxs-lookup"><span data-stu-id="f04d3-129">-Description</span></span>
<span data-ttu-id="f04d3-130">A fő csomópontok száma az ACS-fürtben.</span><span class="sxs-lookup"><span data-stu-id="f04d3-130">The number of master nodes in the ACS cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f04d3-131">-GlobalServiceConfigurationAdditionalProperties</span><span class="sxs-lookup"><span data-stu-id="f04d3-131">-GlobalServiceConfigurationAdditionalProperties</span></span>
<span data-ttu-id="f04d3-132">A globális szolgáltatás konfigurációjának további tulajdonságai</span><span class="sxs-lookup"><span data-stu-id="f04d3-132">Additional properties for the global service configuration.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f04d3-133">-GlobalServiceConfigurationETag</span><span class="sxs-lookup"><span data-stu-id="f04d3-133">-GlobalServiceConfigurationETag</span></span>
<span data-ttu-id="f04d3-134">A frissítések beállítási ETag.</span><span class="sxs-lookup"><span data-stu-id="f04d3-134">The configuration ETag for updates.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f04d3-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f04d3-135">-InputObject</span></span>
<span data-ttu-id="f04d3-136">A operationalization-fürt tulajdonságai</span><span class="sxs-lookup"><span data-stu-id="f04d3-136">The operationalization cluster properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster
Parameter Sets: CreateWithInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f04d3-137">-Hely</span><span class="sxs-lookup"><span data-stu-id="f04d3-137">-Location</span></span>
<span data-ttu-id="f04d3-138">A operationalization-fürt helye.</span><span class="sxs-lookup"><span data-stu-id="f04d3-138">The operationalization cluster's location.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f04d3-139">-MasterCount</span><span class="sxs-lookup"><span data-stu-id="f04d3-139">-MasterCount</span></span>
<span data-ttu-id="f04d3-140">A fő csomópontok száma az ACS-fürtben.</span><span class="sxs-lookup"><span data-stu-id="f04d3-140">The number of master nodes in the ACS cluster.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f04d3-141">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f04d3-141">-Name</span></span>
<span data-ttu-id="f04d3-142">A operationalization-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="f04d3-142">The name of the operationalization cluster.</span></span>

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

### <span data-ttu-id="f04d3-143">-OrchestratorType</span><span class="sxs-lookup"><span data-stu-id="f04d3-143">-OrchestratorType</span></span>
<span data-ttu-id="f04d3-144">Az ACS-fürt Orchestrator típusa.</span><span class="sxs-lookup"><span data-stu-id="f04d3-144">The ACS cluster's orchestrator type.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f04d3-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f04d3-145">-ResourceGroupName</span></span>
<span data-ttu-id="f04d3-146">A operationalization-fürt erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f04d3-146">The name of the resource group for the operationalization cluster.</span></span>

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

### <span data-ttu-id="f04d3-147">-Secret</span><span class="sxs-lookup"><span data-stu-id="f04d3-147">-Secret</span></span>
<span data-ttu-id="f04d3-148">Az ACS-fürt Orchestrator szolgáltatásának fő titka.</span><span class="sxs-lookup"><span data-stu-id="f04d3-148">The ACS cluster's orchestrator service principal secret.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f04d3-149">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="f04d3-149">-SslCertificate</span></span>
<span data-ttu-id="f04d3-150">Az SSL-tanúsítványok a PEM formátumú, Base64-karakterláncként kódolt formában jelennek meg.</span><span class="sxs-lookup"><span data-stu-id="f04d3-150">The SSL certificate data in PEM format encoded as base64 string.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f04d3-151">-SslCName</span><span class="sxs-lookup"><span data-stu-id="f04d3-151">-SslCName</span></span>
<span data-ttu-id="f04d3-152">Az SSL-tanúsítvány CName rekordja.</span><span class="sxs-lookup"><span data-stu-id="f04d3-152">The CName for the SSL certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f04d3-153">-SslKey</span><span class="sxs-lookup"><span data-stu-id="f04d3-153">-SslKey</span></span>
<span data-ttu-id="f04d3-154">A PEM formátumú SSL-kulcsok a Base64-karakterláncként kódolt formában jelennek meg.</span><span class="sxs-lookup"><span data-stu-id="f04d3-154">The SSL key data in PEM format encoded as base64 string.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f04d3-155">-SslStatus</span><span class="sxs-lookup"><span data-stu-id="f04d3-155">-SslStatus</span></span>
<span data-ttu-id="f04d3-156">SSL-állapot</span><span class="sxs-lookup"><span data-stu-id="f04d3-156">SSL status.</span></span>
<span data-ttu-id="f04d3-157">A lehetséges értékek "engedélyezve" és "Letiltva".</span><span class="sxs-lookup"><span data-stu-id="f04d3-157">Possible values are 'Enabled' and 'Disabled'.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f04d3-158">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="f04d3-158">-StorageAccount</span></span>
<span data-ttu-id="f04d3-159">A létrehozása helyett a tárolási fiók URI-ja.</span><span class="sxs-lookup"><span data-stu-id="f04d3-159">The URI to the storage account to use instead of creating one.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f04d3-160">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f04d3-160">-Confirm</span></span>
<span data-ttu-id="f04d3-161">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f04d3-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f04d3-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f04d3-162">-WhatIf</span></span>
<span data-ttu-id="f04d3-163">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f04d3-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f04d3-164">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f04d3-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f04d3-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f04d3-165">CommonParameters</span></span>
<span data-ttu-id="f04d3-166">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f04d3-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f04d3-167">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f04d3-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f04d3-168">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f04d3-168">INPUTS</span></span>

### <span data-ttu-id="f04d3-169">Nincs</span><span class="sxs-lookup"><span data-stu-id="f04d3-169">None</span></span>

## <span data-ttu-id="f04d3-170">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f04d3-170">OUTPUTS</span></span>

### <span data-ttu-id="f04d3-171">Microsoft. Azure. Command. MachineLearningCompute. models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="f04d3-171">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

## <span data-ttu-id="f04d3-172">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f04d3-172">NOTES</span></span>

## <span data-ttu-id="f04d3-173">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f04d3-173">RELATED LINKS</span></span>
