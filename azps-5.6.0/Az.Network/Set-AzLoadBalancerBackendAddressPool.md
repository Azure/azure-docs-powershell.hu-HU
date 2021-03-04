---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azloadbalancerbackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerBackendAddressPool.md
ms.openlocfilehash: 4f34d9b627fc5557af24999dd0d83dd76b17f73c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924578"
---
# <span data-ttu-id="adff6-101">Set-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="adff6-101">Set-AzLoadBalancerBackendAddressPool</span></span>

## <span data-ttu-id="adff6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="adff6-102">SYNOPSIS</span></span>
<span data-ttu-id="adff6-103">Frissíti a háttérkészletet egy loadbalanceren</span><span class="sxs-lookup"><span data-stu-id="adff6-103">Updates the backend pool on a loadbalancer</span></span>

## <span data-ttu-id="adff6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="adff6-104">SYNTAX</span></span>

### <span data-ttu-id="adff6-105">SetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="adff6-105">SetByNameParameterSet</span></span>
```
Set-AzLoadBalancerBackendAddressPool -ResourceGroupName <String> -LoadBalancerName <String> -Name <String>
 -LoadBalancerBackendAddress <PSLoadBalancerBackendAddress[]> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="adff6-106">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="adff6-106">SetByParentObjectParameterSet</span></span>
```
Set-AzLoadBalancerBackendAddressPool -Name <String> -LoadBalancer <PSLoadBalancer>
 -LoadBalancerBackendAddress <PSLoadBalancerBackendAddress[]> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="adff6-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="adff6-107">SetByInputObjectParameterSet</span></span>
```
Set-AzLoadBalancerBackendAddressPool -InputObject <PSBackendAddressPool> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="adff6-108">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="adff6-108">SetByResourceIdParameterSet</span></span>
```
Set-AzLoadBalancerBackendAddressPool -LoadBalancerBackendAddress <PSLoadBalancerBackendAddress[]>
 -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="adff6-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="adff6-109">DESCRIPTION</span></span>
<span data-ttu-id="adff6-110">Frissíti a háttérkészletet egy loadbalanceren</span><span class="sxs-lookup"><span data-stu-id="adff6-110">Updates the backend pool on a loadbalancer</span></span>

## <span data-ttu-id="adff6-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="adff6-111">EXAMPLES</span></span>

### <span data-ttu-id="adff6-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="adff6-112">Example 1</span></span>
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
### <span data-ttu-id="adff6-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="adff6-113">Example 2</span></span>
```powershell
###Set by specific backend from piped loadbalancer and set two IP's
PS C:\> $lb | Set-AzLoadBalancerBackendAddressPool -LoadBalancerBackendAddress $ips -Name $backendPool1
```

### <span data-ttu-id="adff6-114">3. példa</span><span class="sxs-lookup"><span data-stu-id="adff6-114">Example 3</span></span>
```powershell
### #set by ResourceId
PS C:\> Set-AzLoadBalancerBackendAddressPool -ResourceId b2.Id -LoadBalancerBackendAddress $b2.LoadBalancerBackendAddresses
```

## <span data-ttu-id="adff6-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="adff6-115">PARAMETERS</span></span>

### <span data-ttu-id="adff6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adff6-116">-DefaultProfile</span></span>
<span data-ttu-id="adff6-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="adff6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="adff6-118">-Force</span><span class="sxs-lookup"><span data-stu-id="adff6-118">-Force</span></span>
<span data-ttu-id="adff6-119">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="adff6-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="adff6-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="adff6-120">-InputObject</span></span>
<span data-ttu-id="adff6-121">A háttércímkészlet beállítása</span><span class="sxs-lookup"><span data-stu-id="adff6-121">The backend address pool to set</span></span>

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

### <span data-ttu-id="adff6-122">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="adff6-122">-LoadBalancer</span></span>
<span data-ttu-id="adff6-123">A terheléselosztási erőforrás.</span><span class="sxs-lookup"><span data-stu-id="adff6-123">The load balancer resource.</span></span>

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

### <span data-ttu-id="adff6-124">-LoadBalancerBackendAddress</span><span class="sxs-lookup"><span data-stu-id="adff6-124">-LoadBalancerBackendAddress</span></span>
<span data-ttu-id="adff6-125">A háttércímek.</span><span class="sxs-lookup"><span data-stu-id="adff6-125">The backend addresses.</span></span>

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

### <span data-ttu-id="adff6-126">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="adff6-126">-LoadBalancerName</span></span>
<span data-ttu-id="adff6-127">A terheléselosztás neve.</span><span class="sxs-lookup"><span data-stu-id="adff6-127">The name of the load balancer.</span></span>

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

### <span data-ttu-id="adff6-128">-Name</span><span class="sxs-lookup"><span data-stu-id="adff6-128">-Name</span></span>
<span data-ttu-id="adff6-129">A háttérkészlet neve.</span><span class="sxs-lookup"><span data-stu-id="adff6-129">The name of the backend pool.</span></span>

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

### <span data-ttu-id="adff6-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="adff6-130">-PassThru</span></span>
<span data-ttu-id="adff6-131">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="adff6-131">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="adff6-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="adff6-132">-ResourceGroupName</span></span>
<span data-ttu-id="adff6-133">A terheléselosztás erőforráscsoportneve.</span><span class="sxs-lookup"><span data-stu-id="adff6-133">The resource group name of the load balancer.</span></span>

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

### <span data-ttu-id="adff6-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="adff6-134">-ResourceId</span></span>

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

### <span data-ttu-id="adff6-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="adff6-135">-Confirm</span></span>
<span data-ttu-id="adff6-136">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="adff6-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="adff6-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="adff6-137">-WhatIf</span></span>
<span data-ttu-id="adff6-138">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="adff6-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="adff6-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="adff6-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="adff6-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adff6-140">CommonParameters</span></span>
<span data-ttu-id="adff6-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="adff6-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adff6-142">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="adff6-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adff6-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="adff6-143">INPUTS</span></span>

### <span data-ttu-id="adff6-144">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="adff6-144">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="adff6-145">System.String</span><span class="sxs-lookup"><span data-stu-id="adff6-145">System.String</span></span>

## <span data-ttu-id="adff6-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="adff6-146">OUTPUTS</span></span>

### <span data-ttu-id="adff6-147">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="adff6-147">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="adff6-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="adff6-148">NOTES</span></span>

## <span data-ttu-id="adff6-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="adff6-149">RELATED LINKS</span></span>
