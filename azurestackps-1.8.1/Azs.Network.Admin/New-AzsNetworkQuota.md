---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: acda4a136b98a8a83190704a3635bd97ae97a7b2
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840726"
---
# <span data-ttu-id="49631-101">New-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="49631-101">New-AzsNetworkQuota</span></span>

## <span data-ttu-id="49631-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="49631-102">SYNOPSIS</span></span>
<span data-ttu-id="49631-103">Kvóta létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="49631-103">Create or update a quota.</span></span>

## <span data-ttu-id="49631-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="49631-104">SYNTAX</span></span>

```
New-AzsNetworkQuota [-Name] <String> [[-MaxNicsPerSubscription] <Int64>]
 [[-MaxPublicIpsPerSubscription] <Int64>] [[-MaxVirtualNetworkGatewayConnectionsPerSubscription] <Int64>]
 [[-MaxVnetsPerSubscription] <Int64>] [[-MaxVirtualNetworkGatewaysPerSubscription] <Int64>]
 [[-MaxSecurityGroupsPerSubscription] <Int64>] [[-MaxLoadBalancersPerSubscription] <Int64>]
 [[-Location] <String>] [[-MigrationPhase] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49631-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="49631-105">DESCRIPTION</span></span>
<span data-ttu-id="49631-106">Kvóta létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="49631-106">Create or update a quota.</span></span>

## <span data-ttu-id="49631-107">Példák</span><span class="sxs-lookup"><span data-stu-id="49631-107">EXAMPLES</span></span>

### <span data-ttu-id="49631-108">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="49631-108">EXAMPLE 1</span></span>
```
New-AzsNetworkQuota -Name NetworkQuotaDefaultValues
```

<span data-ttu-id="49631-109">Hozzon létre egy új hálózati kvótát az összes alapértelmezett értékkel.</span><span class="sxs-lookup"><span data-stu-id="49631-109">Create a new network quota with all the default values.</span></span>

### <span data-ttu-id="49631-110">2. PÉLDA</span><span class="sxs-lookup"><span data-stu-id="49631-110">EXAMPLE 2</span></span>
```
New-AzsNetworkQuota -Name NetworkQuota1 -MaxNicsPerSubscription 150 -MaxPublicIpsPerSubscription 150
```

<span data-ttu-id="49631-111">Új hálózati kvóta létrehozása a kvótával nem rendelkező alapértelmezett értékekkel</span><span class="sxs-lookup"><span data-stu-id="49631-111">Create a new network quota with non default values for quota.</span></span>

## <span data-ttu-id="49631-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="49631-112">PARAMETERS</span></span>

### <span data-ttu-id="49631-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="49631-113">-Name</span></span>
<span data-ttu-id="49631-114">A hálózati kvóta-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="49631-114">Name of the network quota resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49631-115">-MaxNicsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="49631-115">-MaxNicsPerSubscription</span></span>
<span data-ttu-id="49631-116">Az előfizetésben engedélyezett maximális hálózati adapterek száma.</span><span class="sxs-lookup"><span data-stu-id="49631-116">The maximum NICs allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: 100
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49631-117">-MaxPublicIpsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="49631-117">-MaxPublicIpsPerSubscription</span></span>
<span data-ttu-id="49631-118">Az előfizetésben megengedett legnagyobb nyilvános IP-címek száma.</span><span class="sxs-lookup"><span data-stu-id="49631-118">The maximum public IP addresses allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49631-119">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="49631-119">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span></span>
<span data-ttu-id="49631-120">Az előfizetésben engedélyezett virtuális hálózati átjáró-kapcsolatok maximális száma.</span><span class="sxs-lookup"><span data-stu-id="49631-120">The maximum number of virtual network gateway connections allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: 2
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49631-121">-MaxVnetsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="49631-121">-MaxVnetsPerSubscription</span></span>
<span data-ttu-id="49631-122">Az előfizetéshez engedélyezett virtuális hálózatok maximális száma.</span><span class="sxs-lookup"><span data-stu-id="49631-122">The maxium number of virtual networks allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49631-123">-MaxVirtualNetworkGatewaysPerSubscription</span><span class="sxs-lookup"><span data-stu-id="49631-123">-MaxVirtualNetworkGatewaysPerSubscription</span></span>
<span data-ttu-id="49631-124">Az előfizetésben engedélyezett virtuális hálózati átjárók maximális száma.</span><span class="sxs-lookup"><span data-stu-id="49631-124">The maximum number of virtual network gateways allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49631-125">-MaxSecurityGroupsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="49631-125">-MaxSecurityGroupsPerSubscription</span></span>
<span data-ttu-id="49631-126">Az előfizetésben engedélyezett biztonsági csoportok maximális száma.</span><span class="sxs-lookup"><span data-stu-id="49631-126">The maximum number of security groups allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49631-127">-MaxLoadBalancersPerSubscription</span><span class="sxs-lookup"><span data-stu-id="49631-127">-MaxLoadBalancersPerSubscription</span></span>
<span data-ttu-id="49631-128">Az előfizetésben engedélyezett betöltők maximális száma.</span><span class="sxs-lookup"><span data-stu-id="49631-128">The maximum number of load balancers allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49631-129">-Hely</span><span class="sxs-lookup"><span data-stu-id="49631-129">-Location</span></span>
<span data-ttu-id="49631-130">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="49631-130">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49631-131">-MigrationPhase</span><span class="sxs-lookup"><span data-stu-id="49631-131">-MigrationPhase</span></span>
<span data-ttu-id="49631-132">Az áttelepítés állapota, például a nincs, a felkészülés, a véglegesítés és a megszakítás.</span><span class="sxs-lookup"><span data-stu-id="49631-132">State of migration such as None, Prepare, Commit, and Abort.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: Prepare
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49631-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49631-133">-WhatIf</span></span>
<span data-ttu-id="49631-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="49631-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49631-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="49631-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49631-136">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="49631-136">-Confirm</span></span>
<span data-ttu-id="49631-137">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="49631-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49631-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49631-138">CommonParameters</span></span>
<span data-ttu-id="49631-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="49631-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49631-140">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49631-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49631-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="49631-141">INPUTS</span></span>

## <span data-ttu-id="49631-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="49631-142">OUTPUTS</span></span>

### <span data-ttu-id="49631-143">Microsoft. AzureStack. Management. Network. admin. models. quote</span><span class="sxs-lookup"><span data-stu-id="49631-143">Microsoft.AzureStack.Management.Network.Admin.Models.Quota</span></span>

## <span data-ttu-id="49631-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="49631-144">NOTES</span></span>

## <span data-ttu-id="49631-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="49631-145">RELATED LINKS</span></span>
