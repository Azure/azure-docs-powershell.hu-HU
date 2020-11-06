---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearningcompute/new-azurermmlopcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/New-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/New-AzureRmMlOpCluster.md
ms.openlocfilehash: 8e93847c3a6d993c689d0ac8c40327ddfcbe76af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502552"
---
# <span data-ttu-id="93cfb-101">New-AzureRmMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="93cfb-101">New-AzureRmMlOpCluster</span></span>

## <span data-ttu-id="93cfb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="93cfb-102">SYNOPSIS</span></span>
<span data-ttu-id="93cfb-103">Új operationalization-fürtöt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="93cfb-103">Creates a new operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="93cfb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="93cfb-104">SYNTAX</span></span>

### <span data-ttu-id="93cfb-105">CreateWithInputObject</span><span class="sxs-lookup"><span data-stu-id="93cfb-105">CreateWithInputObject</span></span>
```
New-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> -InputObject <PSOperationalizationCluster>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93cfb-106">CreateWithParameters</span><span class="sxs-lookup"><span data-stu-id="93cfb-106">CreateWithParameters</span></span>
```
New-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> -Location <String> -ClusterType <String>
 [-OrchestratorType <String>] [-ClientId <String>] [-Secret <String>] [-Description <String>]
 [-MasterCount <Int32>] [-AgentCount <Int32>] [-AgentVmSize <String>]
 [-GlobalServiceConfigurationETag <String>] [-SslStatus <String>] [-SslCertificate <String>] [-SslKey <String>]
 [-SslCName <String>] [-StorageAccount <String>] [-AzureContainerRegistry <String>]
 [-DefaultProfile <IAzureContextContainer>] [-GlobalServiceConfigurationAdditionalProperties <Hashtable>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93cfb-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="93cfb-107">DESCRIPTION</span></span>
<span data-ttu-id="93cfb-108">Új operationalization-fürtöt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="93cfb-108">Creates a new operationalization cluster.</span></span> <span data-ttu-id="93cfb-109">Ezzel létrehoz egy cluster objektumot, egy tároló szolgáltatást, ha szükséges, az alkalmazások és az Azure Container beállításjegyzéke.</span><span class="sxs-lookup"><span data-stu-id="93cfb-109">This will create a cluster object, a container service if needed, application insights, and an azure container registry.</span></span>

## <span data-ttu-id="93cfb-110">Példák</span><span class="sxs-lookup"><span data-stu-id="93cfb-110">EXAMPLES</span></span>

### <span data-ttu-id="93cfb-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="93cfb-111">Example 1</span></span>
```
PS C:\> New-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster -Location "East US 2" -ClusterType "ACS" -OrchestratorType "Kubernetes" -ClientId "abc" -Secret "xyz"
```

<span data-ttu-id="93cfb-112">Új operationalization-fürtöt hoz létre az Azure Container Service és a Kubernetes Orchestrator.</span><span class="sxs-lookup"><span data-stu-id="93cfb-112">Creates a new operationalization cluster with azure container service and Kubernetes as the orchestrator.</span></span>

### <span data-ttu-id="93cfb-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="93cfb-113">Example 2</span></span>
```
PS C:\> New-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster -Location "East US 2" -ClusterType "Local"
```

<span data-ttu-id="93cfb-114">Új operationalization-fürtöt hoz létre helyben.</span><span class="sxs-lookup"><span data-stu-id="93cfb-114">Creates a new operationalization cluster locally.</span></span> <span data-ttu-id="93cfb-115">Ezzel létrehoz egy Azure Container-nyilvántartót, az alkalmazások elemzését és a tárolási fiókot, de nem hoz létre tároló szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="93cfb-115">This creates an azure container registry, application insights, and storage account, but does not create a container service.</span></span>

## <span data-ttu-id="93cfb-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="93cfb-116">PARAMETERS</span></span>

### <span data-ttu-id="93cfb-117">-AgentCount</span><span class="sxs-lookup"><span data-stu-id="93cfb-117">-AgentCount</span></span>
<span data-ttu-id="93cfb-118">Az ügynök csomópontjainak száma az ACS-fürtben.</span><span class="sxs-lookup"><span data-stu-id="93cfb-118">The number of agent nodes in the ACS cluster.</span></span>

```yaml
Type: Int32
Parameter Sets: CreateWithParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93cfb-119">-AgentVmSize</span><span class="sxs-lookup"><span data-stu-id="93cfb-119">-AgentVmSize</span></span>
<span data-ttu-id="93cfb-120">Az ügynök csomópontjainak száma az ACS-fürtben.</span><span class="sxs-lookup"><span data-stu-id="93cfb-120">The number of agent nodes in the ACS cluster.</span></span>

```yaml
Type: String
Parameter Sets: CreateWithParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93cfb-121">-AzureContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="93cfb-121">-AzureContainerRegistry</span></span>
<span data-ttu-id="93cfb-122">A létrehozása helyett az Azure Container beállításjegyzékének URI-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="93cfb-122">The URI to the azure container registry to use instead of creating one.</span></span>

```yaml
Type: String
Parameter Sets: CreateWithParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93cfb-123">-ClientId</span><span class="sxs-lookup"><span data-stu-id="93cfb-123">-ClientId</span></span>
<span data-ttu-id="93cfb-124">Az ACS-fürt Orchestrator-szolgáltatásának fő azonosítója.</span><span class="sxs-lookup"><span data-stu-id="93cfb-124">The ACS cluster's orchestrator service principal id.</span></span>

```yaml
Type: String
Parameter Sets: CreateWithParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93cfb-125">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="93cfb-125">-ClusterType</span></span>
<span data-ttu-id="93cfb-126">A operationalization típusa.</span><span class="sxs-lookup"><span data-stu-id="93cfb-126">The operationalization cluster type.</span></span>

```yaml
Type: String
Parameter Sets: CreateWithParameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93cfb-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93cfb-127">-DefaultProfile</span></span>
<span data-ttu-id="93cfb-128">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="93cfb-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="93cfb-129">-Leírás</span><span class="sxs-lookup"><span data-stu-id="93cfb-129">-Description</span></span>
<span data-ttu-id="93cfb-130">A fő csomópontok száma az ACS-fürtben.</span><span class="sxs-lookup"><span data-stu-id="93cfb-130">The number of master nodes in the ACS cluster.</span></span>

```yaml
Type: String
Parameter Sets: CreateWithParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93cfb-131">-GlobalServiceConfigurationAdditionalProperties</span><span class="sxs-lookup"><span data-stu-id="93cfb-131">-GlobalServiceConfigurationAdditionalProperties</span></span>
<span data-ttu-id="93cfb-132">A globális szolgáltatás konfigurációjának további tulajdonságai</span><span class="sxs-lookup"><span data-stu-id="93cfb-132">Additional properties for the global service configuration.</span></span>

```yaml
Type: Hashtable
Parameter Sets: CreateWithParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93cfb-133">-GlobalServiceConfigurationETag</span><span class="sxs-lookup"><span data-stu-id="93cfb-133">-GlobalServiceConfigurationETag</span></span>
<span data-ttu-id="93cfb-134">A frissítések beállítási ETag.</span><span class="sxs-lookup"><span data-stu-id="93cfb-134">The configuration ETag for updates.</span></span>

```yaml
Type: String
Parameter Sets: CreateWithParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93cfb-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="93cfb-135">-InputObject</span></span>
<span data-ttu-id="93cfb-136">A operationalization-fürt tulajdonságai</span><span class="sxs-lookup"><span data-stu-id="93cfb-136">The operationalization cluster properties.</span></span>

```yaml
Type: PSOperationalizationCluster
Parameter Sets: CreateWithInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93cfb-137">-Hely</span><span class="sxs-lookup"><span data-stu-id="93cfb-137">-Location</span></span>
<span data-ttu-id="93cfb-138">A operationalization-fürt helye.</span><span class="sxs-lookup"><span data-stu-id="93cfb-138">The operationalization cluster's location.</span></span>

```yaml
Type: String
Parameter Sets: CreateWithParameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93cfb-139">-MasterCount</span><span class="sxs-lookup"><span data-stu-id="93cfb-139">-MasterCount</span></span>
<span data-ttu-id="93cfb-140">A fő csomópontok száma az ACS-fürtben.</span><span class="sxs-lookup"><span data-stu-id="93cfb-140">The number of master nodes in the ACS cluster.</span></span>

```yaml
Type: Int32
Parameter Sets: CreateWithParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93cfb-141">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="93cfb-141">-Name</span></span>
<span data-ttu-id="93cfb-142">A operationalization-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="93cfb-142">The name of the operationalization cluster.</span></span>

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

### <span data-ttu-id="93cfb-143">-OrchestratorType</span><span class="sxs-lookup"><span data-stu-id="93cfb-143">-OrchestratorType</span></span>
<span data-ttu-id="93cfb-144">Az ACS-fürt Orchestrator típusa.</span><span class="sxs-lookup"><span data-stu-id="93cfb-144">The ACS cluster's orchestrator type.</span></span>

```yaml
Type: String
Parameter Sets: CreateWithParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93cfb-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93cfb-145">-ResourceGroupName</span></span>
<span data-ttu-id="93cfb-146">A operationalization-fürt erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="93cfb-146">The name of the resource group for the operationalization cluster.</span></span>

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

### <span data-ttu-id="93cfb-147">-Secret</span><span class="sxs-lookup"><span data-stu-id="93cfb-147">-Secret</span></span>
<span data-ttu-id="93cfb-148">Az ACS-fürt Orchestrator szolgáltatásának fő titka.</span><span class="sxs-lookup"><span data-stu-id="93cfb-148">The ACS cluster's orchestrator service principal secret.</span></span>

```yaml
Type: String
Parameter Sets: CreateWithParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93cfb-149">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="93cfb-149">-SslCertificate</span></span>
<span data-ttu-id="93cfb-150">Az SSL-tanúsítványok a PEM formátumú, Base64-karakterláncként kódolt formában jelennek meg.</span><span class="sxs-lookup"><span data-stu-id="93cfb-150">The SSL certificate data in PEM format encoded as base64 string.</span></span>

```yaml
Type: String
Parameter Sets: CreateWithParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93cfb-151">-SslCName</span><span class="sxs-lookup"><span data-stu-id="93cfb-151">-SslCName</span></span>
<span data-ttu-id="93cfb-152">Az SSL-tanúsítvány CName rekordja.</span><span class="sxs-lookup"><span data-stu-id="93cfb-152">The CName for the SSL certificate.</span></span>

```yaml
Type: String
Parameter Sets: CreateWithParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93cfb-153">-SslKey</span><span class="sxs-lookup"><span data-stu-id="93cfb-153">-SslKey</span></span>
<span data-ttu-id="93cfb-154">A PEM formátumú SSL-kulcsok a Base64-karakterláncként kódolt formában jelennek meg.</span><span class="sxs-lookup"><span data-stu-id="93cfb-154">The SSL key data in PEM format encoded as base64 string.</span></span>

```yaml
Type: String
Parameter Sets: CreateWithParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93cfb-155">-SslStatus</span><span class="sxs-lookup"><span data-stu-id="93cfb-155">-SslStatus</span></span>
<span data-ttu-id="93cfb-156">SSL-állapot</span><span class="sxs-lookup"><span data-stu-id="93cfb-156">SSL status.</span></span>
<span data-ttu-id="93cfb-157">A lehetséges értékek "engedélyezve" és "Letiltva".</span><span class="sxs-lookup"><span data-stu-id="93cfb-157">Possible values are 'Enabled' and 'Disabled'.</span></span>

```yaml
Type: String
Parameter Sets: CreateWithParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93cfb-158">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="93cfb-158">-StorageAccount</span></span>
<span data-ttu-id="93cfb-159">A létrehozása helyett a tárolási fiók URI-ja.</span><span class="sxs-lookup"><span data-stu-id="93cfb-159">The URI to the storage account to use instead of creating one.</span></span>

```yaml
Type: String
Parameter Sets: CreateWithParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93cfb-160">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="93cfb-160">-Confirm</span></span>
<span data-ttu-id="93cfb-161">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="93cfb-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93cfb-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93cfb-162">-WhatIf</span></span>
<span data-ttu-id="93cfb-163">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="93cfb-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93cfb-164">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="93cfb-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93cfb-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93cfb-165">CommonParameters</span></span>
<span data-ttu-id="93cfb-166">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="93cfb-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93cfb-167">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93cfb-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93cfb-168">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="93cfb-168">INPUTS</span></span>

### <span data-ttu-id="93cfb-169">Nincs</span><span class="sxs-lookup"><span data-stu-id="93cfb-169">None</span></span>

## <span data-ttu-id="93cfb-170">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="93cfb-170">OUTPUTS</span></span>

### <span data-ttu-id="93cfb-171">Microsoft. Azure. Command. MachineLearningCompute. models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="93cfb-171">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

## <span data-ttu-id="93cfb-172">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="93cfb-172">NOTES</span></span>

## <span data-ttu-id="93cfb-173">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="93cfb-173">RELATED LINKS</span></span>

