---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkService.md
ms.openlocfilehash: 75c8f7b52fec0e429820d43f86a8a41798b1d5f7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837176"
---
# <span data-ttu-id="b9bfe-101">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="b9bfe-101">New-AzPrivateLinkService</span></span>

## <span data-ttu-id="b9bfe-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b9bfe-102">SYNOPSIS</span></span>
<span data-ttu-id="b9bfe-103">Privát hivatkozás szolgáltatás létrehozása</span><span class="sxs-lookup"><span data-stu-id="b9bfe-103">Creates a private link service</span></span>

## <span data-ttu-id="b9bfe-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b9bfe-104">SYNTAX</span></span>

```
New-AzPrivateLinkService -Name <String> -ResourceGroupName <String> -Location <String>
 -LoadBalancerFrontendIpConfiguration <PSFrontendIPConfiguration[]>
 -IpConfiguration <PSPrivateLinkServiceIpConfiguration[]> [-Visibility <String[]>] [-AutoApproval <String[]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b9bfe-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b9bfe-105">DESCRIPTION</span></span>
<span data-ttu-id="b9bfe-106">A **New-AzPrivateLinkService** parancsmag létrehoz egy privát hivatkozás szolgáltatást</span><span class="sxs-lookup"><span data-stu-id="b9bfe-106">The **New-AzPrivateLinkService** cmdlet creates a private link service</span></span>

## <span data-ttu-id="b9bfe-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b9bfe-107">EXAMPLES</span></span>

### <span data-ttu-id="b9bfe-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b9bfe-108">Example 1</span></span>
```
$vnet = Get-AzVirtualNetwork -ResourceName "myvnet" -ResourceGroupName "myresourcegroup"
$IPConfig = New-AzPrivateLinkServiceIpConfig -Name "IP-Config" -Subnet $vnet.subnets[1] -PrivateIpAddress "10.0.0.5"
$publicip = Get-AzPublicIpAddress -ResourceGroupName "myresourcegroup"
$frontend = New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
$lb = New-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "myresourcegroup" -Location "West US" -FrontendIpConfiguration $frontend  
New-AzPrivateLinkService -Name "mypls" -ResourceGroupName myresourcegroup -Location "West US" -LoadBalancerFrontendIpConfiguration $frontend -IpConfiguration $IPConfig
```

<span data-ttu-id="b9bfe-109">Ez a példa létrehoz egy privát hivatkozás szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="b9bfe-109">This example creates a private link service.</span></span>

## <span data-ttu-id="b9bfe-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b9bfe-110">PARAMETERS</span></span>

### <span data-ttu-id="b9bfe-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b9bfe-111">-AsJob</span></span>
<span data-ttu-id="b9bfe-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="b9bfe-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b9bfe-113">– Autojóváhagyás</span><span class="sxs-lookup"><span data-stu-id="b9bfe-113">-AutoApproval</span></span>
<span data-ttu-id="b9bfe-114">A privát link szolgáltatás automatikus jóváhagyási előfizetései</span><span class="sxs-lookup"><span data-stu-id="b9bfe-114">The auto approval subscriptions of private link service</span></span>

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

### <span data-ttu-id="b9bfe-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9bfe-115">-DefaultProfile</span></span>
<span data-ttu-id="b9bfe-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b9bfe-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9bfe-117">-Force</span><span class="sxs-lookup"><span data-stu-id="b9bfe-117">-Force</span></span>
<span data-ttu-id="b9bfe-118">Ha egy erőforrást felül szeretne írni, ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b9bfe-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="b9bfe-119">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="b9bfe-119">-IpConfiguration</span></span>
<span data-ttu-id="b9bfe-120">Az IP-konfigurációk</span><span class="sxs-lookup"><span data-stu-id="b9bfe-120">The ip configurations</span></span>

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

### <span data-ttu-id="b9bfe-121">-LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="b9bfe-121">-LoadBalancerFrontendIpConfiguration</span></span>
<span data-ttu-id="b9bfe-122">Az első végpont IP-beállításai</span><span class="sxs-lookup"><span data-stu-id="b9bfe-122">The front end ip configurations</span></span>

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

### <span data-ttu-id="b9bfe-123">-Hely</span><span class="sxs-lookup"><span data-stu-id="b9bfe-123">-Location</span></span>
<span data-ttu-id="b9bfe-124">helyre.</span><span class="sxs-lookup"><span data-stu-id="b9bfe-124">location.</span></span>

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

### <span data-ttu-id="b9bfe-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b9bfe-125">-Name</span></span>
<span data-ttu-id="b9bfe-126">A szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="b9bfe-126">The name of the service.</span></span>

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

### <span data-ttu-id="b9bfe-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9bfe-127">-ResourceGroupName</span></span>
<span data-ttu-id="b9bfe-128">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="b9bfe-128">The resource group name.</span></span>

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

### <span data-ttu-id="b9bfe-129">-Címke</span><span class="sxs-lookup"><span data-stu-id="b9bfe-129">-Tag</span></span>
<span data-ttu-id="b9bfe-130">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="b9bfe-130">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="b9bfe-131">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="b9bfe-131">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="b9bfe-132">-Láthatóság</span><span class="sxs-lookup"><span data-stu-id="b9bfe-132">-Visibility</span></span>
<span data-ttu-id="b9bfe-133">A privát link szolgáltatás láthatósági előfizetései</span><span class="sxs-lookup"><span data-stu-id="b9bfe-133">The visibility subscriptions of private link service</span></span>

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

### <span data-ttu-id="b9bfe-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b9bfe-134">-Confirm</span></span>
<span data-ttu-id="b9bfe-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b9bfe-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9bfe-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9bfe-136">-WhatIf</span></span>
<span data-ttu-id="b9bfe-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b9bfe-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9bfe-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b9bfe-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9bfe-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9bfe-139">CommonParameters</span></span>
<span data-ttu-id="b9bfe-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b9bfe-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9bfe-141">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b9bfe-141">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9bfe-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b9bfe-142">INPUTS</span></span>

### <span data-ttu-id="b9bfe-143">System. String</span><span class="sxs-lookup"><span data-stu-id="b9bfe-143">System.String</span></span>

### <span data-ttu-id="b9bfe-144">Microsoft. Azure. commands. Network. models. PSFrontendIPConfiguration []</span><span class="sxs-lookup"><span data-stu-id="b9bfe-144">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]</span></span>

### <span data-ttu-id="b9bfe-145">Microsoft. Azure. commands. Network. models. PSPrivateLinkServiceIpConfiguration []</span><span class="sxs-lookup"><span data-stu-id="b9bfe-145">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceIpConfiguration[]</span></span>

## <span data-ttu-id="b9bfe-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b9bfe-146">OUTPUTS</span></span>

### <span data-ttu-id="b9bfe-147">Microsoft. Azure. commands. Network. models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="b9bfe-147">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="b9bfe-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b9bfe-148">NOTES</span></span>

## <span data-ttu-id="b9bfe-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b9bfe-149">RELATED LINKS</span></span>

[<span data-ttu-id="b9bfe-150">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="b9bfe-150">Get-AzPrivateLinkService</span></span>](./Get-AzPrivateLinkService.md)

[<span data-ttu-id="b9bfe-151">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="b9bfe-151">Remove-AzPrivateLinkService</span></span>](./Remove-AzPrivateLinkService.md)

[<span data-ttu-id="b9bfe-152">Új – AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="b9bfe-152">New-AzPrivateLinkServiceIpConfig</span></span>](./New-AzPrivateLinkServiceIpConfig.md)
