---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerbackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerBackendAddressPool.md
ms.openlocfilehash: 034e33b1c465f106c1edfa8647fe34233575b801
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187594"
---
# <span data-ttu-id="bd891-101">Set-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="bd891-101">Set-AzLoadBalancerBackendAddressPool</span></span>

## <span data-ttu-id="bd891-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bd891-102">SYNOPSIS</span></span>
<span data-ttu-id="bd891-103">A backend-készlet frissítése egy loadbalancer</span><span class="sxs-lookup"><span data-stu-id="bd891-103">Updates the backend pool on a loadbalancer</span></span>

## <span data-ttu-id="bd891-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bd891-104">SYNTAX</span></span>

### <span data-ttu-id="bd891-105">SetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd891-105">SetByNameParameterSet</span></span>
```
Set-AzLoadBalancerBackendAddressPool -ResourceGroupName <String> -LoadBalancerName <String> -Name <String>
 -LoadBalancerBackendAddress <PSLoadBalancerBackendAddress[]> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd891-106">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd891-106">SetByParentObjectParameterSet</span></span>
```
Set-AzLoadBalancerBackendAddressPool -Name <String> -LoadBalancer <PSLoadBalancer>
 -LoadBalancerBackendAddress <PSLoadBalancerBackendAddress[]> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd891-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd891-107">SetByInputObjectParameterSet</span></span>
```
Set-AzLoadBalancerBackendAddressPool -InputObject <PSBackendAddressPool> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd891-108">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd891-108">SetByResourceIdParameterSet</span></span>
```
Set-AzLoadBalancerBackendAddressPool -LoadBalancerBackendAddress <PSLoadBalancerBackendAddress[]>
 -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bd891-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="bd891-109">DESCRIPTION</span></span>
<span data-ttu-id="bd891-110">A backend-készlet frissítése egy loadbalancer</span><span class="sxs-lookup"><span data-stu-id="bd891-110">Updates the backend pool on a loadbalancer</span></span>

## <span data-ttu-id="bd891-111">Példák</span><span class="sxs-lookup"><span data-stu-id="bd891-111">EXAMPLES</span></span>

### <span data-ttu-id="bd891-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="bd891-112">Example 1</span></span>
```powershell
###Set by name and modified input object
PS C:\> $virtualNetwork = Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroup
PS C:\> $lb = Get-AzLoadBalancer -ResourceGroupName $resourceGroup -Name $loadBalancerName
PS C:\> $ip1 = New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.5" -Name "TestVNetRef" -VirtualNetworkId $virtualNetwork.Id
PS C:\> $ip2 = New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.6" -Name "TestVNetRef2" -VirtualNetworkId $virtualNetwork.Id
PS C:\> $ip3 = New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.7" -Name "TestVNetRef3" -VirtualNetworkId $virtualNetwork.id
PS C:\> $ips = @($ip1, $ip2)
PS C:\> $b2 = Get-AzLoadBalancerBackendAddressPool -ResourceGroupName $resourceGroup -LoadBalancerName $loadBalancerName -Name $backendPool1
PS C:\> $b2.LoadBalancerBackendAddresses.Add($ip3)

PS C:\> Set-AzLoadBalancerBackendAddressPool -InputObject $b2
```
### <span data-ttu-id="bd891-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="bd891-113">Example 2</span></span>
```powershell
###Set by specific backend from piped loadbalancer and set two IP's
PS C:\> $lb | Set-AzLoadBalancerBackendAddressPool -LoadBalancerBackendAddress $ips -Name $backendPool1
```

### <span data-ttu-id="bd891-114">3. példa</span><span class="sxs-lookup"><span data-stu-id="bd891-114">Example 3</span></span>
```powershell
### #set by ResourceId
PS C:\> Set-AzLoadBalancerBackendAddressPool -ResourceId b2.Id -LoadBalancerBackendAddress $b2.LoadBalancerBackendAddresses
```

## <span data-ttu-id="bd891-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bd891-115">PARAMETERS</span></span>

### <span data-ttu-id="bd891-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd891-116">-DefaultProfile</span></span>
<span data-ttu-id="bd891-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bd891-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd891-118">-Force</span><span class="sxs-lookup"><span data-stu-id="bd891-118">-Force</span></span>
<span data-ttu-id="bd891-119">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bd891-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="bd891-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bd891-120">-InputObject</span></span>
<span data-ttu-id="bd891-121">A beállítani kívánt backend-címkészlet</span><span class="sxs-lookup"><span data-stu-id="bd891-121">The backend address pool to set</span></span>

```yaml
Type: PSBackendAddressPool
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd891-122">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="bd891-122">-LoadBalancer</span></span>
<span data-ttu-id="bd891-123">A terheléselosztó erőforrás.</span><span class="sxs-lookup"><span data-stu-id="bd891-123">The load balancer resource.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: SetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bd891-124">-LoadBalancerBackendAddress</span><span class="sxs-lookup"><span data-stu-id="bd891-124">-LoadBalancerBackendAddress</span></span>
<span data-ttu-id="bd891-125">A backend címei.</span><span class="sxs-lookup"><span data-stu-id="bd891-125">The backend addresses.</span></span>

```yaml
Type: PSLoadBalancerBackendAddress[]
Parameter Sets: SetByNameParameterSet, SetByParentObjectParameterSet, SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd891-126">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="bd891-126">-LoadBalancerName</span></span>
<span data-ttu-id="bd891-127">A terheléselosztó neve.</span><span class="sxs-lookup"><span data-stu-id="bd891-127">The name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd891-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bd891-128">-Name</span></span>
<span data-ttu-id="bd891-129">A backend-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="bd891-129">The name of the backend pool.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet, SetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd891-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bd891-130">-PassThru</span></span>
<span data-ttu-id="bd891-131">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="bd891-131">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="bd891-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd891-132">-ResourceGroupName</span></span>
<span data-ttu-id="bd891-133">Az erőforráscsoport neve a terheléselosztó csoportban.</span><span class="sxs-lookup"><span data-stu-id="bd891-133">The resource group name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd891-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bd891-134">-ResourceId</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd891-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="bd891-135">-Confirm</span></span>
<span data-ttu-id="bd891-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bd891-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd891-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd891-137">-WhatIf</span></span>
<span data-ttu-id="bd891-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="bd891-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd891-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bd891-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd891-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd891-140">CommonParameters</span></span>
<span data-ttu-id="bd891-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bd891-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd891-142">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="bd891-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd891-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bd891-143">INPUTS</span></span>

### <span data-ttu-id="bd891-144">Microsoft. Azure. commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="bd891-144">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="bd891-145">System. String</span><span class="sxs-lookup"><span data-stu-id="bd891-145">System.String</span></span>

## <span data-ttu-id="bd891-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bd891-146">OUTPUTS</span></span>

### <span data-ttu-id="bd891-147">Microsoft. Azure. commands. Network. models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="bd891-147">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="bd891-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bd891-148">NOTES</span></span>

## <span data-ttu-id="bd891-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bd891-149">RELATED LINKS</span></span>
