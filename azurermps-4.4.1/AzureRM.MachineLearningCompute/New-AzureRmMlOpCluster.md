---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/New-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/New-AzureRmMlOpCluster.md
ms.openlocfilehash: 222813dc78b4dd7c0118b8146a75ca4d225ce83c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500828"
---
# <span data-ttu-id="a4bf9-101">New-AzureRmMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="a4bf9-101">New-AzureRmMlOpCluster</span></span>

## <span data-ttu-id="a4bf9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a4bf9-102">SYNOPSIS</span></span>
<span data-ttu-id="a4bf9-103">Új operationalization-fürtöt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="a4bf9-103">Creates a new operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a4bf9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a4bf9-104">SYNTAX</span></span>

### <span data-ttu-id="a4bf9-105">Hozzon létre egy új operationalization-fürtöt egy OperationalizationCluster példány-definícióból.</span><span class="sxs-lookup"><span data-stu-id="a4bf9-105">Create a new operationalization cluster from an OperationalizationCluster instance definition.</span></span>
```
New-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> -InputObject <PSOperationalizationCluster>
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="a4bf9-106">Hozzon létre egy új operationalization-fürtöt a parancsmag bemeneti paraméterei közül.</span><span class="sxs-lookup"><span data-stu-id="a4bf9-106">Create a new operationalization cluster from cmdlet input parameters.</span></span>
```
New-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> -Location <String> -ClusterType <String>
 [-OrchestratorType <String>] [-ServicePrincipalName <String>] [-ServicePrincipalSecret <String>]
 [-Description <String>] [-MasterCount <Int32>] [-AgentCount <Int32>] [-AgentVmSize <String>]
 [-GlobalServiceConfigurationETag <String>] [-SslStatus <String>] [-SslCertificate <String>] [-SslKey <String>]
 [-SslCName <String>] [-StorageAccount <String>] [-AzureContainerRegistry <String>]
 [-GlobalServiceConfigurationAdditionalProperties <Hashtable>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="a4bf9-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a4bf9-107">DESCRIPTION</span></span>
<span data-ttu-id="a4bf9-108">Új operationalization-fürtöt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="a4bf9-108">Creates a new operationalization cluster.</span></span> <span data-ttu-id="a4bf9-109">Ezzel létrehoz egy cluster objektumot, egy tároló szolgáltatást, ha szükséges, az alkalmazások és az Azure Container beállításjegyzéke.</span><span class="sxs-lookup"><span data-stu-id="a4bf9-109">This will create a cluster object, a container service if needed, application insights, and an azure container registry.</span></span>

## <span data-ttu-id="a4bf9-110">Példák</span><span class="sxs-lookup"><span data-stu-id="a4bf9-110">EXAMPLES</span></span>

### <span data-ttu-id="a4bf9-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a4bf9-111">Example 1</span></span>
```
PS C:\> New-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster -Location "East US 2" -ClusterType "ACS" -OrchestratorType "Kubernetes" -ClientId "abc" -Secret "xyz"
```

<span data-ttu-id="a4bf9-112">Új operationalization-fürtöt hoz létre az Azure Container Service és a Kubernetes Orchestrator.</span><span class="sxs-lookup"><span data-stu-id="a4bf9-112">Creates a new operationalization cluster with azure container service and Kubernetes as the orchestrator.</span></span>

### <span data-ttu-id="a4bf9-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="a4bf9-113">Example 2</span></span>
```
PS C:\> New-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster -Location "East US 2" -ClusterType "Local"
```

<span data-ttu-id="a4bf9-114">Új operationalization-fürtöt hoz létre helyben.</span><span class="sxs-lookup"><span data-stu-id="a4bf9-114">Creates a new operationalization cluster locally.</span></span> <span data-ttu-id="a4bf9-115">Ezzel létrehoz egy Azure Container-nyilvántartót, az alkalmazások elemzését és a tárolási fiókot, de nem hoz létre tároló szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="a4bf9-115">This creates an azure container registry, application insights, and storage account, but does not create a container service.</span></span>

## <span data-ttu-id="a4bf9-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a4bf9-116">PARAMETERS</span></span>

### <span data-ttu-id="a4bf9-117">-AgentCount</span><span class="sxs-lookup"><span data-stu-id="a4bf9-117">-AgentCount</span></span>
<span data-ttu-id="a4bf9-118">Az ügynök csomópontjainak száma az ACS-fürtben.</span><span class="sxs-lookup"><span data-stu-id="a4bf9-118">The number of agent nodes in the ACS cluster.</span></span>

```yaml
Type: Int32
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4bf9-119">-AgentVmSize</span><span class="sxs-lookup"><span data-stu-id="a4bf9-119">-AgentVmSize</span></span>
<span data-ttu-id="a4bf9-120">Az ügynök csomópontjainak száma az ACS-fürtben.</span><span class="sxs-lookup"><span data-stu-id="a4bf9-120">The number of agent nodes in the ACS cluster.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4bf9-121">-AzureContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="a4bf9-121">-AzureContainerRegistry</span></span>
<span data-ttu-id="a4bf9-122">A létrehozása helyett az Azure Container beállításjegyzékének URI-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a4bf9-122">The URI to the azure container registry to use instead of creating one.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4bf9-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a4bf9-123">-InputObject</span></span>
<span data-ttu-id="a4bf9-124">A operationalization-fürt tulajdonságai</span><span class="sxs-lookup"><span data-stu-id="a4bf9-124">The operationalization cluster properties.</span></span>

```yaml
Type: PSOperationalizationCluster
Parameter Sets: Create a new operationalization cluster from an OperationalizationCluster instance definition.
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4bf9-125">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="a4bf9-125">-ClusterType</span></span>
<span data-ttu-id="a4bf9-126">A operationalization típusa.</span><span class="sxs-lookup"><span data-stu-id="a4bf9-126">The operationalization cluster type.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4bf9-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a4bf9-127">-Confirm</span></span>
<span data-ttu-id="a4bf9-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a4bf9-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4bf9-129">-Leírás</span><span class="sxs-lookup"><span data-stu-id="a4bf9-129">-Description</span></span>
<span data-ttu-id="a4bf9-130">A fő csomópontok száma az ACS-fürtben.</span><span class="sxs-lookup"><span data-stu-id="a4bf9-130">The number of master nodes in the ACS cluster.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4bf9-131">-GlobalServiceConfigurationAdditionalProperties</span><span class="sxs-lookup"><span data-stu-id="a4bf9-131">-GlobalServiceConfigurationAdditionalProperties</span></span>
<span data-ttu-id="a4bf9-132">A globális szolgáltatás konfigurációjának további tulajdonságai</span><span class="sxs-lookup"><span data-stu-id="a4bf9-132">Additional properties for the global service configuration.</span></span>

```yaml
Type: Hashtable
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4bf9-133">-GlobalServiceConfigurationETag</span><span class="sxs-lookup"><span data-stu-id="a4bf9-133">-GlobalServiceConfigurationETag</span></span>
<span data-ttu-id="a4bf9-134">A frissítések beállítási ETag.</span><span class="sxs-lookup"><span data-stu-id="a4bf9-134">The configuration ETag for updates.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4bf9-135">-Hely</span><span class="sxs-lookup"><span data-stu-id="a4bf9-135">-Location</span></span>
<span data-ttu-id="a4bf9-136">A operationalization-fürt helye.</span><span class="sxs-lookup"><span data-stu-id="a4bf9-136">The operationalization cluster's location.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4bf9-137">-MasterCount</span><span class="sxs-lookup"><span data-stu-id="a4bf9-137">-MasterCount</span></span>
<span data-ttu-id="a4bf9-138">A fő csomópontok száma az ACS-fürtben.</span><span class="sxs-lookup"><span data-stu-id="a4bf9-138">The number of master nodes in the ACS cluster.</span></span>

```yaml
Type: Int32
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4bf9-139">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a4bf9-139">-Name</span></span>
<span data-ttu-id="a4bf9-140">A operationalization-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="a4bf9-140">The name of the operationalization cluster.</span></span>

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

### <span data-ttu-id="a4bf9-141">-OrchestratorType</span><span class="sxs-lookup"><span data-stu-id="a4bf9-141">-OrchestratorType</span></span>
<span data-ttu-id="a4bf9-142">Az ACS-fürt Orchestrator típusa.</span><span class="sxs-lookup"><span data-stu-id="a4bf9-142">The ACS cluster's orchestrator type.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4bf9-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4bf9-143">-ResourceGroupName</span></span>
<span data-ttu-id="a4bf9-144">A operationalization-fürt erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a4bf9-144">The name of the resource group for the operationalization cluster.</span></span>

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

### <span data-ttu-id="a4bf9-145">-ClientId</span><span class="sxs-lookup"><span data-stu-id="a4bf9-145">-ClientId</span></span>
<span data-ttu-id="a4bf9-146">Az ACS-fürt Orchestrator-szolgáltatásának fő azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a4bf9-146">The ACS cluster's orchestrator service principal id.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4bf9-147">-Secret</span><span class="sxs-lookup"><span data-stu-id="a4bf9-147">-Secret</span></span>
<span data-ttu-id="a4bf9-148">Az ACS-fürt Orchestrator szolgáltatásának fő titka.</span><span class="sxs-lookup"><span data-stu-id="a4bf9-148">The ACS cluster's orchestrator service principal secret.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4bf9-149">-SslCName</span><span class="sxs-lookup"><span data-stu-id="a4bf9-149">-SslCName</span></span>
<span data-ttu-id="a4bf9-150">Az SSL-tanúsítvány CName rekordja.</span><span class="sxs-lookup"><span data-stu-id="a4bf9-150">The CName for the SSL certificate.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4bf9-151">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="a4bf9-151">-SslCertificate</span></span>
<span data-ttu-id="a4bf9-152">Az SSL-tanúsítványok a PEM formátumú, Base64-karakterláncként kódolt formában jelennek meg.</span><span class="sxs-lookup"><span data-stu-id="a4bf9-152">The SSL certificate data in PEM format encoded as base64 string.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4bf9-153">-SslKey</span><span class="sxs-lookup"><span data-stu-id="a4bf9-153">-SslKey</span></span>
<span data-ttu-id="a4bf9-154">A PEM formátumú SSL-kulcsok a Base64-karakterláncként kódolt formában jelennek meg.</span><span class="sxs-lookup"><span data-stu-id="a4bf9-154">The SSL key data in PEM format encoded as base64 string.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4bf9-155">-SslStatus</span><span class="sxs-lookup"><span data-stu-id="a4bf9-155">-SslStatus</span></span>
<span data-ttu-id="a4bf9-156">SSL-állapot</span><span class="sxs-lookup"><span data-stu-id="a4bf9-156">SSL status.</span></span>
<span data-ttu-id="a4bf9-157">A lehetséges értékek "engedélyezve" és "Letiltva".</span><span class="sxs-lookup"><span data-stu-id="a4bf9-157">Possible values are 'Enabled' and 'Disabled'.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4bf9-158">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="a4bf9-158">-StorageAccount</span></span>
<span data-ttu-id="a4bf9-159">A létrehozása helyett a tárolási fiók URI-ja.</span><span class="sxs-lookup"><span data-stu-id="a4bf9-159">The URI to the storage account to use instead of creating one.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4bf9-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4bf9-160">-WhatIf</span></span>
<span data-ttu-id="a4bf9-161">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a4bf9-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4bf9-162">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a4bf9-162">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="a4bf9-163">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a4bf9-163">INPUTS</span></span>

### <span data-ttu-id="a4bf9-164">Nincs</span><span class="sxs-lookup"><span data-stu-id="a4bf9-164">None</span></span>


## <span data-ttu-id="a4bf9-165">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a4bf9-165">OUTPUTS</span></span>

### <span data-ttu-id="a4bf9-166">Microsoft. Azure. Command. MachineLearningCompute. models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="a4bf9-166">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>


## <span data-ttu-id="a4bf9-167">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a4bf9-167">NOTES</span></span>

## <span data-ttu-id="a4bf9-168">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a4bf9-168">RELATED LINKS</span></span>

