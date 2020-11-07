---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Remove-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Remove-AzureRmMlOpCluster.md
ms.openlocfilehash: 63e401c09a2d224b53d260855990198a409d4846
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93673107"
---
# <span data-ttu-id="58a18-101">Remove-AzureRmMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="58a18-101">Remove-AzureRmMlOpCluster</span></span>

## <span data-ttu-id="58a18-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="58a18-102">SYNOPSIS</span></span>
<span data-ttu-id="58a18-103">Eltávolít egy operationalization-fürtöt.</span><span class="sxs-lookup"><span data-stu-id="58a18-103">Removes an operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58a18-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="58a18-104">SYNTAX</span></span>

### <span data-ttu-id="58a18-105">Operationalization-fürt eltávolítása a parancsmag bemeneti paramétereivel</span><span class="sxs-lookup"><span data-stu-id="58a18-105">Remove an operationalization cluster from cmdlet input parameters.</span></span>
```
Remove-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="58a18-106">Operationalization-fürt eltávolítása OperationalizationCluster-példányból</span><span class="sxs-lookup"><span data-stu-id="58a18-106">Remove an operationalization cluster from an OperationalizationCluster instance definition.</span></span>
```
Remove-AzureRmMlOpCluster -InputObject <PSOperationalizationCluster> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="58a18-107">Operationalization-fürt eltávolítása Azure Resouce-azonosítóból.</span><span class="sxs-lookup"><span data-stu-id="58a18-107">Remove an operationalization cluster from an Azure resouce id.</span></span>
```
Remove-AzureRmMlOpCluster -ResourceId <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="58a18-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="58a18-108">DESCRIPTION</span></span>
<span data-ttu-id="58a18-109">Eltávolít egy operationalization-fürtöt.</span><span class="sxs-lookup"><span data-stu-id="58a18-109">Removes an operationalization cluster.</span></span> <span data-ttu-id="58a18-110">Előfordulhat, hogy a fürthöz társított egyes erőforrások nem törlődnek.</span><span class="sxs-lookup"><span data-stu-id="58a18-110">Some resources associated with the cluster might not all be removed.</span></span> <span data-ttu-id="58a18-111">Az Azure Container szolgáltatás például eltűnik, de a hozzájuk tartozó VMs nem.</span><span class="sxs-lookup"><span data-stu-id="58a18-111">For example, the Azure container service will get removed, but the associated VMs do not.</span></span> <span data-ttu-id="58a18-112">A tárolási fiók, a tároló-nyilvántartó és az alkalmazás-elemzések nem törlődnek diagnosztikai adatok esetében.</span><span class="sxs-lookup"><span data-stu-id="58a18-112">The storage account, container registry, and application insights are not removed for diagnostic information.</span></span>

## <span data-ttu-id="58a18-113">Példák</span><span class="sxs-lookup"><span data-stu-id="58a18-113">EXAMPLES</span></span>

### <span data-ttu-id="58a18-114">Példa 1</span><span class="sxs-lookup"><span data-stu-id="58a18-114">Example 1</span></span>
```
PS C:\> Remove-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster
```

### <span data-ttu-id="58a18-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="58a18-115">Example 2</span></span>
```
PS C:\> Get-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster | Remove-AzureRmMlOpCluster 
```

## <span data-ttu-id="58a18-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="58a18-116">PARAMETERS</span></span>

### <span data-ttu-id="58a18-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="58a18-117">-InputObject</span></span>
<span data-ttu-id="58a18-118">A operationalization cluster objektum</span><span class="sxs-lookup"><span data-stu-id="58a18-118">The operationalization cluster object.</span></span>

```yaml
Type: PSOperationalizationCluster
Parameter Sets: Remove an operationalization cluster from an OperationalizationCluster instance definition.
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="58a18-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="58a18-119">-Confirm</span></span>
<span data-ttu-id="58a18-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="58a18-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58a18-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="58a18-121">-Name</span></span>
<span data-ttu-id="58a18-122">A operationalization-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="58a18-122">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Remove an operationalization cluster from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58a18-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58a18-123">-ResourceGroupName</span></span>
<span data-ttu-id="58a18-124">A operationalization-fürt erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="58a18-124">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Remove an operationalization cluster from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58a18-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="58a18-125">-ResourceId</span></span>
<span data-ttu-id="58a18-126">Az Azure Resource id a operationalization-fürthöz.</span><span class="sxs-lookup"><span data-stu-id="58a18-126">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Remove an operationalization cluster from an Azure resouce id.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58a18-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58a18-127">-WhatIf</span></span>
<span data-ttu-id="58a18-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="58a18-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58a18-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="58a18-129">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="58a18-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="58a18-130">INPUTS</span></span>

### <span data-ttu-id="58a18-131">Microsoft. Azure. Command. MachineLearningCompute. models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="58a18-131">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>
### <span data-ttu-id="58a18-132">System. String</span><span class="sxs-lookup"><span data-stu-id="58a18-132">System.String</span></span>


## <span data-ttu-id="58a18-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="58a18-133">OUTPUTS</span></span>

### <span data-ttu-id="58a18-134">System. Void</span><span class="sxs-lookup"><span data-stu-id="58a18-134">System.Void</span></span>


## <span data-ttu-id="58a18-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="58a18-135">NOTES</span></span>

## <span data-ttu-id="58a18-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="58a18-136">RELATED LINKS</span></span>

