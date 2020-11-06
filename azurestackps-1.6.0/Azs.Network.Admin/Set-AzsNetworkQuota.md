---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c2867f0c438f1f8752137f680365ecade255d291
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93490996"
---
# <span data-ttu-id="ef8e2-101">Set-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="ef8e2-101">Set-AzsNetworkQuota</span></span>

## <span data-ttu-id="ef8e2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ef8e2-102">SYNOPSIS</span></span>
<span data-ttu-id="ef8e2-103">Kvóta létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="ef8e2-103">Create or update a quota.</span></span>

## <span data-ttu-id="ef8e2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ef8e2-104">SYNTAX</span></span>

### <span data-ttu-id="ef8e2-105">Kvóták (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ef8e2-105">Quotas (Default)</span></span>
```
Set-AzsNetworkQuota -Name <String> [-MaxNicsPerSubscription <Int64>] [-MaxPublicIpsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxSecurityGroupsPerSubscription <Int64>]
 [-MaxLoadBalancersPerSubscription <Int64>] [-Location <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef8e2-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="ef8e2-106">ResourceId</span></span>
```
Set-AzsNetworkQuota [-MaxNicsPerSubscription <Int64>] [-MaxPublicIpsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxSecurityGroupsPerSubscription <Int64>]
 [-MaxLoadBalancersPerSubscription <Int64>] -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef8e2-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="ef8e2-107">InputObject</span></span>
```
Set-AzsNetworkQuota [-MaxNicsPerSubscription <Int64>] [-MaxPublicIpsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxSecurityGroupsPerSubscription <Int64>]
 [-MaxLoadBalancersPerSubscription <Int64>] -InputObject <Quota> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef8e2-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="ef8e2-108">DESCRIPTION</span></span>
<span data-ttu-id="ef8e2-109">Kvóta létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="ef8e2-109">Create or update a quota.</span></span>

## <span data-ttu-id="ef8e2-110">Példák</span><span class="sxs-lookup"><span data-stu-id="ef8e2-110">EXAMPLES</span></span>

### <span data-ttu-id="ef8e2-111">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="ef8e2-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsNetworkQuota -Name NetworkQuota1 -MaxVnetsPerSubscription 20
```

<span data-ttu-id="ef8e2-112">Hálózat kvótájának frissítése név szerint</span><span class="sxs-lookup"><span data-stu-id="ef8e2-112">Update a network quota by name.</span></span>

### <span data-ttu-id="ef8e2-113">--------------------------PÉLDA 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="ef8e2-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Set-AzsNetworkQuota -Name NetworkQuota1 -MaxPublicIpsPerSubscription 75 -MaxNicsPerSubscription 100
```

<span data-ttu-id="ef8e2-114">Hálózat kvótájának frissítése név szerint</span><span class="sxs-lookup"><span data-stu-id="ef8e2-114">Update a network quota by name.</span></span>

## <span data-ttu-id="ef8e2-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ef8e2-115">PARAMETERS</span></span>

### <span data-ttu-id="ef8e2-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ef8e2-116">-InputObject</span></span>
<span data-ttu-id="ef8e2-117">Get-AzsNetworkQuota által visszaadott Posbbily módosított hálózati kvóta</span><span class="sxs-lookup"><span data-stu-id="ef8e2-117">Posbbily modified network quota returned by Get-AzsNetworkQuota</span></span>

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

### <span data-ttu-id="ef8e2-118">-Hely</span><span class="sxs-lookup"><span data-stu-id="ef8e2-118">-Location</span></span>
<span data-ttu-id="ef8e2-119">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="ef8e2-119">Location of the resource.</span></span>

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

### <span data-ttu-id="ef8e2-120">-MaxLoadBalancersPerSubscription</span><span class="sxs-lookup"><span data-stu-id="ef8e2-120">-MaxLoadBalancersPerSubscription</span></span>
<span data-ttu-id="ef8e2-121">Az előfizetésben engedélyezett betöltők maximális száma.</span><span class="sxs-lookup"><span data-stu-id="ef8e2-121">The maximum number of load balancers allowed per subscription.</span></span>

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

### <span data-ttu-id="ef8e2-122">-MaxNicsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="ef8e2-122">-MaxNicsPerSubscription</span></span>
<span data-ttu-id="ef8e2-123">Az előfizetésben engedélyezett maximális hálózati adapterek száma.</span><span class="sxs-lookup"><span data-stu-id="ef8e2-123">The maximum NICs allowed per subscription.</span></span>

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

### <span data-ttu-id="ef8e2-124">-MaxPublicIpsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="ef8e2-124">-MaxPublicIpsPerSubscription</span></span>
<span data-ttu-id="ef8e2-125">Az előfizetésben megengedett legnagyobb nyilvános IP-címek száma.</span><span class="sxs-lookup"><span data-stu-id="ef8e2-125">The maximum public IP addresses allowed per subscription.</span></span>

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

### <span data-ttu-id="ef8e2-126">-MaxSecurityGroupsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="ef8e2-126">-MaxSecurityGroupsPerSubscription</span></span>
<span data-ttu-id="ef8e2-127">Az előfizetésben engedélyezett biztonsági csoportok maximális száma.</span><span class="sxs-lookup"><span data-stu-id="ef8e2-127">The maximum number of security groups allowed per subscription.</span></span>

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

### <span data-ttu-id="ef8e2-128">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="ef8e2-128">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span></span>
<span data-ttu-id="ef8e2-129">Az előfizetésben engedélyezett virtuális hálózati átjáró-kapcsolatok maximális száma.</span><span class="sxs-lookup"><span data-stu-id="ef8e2-129">The maximum number of virtual network gateway connections allowed per subscription.</span></span>

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

### <span data-ttu-id="ef8e2-130">-MaxVirtualNetworkGatewaysPerSubscription</span><span class="sxs-lookup"><span data-stu-id="ef8e2-130">-MaxVirtualNetworkGatewaysPerSubscription</span></span>
<span data-ttu-id="ef8e2-131">Az előfizetésben engedélyezett virtuális hálózati átjárók maximális száma.</span><span class="sxs-lookup"><span data-stu-id="ef8e2-131">The maximum number of virtual network gateways allowed per subscription.</span></span>

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

### <span data-ttu-id="ef8e2-132">-MaxVnetsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="ef8e2-132">-MaxVnetsPerSubscription</span></span>
<span data-ttu-id="ef8e2-133">Az előfizetéshez engedélyezett virtuális hálózatok maximális száma.</span><span class="sxs-lookup"><span data-stu-id="ef8e2-133">The maxium number of virtual networks allowed per subscription.</span></span>

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

### <span data-ttu-id="ef8e2-134">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ef8e2-134">-Name</span></span>
<span data-ttu-id="ef8e2-135">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="ef8e2-135">Name of the resource.</span></span>

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

### <span data-ttu-id="ef8e2-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ef8e2-136">-ResourceId</span></span>
<span data-ttu-id="ef8e2-137">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="ef8e2-137">The resource id.</span></span>

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

### <span data-ttu-id="ef8e2-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ef8e2-138">-Confirm</span></span>
<span data-ttu-id="ef8e2-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ef8e2-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef8e2-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef8e2-140">-WhatIf</span></span>
<span data-ttu-id="ef8e2-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ef8e2-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef8e2-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ef8e2-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef8e2-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef8e2-143">CommonParameters</span></span>
<span data-ttu-id="ef8e2-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ef8e2-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef8e2-145">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef8e2-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef8e2-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ef8e2-146">INPUTS</span></span>

## <span data-ttu-id="ef8e2-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ef8e2-147">OUTPUTS</span></span>

### <span data-ttu-id="ef8e2-148">Microsoft. AzureStack. Management. Network. admin. models. quote</span><span class="sxs-lookup"><span data-stu-id="ef8e2-148">Microsoft.AzureStack.Management.Network.Admin.Models.Quota</span></span>

## <span data-ttu-id="ef8e2-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ef8e2-149">NOTES</span></span>

## <span data-ttu-id="ef8e2-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ef8e2-150">RELATED LINKS</span></span>

