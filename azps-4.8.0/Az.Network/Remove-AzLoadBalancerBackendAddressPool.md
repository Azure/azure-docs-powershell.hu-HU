---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerbackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPool.md
ms.openlocfilehash: 691a45899480485f35164d4f18aea1595f70fbc9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94172938"
---
# <span data-ttu-id="09ce0-101">Remove-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="09ce0-101">Remove-AzLoadBalancerBackendAddressPool</span></span>

## <span data-ttu-id="09ce0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="09ce0-102">SYNOPSIS</span></span>
<span data-ttu-id="09ce0-103">Backend-készlet eltávolítása a terheléselosztó webhelyről</span><span class="sxs-lookup"><span data-stu-id="09ce0-103">Removes a backend pool from a load balancer</span></span>

## <span data-ttu-id="09ce0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="09ce0-104">SYNTAX</span></span>

### <span data-ttu-id="09ce0-105">DeleteByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="09ce0-105">DeleteByNameParameterSet</span></span>
```
Remove-AzLoadBalancerBackendAddressPool -ResourceGroupName <String> -Name <String> [-LoadBalancerName <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09ce0-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="09ce0-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzLoadBalancerBackendAddressPool -Name <String> [-LoadBalancerName <String>]
 -LoadBalancer <PSLoadBalancer> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="09ce0-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="09ce0-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzLoadBalancerBackendAddressPool [-LoadBalancerName <String>] [-InputObject <PSBackendAddressPool>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09ce0-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="09ce0-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzLoadBalancerBackendAddressPool [-LoadBalancerName <String>] -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09ce0-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="09ce0-109">DESCRIPTION</span></span>
<span data-ttu-id="09ce0-110">Backend-készlet eltávolítása a terheléselosztó webhelyről</span><span class="sxs-lookup"><span data-stu-id="09ce0-110">Removes a backend pool from a load balancer</span></span>

## <span data-ttu-id="09ce0-111">Példák</span><span class="sxs-lookup"><span data-stu-id="09ce0-111">EXAMPLES</span></span>

### <span data-ttu-id="09ce0-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="09ce0-112">Example 1</span></span>
```powershell
##removing by passing lb object via pipeline
PS C:\> $lb | Remove-AzLoadBalancerBackendAddressPool -Name $backendPool1
```

### <span data-ttu-id="09ce0-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="09ce0-113">Example 2</span></span>
```powershell
##removing by passing input object
PS C:\> Remove-AzLoadBalancerBackendAddressPool -InputObject $backendPoolObject
```

### <span data-ttu-id="09ce0-114">3. példa</span><span class="sxs-lookup"><span data-stu-id="09ce0-114">Example 3</span></span>
```powershell
##removing by passing input object
PS C:\> Remove-AzLoadBalancerBackendAddressPool -ResourceId $backendPoolObject.Id
```

## <span data-ttu-id="09ce0-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="09ce0-115">PARAMETERS</span></span>

### <span data-ttu-id="09ce0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09ce0-116">-DefaultProfile</span></span>
<span data-ttu-id="09ce0-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="09ce0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09ce0-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="09ce0-118">-InputObject</span></span>
<span data-ttu-id="09ce0-119">Az eltávolítandó backend-címkészlet</span><span class="sxs-lookup"><span data-stu-id="09ce0-119">The backend address pool to remove</span></span>

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

### <span data-ttu-id="09ce0-120">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="09ce0-120">-LoadBalancer</span></span>
<span data-ttu-id="09ce0-121">A terheléselosztó erőforrás.</span><span class="sxs-lookup"><span data-stu-id="09ce0-121">The load balancer resource.</span></span>

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

### <span data-ttu-id="09ce0-122">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="09ce0-122">-LoadBalancerName</span></span>
<span data-ttu-id="09ce0-123">A terheléselosztó neve.</span><span class="sxs-lookup"><span data-stu-id="09ce0-123">The name of the load balancer.</span></span>

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

### <span data-ttu-id="09ce0-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="09ce0-124">-Name</span></span>
<span data-ttu-id="09ce0-125">A terheléselosztó neve.</span><span class="sxs-lookup"><span data-stu-id="09ce0-125">The name of the load balancer.</span></span>

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

### <span data-ttu-id="09ce0-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="09ce0-126">-PassThru</span></span>
<span data-ttu-id="09ce0-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="09ce0-127">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="09ce0-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09ce0-128">-ResourceGroupName</span></span>
<span data-ttu-id="09ce0-129">Az erőforráscsoport neve a terheléselosztó csoportban.</span><span class="sxs-lookup"><span data-stu-id="09ce0-129">The resource group name of the load balancer.</span></span>

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

### <span data-ttu-id="09ce0-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="09ce0-130">-ResourceId</span></span>

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

### <span data-ttu-id="09ce0-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="09ce0-131">-Confirm</span></span>
<span data-ttu-id="09ce0-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="09ce0-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09ce0-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09ce0-133">-WhatIf</span></span>
<span data-ttu-id="09ce0-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="09ce0-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09ce0-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="09ce0-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09ce0-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09ce0-136">CommonParameters</span></span>
<span data-ttu-id="09ce0-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="09ce0-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09ce0-138">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="09ce0-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09ce0-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="09ce0-139">INPUTS</span></span>

### <span data-ttu-id="09ce0-140">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="09ce0-140">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="09ce0-141">System. String</span><span class="sxs-lookup"><span data-stu-id="09ce0-141">System.String</span></span>

## <span data-ttu-id="09ce0-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="09ce0-142">OUTPUTS</span></span>

### <span data-ttu-id="09ce0-143">Microsoft. Azure. commands. Network. models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="09ce0-143">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="09ce0-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="09ce0-144">NOTES</span></span>

## <span data-ttu-id="09ce0-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="09ce0-145">RELATED LINKS</span></span>
