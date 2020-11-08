---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkService.md
ms.openlocfilehash: 0b4cc79358723e6249a0c9d4e22929e224165402
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013263"
---
# <span data-ttu-id="0f0c1-101">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="0f0c1-101">New-AzPrivateLinkService</span></span>

## <span data-ttu-id="0f0c1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0f0c1-102">SYNOPSIS</span></span>
<span data-ttu-id="0f0c1-103">Privát hivatkozás szolgáltatás létrehozása</span><span class="sxs-lookup"><span data-stu-id="0f0c1-103">Creates a private link service</span></span>

## <span data-ttu-id="0f0c1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0f0c1-104">SYNTAX</span></span>

```
New-AzPrivateLinkService -Name <String> -ResourceGroupName <String> -Location <String>
 -LoadBalancerFrontendIpConfiguration <PSFrontendIPConfiguration[]>
 -IpConfiguration <PSPrivateLinkServiceIpConfiguration[]> [-Visibility <String[]>] [-AutoApproval <String[]>] [-EnableProxyProtocol]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0f0c1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0f0c1-105">DESCRIPTION</span></span>
<span data-ttu-id="0f0c1-106">A **New-AzPrivateLinkService** parancsmag létrehoz egy privát hivatkozás szolgáltatást</span><span class="sxs-lookup"><span data-stu-id="0f0c1-106">The **New-AzPrivateLinkService** cmdlet creates a private link service</span></span>

## <span data-ttu-id="0f0c1-107">Példák</span><span class="sxs-lookup"><span data-stu-id="0f0c1-107">EXAMPLES</span></span>

### <span data-ttu-id="0f0c1-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="0f0c1-108">Example 1</span></span>
```
$vnet = Get-AzVirtualNetwork -ResourceName "myvnet" -ResourceGroupName "myresourcegroup"
$IPConfig = New-AzPrivateLinkServiceIpConfig -Name "IP-Config" -Subnet $vnet.subnets[1] -PrivateIpAddress "10.0.0.5"
$publicip = Get-AzPublicIpAddress -ResourceGroupName "myresourcegroup"
$frontend = New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
$lb = New-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "myresourcegroup" -Location "West US" -FrontendIpConfiguration $frontend  
New-AzPrivateLinkService -Name "mypls" -ResourceGroupName myresourcegroup -Location "West US" -LoadBalancerFrontendIpConfiguration $frontend -IpConfiguration $IPConfig
```

<span data-ttu-id="0f0c1-109">Ez a példa létrehoz egy privát hivatkozás szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="0f0c1-109">This example creates a private link service.</span></span>

## <span data-ttu-id="0f0c1-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0f0c1-110">PARAMETERS</span></span>

### <span data-ttu-id="0f0c1-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0f0c1-111">-AsJob</span></span>
<span data-ttu-id="0f0c1-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="0f0c1-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f0c1-113">– Autojóváhagyás</span><span class="sxs-lookup"><span data-stu-id="0f0c1-113">-AutoApproval</span></span>
<span data-ttu-id="0f0c1-114">A privát link szolgáltatás automatikus jóváhagyási előfizetései</span><span class="sxs-lookup"><span data-stu-id="0f0c1-114">The auto approval subscriptions of private link service</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f0c1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f0c1-115">-DefaultProfile</span></span>
<span data-ttu-id="0f0c1-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0f0c1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f0c1-117">-EnableProxyProtocol</span><span class="sxs-lookup"><span data-stu-id="0f0c1-117">-EnableProxyProtocol</span></span>
<span data-ttu-id="0f0c1-118">Engedélyezze a proxy protokollt a privát hivatkozás szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="0f0c1-118">Enable proxy protocol for the private link service.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f0c1-119">-Force</span><span class="sxs-lookup"><span data-stu-id="0f0c1-119">-Force</span></span>
<span data-ttu-id="0f0c1-120">Ha egy erőforrást felül szeretne írni, ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0f0c1-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f0c1-121">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="0f0c1-121">-IpConfiguration</span></span>
<span data-ttu-id="0f0c1-122">Az IP-konfigurációk</span><span class="sxs-lookup"><span data-stu-id="0f0c1-122">The ip configurations</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceIpConfiguration[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f0c1-123">-LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="0f0c1-123">-LoadBalancerFrontendIpConfiguration</span></span>
<span data-ttu-id="0f0c1-124">Az első végpont IP-beállításai</span><span class="sxs-lookup"><span data-stu-id="0f0c1-124">The front end ip configurations</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f0c1-125">-Hely</span><span class="sxs-lookup"><span data-stu-id="0f0c1-125">-Location</span></span>
<span data-ttu-id="0f0c1-126">helyre.</span><span class="sxs-lookup"><span data-stu-id="0f0c1-126">location.</span></span>

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

### <span data-ttu-id="0f0c1-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0f0c1-127">-Name</span></span>
<span data-ttu-id="0f0c1-128">A szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="0f0c1-128">The name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f0c1-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f0c1-129">-ResourceGroupName</span></span>
<span data-ttu-id="0f0c1-130">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="0f0c1-130">The resource group name.</span></span>

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

### <span data-ttu-id="0f0c1-131">-Címke</span><span class="sxs-lookup"><span data-stu-id="0f0c1-131">-Tag</span></span>
<span data-ttu-id="0f0c1-132">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="0f0c1-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="0f0c1-133">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="0f0c1-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f0c1-134">-Láthatóság</span><span class="sxs-lookup"><span data-stu-id="0f0c1-134">-Visibility</span></span>
<span data-ttu-id="0f0c1-135">A privát link szolgáltatás láthatósági előfizetései</span><span class="sxs-lookup"><span data-stu-id="0f0c1-135">The visibility subscriptions of private link service</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f0c1-136">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0f0c1-136">-Confirm</span></span>
<span data-ttu-id="0f0c1-137">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0f0c1-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f0c1-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f0c1-138">-WhatIf</span></span>
<span data-ttu-id="0f0c1-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0f0c1-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f0c1-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0f0c1-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f0c1-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f0c1-141">CommonParameters</span></span>
<span data-ttu-id="0f0c1-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0f0c1-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f0c1-143">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="0f0c1-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f0c1-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0f0c1-144">INPUTS</span></span>

### <span data-ttu-id="0f0c1-145">System. String</span><span class="sxs-lookup"><span data-stu-id="0f0c1-145">System.String</span></span>

### <span data-ttu-id="0f0c1-146">Microsoft. Azure. commands. Network. models. PSFrontendIPConfiguration []</span><span class="sxs-lookup"><span data-stu-id="0f0c1-146">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]</span></span>

### <span data-ttu-id="0f0c1-147">Microsoft. Azure. commands. Network. models. PSPrivateLinkServiceIpConfiguration []</span><span class="sxs-lookup"><span data-stu-id="0f0c1-147">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceIpConfiguration[]</span></span>

## <span data-ttu-id="0f0c1-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0f0c1-148">OUTPUTS</span></span>

### <span data-ttu-id="0f0c1-149">Microsoft. Azure. commands. Network. models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="0f0c1-149">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="0f0c1-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0f0c1-150">NOTES</span></span>

## <span data-ttu-id="0f0c1-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0f0c1-151">RELATED LINKS</span></span>

[<span data-ttu-id="0f0c1-152">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="0f0c1-152">Get-AzPrivateLinkService</span></span>](./Get-AzPrivateLinkService.md)

[<span data-ttu-id="0f0c1-153">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="0f0c1-153">Remove-AzPrivateLinkService</span></span>](./Remove-AzPrivateLinkService.md)

[<span data-ttu-id="0f0c1-154">Új – AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="0f0c1-154">New-AzPrivateLinkServiceIpConfig</span></span>](./New-AzPrivateLinkServiceIpConfig.md)
