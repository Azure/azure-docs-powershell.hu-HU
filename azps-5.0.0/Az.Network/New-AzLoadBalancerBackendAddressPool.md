---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerbackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressPool.md
ms.openlocfilehash: e106656124aea48dff6c7fd7183027e183dce93b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193969"
---
# <span data-ttu-id="0fcc2-101">New-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="0fcc2-101">New-AzLoadBalancerBackendAddressPool</span></span>

## <span data-ttu-id="0fcc2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0fcc2-102">SYNOPSIS</span></span>
<span data-ttu-id="0fcc2-103">Backend-címkészletet hoz létre egy loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="0fcc2-103">Creates a backend address pool on a loadbalancer.</span></span> 

## <span data-ttu-id="0fcc2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0fcc2-104">SYNTAX</span></span>

### <span data-ttu-id="0fcc2-105">CreateByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0fcc2-105">CreateByNameParameterSet</span></span>
```
New-AzLoadBalancerBackendAddressPool -ResourceGroupName <String> -LoadBalancerName <String> -Name <String>
 [-LoadBalancerBackendAddress <PSLoadBalancerBackendAddress[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0fcc2-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0fcc2-106">CreateByParentObjectParameterSet</span></span>
```
New-AzLoadBalancerBackendAddressPool -LoadBalancer <PSLoadBalancer> -Name <String>
 [-LoadBalancerBackendAddress <PSLoadBalancerBackendAddress[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0fcc2-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="0fcc2-107">DESCRIPTION</span></span>
<span data-ttu-id="0fcc2-108">Backend-címkészletet hoz létre egy loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="0fcc2-108">Creates a backend address pool on a loadbalancer.</span></span> <span data-ttu-id="0fcc2-109">Lehetővé teszi a specifiying egy tömb PSLoadBalancerBackendAddress.</span><span class="sxs-lookup"><span data-stu-id="0fcc2-109">Allows for specifiying a array of PSLoadBalancerBackendAddress.</span></span> 
## <span data-ttu-id="0fcc2-110">Példák</span><span class="sxs-lookup"><span data-stu-id="0fcc2-110">EXAMPLES</span></span>

### <span data-ttu-id="0fcc2-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="0fcc2-111">Example 1</span></span>
```powershell
## create by passing loadbalancer without Ips
PS C:\> $virtualNetwork = Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroup
PS C:\> $lb = Get-AzLoadBalancer -ResourceGroupName $resourceGroup -Name $loadBalancerName
PS C:\> $ip1 = New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.5" -Name "TestVNetRef" -VirtualNetworkId $virtualNetwork.Id
PS C:\> $ip2 = New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.6" -Name "TestVNetRef2" -VirtualNetworkId $virtualNetwork.Id
PS C:\> $ips = @($ip1, $ip2)

PS C:\> $lb | New-AzLoadBalancerBackendAddressPool -Name $backendPool1
```

### <span data-ttu-id="0fcc2-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="0fcc2-112">Example 2</span></span>
```powershell
## create by passing loadbalancer with ips
PS C:\> $lb | New-AzLoadBalancerBackendAddressPool -Name $backendPool7 -LoadBalancerBackendAddress $ips
```

### <span data-ttu-id="0fcc2-113">3. példa</span><span class="sxs-lookup"><span data-stu-id="0fcc2-113">Example 3</span></span>
```powershell
## create by name without ips
PS C:\> New-AzLoadBalancerBackendAddressPool -ResourceGroupName $resourceGroup -LoadBalancerName $loadBalancerName -Name $backendPool3
```

### <span data-ttu-id="0fcc2-114">4. példa</span><span class="sxs-lookup"><span data-stu-id="0fcc2-114">Example 4</span></span>
```powershell
## create by name with ips
PS C:\> New-AzLoadBalancerBackendAddressPool -ResourceGroupName $resourceGroup -LoadBalancerName $loadBalancerName -Name $backendPool3 -LoadBalancerBackendAddress $ips
```

## <span data-ttu-id="0fcc2-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0fcc2-115">PARAMETERS</span></span>

### <span data-ttu-id="0fcc2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fcc2-116">-DefaultProfile</span></span>
<span data-ttu-id="0fcc2-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0fcc2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0fcc2-118">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0fcc2-118">-LoadBalancer</span></span>
<span data-ttu-id="0fcc2-119">A terheléselosztó erőforrás.</span><span class="sxs-lookup"><span data-stu-id="0fcc2-119">The load balancer resource.</span></span>

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

### <span data-ttu-id="0fcc2-120">-LoadBalancerBackendAddress</span><span class="sxs-lookup"><span data-stu-id="0fcc2-120">-LoadBalancerBackendAddress</span></span>
<span data-ttu-id="0fcc2-121">A backend címei.</span><span class="sxs-lookup"><span data-stu-id="0fcc2-121">The backend addresses.</span></span>

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

### <span data-ttu-id="0fcc2-122">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="0fcc2-122">-LoadBalancerName</span></span>
<span data-ttu-id="0fcc2-123">A terheléselosztó neve.</span><span class="sxs-lookup"><span data-stu-id="0fcc2-123">The name of the load balancer.</span></span>

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

### <span data-ttu-id="0fcc2-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0fcc2-124">-Name</span></span>
<span data-ttu-id="0fcc2-125">A backend-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="0fcc2-125">The name of the backend pool.</span></span>

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

### <span data-ttu-id="0fcc2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fcc2-126">-ResourceGroupName</span></span>
<span data-ttu-id="0fcc2-127">Az erőforráscsoport neve a terheléselosztó csoportban.</span><span class="sxs-lookup"><span data-stu-id="0fcc2-127">The resource group name of the load balancer.</span></span>

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

### <span data-ttu-id="0fcc2-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0fcc2-128">-Confirm</span></span>
<span data-ttu-id="0fcc2-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0fcc2-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0fcc2-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0fcc2-130">-WhatIf</span></span>
<span data-ttu-id="0fcc2-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0fcc2-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0fcc2-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0fcc2-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0fcc2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fcc2-133">CommonParameters</span></span>
<span data-ttu-id="0fcc2-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0fcc2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fcc2-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="0fcc2-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fcc2-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0fcc2-136">INPUTS</span></span>

### <span data-ttu-id="0fcc2-137">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0fcc2-137">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="0fcc2-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0fcc2-138">OUTPUTS</span></span>

### <span data-ttu-id="0fcc2-139">Microsoft. Azure. commands. Network. models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="0fcc2-139">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="0fcc2-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0fcc2-140">NOTES</span></span>

## <span data-ttu-id="0fcc2-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0fcc2-141">RELATED LINKS</span></span>
