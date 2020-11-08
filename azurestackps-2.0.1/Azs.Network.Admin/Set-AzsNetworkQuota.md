---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/set-azsnetworkquota
schema: 2.0.0
ms.openlocfilehash: c2cc0e7a22d7e581eece9004950b54bc0151fad3
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/24/2020
ms.locfileid: "94015262"
---
# <span data-ttu-id="0dbaf-101">Set-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="0dbaf-101">Set-AzsNetworkQuota</span></span>

## <span data-ttu-id="0dbaf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0dbaf-102">SYNOPSIS</span></span>
<span data-ttu-id="0dbaf-103">Kvóta létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="0dbaf-103">Create or update a quota.</span></span>

## <span data-ttu-id="0dbaf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0dbaf-104">SYNTAX</span></span>

### <span data-ttu-id="0dbaf-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0dbaf-105">UpdateExpanded (Default)</span></span>
```
Set-AzsNetworkQuota -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-MaxLoadBalancersPerSubscription <Int64>] [-MaxNicsPerSubscription <Int64>]
 [-MaxPublicIpsPerSubscription <Int64>] [-MaxSecurityGroupsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0dbaf-106">Frissítés</span><span class="sxs-lookup"><span data-stu-id="0dbaf-106">Update</span></span>
```
Set-AzsNetworkQuota -Name <String> -Quota <IQuota> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0dbaf-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="0dbaf-107">DESCRIPTION</span></span>
<span data-ttu-id="0dbaf-108">Kvóta létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="0dbaf-108">Create or update a quota.</span></span>

## <span data-ttu-id="0dbaf-109">Példák</span><span class="sxs-lookup"><span data-stu-id="0dbaf-109">EXAMPLES</span></span>

### <span data-ttu-id="0dbaf-110">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="0dbaf-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsNetworkQuota -Name NetworkQuota1 -MaxVnetsPerSubscription 20
```

<span data-ttu-id="0dbaf-111">Hálózat kvótájának frissítése név szerint</span><span class="sxs-lookup"><span data-stu-id="0dbaf-111">Update a network quota by name.</span></span>

### <span data-ttu-id="0dbaf-112">--------------------------PÉLDA 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="0dbaf-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Set-AzsNetworkQuota -Name NetworkQuota1 -MaxPublicIpsPerSubscription 75 -MaxNicsPerSubscription 100
```

<span data-ttu-id="0dbaf-113">Hálózat kvótájának frissítése név szerint</span><span class="sxs-lookup"><span data-stu-id="0dbaf-113">Update a network quota by name.</span></span>

## <span data-ttu-id="0dbaf-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0dbaf-114">PARAMETERS</span></span>

### <span data-ttu-id="0dbaf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0dbaf-115">-DefaultProfile</span></span>
<span data-ttu-id="0dbaf-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0dbaf-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0dbaf-117">-Hely</span><span class="sxs-lookup"><span data-stu-id="0dbaf-117">-Location</span></span>
<span data-ttu-id="0dbaf-118">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="0dbaf-118">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Name
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0dbaf-119">-MaxLoadBalancersPerSubscription</span><span class="sxs-lookup"><span data-stu-id="0dbaf-119">-MaxLoadBalancersPerSubscription</span></span>
<span data-ttu-id="0dbaf-120">A bérlői előfizetések maximális száma a terheléselosztási szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="0dbaf-120">Maximum number of load balancers a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0dbaf-121">-MaxNicsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="0dbaf-121">-MaxNicsPerSubscription</span></span>
<span data-ttu-id="0dbaf-122">A bérlői előfizetésben használható hálózati adapterek maximális száma</span><span class="sxs-lookup"><span data-stu-id="0dbaf-122">Maximum number of NICs a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0dbaf-123">-MaxPublicIpsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="0dbaf-123">-MaxPublicIpsPerSubscription</span></span>
<span data-ttu-id="0dbaf-124">Nyilvános IP-címek maximális száma: a bérlői előfizetésben megadható.</span><span class="sxs-lookup"><span data-stu-id="0dbaf-124">Maximum number of public IP addresses a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0dbaf-125">-MaxSecurityGroupsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="0dbaf-125">-MaxSecurityGroupsPerSubscription</span></span>
<span data-ttu-id="0dbaf-126">Azoknak a biztonsági csoportoknak a maximális száma, amelyekhez bérlői előfizetés tud rendelkezni.</span><span class="sxs-lookup"><span data-stu-id="0dbaf-126">Maximum number of security groups a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0dbaf-127">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="0dbaf-127">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span></span>
<span data-ttu-id="0dbaf-128">Virtuális hálózati átjárók maximális száma a bérlői előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="0dbaf-128">Maximum number of virtual network gateway Connections a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0dbaf-129">-MaxVirtualNetworkGatewaysPerSubscription</span><span class="sxs-lookup"><span data-stu-id="0dbaf-129">-MaxVirtualNetworkGatewaysPerSubscription</span></span>
<span data-ttu-id="0dbaf-130">Azoknak a virtuális hálózati átjáróknak a maximális száma, amelyeknek a bérlői előfizetése rendelkezésére áll.</span><span class="sxs-lookup"><span data-stu-id="0dbaf-130">Maximum number of virtual network gateways a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0dbaf-131">-MaxVnetsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="0dbaf-131">-MaxVnetsPerSubscription</span></span>
<span data-ttu-id="0dbaf-132">Azoknak a virtuális hálózatoknak a maximális száma, amelyekhez bérlői előfizetés tud rendelkezni.</span><span class="sxs-lookup"><span data-stu-id="0dbaf-132">Maximum number of virtual networks a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0dbaf-133">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0dbaf-133">-Name</span></span>
<span data-ttu-id="0dbaf-134">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="0dbaf-134">Name of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0dbaf-135">-Kvóta</span><span class="sxs-lookup"><span data-stu-id="0dbaf-135">-Quota</span></span>
<span data-ttu-id="0dbaf-136">Hálózati kvóta-erőforrás</span><span class="sxs-lookup"><span data-stu-id="0dbaf-136">Network quota resource.</span></span>
<span data-ttu-id="0dbaf-137">A kivitelezéshez tekintse meg a kvóta tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="0dbaf-137">To construct, see NOTES section for QUOTA properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IQuota
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="0dbaf-138">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0dbaf-138">-SubscriptionId</span></span>
<span data-ttu-id="0dbaf-139">Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="0dbaf-139">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="0dbaf-140">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="0dbaf-140">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0dbaf-141">-Címke</span><span class="sxs-lookup"><span data-stu-id="0dbaf-141">-Tag</span></span>
<span data-ttu-id="0dbaf-142">A kulcs érték párok listája</span><span class="sxs-lookup"><span data-stu-id="0dbaf-142">List of key value pairs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0dbaf-143">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0dbaf-143">-Confirm</span></span>
<span data-ttu-id="0dbaf-144">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0dbaf-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0dbaf-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0dbaf-145">-WhatIf</span></span>
<span data-ttu-id="0dbaf-146">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0dbaf-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0dbaf-147">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0dbaf-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0dbaf-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0dbaf-148">CommonParameters</span></span>
<span data-ttu-id="0dbaf-149">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0dbaf-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0dbaf-150">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="0dbaf-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0dbaf-151">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0dbaf-151">INPUTS</span></span>

### <span data-ttu-id="0dbaf-152">Microsoft. Azure. PowerShell. parancsmagok. NetworkAdmin. modellek. Api20150615. IQuota</span><span class="sxs-lookup"><span data-stu-id="0dbaf-152">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IQuota</span></span>

## <span data-ttu-id="0dbaf-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0dbaf-153">OUTPUTS</span></span>

### <span data-ttu-id="0dbaf-154">Microsoft. Azure. PowerShell. parancsmagok. NetworkAdmin. modellek. Api20150615. IQuota</span><span class="sxs-lookup"><span data-stu-id="0dbaf-154">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IQuota</span></span>



## <span data-ttu-id="0dbaf-155">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0dbaf-155">NOTES</span></span>

<span data-ttu-id="0dbaf-156">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="0dbaf-156">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0dbaf-157">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="0dbaf-157">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="0dbaf-158">KVÓTA <IQuota> : hálózati kvóta-erőforrás.</span><span class="sxs-lookup"><span data-stu-id="0dbaf-158">QUOTA <IQuota>: Network quota resource.</span></span>
  - <span data-ttu-id="0dbaf-159">`[Tag <IResourceTags>]`: A kulcsok érték párok listája.</span><span class="sxs-lookup"><span data-stu-id="0dbaf-159">`[Tag <IResourceTags>]`: List of key value pairs.</span></span>
    - <span data-ttu-id="0dbaf-160">`[(Any) <String>]`: Ez azt jelzi, hogy az objektumhoz bármely tulajdonság hozzá lehet adni.</span><span class="sxs-lookup"><span data-stu-id="0dbaf-160">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="0dbaf-161">`[MaxLoadBalancersPerSubscription <Int64?>]`: A betöltők maximális száma a bérlői előfizetés rendelkezésére áll.</span><span class="sxs-lookup"><span data-stu-id="0dbaf-161">`[MaxLoadBalancersPerSubscription <Int64?>]`: Maximum number of load balancers a tenant subscription can provision.</span></span>
  - <span data-ttu-id="0dbaf-162">`[MaxNicsPerSubscription <Int64?>]`: A bérlői előfizetésben használható hálózati adapterek maximális száma</span><span class="sxs-lookup"><span data-stu-id="0dbaf-162">`[MaxNicsPerSubscription <Int64?>]`: Maximum number of NICs a tenant subscription can provision.</span></span>
  - <span data-ttu-id="0dbaf-163">`[MaxPublicIpsPerSubscription <Int64?>]`: Nyilvános IP-címek maximális száma: a bérlői előfizetésben megadható.</span><span class="sxs-lookup"><span data-stu-id="0dbaf-163">`[MaxPublicIpsPerSubscription <Int64?>]`: Maximum number of public IP addresses a tenant subscription can provision.</span></span>
  - <span data-ttu-id="0dbaf-164">`[MaxSecurityGroupsPerSubscription <Int64?>]`: A bérlői előfizetést tartalmazó biztonsági csoportok maximális száma</span><span class="sxs-lookup"><span data-stu-id="0dbaf-164">`[MaxSecurityGroupsPerSubscription <Int64?>]`: Maximum number of security groups a tenant subscription can provision.</span></span>
  - <span data-ttu-id="0dbaf-165">`[MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64?>]`: A virtuális hálózati átjárók által biztosított kapcsolatok maximális száma a bérlői előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="0dbaf-165">`[MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64?>]`: Maximum number of virtual network gateway Connections a tenant subscription can provision.</span></span>
  - <span data-ttu-id="0dbaf-166">`[MaxVirtualNetworkGatewaysPerSubscription <Int64?>]`: Azoknak a virtuális hálózati átjáróknak a maximális száma, amelyeknek a bérlői előfizetése rendelkezésére áll.</span><span class="sxs-lookup"><span data-stu-id="0dbaf-166">`[MaxVirtualNetworkGatewaysPerSubscription <Int64?>]`: Maximum number of virtual network gateways a tenant subscription can provision.</span></span>
  - <span data-ttu-id="0dbaf-167">`[MaxVnetsPerSubscription <Int64?>]`: A virtuális hálózatok maximális száma, amely a bérlői előfizetést képes biztosítani.</span><span class="sxs-lookup"><span data-stu-id="0dbaf-167">`[MaxVnetsPerSubscription <Int64?>]`: Maximum number of virtual networks a tenant subscription can provision.</span></span>

## <span data-ttu-id="0dbaf-168">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0dbaf-168">RELATED LINKS</span></span>

