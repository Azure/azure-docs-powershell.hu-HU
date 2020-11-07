---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearningcompute/remove-azurermmlopcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Remove-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Remove-AzureRmMlOpCluster.md
ms.openlocfilehash: 9836856ffd663939de8ca0e28635d81785c9c898
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/21/2020
ms.locfileid: "93680918"
---
# <span data-ttu-id="dfe3f-101">Remove-AzureRmMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="dfe3f-101">Remove-AzureRmMlOpCluster</span></span>

## <span data-ttu-id="dfe3f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dfe3f-102">SYNOPSIS</span></span>
<span data-ttu-id="dfe3f-103">Eltávolít egy operationalization-fürtöt.</span><span class="sxs-lookup"><span data-stu-id="dfe3f-103">Removes an operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dfe3f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dfe3f-104">SYNTAX</span></span>

### <span data-ttu-id="dfe3f-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="dfe3f-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeAllResources] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dfe3f-106">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="dfe3f-106">RemoveByInputObject</span></span>
```
Remove-AzureRmMlOpCluster -InputObject <PSOperationalizationCluster> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeAllResources] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dfe3f-107">RemoveByResourceId</span><span class="sxs-lookup"><span data-stu-id="dfe3f-107">RemoveByResourceId</span></span>
```
Remove-AzureRmMlOpCluster -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeAllResources] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dfe3f-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="dfe3f-108">DESCRIPTION</span></span>
<span data-ttu-id="dfe3f-109">Eltávolít egy operationalization-fürtöt.</span><span class="sxs-lookup"><span data-stu-id="dfe3f-109">Removes an operationalization cluster.</span></span> <span data-ttu-id="dfe3f-110">Előfordulhat, hogy a fürthöz társított egyes erőforrások nem törlődnek.</span><span class="sxs-lookup"><span data-stu-id="dfe3f-110">Some resources associated with the cluster might not all be removed.</span></span> <span data-ttu-id="dfe3f-111">Az Azure Container szolgáltatás például eltűnik, de a hozzájuk tartozó VMs nem.</span><span class="sxs-lookup"><span data-stu-id="dfe3f-111">For example, the Azure container service will get removed, but the associated VMs do not.</span></span> <span data-ttu-id="dfe3f-112">A tárolási fiók, a tároló-nyilvántartó és az alkalmazás-elemzések nem törlődnek diagnosztikai adatok esetében.</span><span class="sxs-lookup"><span data-stu-id="dfe3f-112">The storage account, container registry, and application insights are not removed for diagnostic information.</span></span>

## <span data-ttu-id="dfe3f-113">Példák</span><span class="sxs-lookup"><span data-stu-id="dfe3f-113">EXAMPLES</span></span>

### <span data-ttu-id="dfe3f-114">Példa 1</span><span class="sxs-lookup"><span data-stu-id="dfe3f-114">Example 1</span></span>
```
PS C:\> Remove-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster
```

### <span data-ttu-id="dfe3f-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="dfe3f-115">Example 2</span></span>
```
PS C:\> Get-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster | Remove-AzureRmMlOpCluster
```

## <span data-ttu-id="dfe3f-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dfe3f-116">PARAMETERS</span></span>

### <span data-ttu-id="dfe3f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfe3f-117">-DefaultProfile</span></span>
<span data-ttu-id="dfe3f-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dfe3f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dfe3f-119">-IncludeAllResources</span><span class="sxs-lookup"><span data-stu-id="dfe3f-119">-IncludeAllResources</span></span>
<span data-ttu-id="dfe3f-120">Eltávolítja a fürttel létrehozott összes erőforrást.</span><span class="sxs-lookup"><span data-stu-id="dfe3f-120">Removes all resources that were created with the cluster.</span></span>

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

### <span data-ttu-id="dfe3f-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dfe3f-121">-InputObject</span></span>
<span data-ttu-id="dfe3f-122">A operationalization cluster objektum</span><span class="sxs-lookup"><span data-stu-id="dfe3f-122">The operationalization cluster object.</span></span>

```yaml
Type: PSOperationalizationCluster
Parameter Sets: RemoveByInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dfe3f-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="dfe3f-123">-Name</span></span>
<span data-ttu-id="dfe3f-124">A operationalization-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="dfe3f-124">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfe3f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfe3f-125">-ResourceGroupName</span></span>
<span data-ttu-id="dfe3f-126">A operationalization-fürt erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="dfe3f-126">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfe3f-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dfe3f-127">-ResourceId</span></span>
<span data-ttu-id="dfe3f-128">Az Azure Resource id a operationalization-fürthöz.</span><span class="sxs-lookup"><span data-stu-id="dfe3f-128">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dfe3f-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="dfe3f-129">-Confirm</span></span>
<span data-ttu-id="dfe3f-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="dfe3f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dfe3f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfe3f-131">-WhatIf</span></span>
<span data-ttu-id="dfe3f-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="dfe3f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dfe3f-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="dfe3f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dfe3f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfe3f-134">CommonParameters</span></span>
<span data-ttu-id="dfe3f-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dfe3f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfe3f-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dfe3f-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfe3f-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dfe3f-137">INPUTS</span></span>

### <span data-ttu-id="dfe3f-138">Microsoft. Azure. Command. MachineLearningCompute. models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="dfe3f-138">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

### <span data-ttu-id="dfe3f-139">System. String</span><span class="sxs-lookup"><span data-stu-id="dfe3f-139">System.String</span></span>

## <span data-ttu-id="dfe3f-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dfe3f-140">OUTPUTS</span></span>

### <span data-ttu-id="dfe3f-141">System. Void</span><span class="sxs-lookup"><span data-stu-id="dfe3f-141">System.Void</span></span>

## <span data-ttu-id="dfe3f-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dfe3f-142">NOTES</span></span>

## <span data-ttu-id="dfe3f-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dfe3f-143">RELATED LINKS</span></span>

