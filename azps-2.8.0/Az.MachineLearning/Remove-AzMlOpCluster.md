---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearningCompute.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/remove-azmlopcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlOpCluster.md
ms.openlocfilehash: de297c94be69773d07efedfae42ccc029fc13414
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93665962"
---
# <span data-ttu-id="79cc2-101">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="79cc2-101">Remove-AzMlOpCluster</span></span>

## <span data-ttu-id="79cc2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="79cc2-102">SYNOPSIS</span></span>
<span data-ttu-id="79cc2-103">Eltávolít egy operationalization-fürtöt.</span><span class="sxs-lookup"><span data-stu-id="79cc2-103">Removes an operationalization cluster.</span></span>

## <span data-ttu-id="79cc2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="79cc2-104">SYNTAX</span></span>

### <span data-ttu-id="79cc2-105">RemoveByNameAndResourceGroup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="79cc2-105">RemoveByNameAndResourceGroup (Default)</span></span>
```
Remove-AzMlOpCluster -ResourceGroupName <String> -Name <String> [-IncludeAllResources]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79cc2-106">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="79cc2-106">RemoveByInputObject</span></span>
```
Remove-AzMlOpCluster -InputObject <PSOperationalizationCluster> [-IncludeAllResources]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79cc2-107">RemoveByResourceId</span><span class="sxs-lookup"><span data-stu-id="79cc2-107">RemoveByResourceId</span></span>
```
Remove-AzMlOpCluster -ResourceId <String> [-IncludeAllResources] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79cc2-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="79cc2-108">DESCRIPTION</span></span>
<span data-ttu-id="79cc2-109">Eltávolít egy operationalization-fürtöt.</span><span class="sxs-lookup"><span data-stu-id="79cc2-109">Removes an operationalization cluster.</span></span> <span data-ttu-id="79cc2-110">Előfordulhat, hogy a fürthöz társított egyes erőforrások nem törlődnek.</span><span class="sxs-lookup"><span data-stu-id="79cc2-110">Some resources associated with the cluster might not all be removed.</span></span> <span data-ttu-id="79cc2-111">Az Azure Container szolgáltatás például eltűnik, de a hozzájuk tartozó VMs nem.</span><span class="sxs-lookup"><span data-stu-id="79cc2-111">For example, the Azure container service will get removed, but the associated VMs do not.</span></span> <span data-ttu-id="79cc2-112">A tárolási fiók, a tároló-nyilvántartó és az alkalmazás-elemzések nem törlődnek diagnosztikai adatok esetében.</span><span class="sxs-lookup"><span data-stu-id="79cc2-112">The storage account, container registry, and application insights are not removed for diagnostic information.</span></span>

## <span data-ttu-id="79cc2-113">Példák</span><span class="sxs-lookup"><span data-stu-id="79cc2-113">EXAMPLES</span></span>

### <span data-ttu-id="79cc2-114">Példa 1</span><span class="sxs-lookup"><span data-stu-id="79cc2-114">Example 1</span></span>
```
PS C:\> Remove-AzMlOpCluster -ResourceGroupName my-group -Name my-cluster
```

### <span data-ttu-id="79cc2-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="79cc2-115">Example 2</span></span>
```
PS C:\> Get-AzMlOpCluster -ResourceGroupName my-group -Name my-cluster | Remove-AzMlOpCluster
```

## <span data-ttu-id="79cc2-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="79cc2-116">PARAMETERS</span></span>

### <span data-ttu-id="79cc2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79cc2-117">-DefaultProfile</span></span>
<span data-ttu-id="79cc2-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="79cc2-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79cc2-119">-IncludeAllResources</span><span class="sxs-lookup"><span data-stu-id="79cc2-119">-IncludeAllResources</span></span>
<span data-ttu-id="79cc2-120">Eltávolítja a fürttel létrehozott összes erőforrást.</span><span class="sxs-lookup"><span data-stu-id="79cc2-120">Removes all resources that were created with the cluster.</span></span>

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

### <span data-ttu-id="79cc2-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="79cc2-121">-InputObject</span></span>
<span data-ttu-id="79cc2-122">A operationalization cluster objektum</span><span class="sxs-lookup"><span data-stu-id="79cc2-122">The operationalization cluster object.</span></span>

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

### <span data-ttu-id="79cc2-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="79cc2-123">-Name</span></span>
<span data-ttu-id="79cc2-124">A operationalization-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="79cc2-124">The name of the operationalization cluster.</span></span>

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

### <span data-ttu-id="79cc2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79cc2-125">-ResourceGroupName</span></span>
<span data-ttu-id="79cc2-126">A operationalization-fürt erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="79cc2-126">The name of the resource group for the operationalization cluster.</span></span>

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

### <span data-ttu-id="79cc2-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="79cc2-127">-ResourceId</span></span>
<span data-ttu-id="79cc2-128">Az Azure Resource id a operationalization-fürthöz.</span><span class="sxs-lookup"><span data-stu-id="79cc2-128">The Azure resource id for the operationalization cluster.</span></span>

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

### <span data-ttu-id="79cc2-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="79cc2-129">-Confirm</span></span>
<span data-ttu-id="79cc2-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="79cc2-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79cc2-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79cc2-131">-WhatIf</span></span>
<span data-ttu-id="79cc2-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="79cc2-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79cc2-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="79cc2-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79cc2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79cc2-134">CommonParameters</span></span>
<span data-ttu-id="79cc2-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="79cc2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79cc2-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79cc2-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79cc2-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="79cc2-137">INPUTS</span></span>

### <span data-ttu-id="79cc2-138">Microsoft. Azure. Command. MachineLearningCompute. models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="79cc2-138">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

### <span data-ttu-id="79cc2-139">System. String</span><span class="sxs-lookup"><span data-stu-id="79cc2-139">System.String</span></span>

## <span data-ttu-id="79cc2-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="79cc2-140">OUTPUTS</span></span>

### <span data-ttu-id="79cc2-141">System. Void</span><span class="sxs-lookup"><span data-stu-id="79cc2-141">System.Void</span></span>

## <span data-ttu-id="79cc2-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="79cc2-142">NOTES</span></span>

## <span data-ttu-id="79cc2-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="79cc2-143">RELATED LINKS</span></span>
