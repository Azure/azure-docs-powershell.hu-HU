---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: CC033DA8-FACC-44E2-82F9-E30FADBF8926
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: c1c630c39039d39b1957ccab78bb96d8f085176c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185965"
---
# <span data-ttu-id="69c66-101">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="69c66-101">Remove-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="69c66-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="69c66-102">SYNOPSIS</span></span>
<span data-ttu-id="69c66-103">Request útválasztási szabály eltávolítása egy alkalmazás-átjáróról.</span><span class="sxs-lookup"><span data-stu-id="69c66-103">Removes a request routing rule from an application gateway.</span></span>

## <span data-ttu-id="69c66-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="69c66-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayRequestRoutingRule -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69c66-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="69c66-105">DESCRIPTION</span></span>
<span data-ttu-id="69c66-106">A **Remove-AzApplicationGatewayRequestRoutingRule** parancsmag eltávolítja a kérések útválasztási szabályát egy Azure Application Gateway-ből.</span><span class="sxs-lookup"><span data-stu-id="69c66-106">The **Remove-AzApplicationGatewayRequestRoutingRule** cmdlet removes a request routing rule from an Azure application gateway.</span></span>

## <span data-ttu-id="69c66-107">Példák</span><span class="sxs-lookup"><span data-stu-id="69c66-107">EXAMPLES</span></span>

### <span data-ttu-id="69c66-108">1. példa: a Request Routing Rule eltávolítása egy alkalmazás-átjáróról</span><span class="sxs-lookup"><span data-stu-id="69c66-108">Example 1: Remove a request routing rule from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule02"
```

<span data-ttu-id="69c66-109">Az első parancs beolvassa az Application Gatewayt, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="69c66-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="69c66-110">A második parancs eltávolítja a Rule02 nevű "Request Routing" szabályt a $AppGw-ban tárolt alkalmazás-átjáróról.</span><span class="sxs-lookup"><span data-stu-id="69c66-110">The second command removes the request routing rule named Rule02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="69c66-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="69c66-111">PARAMETERS</span></span>

### <span data-ttu-id="69c66-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="69c66-112">-ApplicationGateway</span></span>
<span data-ttu-id="69c66-113">Annak az alkalmazásnak az átjáróját adja meg, amelyből el szeretné távolítani a kérések útválasztási szabályát.</span><span class="sxs-lookup"><span data-stu-id="69c66-113">Specifies the application gateway from which to remove a request routing rule.</span></span>

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

### <span data-ttu-id="69c66-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69c66-114">-DefaultProfile</span></span>
<span data-ttu-id="69c66-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="69c66-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69c66-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="69c66-116">-Name</span></span>
<span data-ttu-id="69c66-117">Annak a kérési művelettervi szabálynak a neve, amelyhez a parancsmag törlődik.</span><span class="sxs-lookup"><span data-stu-id="69c66-117">Specifies the name of the request routing rule for which this cmdlet removes.</span></span>

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

### <span data-ttu-id="69c66-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69c66-118">CommonParameters</span></span>
<span data-ttu-id="69c66-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="69c66-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69c66-120">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69c66-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69c66-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="69c66-121">INPUTS</span></span>

### <span data-ttu-id="69c66-122">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="69c66-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="69c66-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="69c66-123">OUTPUTS</span></span>

### <span data-ttu-id="69c66-124">Microsoft. Azure. commands. Network. models. PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="69c66-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="69c66-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="69c66-125">NOTES</span></span>

## <span data-ttu-id="69c66-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="69c66-126">RELATED LINKS</span></span>

[<span data-ttu-id="69c66-127">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="69c66-127">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="69c66-128">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="69c66-128">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="69c66-129">Új – AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="69c66-129">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="69c66-130">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="69c66-130">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)

