---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6FBFAEFF-786D-440A-94B2-8C27BE033A0A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: c415fb890240ea6f4fb03b71c3a249eece1ba02b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203264"
---
# <span data-ttu-id="a432f-101">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a432f-101">Add-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="a432f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a432f-102">SYNOPSIS</span></span>
<span data-ttu-id="a432f-103">Háttércímkészletet ad hozzá egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="a432f-103">Adds a back-end address pool to an application gateway.</span></span>

## <span data-ttu-id="a432f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a432f-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayBackendAddressPool -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-BackendIPAddresses <String[]>] [-BackendFqdns <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a432f-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a432f-105">DESCRIPTION</span></span>
<span data-ttu-id="a432f-106">Az **Add-AzApplicationGatewayBackendAddressPool** parancsmag hozzáad egy háttércímkészletet egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="a432f-106">The **Add-AzApplicationGatewayBackendAddressPool** cmdlet adds a back-end address pool to an application gateway.</span></span>
<span data-ttu-id="a432f-107">A háttércímek IP-címek, teljes tartománynév (FQDN) vagy IP-konfigurációs IP-címek használatával is megadva.</span><span class="sxs-lookup"><span data-stu-id="a432f-107">A back-end address can be specified using an IP address, a fully-qualified domain name (FQDN) or IP configuration IDs.</span></span>

## <span data-ttu-id="a432f-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a432f-108">EXAMPLES</span></span>

### <span data-ttu-id="a432f-109">1. példa: Háttércímkészlet hozzáadása háttérkiszolgáló teljes tartományának használatával</span><span class="sxs-lookup"><span data-stu-id="a432f-109">Example 1: Add a back-end address pool by using a back-end server FQDN</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendFqdns "contoso1.com", " contoso1.com"
```

<span data-ttu-id="a432f-110">Az első parancs az ApplicationGateway01 nevű alkalmazás-átjárót az ResourceGroup01 nevű erőforráscsoportban tárolja a $AppGw változóban. A második parancs a teljes tartományon keresztül hozzáadja a $AppGw az alkalmazás-átjáró háttércímkészletét.</span><span class="sxs-lookup"><span data-stu-id="a432f-110">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command adds the back-end address pool of the application gateway stored in $AppGw by using FQDNs.</span></span>

### <span data-ttu-id="a432f-111">2. példa: Háttércímkészlet hozzáadása háttérkiszolgálói IP-címek használatával</span><span class="sxs-lookup"><span data-stu-id="a432f-111">Example 2: Add a back-end address pool by using backend server IP addresses</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayBackendAddressPool -ApplicationGateway $ AppGw -Name "Pool02" -BackendIPAddresses "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="a432f-112">Az első parancs az ApplicationGateway01 nevű alkalmazás-átjárót az ResourceGroup01 nevű erőforráscsoportban tárolja a $AppGw változóban. A második parancs IP-címek használatával hozzáadja az adott helyen tárolt alkalmazás$AppGw címkészletét.</span><span class="sxs-lookup"><span data-stu-id="a432f-112">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command adds the back-end address pool of the application gateway stored in $AppGw by using IP addresses.</span></span>

## <span data-ttu-id="a432f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a432f-113">PARAMETERS</span></span>

### <span data-ttu-id="a432f-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a432f-114">-ApplicationGateway</span></span>
<span data-ttu-id="a432f-115">Megadja azt az alkalmazás-átjárót, amelyhez ez a parancsmag hozzáad egy háttércímkészletet.</span><span class="sxs-lookup"><span data-stu-id="a432f-115">Specifies the application gateway to which this cmdlet adds a back-end address pool.</span></span>

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

### <span data-ttu-id="a432f-116">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="a432f-116">-BackendFqdns</span></span>
<span data-ttu-id="a432f-117">Megadja a háttérkiszolgálói FQDN-ek listáját, amelyeket ez a parancsmag háttérkiszolgáló-készletként ad hozzá.</span><span class="sxs-lookup"><span data-stu-id="a432f-117">Specifies a list of backend FQDNs which this cmdlet adds as a back-end server pool.</span></span>

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

### <span data-ttu-id="a432f-118">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="a432f-118">-BackendIPAddresses</span></span>
<span data-ttu-id="a432f-119">Megadja a háttér-IP-címek listáját, amelyeket ez a parancsmag háttérkiszolgáló-készletként ad hozzá.</span><span class="sxs-lookup"><span data-stu-id="a432f-119">Specifies a list of back-end IP addresses which this cmdlet adds as a back-end server pool.</span></span>

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

### <span data-ttu-id="a432f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a432f-120">-DefaultProfile</span></span>
<span data-ttu-id="a432f-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a432f-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a432f-122">-Name</span><span class="sxs-lookup"><span data-stu-id="a432f-122">-Name</span></span>
<span data-ttu-id="a432f-123">A parancsmag által hozzáadt háttérkiszolgáló-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="a432f-123">Specifies the name of the back-end server pool that this cmdlet adds.</span></span>

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

### <span data-ttu-id="a432f-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a432f-124">-Confirm</span></span>
<span data-ttu-id="a432f-125">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a432f-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a432f-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a432f-126">-WhatIf</span></span>
<span data-ttu-id="a432f-127">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a432f-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a432f-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a432f-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a432f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a432f-129">CommonParameters</span></span>
<span data-ttu-id="a432f-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a432f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a432f-131">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a432f-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a432f-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a432f-132">INPUTS</span></span>

### <span data-ttu-id="a432f-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a432f-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a432f-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a432f-134">OUTPUTS</span></span>

### <span data-ttu-id="a432f-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a432f-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a432f-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a432f-136">NOTES</span></span>

## <span data-ttu-id="a432f-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a432f-137">RELATED LINKS</span></span>

[<span data-ttu-id="a432f-138">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a432f-138">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="a432f-139">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a432f-139">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="a432f-140">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a432f-140">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="a432f-141">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a432f-141">Remove-AzApplicationGatewayBackendAddressPool</span></span>](./Remove-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="a432f-142">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a432f-142">Set-AzApplicationGatewayBackendAddressPool</span></span>](./Set-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="a432f-143">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="a432f-143">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)
