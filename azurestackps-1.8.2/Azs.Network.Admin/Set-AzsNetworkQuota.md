---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8d20f84d91c110ae1f4e55508b33f758fc0d5583
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94016887"
---
# <span data-ttu-id="a4c2e-101">Set-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="a4c2e-101">Set-AzsNetworkQuota</span></span>

## <span data-ttu-id="a4c2e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a4c2e-102">SYNOPSIS</span></span>
<span data-ttu-id="a4c2e-103">Kvóta létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="a4c2e-103">Create or update a quota.</span></span>

## <span data-ttu-id="a4c2e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a4c2e-104">SYNTAX</span></span>

### <span data-ttu-id="a4c2e-105">Kvóták (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a4c2e-105">Quotas (Default)</span></span>
```
Set-AzsNetworkQuota -Name <String> [-MaxNicsPerSubscription <Int64>] [-MaxPublicIpsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxSecurityGroupsPerSubscription <Int64>]
 [-MaxLoadBalancersPerSubscription <Int64>] [-Location <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4c2e-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="a4c2e-106">ResourceId</span></span>
```
Set-AzsNetworkQuota [-MaxNicsPerSubscription <Int64>] [-MaxPublicIpsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxSecurityGroupsPerSubscription <Int64>]
 [-MaxLoadBalancersPerSubscription <Int64>] -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4c2e-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="a4c2e-107">InputObject</span></span>
```
Set-AzsNetworkQuota [-MaxNicsPerSubscription <Int64>] [-MaxPublicIpsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxSecurityGroupsPerSubscription <Int64>]
 [-MaxLoadBalancersPerSubscription <Int64>] -InputObject <Quota> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4c2e-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="a4c2e-108">DESCRIPTION</span></span>
<span data-ttu-id="a4c2e-109">Kvóta létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="a4c2e-109">Create or update a quota.</span></span>

## <span data-ttu-id="a4c2e-110">Példák</span><span class="sxs-lookup"><span data-stu-id="a4c2e-110">EXAMPLES</span></span>

### <span data-ttu-id="a4c2e-111">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="a4c2e-111">EXAMPLE 1</span></span>
```
Set-AzsNetworkQuota -Name NetworkQuota1 -MaxVnetsPerSubscription 20
```

<span data-ttu-id="a4c2e-112">Hálózat kvótájának frissítése név szerint</span><span class="sxs-lookup"><span data-stu-id="a4c2e-112">Update a network quota by name.</span></span>

### <span data-ttu-id="a4c2e-113">2. PÉLDA</span><span class="sxs-lookup"><span data-stu-id="a4c2e-113">EXAMPLE 2</span></span>
```
Set-AzsNetworkQuota -Name NetworkQuota1 -MaxPublicIpsPerSubscription 75 -MaxNicsPerSubscription 100
```

<span data-ttu-id="a4c2e-114">Hálózat kvótájának frissítése név szerint</span><span class="sxs-lookup"><span data-stu-id="a4c2e-114">Update a network quota by name.</span></span>

## <span data-ttu-id="a4c2e-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a4c2e-115">PARAMETERS</span></span>

### <span data-ttu-id="a4c2e-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a4c2e-116">-Name</span></span>
<span data-ttu-id="a4c2e-117">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="a4c2e-117">Name of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Quotas
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4c2e-118">-MaxNicsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="a4c2e-118">-MaxNicsPerSubscription</span></span>
<span data-ttu-id="a4c2e-119">Az előfizetésben engedélyezett maximális hálózati adapterek száma.</span><span class="sxs-lookup"><span data-stu-id="a4c2e-119">The maximum NICs allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4c2e-120">-MaxPublicIpsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="a4c2e-120">-MaxPublicIpsPerSubscription</span></span>
<span data-ttu-id="a4c2e-121">Az előfizetésben megengedett legnagyobb nyilvános IP-címek száma.</span><span class="sxs-lookup"><span data-stu-id="a4c2e-121">The maximum public IP addresses allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4c2e-122">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="a4c2e-122">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span></span>
<span data-ttu-id="a4c2e-123">Az előfizetésben engedélyezett virtuális hálózati átjáró-kapcsolatok maximális száma.</span><span class="sxs-lookup"><span data-stu-id="a4c2e-123">The maximum number of virtual network gateway connections allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4c2e-124">-MaxVnetsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="a4c2e-124">-MaxVnetsPerSubscription</span></span>
<span data-ttu-id="a4c2e-125">Az előfizetéshez engedélyezett virtuális hálózatok maximális száma.</span><span class="sxs-lookup"><span data-stu-id="a4c2e-125">The maxium number of virtual networks allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4c2e-126">-MaxVirtualNetworkGatewaysPerSubscription</span><span class="sxs-lookup"><span data-stu-id="a4c2e-126">-MaxVirtualNetworkGatewaysPerSubscription</span></span>
<span data-ttu-id="a4c2e-127">Az előfizetésben engedélyezett virtuális hálózati átjárók maximális száma.</span><span class="sxs-lookup"><span data-stu-id="a4c2e-127">The maximum number of virtual network gateways allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4c2e-128">-MaxSecurityGroupsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="a4c2e-128">-MaxSecurityGroupsPerSubscription</span></span>
<span data-ttu-id="a4c2e-129">Az előfizetésben engedélyezett biztonsági csoportok maximális száma.</span><span class="sxs-lookup"><span data-stu-id="a4c2e-129">The maximum number of security groups allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4c2e-130">-MaxLoadBalancersPerSubscription</span><span class="sxs-lookup"><span data-stu-id="a4c2e-130">-MaxLoadBalancersPerSubscription</span></span>
<span data-ttu-id="a4c2e-131">Az előfizetésben engedélyezett betöltők maximális száma.</span><span class="sxs-lookup"><span data-stu-id="a4c2e-131">The maximum number of load balancers allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4c2e-132">-Hely</span><span class="sxs-lookup"><span data-stu-id="a4c2e-132">-Location</span></span>
<span data-ttu-id="a4c2e-133">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="a4c2e-133">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Quotas
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4c2e-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a4c2e-134">-ResourceId</span></span>
<span data-ttu-id="a4c2e-135">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="a4c2e-135">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4c2e-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a4c2e-136">-InputObject</span></span>
<span data-ttu-id="a4c2e-137">Get-AzsNetworkQuota által visszaadott Posbbily módosított hálózati kvóta</span><span class="sxs-lookup"><span data-stu-id="a4c2e-137">Posbbily modified network quota returned by Get-AzsNetworkQuota</span></span>

```yaml
Type: Quota
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a4c2e-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4c2e-138">-WhatIf</span></span>
<span data-ttu-id="a4c2e-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a4c2e-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4c2e-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a4c2e-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4c2e-141">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a4c2e-141">-Confirm</span></span>
<span data-ttu-id="a4c2e-142">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a4c2e-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4c2e-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4c2e-143">CommonParameters</span></span>
<span data-ttu-id="a4c2e-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a4c2e-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4c2e-145">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4c2e-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4c2e-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a4c2e-146">INPUTS</span></span>

## <span data-ttu-id="a4c2e-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a4c2e-147">OUTPUTS</span></span>

### <span data-ttu-id="a4c2e-148">Microsoft. AzureStack. Management. Network. admin. models. quote</span><span class="sxs-lookup"><span data-stu-id="a4c2e-148">Microsoft.AzureStack.Management.Network.Admin.Models.Quota</span></span>

## <span data-ttu-id="a4c2e-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a4c2e-149">NOTES</span></span>

## <span data-ttu-id="a4c2e-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a4c2e-150">RELATED LINKS</span></span>
