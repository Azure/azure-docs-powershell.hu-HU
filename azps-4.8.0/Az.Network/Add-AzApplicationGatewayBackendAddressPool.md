---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6FBFAEFF-786D-440A-94B2-8C27BE033A0A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: c415fb890240ea6f4fb03b71c3a249eece1ba02b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181118"
---
# <span data-ttu-id="4963e-101">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4963e-101">Add-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="4963e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4963e-102">SYNOPSIS</span></span>
<span data-ttu-id="4963e-103">Egy végponti címkészletet ad hozzá egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="4963e-103">Adds a back-end address pool to an application gateway.</span></span>

## <span data-ttu-id="4963e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4963e-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayBackendAddressPool -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-BackendIPAddresses <String[]>] [-BackendFqdns <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4963e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4963e-105">DESCRIPTION</span></span>
<span data-ttu-id="4963e-106">A **Add-AzApplicationGatewayBackendAddressPool** parancsmag az alkalmazás-átjáróhoz ad hozzá egy háttér-végponti címkészletet.</span><span class="sxs-lookup"><span data-stu-id="4963e-106">The **Add-AzApplicationGatewayBackendAddressPool** cmdlet adds a back-end address pool to an application gateway.</span></span>
<span data-ttu-id="4963e-107">A végpontok címe megadható IP-cím, teljesen minősített tartománynév (FQDN) vagy IP-konfigurációs azonosítók használatával.</span><span class="sxs-lookup"><span data-stu-id="4963e-107">A back-end address can be specified using an IP address, a fully-qualified domain name (FQDN) or IP configuration IDs.</span></span>

## <span data-ttu-id="4963e-108">Példák</span><span class="sxs-lookup"><span data-stu-id="4963e-108">EXAMPLES</span></span>

### <span data-ttu-id="4963e-109">1. példa: back-end-Címkészlet hozzáadása a back-end Server FQDN használatával</span><span class="sxs-lookup"><span data-stu-id="4963e-109">Example 1: Add a back-end address pool by using a back-end server FQDN</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendFqdns "contoso1.com", " contoso1.com"
```

<span data-ttu-id="4963e-110">Az első parancs a ResourceGroup01 nevű erőforráscsoport ApplicationGateway01 nevű alkalmazás-átjáróját kapja meg, és a $AppGw változóban tárolja. A második parancs a teljes tartománynevek segítségével felveszi az $AppGw tárolt, a teljes tartománynevet.</span><span class="sxs-lookup"><span data-stu-id="4963e-110">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command adds the back-end address pool of the application gateway stored in $AppGw by using FQDNs.</span></span>

### <span data-ttu-id="4963e-111">2. példa: back-end-Címkészlet hozzáadása a backend-kiszolgálók IP-címeivel</span><span class="sxs-lookup"><span data-stu-id="4963e-111">Example 2: Add a back-end address pool by using backend server IP addresses</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayBackendAddressPool -ApplicationGateway $ AppGw -Name "Pool02" -BackendIPAddresses "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="4963e-112">Az első parancs a ResourceGroup01 nevű erőforráscsoport ApplicationGateway01 nevű alkalmazás-átjáróját kapja meg, és a $AppGw változóban tárolja. A második parancs hozzáadja az $AppGwban tárolt, az IP-címekkel ellátott, az alkalmazás átjárójának végponti címkészletet.</span><span class="sxs-lookup"><span data-stu-id="4963e-112">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command adds the back-end address pool of the application gateway stored in $AppGw by using IP addresses.</span></span>

## <span data-ttu-id="4963e-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4963e-113">PARAMETERS</span></span>

### <span data-ttu-id="4963e-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4963e-114">-ApplicationGateway</span></span>
<span data-ttu-id="4963e-115">Annak az alkalmazásnak az átjáróját adja meg, amelyre a parancsmag a back-end címkészletet adja.</span><span class="sxs-lookup"><span data-stu-id="4963e-115">Specifies the application gateway to which this cmdlet adds a back-end address pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4963e-116">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="4963e-116">-BackendFqdns</span></span>
<span data-ttu-id="4963e-117">A backend-kiszolgálók készlete, amelyet a parancsmag a back-end Server-készletként ad vissza.</span><span class="sxs-lookup"><span data-stu-id="4963e-117">Specifies a list of backend FQDNs which this cmdlet adds as a back-end server pool.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4963e-118">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="4963e-118">-BackendIPAddresses</span></span>
<span data-ttu-id="4963e-119">Azon back-end IP-címek listáját adja meg, amelyeket a parancsmag a back-end Server-készletként ad vissza.</span><span class="sxs-lookup"><span data-stu-id="4963e-119">Specifies a list of back-end IP addresses which this cmdlet adds as a back-end server pool.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4963e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4963e-120">-DefaultProfile</span></span>
<span data-ttu-id="4963e-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4963e-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4963e-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4963e-122">-Name</span></span>
<span data-ttu-id="4963e-123">Annak a végfelhasználói készletnek a nevét adja meg, amelyre a parancsmag ad.</span><span class="sxs-lookup"><span data-stu-id="4963e-123">Specifies the name of the back-end server pool that this cmdlet adds.</span></span>

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

### <span data-ttu-id="4963e-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4963e-124">-Confirm</span></span>
<span data-ttu-id="4963e-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4963e-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4963e-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4963e-126">-WhatIf</span></span>
<span data-ttu-id="4963e-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4963e-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4963e-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4963e-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4963e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4963e-129">CommonParameters</span></span>
<span data-ttu-id="4963e-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4963e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4963e-131">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4963e-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4963e-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4963e-132">INPUTS</span></span>

### <span data-ttu-id="4963e-133">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4963e-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4963e-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4963e-134">OUTPUTS</span></span>

### <span data-ttu-id="4963e-135">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4963e-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4963e-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4963e-136">NOTES</span></span>

## <span data-ttu-id="4963e-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4963e-137">RELATED LINKS</span></span>

[<span data-ttu-id="4963e-138">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4963e-138">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="4963e-139">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4963e-139">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="4963e-140">Új – AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4963e-140">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="4963e-141">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4963e-141">Remove-AzApplicationGatewayBackendAddressPool</span></span>](./Remove-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="4963e-142">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4963e-142">Set-AzApplicationGatewayBackendAddressPool</span></span>](./Set-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="4963e-143">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="4963e-143">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)
