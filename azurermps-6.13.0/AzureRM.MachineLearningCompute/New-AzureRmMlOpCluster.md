---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearningcompute/new-azurermmlopcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/New-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/New-AzureRmMlOpCluster.md
ms.openlocfilehash: c4092d89f8b541db92737b71e534fcc1d4d917f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495995"
---
# <span data-ttu-id="6a7f4-101">New-AzureRmMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="6a7f4-101">New-AzureRmMlOpCluster</span></span>

## <span data-ttu-id="6a7f4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6a7f4-102">SYNOPSIS</span></span>
<span data-ttu-id="6a7f4-103">Új operationalization-fürtöt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="6a7f4-103">Creates a new operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6a7f4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6a7f4-104">SYNTAX</span></span>

### <span data-ttu-id="6a7f4-105">CreateWithInputObject</span><span class="sxs-lookup"><span data-stu-id="6a7f4-105">CreateWithInputObject</span></span>
```
New-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> -InputObject <PSOperationalizationCluster>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a7f4-106">CreateWithParameters</span><span class="sxs-lookup"><span data-stu-id="6a7f4-106">CreateWithParameters</span></span>
```
New-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> -Location <String> -ClusterType <String>
 [-OrchestratorType <String>] [-ClientId <String>] [-Secret <String>] [-Description <String>]
 [-MasterCount <Int32>] [-AgentCount <Int32>] [-AgentVmSize <String>]
 [-GlobalServiceConfigurationETag <String>] [-SslStatus <String>] [-SslCertificate <String>] [-SslKey <String>]
 [-SslCName <String>] [-StorageAccount <String>] [-AzureContainerRegistry <String>]
 [-DefaultProfile <IAzureContextContainer>] [-GlobalServiceConfigurationAdditionalProperties <Hashtable>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a7f4-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="6a7f4-107">DESCRIPTION</span></span>
<span data-ttu-id="6a7f4-108">Új operationalization-fürtöt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="6a7f4-108">Creates a new operationalization cluster.</span></span> <span data-ttu-id="6a7f4-109">Ezzel létrehoz egy cluster objektumot, egy tároló szolgáltatást, ha szükséges, az alkalmazások és az Azure Container beállításjegyzéke.</span><span class="sxs-lookup"><span data-stu-id="6a7f4-109">This will create a cluster object, a container service if needed, application insights, and an azure container registry.</span></span>

## <span data-ttu-id="6a7f4-110">Példák</span><span class="sxs-lookup"><span data-stu-id="6a7f4-110">EXAMPLES</span></span>

### <span data-ttu-id="6a7f4-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="6a7f4-111">Example 1</span></span>
```
PS C:\> New-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster -Location "East US 2" -ClusterType "ACS" -OrchestratorType "Kubernetes" -ClientId "abc" -Secret "xyz"
```

<span data-ttu-id="6a7f4-112">Új operationalization-fürtöt hoz létre az Azure Container Service és a Kubernetes Orchestrator.</span><span class="sxs-lookup"><span data-stu-id="6a7f4-112">Creates a new operationalization cluster with azure container service and Kubernetes as the orchestrator.</span></span>

### <span data-ttu-id="6a7f4-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="6a7f4-113">Example 2</span></span>
```
PS C:\> New-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster -Location "East US 2" -ClusterType "Local"
```

<span data-ttu-id="6a7f4-114">Új operationalization-fürtöt hoz létre helyben.</span><span class="sxs-lookup"><span data-stu-id="6a7f4-114">Creates a new operationalization cluster locally.</span></span> <span data-ttu-id="6a7f4-115">Ezzel létrehoz egy Azure Container-nyilvántartót, az alkalmazások elemzését és a tárolási fiókot, de nem hoz létre tároló szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="6a7f4-115">This creates an azure container registry, application insights, and storage account, but does not create a container service.</span></span>

## <span data-ttu-id="6a7f4-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6a7f4-116">PARAMETERS</span></span>

### <span data-ttu-id="6a7f4-117">-AgentCount</span><span class="sxs-lookup"><span data-stu-id="6a7f4-117">-AgentCount</span></span>
<span data-ttu-id="6a7f4-118">Az ügynök csomópontjainak száma az ACS-fürtben.</span><span class="sxs-lookup"><span data-stu-id="6a7f4-118">The number of agent nodes in the ACS cluster.</span></span>

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

### <span data-ttu-id="6a7f4-119">-AgentVmSize</span><span class="sxs-lookup"><span data-stu-id="6a7f4-119">-AgentVmSize</span></span>
<span data-ttu-id="6a7f4-120">Az ügynök csomópontjainak száma az ACS-fürtben.</span><span class="sxs-lookup"><span data-stu-id="6a7f4-120">The number of agent nodes in the ACS cluster.</span></span>

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

### <span data-ttu-id="6a7f4-121">-AzureContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="6a7f4-121">-AzureContainerRegistry</span></span>
<span data-ttu-id="6a7f4-122">A létrehozása helyett az Azure Container beállításjegyzékének URI-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="6a7f4-122">The URI to the azure container registry to use instead of creating one.</span></span>

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

### <span data-ttu-id="6a7f4-123">-ClientId</span><span class="sxs-lookup"><span data-stu-id="6a7f4-123">-ClientId</span></span>
<span data-ttu-id="6a7f4-124">Az ACS-fürt Orchestrator-szolgáltatásának fő azonosítója.</span><span class="sxs-lookup"><span data-stu-id="6a7f4-124">The ACS cluster's orchestrator service principal id.</span></span>

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

### <span data-ttu-id="6a7f4-125">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="6a7f4-125">-ClusterType</span></span>
<span data-ttu-id="6a7f4-126">A operationalization típusa.</span><span class="sxs-lookup"><span data-stu-id="6a7f4-126">The operationalization cluster type.</span></span>

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

### <span data-ttu-id="6a7f4-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a7f4-127">-DefaultProfile</span></span>
<span data-ttu-id="6a7f4-128">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6a7f4-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a7f4-129">-Leírás</span><span class="sxs-lookup"><span data-stu-id="6a7f4-129">-Description</span></span>
<span data-ttu-id="6a7f4-130">A fő csomópontok száma az ACS-fürtben.</span><span class="sxs-lookup"><span data-stu-id="6a7f4-130">The number of master nodes in the ACS cluster.</span></span>

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

### <span data-ttu-id="6a7f4-131">-GlobalServiceConfigurationAdditionalProperties</span><span class="sxs-lookup"><span data-stu-id="6a7f4-131">-GlobalServiceConfigurationAdditionalProperties</span></span>
<span data-ttu-id="6a7f4-132">A globális szolgáltatás konfigurációjának további tulajdonságai</span><span class="sxs-lookup"><span data-stu-id="6a7f4-132">Additional properties for the global service configuration.</span></span>

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

### <span data-ttu-id="6a7f4-133">-GlobalServiceConfigurationETag</span><span class="sxs-lookup"><span data-stu-id="6a7f4-133">-GlobalServiceConfigurationETag</span></span>
<span data-ttu-id="6a7f4-134">A frissítések beállítási ETag.</span><span class="sxs-lookup"><span data-stu-id="6a7f4-134">The configuration ETag for updates.</span></span>

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

### <span data-ttu-id="6a7f4-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6a7f4-135">-InputObject</span></span>
<span data-ttu-id="6a7f4-136">A operationalization-fürt tulajdonságai</span><span class="sxs-lookup"><span data-stu-id="6a7f4-136">The operationalization cluster properties.</span></span>

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

### <span data-ttu-id="6a7f4-137">-Hely</span><span class="sxs-lookup"><span data-stu-id="6a7f4-137">-Location</span></span>
<span data-ttu-id="6a7f4-138">A operationalization-fürt helye.</span><span class="sxs-lookup"><span data-stu-id="6a7f4-138">The operationalization cluster's location.</span></span>

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

### <span data-ttu-id="6a7f4-139">-MasterCount</span><span class="sxs-lookup"><span data-stu-id="6a7f4-139">-MasterCount</span></span>
<span data-ttu-id="6a7f4-140">A fő csomópontok száma az ACS-fürtben.</span><span class="sxs-lookup"><span data-stu-id="6a7f4-140">The number of master nodes in the ACS cluster.</span></span>

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

### <span data-ttu-id="6a7f4-141">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6a7f4-141">-Name</span></span>
<span data-ttu-id="6a7f4-142">A operationalization-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="6a7f4-142">The name of the operationalization cluster.</span></span>

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

### <span data-ttu-id="6a7f4-143">-OrchestratorType</span><span class="sxs-lookup"><span data-stu-id="6a7f4-143">-OrchestratorType</span></span>
<span data-ttu-id="6a7f4-144">Az ACS-fürt Orchestrator típusa.</span><span class="sxs-lookup"><span data-stu-id="6a7f4-144">The ACS cluster's orchestrator type.</span></span>

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

### <span data-ttu-id="6a7f4-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a7f4-145">-ResourceGroupName</span></span>
<span data-ttu-id="6a7f4-146">A operationalization-fürt erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6a7f4-146">The name of the resource group for the operationalization cluster.</span></span>

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

### <span data-ttu-id="6a7f4-147">-Secret</span><span class="sxs-lookup"><span data-stu-id="6a7f4-147">-Secret</span></span>
<span data-ttu-id="6a7f4-148">Az ACS-fürt Orchestrator szolgáltatásának fő titka.</span><span class="sxs-lookup"><span data-stu-id="6a7f4-148">The ACS cluster's orchestrator service principal secret.</span></span>

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

### <span data-ttu-id="6a7f4-149">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="6a7f4-149">-SslCertificate</span></span>
<span data-ttu-id="6a7f4-150">Az SSL-tanúsítványok a PEM formátumú, Base64-karakterláncként kódolt formában jelennek meg.</span><span class="sxs-lookup"><span data-stu-id="6a7f4-150">The SSL certificate data in PEM format encoded as base64 string.</span></span>

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

### <span data-ttu-id="6a7f4-151">-SslCName</span><span class="sxs-lookup"><span data-stu-id="6a7f4-151">-SslCName</span></span>
<span data-ttu-id="6a7f4-152">Az SSL-tanúsítvány CName rekordja.</span><span class="sxs-lookup"><span data-stu-id="6a7f4-152">The CName for the SSL certificate.</span></span>

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

### <span data-ttu-id="6a7f4-153">-SslKey</span><span class="sxs-lookup"><span data-stu-id="6a7f4-153">-SslKey</span></span>
<span data-ttu-id="6a7f4-154">A PEM formátumú SSL-kulcsok a Base64-karakterláncként kódolt formában jelennek meg.</span><span class="sxs-lookup"><span data-stu-id="6a7f4-154">The SSL key data in PEM format encoded as base64 string.</span></span>

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

### <span data-ttu-id="6a7f4-155">-SslStatus</span><span class="sxs-lookup"><span data-stu-id="6a7f4-155">-SslStatus</span></span>
<span data-ttu-id="6a7f4-156">SSL-állapot</span><span class="sxs-lookup"><span data-stu-id="6a7f4-156">SSL status.</span></span>
<span data-ttu-id="6a7f4-157">A lehetséges értékek "engedélyezve" és "Letiltva".</span><span class="sxs-lookup"><span data-stu-id="6a7f4-157">Possible values are 'Enabled' and 'Disabled'.</span></span>

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

### <span data-ttu-id="6a7f4-158">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="6a7f4-158">-StorageAccount</span></span>
<span data-ttu-id="6a7f4-159">A létrehozása helyett a tárolási fiók URI-ja.</span><span class="sxs-lookup"><span data-stu-id="6a7f4-159">The URI to the storage account to use instead of creating one.</span></span>

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

### <span data-ttu-id="6a7f4-160">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6a7f4-160">-Confirm</span></span>
<span data-ttu-id="6a7f4-161">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6a7f4-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a7f4-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a7f4-162">-WhatIf</span></span>
<span data-ttu-id="6a7f4-163">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6a7f4-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a7f4-164">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6a7f4-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a7f4-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a7f4-165">CommonParameters</span></span>
<span data-ttu-id="6a7f4-166">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6a7f4-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a7f4-167">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a7f4-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a7f4-168">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6a7f4-168">INPUTS</span></span>

### <span data-ttu-id="6a7f4-169">Nincs</span><span class="sxs-lookup"><span data-stu-id="6a7f4-169">None</span></span>

## <span data-ttu-id="6a7f4-170">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6a7f4-170">OUTPUTS</span></span>

### <span data-ttu-id="6a7f4-171">Microsoft. Azure. Command. MachineLearningCompute. models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="6a7f4-171">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

## <span data-ttu-id="6a7f4-172">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6a7f4-172">NOTES</span></span>

## <span data-ttu-id="6a7f4-173">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6a7f4-173">RELATED LINKS</span></span>
