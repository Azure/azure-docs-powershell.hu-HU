---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 40198C86-A4EB-494A-86D5-DF632518EB95
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: 9cd7cd0b859ff806b084ebfe1c76e07aed3a7c43
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014326"
---
# <span data-ttu-id="b8cf6-101">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="b8cf6-101">Add-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="b8cf6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b8cf6-102">SYNOPSIS</span></span>
<span data-ttu-id="b8cf6-103">Az előtér-portot hozzáadja az alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="b8cf6-103">Adds a front-end port to an application gateway.</span></span>

## <span data-ttu-id="b8cf6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b8cf6-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayFrontendPort -ApplicationGateway <PSApplicationGateway> -Name <String> -Port <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8cf6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b8cf6-105">DESCRIPTION</span></span>
<span data-ttu-id="b8cf6-106">Az **Add-AzApplicationGatewayFrontendPort** parancsmag egy előtér-portot ad az alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="b8cf6-106">The **Add-AzApplicationGatewayFrontendPort** cmdlet adds a front-end port to an application gateway.</span></span>

## <span data-ttu-id="b8cf6-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b8cf6-107">EXAMPLES</span></span>

### <span data-ttu-id="b8cf6-108">1. példa: előtér-végpont hozzáadása az alkalmazás-átjáróhoz</span><span class="sxs-lookup"><span data-stu-id="b8cf6-108">Example 1: Add a front-end port to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="b8cf6-109">Az első parancs megkapja a ApplicationGateway01 nevű alkalmazás-átjárót, amely a ResourceGroup01 nevű erőforráscsoport csoportjába tartozik, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="b8cf6-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="b8cf6-110">A második parancs hozzáadja a 80-as portot az $AppGw tárolt alkalmazási átjáróhoz, és megnevezi a port FrontEndPort01.</span><span class="sxs-lookup"><span data-stu-id="b8cf6-110">The second command adds port 80 as a front-end port for the application gateway stored in $AppGw and names the port FrontEndPort01.</span></span>

## <span data-ttu-id="b8cf6-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b8cf6-111">PARAMETERS</span></span>

### <span data-ttu-id="b8cf6-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b8cf6-112">-ApplicationGateway</span></span>
<span data-ttu-id="b8cf6-113">Annak az alkalmazásnak az átjáróját adja meg, amelyre a parancsmag az előtér-portot adja hozzá.</span><span class="sxs-lookup"><span data-stu-id="b8cf6-113">Specifies the application gateway to which this cmdlet adds a front-end port.</span></span>

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

### <span data-ttu-id="b8cf6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8cf6-114">-DefaultProfile</span></span>
<span data-ttu-id="b8cf6-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b8cf6-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8cf6-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b8cf6-116">-Name</span></span>
<span data-ttu-id="b8cf6-117">Az előtér-port nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b8cf6-117">Specifies the name of the front-end port.</span></span>

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

### <span data-ttu-id="b8cf6-118">-Port</span><span class="sxs-lookup"><span data-stu-id="b8cf6-118">-Port</span></span>
<span data-ttu-id="b8cf6-119">A portszámot adja meg.</span><span class="sxs-lookup"><span data-stu-id="b8cf6-119">Specifies the port number.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8cf6-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8cf6-120">CommonParameters</span></span>
<span data-ttu-id="b8cf6-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b8cf6-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8cf6-122">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8cf6-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8cf6-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b8cf6-123">INPUTS</span></span>

### <span data-ttu-id="b8cf6-124">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b8cf6-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b8cf6-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b8cf6-125">OUTPUTS</span></span>

### <span data-ttu-id="b8cf6-126">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b8cf6-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b8cf6-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b8cf6-127">NOTES</span></span>

## <span data-ttu-id="b8cf6-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b8cf6-128">RELATED LINKS</span></span>

[<span data-ttu-id="b8cf6-129">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="b8cf6-129">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="b8cf6-130">Új – AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="b8cf6-130">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="b8cf6-131">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="b8cf6-131">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="b8cf6-132">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="b8cf6-132">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


