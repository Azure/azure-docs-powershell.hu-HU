---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerbackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPool.md
ms.openlocfilehash: 691a45899480485f35164d4f18aea1595f70fbc9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202573"
---
# <span data-ttu-id="5db52-101">Remove-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="5db52-101">Remove-AzLoadBalancerBackendAddressPool</span></span>

## <span data-ttu-id="5db52-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5db52-102">SYNOPSIS</span></span>
<span data-ttu-id="5db52-103">Háttérkészlet eltávolítása a terheléselosztásból</span><span class="sxs-lookup"><span data-stu-id="5db52-103">Removes a backend pool from a load balancer</span></span>

## <span data-ttu-id="5db52-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5db52-104">SYNTAX</span></span>

### <span data-ttu-id="5db52-105">DeleteByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5db52-105">DeleteByNameParameterSet</span></span>
```
Remove-AzLoadBalancerBackendAddressPool -ResourceGroupName <String> -Name <String> [-LoadBalancerName <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5db52-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5db52-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzLoadBalancerBackendAddressPool -Name <String> [-LoadBalancerName <String>]
 -LoadBalancer <PSLoadBalancer> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5db52-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5db52-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzLoadBalancerBackendAddressPool [-LoadBalancerName <String>] [-InputObject <PSBackendAddressPool>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5db52-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5db52-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzLoadBalancerBackendAddressPool [-LoadBalancerName <String>] -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5db52-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5db52-109">DESCRIPTION</span></span>
<span data-ttu-id="5db52-110">Háttérkészlet eltávolítása a terheléselosztásból</span><span class="sxs-lookup"><span data-stu-id="5db52-110">Removes a backend pool from a load balancer</span></span>

## <span data-ttu-id="5db52-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5db52-111">EXAMPLES</span></span>

### <span data-ttu-id="5db52-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="5db52-112">Example 1</span></span>
```powershell
##removing by passing lb object via pipeline
PS C:\> $lb | Remove-AzLoadBalancerBackendAddressPool -Name $backendPool1
```

### <span data-ttu-id="5db52-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="5db52-113">Example 2</span></span>
```powershell
##removing by passing input object
PS C:\> Remove-AzLoadBalancerBackendAddressPool -InputObject $backendPoolObject
```

### <span data-ttu-id="5db52-114">3. példa</span><span class="sxs-lookup"><span data-stu-id="5db52-114">Example 3</span></span>
```powershell
##removing by passing input object
PS C:\> Remove-AzLoadBalancerBackendAddressPool -ResourceId $backendPoolObject.Id
```

## <span data-ttu-id="5db52-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5db52-115">PARAMETERS</span></span>

### <span data-ttu-id="5db52-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5db52-116">-DefaultProfile</span></span>
<span data-ttu-id="5db52-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5db52-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5db52-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5db52-118">-InputObject</span></span>
<span data-ttu-id="5db52-119">A háttércímkészlet eltávolítható</span><span class="sxs-lookup"><span data-stu-id="5db52-119">The backend address pool to remove</span></span>

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

### <span data-ttu-id="5db52-120">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5db52-120">-LoadBalancer</span></span>
<span data-ttu-id="5db52-121">A terheléselosztási erőforrás.</span><span class="sxs-lookup"><span data-stu-id="5db52-121">The load balancer resource.</span></span>

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

### <span data-ttu-id="5db52-122">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="5db52-122">-LoadBalancerName</span></span>
<span data-ttu-id="5db52-123">A terheléselosztás neve.</span><span class="sxs-lookup"><span data-stu-id="5db52-123">The name of the load balancer.</span></span>

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

### <span data-ttu-id="5db52-124">-Name</span><span class="sxs-lookup"><span data-stu-id="5db52-124">-Name</span></span>
<span data-ttu-id="5db52-125">A terheléselosztás neve.</span><span class="sxs-lookup"><span data-stu-id="5db52-125">The name of the load balancer.</span></span>

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

### <span data-ttu-id="5db52-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5db52-126">-PassThru</span></span>
<span data-ttu-id="5db52-127">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="5db52-127">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="5db52-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5db52-128">-ResourceGroupName</span></span>
<span data-ttu-id="5db52-129">A terheléselosztás erőforráscsoportneve.</span><span class="sxs-lookup"><span data-stu-id="5db52-129">The resource group name of the load balancer.</span></span>

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

### <span data-ttu-id="5db52-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5db52-130">-ResourceId</span></span>

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

### <span data-ttu-id="5db52-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5db52-131">-Confirm</span></span>
<span data-ttu-id="5db52-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="5db52-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5db52-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5db52-133">-WhatIf</span></span>
<span data-ttu-id="5db52-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="5db52-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5db52-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5db52-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5db52-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5db52-136">CommonParameters</span></span>
<span data-ttu-id="5db52-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5db52-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5db52-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5db52-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5db52-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5db52-139">INPUTS</span></span>

### <span data-ttu-id="5db52-140">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5db52-140">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="5db52-141">System.String</span><span class="sxs-lookup"><span data-stu-id="5db52-141">System.String</span></span>

## <span data-ttu-id="5db52-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5db52-142">OUTPUTS</span></span>

### <span data-ttu-id="5db52-143">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="5db52-143">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="5db52-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5db52-144">NOTES</span></span>

## <span data-ttu-id="5db52-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5db52-145">RELATED LINKS</span></span>
