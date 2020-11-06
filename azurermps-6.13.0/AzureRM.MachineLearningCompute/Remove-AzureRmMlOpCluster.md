---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearningcompute/remove-azurermmlopcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Remove-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Remove-AzureRmMlOpCluster.md
ms.openlocfilehash: 5619b9ca4e7f5593a20baf04951d0d5594b31215
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493674"
---
# <span data-ttu-id="92fd7-101">Remove-AzureRmMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="92fd7-101">Remove-AzureRmMlOpCluster</span></span>

## <span data-ttu-id="92fd7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="92fd7-102">SYNOPSIS</span></span>
<span data-ttu-id="92fd7-103">Eltávolít egy operationalization-fürtöt.</span><span class="sxs-lookup"><span data-stu-id="92fd7-103">Removes an operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="92fd7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="92fd7-104">SYNTAX</span></span>

### <span data-ttu-id="92fd7-105">RemoveByNameAndResourceGroup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="92fd7-105">RemoveByNameAndResourceGroup (Default)</span></span>
```
Remove-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> [-IncludeAllResources]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92fd7-106">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="92fd7-106">RemoveByInputObject</span></span>
```
Remove-AzureRmMlOpCluster -InputObject <PSOperationalizationCluster> [-IncludeAllResources]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92fd7-107">RemoveByResourceId</span><span class="sxs-lookup"><span data-stu-id="92fd7-107">RemoveByResourceId</span></span>
```
Remove-AzureRmMlOpCluster -ResourceId <String> [-IncludeAllResources]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92fd7-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="92fd7-108">DESCRIPTION</span></span>
<span data-ttu-id="92fd7-109">Eltávolít egy operationalization-fürtöt.</span><span class="sxs-lookup"><span data-stu-id="92fd7-109">Removes an operationalization cluster.</span></span> <span data-ttu-id="92fd7-110">Előfordulhat, hogy a fürthöz társított egyes erőforrások nem törlődnek.</span><span class="sxs-lookup"><span data-stu-id="92fd7-110">Some resources associated with the cluster might not all be removed.</span></span> <span data-ttu-id="92fd7-111">Az Azure Container szolgáltatás például eltűnik, de a hozzájuk tartozó VMs nem.</span><span class="sxs-lookup"><span data-stu-id="92fd7-111">For example, the Azure container service will get removed, but the associated VMs do not.</span></span> <span data-ttu-id="92fd7-112">A tárolási fiók, a tároló-nyilvántartó és az alkalmazás-elemzések nem törlődnek diagnosztikai adatok esetében.</span><span class="sxs-lookup"><span data-stu-id="92fd7-112">The storage account, container registry, and application insights are not removed for diagnostic information.</span></span>

## <span data-ttu-id="92fd7-113">Példák</span><span class="sxs-lookup"><span data-stu-id="92fd7-113">EXAMPLES</span></span>

### <span data-ttu-id="92fd7-114">Példa 1</span><span class="sxs-lookup"><span data-stu-id="92fd7-114">Example 1</span></span>
```
PS C:\> Remove-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster
```

### <span data-ttu-id="92fd7-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="92fd7-115">Example 2</span></span>
```
PS C:\> Get-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster | Remove-AzureRmMlOpCluster
```

## <span data-ttu-id="92fd7-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="92fd7-116">PARAMETERS</span></span>

### <span data-ttu-id="92fd7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92fd7-117">-DefaultProfile</span></span>
<span data-ttu-id="92fd7-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="92fd7-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92fd7-119">-IncludeAllResources</span><span class="sxs-lookup"><span data-stu-id="92fd7-119">-IncludeAllResources</span></span>
<span data-ttu-id="92fd7-120">Eltávolítja a fürttel létrehozott összes erőforrást.</span><span class="sxs-lookup"><span data-stu-id="92fd7-120">Removes all resources that were created with the cluster.</span></span>

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

### <span data-ttu-id="92fd7-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="92fd7-121">-InputObject</span></span>
<span data-ttu-id="92fd7-122">A operationalization cluster objektum</span><span class="sxs-lookup"><span data-stu-id="92fd7-122">The operationalization cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster
Parameter Sets: RemoveByInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="92fd7-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="92fd7-123">-Name</span></span>
<span data-ttu-id="92fd7-124">A operationalization-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="92fd7-124">The name of the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92fd7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92fd7-125">-ResourceGroupName</span></span>
<span data-ttu-id="92fd7-126">A operationalization-fürt erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="92fd7-126">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92fd7-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="92fd7-127">-ResourceId</span></span>
<span data-ttu-id="92fd7-128">Az Azure Resource id a operationalization-fürthöz.</span><span class="sxs-lookup"><span data-stu-id="92fd7-128">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92fd7-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="92fd7-129">-Confirm</span></span>
<span data-ttu-id="92fd7-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="92fd7-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92fd7-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92fd7-131">-WhatIf</span></span>
<span data-ttu-id="92fd7-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="92fd7-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92fd7-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="92fd7-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92fd7-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92fd7-134">CommonParameters</span></span>
<span data-ttu-id="92fd7-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="92fd7-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92fd7-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92fd7-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92fd7-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="92fd7-137">INPUTS</span></span>

### <span data-ttu-id="92fd7-138">Microsoft. Azure. Command. MachineLearningCompute. models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="92fd7-138">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>
<span data-ttu-id="92fd7-139">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="92fd7-139">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="92fd7-140">System. String</span><span class="sxs-lookup"><span data-stu-id="92fd7-140">System.String</span></span>

## <span data-ttu-id="92fd7-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="92fd7-141">OUTPUTS</span></span>

### <span data-ttu-id="92fd7-142">System. Void</span><span class="sxs-lookup"><span data-stu-id="92fd7-142">System.Void</span></span>

## <span data-ttu-id="92fd7-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="92fd7-143">NOTES</span></span>

## <span data-ttu-id="92fd7-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="92fd7-144">RELATED LINKS</span></span>
