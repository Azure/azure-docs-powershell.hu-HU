---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/new-azsnetworkquota
schema: 2.0.0
ms.openlocfilehash: 554ebe0e6c4ef8a4b0d262071595c0dc6336f482
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94016870"
---
# <span data-ttu-id="88b5a-101">New-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="88b5a-101">New-AzsNetworkQuota</span></span>

## <span data-ttu-id="88b5a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="88b5a-102">SYNOPSIS</span></span>
<span data-ttu-id="88b5a-103">Kvóta létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="88b5a-103">Create or update a quota.</span></span>

## <span data-ttu-id="88b5a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="88b5a-104">SYNTAX</span></span>

### <span data-ttu-id="88b5a-105">CreateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="88b5a-105">CreateExpanded (Default)</span></span>
```
New-AzsNetworkQuota -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-MaxLoadBalancersPerSubscription <Int64>] [-MaxNicsPerSubscription <Int64>]
 [-MaxPublicIpsPerSubscription <Int64>] [-MaxSecurityGroupsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="88b5a-106">Létrehozása</span><span class="sxs-lookup"><span data-stu-id="88b5a-106">Create</span></span>
```
New-AzsNetworkQuota -Name <String> -Quota <IQuota> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="88b5a-107">CreateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="88b5a-107">CreateViaIdentity</span></span>
```
New-AzsNetworkQuota -InputObject <INetworkAdminIdentity> -Quota <IQuota> [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="88b5a-108">CreateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="88b5a-108">CreateViaIdentityExpanded</span></span>
```
New-AzsNetworkQuota -InputObject <INetworkAdminIdentity> [-MaxLoadBalancersPerSubscription <Int64>]
 [-MaxNicsPerSubscription <Int64>] [-MaxPublicIpsPerSubscription <Int64>]
 [-MaxSecurityGroupsPerSubscription <Int64>] [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="88b5a-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="88b5a-109">DESCRIPTION</span></span>
<span data-ttu-id="88b5a-110">Kvóta létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="88b5a-110">Create or update a quota.</span></span>

## <span data-ttu-id="88b5a-111">Példák</span><span class="sxs-lookup"><span data-stu-id="88b5a-111">EXAMPLES</span></span>

### <span data-ttu-id="88b5a-112">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="88b5a-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsNetworkQuota -Name NetworkQuotaDefaultValues
```

<span data-ttu-id="88b5a-113">Hozzon létre egy új hálózati kvótát az összes alapértelmezett értékkel.</span><span class="sxs-lookup"><span data-stu-id="88b5a-113">Create a new network quota with all the default values.</span></span>

### <span data-ttu-id="88b5a-114">--------------------------PÉLDA 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="88b5a-114">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
New-AzsNetworkQuota -Name NetworkQuota1 -MaxNicsPerSubscription 150 -MaxPublicIpsPerSubscription 150
```
<span data-ttu-id="88b5a-115">Új hálózati kvóta létrehozása a kvótával nem rendelkező alapértelmezett értékekkel</span><span class="sxs-lookup"><span data-stu-id="88b5a-115">Create a new network quota with non default values for quota.</span></span>



## <span data-ttu-id="88b5a-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="88b5a-116">PARAMETERS</span></span>

### <span data-ttu-id="88b5a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88b5a-117">-DefaultProfile</span></span>
<span data-ttu-id="88b5a-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="88b5a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88b5a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="88b5a-119">-InputObject</span></span>
<span data-ttu-id="88b5a-120">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="88b5a-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.INetworkAdminIdentity
Parameter Sets: CreateViaIdentity, CreateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="88b5a-121">-Hely</span><span class="sxs-lookup"><span data-stu-id="88b5a-121">-Location</span></span>
<span data-ttu-id="88b5a-122">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="88b5a-122">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Name
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="88b5a-123">-MaxLoadBalancersPerSubscription</span><span class="sxs-lookup"><span data-stu-id="88b5a-123">-MaxLoadBalancersPerSubscription</span></span>
<span data-ttu-id="88b5a-124">A bérlői előfizetések maximális száma a terheléselosztási szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="88b5a-124">Maximum number of load balancers a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="88b5a-125">-MaxNicsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="88b5a-125">-MaxNicsPerSubscription</span></span>
<span data-ttu-id="88b5a-126">A bérlői előfizetésben használható hálózati adapterek maximális száma</span><span class="sxs-lookup"><span data-stu-id="88b5a-126">Maximum number of NICs a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 100
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="88b5a-127">-MaxPublicIpsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="88b5a-127">-MaxPublicIpsPerSubscription</span></span>
<span data-ttu-id="88b5a-128">Nyilvános IP-címek maximális száma: a bérlői előfizetésben megadható.</span><span class="sxs-lookup"><span data-stu-id="88b5a-128">Maximum number of public IP addresses a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="88b5a-129">-MaxSecurityGroupsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="88b5a-129">-MaxSecurityGroupsPerSubscription</span></span>
<span data-ttu-id="88b5a-130">Azoknak a biztonsági csoportoknak a maximális száma, amelyekhez bérlői előfizetés tud rendelkezni.</span><span class="sxs-lookup"><span data-stu-id="88b5a-130">Maximum number of security groups a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="88b5a-131">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="88b5a-131">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span></span>
<span data-ttu-id="88b5a-132">Virtuális hálózati átjárók maximális száma a bérlői előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="88b5a-132">Maximum number of virtual network gateway Connections a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 2
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="88b5a-133">-MaxVirtualNetworkGatewaysPerSubscription</span><span class="sxs-lookup"><span data-stu-id="88b5a-133">-MaxVirtualNetworkGatewaysPerSubscription</span></span>
<span data-ttu-id="88b5a-134">Azoknak a virtuális hálózati átjáróknak a maximális száma, amelyeknek a bérlői előfizetése rendelkezésére áll.</span><span class="sxs-lookup"><span data-stu-id="88b5a-134">Maximum number of virtual network gateways a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="88b5a-135">-MaxVnetsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="88b5a-135">-MaxVnetsPerSubscription</span></span>
<span data-ttu-id="88b5a-136">Azoknak a virtuális hálózatoknak a maximális száma, amelyekhez bérlői előfizetés tud rendelkezni.</span><span class="sxs-lookup"><span data-stu-id="88b5a-136">Maximum number of virtual networks a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="88b5a-137">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="88b5a-137">-Name</span></span>
<span data-ttu-id="88b5a-138">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="88b5a-138">Name of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="88b5a-139">-Kvóta</span><span class="sxs-lookup"><span data-stu-id="88b5a-139">-Quota</span></span>
<span data-ttu-id="88b5a-140">Hálózati kvóta-erőforrás</span><span class="sxs-lookup"><span data-stu-id="88b5a-140">Network quota resource.</span></span>
<span data-ttu-id="88b5a-141">A kivitelezéshez tekintse meg a kvóta tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="88b5a-141">To construct, see NOTES section for QUOTA properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IQuota
Parameter Sets: Create, CreateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="88b5a-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="88b5a-142">-SubscriptionId</span></span>
<span data-ttu-id="88b5a-143">Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="88b5a-143">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="88b5a-144">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="88b5a-144">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="88b5a-145">-Címke</span><span class="sxs-lookup"><span data-stu-id="88b5a-145">-Tag</span></span>
<span data-ttu-id="88b5a-146">A kulcs érték párok listája</span><span class="sxs-lookup"><span data-stu-id="88b5a-146">List of key value pairs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="88b5a-147">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="88b5a-147">-Confirm</span></span>
<span data-ttu-id="88b5a-148">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="88b5a-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88b5a-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88b5a-149">-WhatIf</span></span>
<span data-ttu-id="88b5a-150">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="88b5a-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88b5a-151">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="88b5a-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88b5a-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88b5a-152">CommonParameters</span></span>
<span data-ttu-id="88b5a-153">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="88b5a-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88b5a-154">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="88b5a-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88b5a-155">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="88b5a-155">INPUTS</span></span>

### <span data-ttu-id="88b5a-156">Microsoft. Azure. PowerShell. parancsmagok. NetworkAdmin. modellek. Api20150615. IQuota</span><span class="sxs-lookup"><span data-stu-id="88b5a-156">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IQuota</span></span>

### <span data-ttu-id="88b5a-157">Microsoft. Azure. PowerShell. parancsmagok. NetworkAdmin. models. INetworkAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="88b5a-157">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.INetworkAdminIdentity</span></span>

## <span data-ttu-id="88b5a-158">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="88b5a-158">OUTPUTS</span></span>

### <span data-ttu-id="88b5a-159">Microsoft. Azure. PowerShell. parancsmagok. NetworkAdmin. modellek. Api20150615. IQuota</span><span class="sxs-lookup"><span data-stu-id="88b5a-159">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IQuota</span></span>



## <span data-ttu-id="88b5a-160">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="88b5a-160">NOTES</span></span>

<span data-ttu-id="88b5a-161">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="88b5a-161">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="88b5a-162">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="88b5a-162">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="88b5a-163">INPUTOBJECT <INetworkAdminIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="88b5a-163">INPUTOBJECT <INetworkAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="88b5a-164">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="88b5a-164">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="88b5a-165">`[Location <String>]`: Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="88b5a-165">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="88b5a-166">`[ResourceName <String>]`: Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="88b5a-166">`[ResourceName <String>]`: Name of the resource.</span></span>
  - <span data-ttu-id="88b5a-167">`[SubscriptionId <String>]`: Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="88b5a-167">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="88b5a-168">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="88b5a-168">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="88b5a-169">KVÓTA <IQuota> : hálózati kvóta-erőforrás.</span><span class="sxs-lookup"><span data-stu-id="88b5a-169">QUOTA <IQuota>: Network quota resource.</span></span>
  - <span data-ttu-id="88b5a-170">`[Tag <IResourceTags>]`: A kulcsok érték párok listája.</span><span class="sxs-lookup"><span data-stu-id="88b5a-170">`[Tag <IResourceTags>]`: List of key value pairs.</span></span>
    - <span data-ttu-id="88b5a-171">`[(Any) <String>]`: Ez azt jelzi, hogy az objektumhoz bármely tulajdonság hozzá lehet adni.</span><span class="sxs-lookup"><span data-stu-id="88b5a-171">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="88b5a-172">`[MaxLoadBalancersPerSubscription <Int64?>]`: A betöltők maximális száma a bérlői előfizetés rendelkezésére áll.</span><span class="sxs-lookup"><span data-stu-id="88b5a-172">`[MaxLoadBalancersPerSubscription <Int64?>]`: Maximum number of load balancers a tenant subscription can provision.</span></span>
  - <span data-ttu-id="88b5a-173">`[MaxNicsPerSubscription <Int64?>]`: A bérlői előfizetésben használható hálózati adapterek maximális száma</span><span class="sxs-lookup"><span data-stu-id="88b5a-173">`[MaxNicsPerSubscription <Int64?>]`: Maximum number of NICs a tenant subscription can provision.</span></span>
  - <span data-ttu-id="88b5a-174">`[MaxPublicIpsPerSubscription <Int64?>]`: Nyilvános IP-címek maximális száma: a bérlői előfizetésben megadható.</span><span class="sxs-lookup"><span data-stu-id="88b5a-174">`[MaxPublicIpsPerSubscription <Int64?>]`: Maximum number of public IP addresses a tenant subscription can provision.</span></span>
  - <span data-ttu-id="88b5a-175">`[MaxSecurityGroupsPerSubscription <Int64?>]`: A bérlői előfizetést tartalmazó biztonsági csoportok maximális száma</span><span class="sxs-lookup"><span data-stu-id="88b5a-175">`[MaxSecurityGroupsPerSubscription <Int64?>]`: Maximum number of security groups a tenant subscription can provision.</span></span>
  - <span data-ttu-id="88b5a-176">`[MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64?>]`: A virtuális hálózati átjárók által biztosított kapcsolatok maximális száma a bérlői előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="88b5a-176">`[MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64?>]`: Maximum number of virtual network gateway Connections a tenant subscription can provision.</span></span>
  - <span data-ttu-id="88b5a-177">`[MaxVirtualNetworkGatewaysPerSubscription <Int64?>]`: Azoknak a virtuális hálózati átjáróknak a maximális száma, amelyeknek a bérlői előfizetése rendelkezésére áll.</span><span class="sxs-lookup"><span data-stu-id="88b5a-177">`[MaxVirtualNetworkGatewaysPerSubscription <Int64?>]`: Maximum number of virtual network gateways a tenant subscription can provision.</span></span>
  - <span data-ttu-id="88b5a-178">`[MaxVnetsPerSubscription <Int64?>]`: A virtuális hálózatok maximális száma, amely a bérlői előfizetést képes biztosítani.</span><span class="sxs-lookup"><span data-stu-id="88b5a-178">`[MaxVnetsPerSubscription <Int64?>]`: Maximum number of virtual networks a tenant subscription can provision.</span></span>

## <span data-ttu-id="88b5a-179">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="88b5a-179">RELATED LINKS</span></span>

