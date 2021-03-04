---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azloadbalancerbackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPool.md
ms.openlocfilehash: 6e12cc4bb296a1c523547aebc44c6992dd2b687e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940130"
---
# <span data-ttu-id="07a87-101">Remove-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="07a87-101">Remove-AzLoadBalancerBackendAddressPool</span></span>

## <span data-ttu-id="07a87-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07a87-102">SYNOPSIS</span></span>
<span data-ttu-id="07a87-103">Háttérkészlet eltávolítása a terheléselosztásból</span><span class="sxs-lookup"><span data-stu-id="07a87-103">Removes a backend pool from a load balancer</span></span>

## <span data-ttu-id="07a87-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="07a87-104">SYNTAX</span></span>

### <span data-ttu-id="07a87-105">DeleteByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="07a87-105">DeleteByNameParameterSet</span></span>
```
Remove-AzLoadBalancerBackendAddressPool -ResourceGroupName <String> -Name <String> [-LoadBalancerName <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07a87-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="07a87-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzLoadBalancerBackendAddressPool -Name <String> [-LoadBalancerName <String>]
 -LoadBalancer <PSLoadBalancer> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="07a87-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="07a87-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzLoadBalancerBackendAddressPool [-LoadBalancerName <String>] [-InputObject <PSBackendAddressPool>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07a87-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="07a87-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzLoadBalancerBackendAddressPool [-LoadBalancerName <String>] -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07a87-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="07a87-109">DESCRIPTION</span></span>
<span data-ttu-id="07a87-110">Háttérkészlet eltávolítása a terheléselosztásból</span><span class="sxs-lookup"><span data-stu-id="07a87-110">Removes a backend pool from a load balancer</span></span>

## <span data-ttu-id="07a87-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="07a87-111">EXAMPLES</span></span>

### <span data-ttu-id="07a87-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="07a87-112">Example 1</span></span>
```powershell
##removing by passing lb object via pipeline
PS C:\> $lb | Remove-AzLoadBalancerBackendAddressPool -Name $backendPool1
```

### <span data-ttu-id="07a87-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="07a87-113">Example 2</span></span>
```powershell
##removing by passing input object
PS C:\> Remove-AzLoadBalancerBackendAddressPool -InputObject $backendPoolObject
```

### <span data-ttu-id="07a87-114">3. példa</span><span class="sxs-lookup"><span data-stu-id="07a87-114">Example 3</span></span>
```powershell
##removing by passing input object
PS C:\> Remove-AzLoadBalancerBackendAddressPool -ResourceId $backendPoolObject.Id
```

## <span data-ttu-id="07a87-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="07a87-115">PARAMETERS</span></span>

### <span data-ttu-id="07a87-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07a87-116">-DefaultProfile</span></span>
<span data-ttu-id="07a87-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="07a87-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07a87-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="07a87-118">-InputObject</span></span>
<span data-ttu-id="07a87-119">A háttércímkészlet eltávolítható</span><span class="sxs-lookup"><span data-stu-id="07a87-119">The backend address pool to remove</span></span>

```yaml
Type: PSBackendAddressPool
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07a87-120">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="07a87-120">-LoadBalancer</span></span>
<span data-ttu-id="07a87-121">A terheléselosztási erőforrás.</span><span class="sxs-lookup"><span data-stu-id="07a87-121">The load balancer resource.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="07a87-122">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="07a87-122">-LoadBalancerName</span></span>
<span data-ttu-id="07a87-123">A terheléselosztás neve.</span><span class="sxs-lookup"><span data-stu-id="07a87-123">The name of the load balancer.</span></span>

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

### <span data-ttu-id="07a87-124">-Name</span><span class="sxs-lookup"><span data-stu-id="07a87-124">-Name</span></span>
<span data-ttu-id="07a87-125">A terheléselosztás neve.</span><span class="sxs-lookup"><span data-stu-id="07a87-125">The name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: DeleteByNameParameterSet, DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07a87-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="07a87-126">-PassThru</span></span>
<span data-ttu-id="07a87-127">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="07a87-127">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="07a87-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07a87-128">-ResourceGroupName</span></span>
<span data-ttu-id="07a87-129">A terheléselosztás erőforráscsoportneve.</span><span class="sxs-lookup"><span data-stu-id="07a87-129">The resource group name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07a87-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="07a87-130">-ResourceId</span></span>

```yaml
Type: String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07a87-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="07a87-131">-Confirm</span></span>
<span data-ttu-id="07a87-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="07a87-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07a87-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07a87-133">-WhatIf</span></span>
<span data-ttu-id="07a87-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="07a87-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07a87-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="07a87-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07a87-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07a87-136">CommonParameters</span></span>
<span data-ttu-id="07a87-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07a87-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07a87-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="07a87-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07a87-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="07a87-139">INPUTS</span></span>

### <span data-ttu-id="07a87-140">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="07a87-140">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="07a87-141">System.String</span><span class="sxs-lookup"><span data-stu-id="07a87-141">System.String</span></span>

## <span data-ttu-id="07a87-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="07a87-142">OUTPUTS</span></span>

### <span data-ttu-id="07a87-143">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="07a87-143">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="07a87-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="07a87-144">NOTES</span></span>

## <span data-ttu-id="07a87-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="07a87-145">RELATED LINKS</span></span>
