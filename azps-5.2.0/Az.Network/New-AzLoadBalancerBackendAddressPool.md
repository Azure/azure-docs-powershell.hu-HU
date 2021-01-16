---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerbackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressPool.md
ms.openlocfilehash: e106656124aea48dff6c7fd7183027e183dce93b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341333"
---
# <span data-ttu-id="fd456-101">New-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="fd456-101">New-AzLoadBalancerBackendAddressPool</span></span>

## <span data-ttu-id="fd456-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd456-102">SYNOPSIS</span></span>
<span data-ttu-id="fd456-103">Háttércímkészletet hoz létre egy loadbalancer eszközben.</span><span class="sxs-lookup"><span data-stu-id="fd456-103">Creates a backend address pool on a loadbalancer.</span></span> 

## <span data-ttu-id="fd456-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fd456-104">SYNTAX</span></span>

### <span data-ttu-id="fd456-105">CreateByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd456-105">CreateByNameParameterSet</span></span>
```
New-AzLoadBalancerBackendAddressPool -ResourceGroupName <String> -LoadBalancerName <String> -Name <String>
 [-LoadBalancerBackendAddress <PSLoadBalancerBackendAddress[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd456-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd456-106">CreateByParentObjectParameterSet</span></span>
```
New-AzLoadBalancerBackendAddressPool -LoadBalancer <PSLoadBalancer> -Name <String>
 [-LoadBalancerBackendAddress <PSLoadBalancerBackendAddress[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd456-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fd456-107">DESCRIPTION</span></span>
<span data-ttu-id="fd456-108">Háttércímkészletet hoz létre egy loadbalancer eszközben.</span><span class="sxs-lookup"><span data-stu-id="fd456-108">Creates a backend address pool on a loadbalancer.</span></span> <span data-ttu-id="fd456-109">Lehetővé teszi a PSLoadBalancerBackendAddress tömbje megírását.</span><span class="sxs-lookup"><span data-stu-id="fd456-109">Allows for specifiying a array of PSLoadBalancerBackendAddress.</span></span> 
## <span data-ttu-id="fd456-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fd456-110">EXAMPLES</span></span>

### <span data-ttu-id="fd456-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="fd456-111">Example 1</span></span>
```powershell
## create by passing loadbalancer without Ips
PS C:\> $virtualNetwork = Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroup
PS C:\> $lb = Get-AzLoadBalancer -ResourceGroupName $resourceGroup -Name $loadBalancerName
PS C:\> $ip1 = New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.5" -Name "TestVNetRef" -VirtualNetworkId $virtualNetwork.Id
PS C:\> $ip2 = New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.6" -Name "TestVNetRef2" -VirtualNetworkId $virtualNetwork.Id
PS C:\> $ips = @($ip1, $ip2)

PS C:\> $lb | New-AzLoadBalancerBackendAddressPool -Name $backendPool1
```

### <span data-ttu-id="fd456-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="fd456-112">Example 2</span></span>
```powershell
## create by passing loadbalancer with ips
PS C:\> $lb | New-AzLoadBalancerBackendAddressPool -Name $backendPool7 -LoadBalancerBackendAddress $ips
```

### <span data-ttu-id="fd456-113">3. példa</span><span class="sxs-lookup"><span data-stu-id="fd456-113">Example 3</span></span>
```powershell
## create by name without ips
PS C:\> New-AzLoadBalancerBackendAddressPool -ResourceGroupName $resourceGroup -LoadBalancerName $loadBalancerName -Name $backendPool3
```

### <span data-ttu-id="fd456-114">4. példa</span><span class="sxs-lookup"><span data-stu-id="fd456-114">Example 4</span></span>
```powershell
## create by name with ips
PS C:\> New-AzLoadBalancerBackendAddressPool -ResourceGroupName $resourceGroup -LoadBalancerName $loadBalancerName -Name $backendPool3 -LoadBalancerBackendAddress $ips
```

## <span data-ttu-id="fd456-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fd456-115">PARAMETERS</span></span>

### <span data-ttu-id="fd456-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd456-116">-DefaultProfile</span></span>
<span data-ttu-id="fd456-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fd456-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd456-118">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="fd456-118">-LoadBalancer</span></span>
<span data-ttu-id="fd456-119">A terheléselosztási erőforrás.</span><span class="sxs-lookup"><span data-stu-id="fd456-119">The load balancer resource.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd456-120">-LoadBalancerBackendAddress</span><span class="sxs-lookup"><span data-stu-id="fd456-120">-LoadBalancerBackendAddress</span></span>
<span data-ttu-id="fd456-121">A háttércímek.</span><span class="sxs-lookup"><span data-stu-id="fd456-121">The backend addresses.</span></span>

```yaml
Type: PSLoadBalancerBackendAddress[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd456-122">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="fd456-122">-LoadBalancerName</span></span>
<span data-ttu-id="fd456-123">A terheléselosztás neve.</span><span class="sxs-lookup"><span data-stu-id="fd456-123">The name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd456-124">-Name</span><span class="sxs-lookup"><span data-stu-id="fd456-124">-Name</span></span>
<span data-ttu-id="fd456-125">A háttérkészlet neve.</span><span class="sxs-lookup"><span data-stu-id="fd456-125">The name of the backend pool.</span></span>

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

### <span data-ttu-id="fd456-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd456-126">-ResourceGroupName</span></span>
<span data-ttu-id="fd456-127">A terheléselosztás erőforráscsoportneve.</span><span class="sxs-lookup"><span data-stu-id="fd456-127">The resource group name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd456-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fd456-128">-Confirm</span></span>
<span data-ttu-id="fd456-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="fd456-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd456-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd456-130">-WhatIf</span></span>
<span data-ttu-id="fd456-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="fd456-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd456-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fd456-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd456-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd456-133">CommonParameters</span></span>
<span data-ttu-id="fd456-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd456-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd456-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fd456-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd456-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fd456-136">INPUTS</span></span>

### <span data-ttu-id="fd456-137">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="fd456-137">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="fd456-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fd456-138">OUTPUTS</span></span>

### <span data-ttu-id="fd456-139">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="fd456-139">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="fd456-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fd456-140">NOTES</span></span>

## <span data-ttu-id="fd456-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fd456-141">RELATED LINKS</span></span>
