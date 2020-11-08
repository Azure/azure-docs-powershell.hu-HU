---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6C90AF6C-3193-4D75-A78F-3EC315C6D7DF
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 81b750188a85add491e519c023c765f302e31dea
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024592"
---
# <span data-ttu-id="36521-101">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="36521-101">Remove-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="36521-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="36521-102">SYNOPSIS</span></span>
<span data-ttu-id="36521-103">A HTTP-figyelők eltávolítása egy alkalmazás-átjáróról.</span><span class="sxs-lookup"><span data-stu-id="36521-103">Removes an HTTP listener from an application gateway.</span></span>

## <span data-ttu-id="36521-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="36521-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayHttpListener -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36521-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="36521-105">DESCRIPTION</span></span>
<span data-ttu-id="36521-106">A **Remove-AzApplicationGatewayHttpListener** parancsmag ELTÁVOLÍTJA a http-figyelőt egy Azure Application Gateway-webhelyről.</span><span class="sxs-lookup"><span data-stu-id="36521-106">The **Remove-AzApplicationGatewayHttpListener** cmdlet removes an HTTP listener from an Azure application gateway.</span></span>

## <span data-ttu-id="36521-107">Példák</span><span class="sxs-lookup"><span data-stu-id="36521-107">EXAMPLES</span></span>

### <span data-ttu-id="36521-108">1. példa: az alkalmazás-átjárók HTTP-figyelésének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="36521-108">Example 1: Remove an application gateway HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener02"
```

<span data-ttu-id="36521-109">Az első parancs beolvassa az Application Gatewayt, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="36521-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="36521-110">A második parancs eltávolítja a Listener02 nevű HTTP-figyelőt a $AppGwban tárolt alkalmazás-átjáróról.</span><span class="sxs-lookup"><span data-stu-id="36521-110">The second command removes the HTTP listener named Listener02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="36521-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="36521-111">PARAMETERS</span></span>

### <span data-ttu-id="36521-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="36521-112">-ApplicationGateway</span></span>
<span data-ttu-id="36521-113">Annak az alkalmazásnak az átjáróját adja meg, amelyből el szeretné távolítani a HTTP-figyelőt.</span><span class="sxs-lookup"><span data-stu-id="36521-113">Specifies the application gateway from which to remove an HTTP listener.</span></span>

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

### <span data-ttu-id="36521-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36521-114">-DefaultProfile</span></span>
<span data-ttu-id="36521-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="36521-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36521-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="36521-116">-Name</span></span>
<span data-ttu-id="36521-117">Megadja annak a HTTP-figyelőnek a nevét, amely a parancsmag eltávolítását okozta.</span><span class="sxs-lookup"><span data-stu-id="36521-117">Specifies the name of the HTTP listener that this cmdlet removes.</span></span>

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

### <span data-ttu-id="36521-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36521-118">CommonParameters</span></span>
<span data-ttu-id="36521-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="36521-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36521-120">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36521-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36521-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="36521-121">INPUTS</span></span>

### <span data-ttu-id="36521-122">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="36521-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="36521-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="36521-123">OUTPUTS</span></span>

### <span data-ttu-id="36521-124">Microsoft. Azure. commands. Network. models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="36521-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="36521-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="36521-125">NOTES</span></span>

## <span data-ttu-id="36521-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="36521-126">RELATED LINKS</span></span>

[<span data-ttu-id="36521-127">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="36521-127">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="36521-128">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="36521-128">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="36521-129">Új – AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="36521-129">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="36521-130">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="36521-130">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


