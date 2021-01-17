---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerbackendaddressconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressConfig.md
ms.openlocfilehash: 3c3cc0e5da1cc8afbc6160acf13c3ef94eb02e34
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468974"
---
# <span data-ttu-id="7e62d-101">New-AzLoadBalancerBackendAddressConfig</span><span class="sxs-lookup"><span data-stu-id="7e62d-101">New-AzLoadBalancerBackendAddressConfig</span></span>

## <span data-ttu-id="7e62d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e62d-102">SYNOPSIS</span></span>
<span data-ttu-id="7e62d-103">Egy terheléselegyenítő háttércím-konfigját adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="7e62d-103">Returns a load balancer backend address config.</span></span> 

## <span data-ttu-id="7e62d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7e62d-104">SYNTAX</span></span>

### <span data-ttu-id="7e62d-105">SetByResourcePublicIpAddress (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7e62d-105">SetByResourcePublicIpAddress (Default)</span></span>
```
New-AzLoadBalancerBackendAddressConfig -IpAddress <String> -Name <String> -VirtualNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e62d-106">SetByResourceFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="7e62d-106">SetByResourceFrontendIPConfiguration</span></span>
```
New-AzLoadBalancerBackendAddressConfig -Name <String> -LoadBalancerFrontendIPConfigurationId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e62d-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7e62d-107">DESCRIPTION</span></span>
<span data-ttu-id="7e62d-108">Egy terheléselegyenítő háttércím-konfigját adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="7e62d-108">Returns a load balancer backend address config.</span></span> 

## <span data-ttu-id="7e62d-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7e62d-109">EXAMPLES</span></span>

### <span data-ttu-id="7e62d-110">1. példa: Új loadbalancer-cím konfig virtuális hálózati hivatkozással</span><span class="sxs-lookup"><span data-stu-id="7e62d-110">Example 1: New loadbalancer address config with virtual network reference</span></span>
```powershell
PS C:\> $virtualNetwork = Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroup
New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.5" -Name "TestVNetRef" -VirtualNetworkId $virtualNetwork.Id
```

### <span data-ttu-id="7e62d-111">2. példa: Új loadbalancer-címkonfiguráció loadbalancer frontend ip configuration reference</span><span class="sxs-lookup"><span data-stu-id="7e62d-111">Example 2: New loadbalancer address config with loadbalancer frontend ip configuration reference</span></span>
```powershell
PS C:\> $frontend = New-AzLoadBalancerFrontendIpConfig -Name $frontendName -PublicIpAddress $publicip
New-AzLoadBalancerBackendAddressConfig -LoadBalancerFrontendIPConfigurationId $frontend.Id -Name "TestLBFERef"
```

## <span data-ttu-id="7e62d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7e62d-112">PARAMETERS</span></span>

### <span data-ttu-id="7e62d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e62d-113">-DefaultProfile</span></span>
<span data-ttu-id="7e62d-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7e62d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e62d-115">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="7e62d-115">-IpAddress</span></span>
<span data-ttu-id="7e62d-116">A háttérkészlethez hozzáadható IPAddress</span><span class="sxs-lookup"><span data-stu-id="7e62d-116">The IPAddress to add to the backend pool</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourcePublicIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e62d-117">-LoadBalancerFrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="7e62d-117">-LoadBalancerFrontendIPConfigurationId</span></span>
<span data-ttu-id="7e62d-118">The load balancer frontend ip configuration associated with Backend Address config</span><span class="sxs-lookup"><span data-stu-id="7e62d-118">The load balancer frontend ip configuration associated with Backend Address config</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceFrontendIPConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e62d-119">-Name</span><span class="sxs-lookup"><span data-stu-id="7e62d-119">-Name</span></span>
<span data-ttu-id="7e62d-120">A Backend Address (Háttércím) konfigurációs fájl neve</span><span class="sxs-lookup"><span data-stu-id="7e62d-120">The name of the Backend Address config</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e62d-121">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="7e62d-121">-VirtualNetworkId</span></span>
<span data-ttu-id="7e62d-122">The virtual network associated with Backend Address config</span><span class="sxs-lookup"><span data-stu-id="7e62d-122">The virtual network associated with Backend Address config</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourcePublicIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e62d-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7e62d-123">-Confirm</span></span>
<span data-ttu-id="7e62d-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7e62d-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e62d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e62d-125">-WhatIf</span></span>
<span data-ttu-id="7e62d-126">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7e62d-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7e62d-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7e62d-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e62d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e62d-128">CommonParameters</span></span>
<span data-ttu-id="7e62d-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e62d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e62d-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7e62d-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e62d-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7e62d-131">INPUTS</span></span>

### <span data-ttu-id="7e62d-132">System.String</span><span class="sxs-lookup"><span data-stu-id="7e62d-132">System.String</span></span>

### <span data-ttu-id="7e62d-133">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7e62d-133">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="7e62d-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7e62d-134">OUTPUTS</span></span>

### <span data-ttu-id="7e62d-135">Microsoft.Azure.Commands.Network.Models.PSLoadBalancerBackendAddress</span><span class="sxs-lookup"><span data-stu-id="7e62d-135">Microsoft.Azure.Commands.Network.Models.PSLoadBalancerBackendAddress</span></span>

## <span data-ttu-id="7e62d-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7e62d-136">NOTES</span></span>

## <span data-ttu-id="7e62d-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7e62d-137">RELATED LINKS</span></span>
