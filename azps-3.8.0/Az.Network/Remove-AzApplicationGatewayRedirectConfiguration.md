---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: fdd461ea2908e59ba824b09a49bed3b6b8f4d38f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94002802"
---
# <span data-ttu-id="c37ac-101">Remove-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="c37ac-101">Remove-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="c37ac-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c37ac-102">SYNOPSIS</span></span>
<span data-ttu-id="c37ac-103">Átirányítási konfiguráció eltávolítása egy meglévő alkalmazás-átjáróról.</span><span class="sxs-lookup"><span data-stu-id="c37ac-103">Removes a redirect configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="c37ac-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c37ac-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayRedirectConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c37ac-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c37ac-105">DESCRIPTION</span></span>
<span data-ttu-id="c37ac-106">A **Remove-AzApplicationGatewayRedirectConfiguration** parancsmag egy meglévő alkalmazás-átjáróból távolítja el az átirányítás konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="c37ac-106">The **Remove-AzApplicationGatewayRedirectConfiguration** cmdlet removes a redirect configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="c37ac-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c37ac-107">EXAMPLES</span></span>

### <span data-ttu-id="c37ac-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c37ac-108">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\>$AppGw = Remove-AzApplicationGatewayRedirectConfiguration -ApplicationGateway $AppGw -Name "Redirect01"
```

<span data-ttu-id="c37ac-109">Az első parancs beolvassa az Application Gatewayt, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="c37ac-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="c37ac-110">A második parancs eltávolítja a Redirect01 nevű átirányítás-konfigurációt az $AppGw-ban tárolt alkalmazás-átjáróról.</span><span class="sxs-lookup"><span data-stu-id="c37ac-110">The second command removes the redirect configuration named Redirect01 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="c37ac-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c37ac-111">PARAMETERS</span></span>

### <span data-ttu-id="c37ac-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c37ac-112">-ApplicationGateway</span></span>
<span data-ttu-id="c37ac-113">A applicationGateway</span><span class="sxs-lookup"><span data-stu-id="c37ac-113">The applicationGateway</span></span>

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

### <span data-ttu-id="c37ac-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c37ac-114">-DefaultProfile</span></span>
<span data-ttu-id="c37ac-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c37ac-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c37ac-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c37ac-116">-Name</span></span>
<span data-ttu-id="c37ac-117">Az átirányítási konfiguráció neve</span><span class="sxs-lookup"><span data-stu-id="c37ac-117">The name of the redirect configuration</span></span>

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

### <span data-ttu-id="c37ac-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c37ac-118">CommonParameters</span></span>
<span data-ttu-id="c37ac-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c37ac-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c37ac-120">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c37ac-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c37ac-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c37ac-121">INPUTS</span></span>

### <span data-ttu-id="c37ac-122">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c37ac-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c37ac-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c37ac-123">OUTPUTS</span></span>

### <span data-ttu-id="c37ac-124">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c37ac-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c37ac-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c37ac-125">NOTES</span></span>

## <span data-ttu-id="c37ac-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c37ac-126">RELATED LINKS</span></span>

[<span data-ttu-id="c37ac-127">Add-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="c37ac-127">Add-AzApplicationGatewayRedirectConfiguration</span></span>](./Add-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="c37ac-128">Get-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="c37ac-128">Get-AzApplicationGatewayRedirectConfiguration</span></span>](./Get-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="c37ac-129">Új – AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="c37ac-129">New-AzApplicationGatewayRedirectConfiguration</span></span>](./New-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="c37ac-130">Set-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="c37ac-130">Set-AzApplicationGatewayRedirectConfiguration</span></span>](./Set-AzApplicationGatewayRedirectConfiguration.md)
