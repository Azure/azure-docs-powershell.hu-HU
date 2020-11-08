---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 289B761C-1A1D-46D2-8755-B6B6A4758EFC
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 8abfca99729dcbf99592a8efcb191e6a7883e3b4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94002813"
---
# <span data-ttu-id="b1b0f-101">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="b1b0f-101">Remove-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="b1b0f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b1b0f-102">SYNOPSIS</span></span>
<span data-ttu-id="b1b0f-103">Az előtér IP-konfigurációjának eltávolítása egy alkalmazás-átjáróról.</span><span class="sxs-lookup"><span data-stu-id="b1b0f-103">Removes a front-end IP configuration from an application gateway.</span></span>

## <span data-ttu-id="b1b0f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b1b0f-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayFrontendIPConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1b0f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b1b0f-105">DESCRIPTION</span></span>
<span data-ttu-id="b1b0f-106">A **Remove-AzApplicationGatewayFrontendIPConfig** parancsmag az Azure Application Gateway-ből eltávolítja az IP-felületet.</span><span class="sxs-lookup"><span data-stu-id="b1b0f-106">The **Remove-AzApplicationGatewayFrontendIPConfig** cmdlet removes frontend IP from an Azure application gateway.</span></span>

## <span data-ttu-id="b1b0f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b1b0f-107">EXAMPLES</span></span>

### <span data-ttu-id="b1b0f-108">Példa 1: előtér IP-konfigurációjának eltávolítása</span><span class="sxs-lookup"><span data-stu-id="b1b0f-108">Example 1: Remove a front-end IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIP02"
```

<span data-ttu-id="b1b0f-109">Az első parancs a ApplicationGateway01 nevű alkalmazás-átjárót kapja, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="b1b0f-109">The first command gets an application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="b1b0f-110">A második parancs eltávolítja a FrontEndIP02 nevű előtér-IP-konfigurációt az $AppGw-ban tárolt alkalmazás-átjáróról.</span><span class="sxs-lookup"><span data-stu-id="b1b0f-110">The second command removes the front-end IP configuration named FrontEndIP02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="b1b0f-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b1b0f-111">PARAMETERS</span></span>

### <span data-ttu-id="b1b0f-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b1b0f-112">-ApplicationGateway</span></span>
<span data-ttu-id="b1b0f-113">Annak az alkalmazásnak az átjáróját adja meg, amelyből el szeretné távolítani az előtér IP-konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="b1b0f-113">Specifies an application gateway from which to remove a front-end IP configuration.</span></span>

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

### <span data-ttu-id="b1b0f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1b0f-114">-DefaultProfile</span></span>
<span data-ttu-id="b1b0f-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b1b0f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1b0f-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b1b0f-116">-Name</span></span>
<span data-ttu-id="b1b0f-117">Az eltávolítandó előtér IP-konfigurációjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b1b0f-117">Specifies the name of a front-end IP configuration to remove.</span></span>

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

### <span data-ttu-id="b1b0f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1b0f-118">CommonParameters</span></span>
<span data-ttu-id="b1b0f-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b1b0f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1b0f-120">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1b0f-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1b0f-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b1b0f-121">INPUTS</span></span>

### <span data-ttu-id="b1b0f-122">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b1b0f-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b1b0f-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b1b0f-123">OUTPUTS</span></span>

### <span data-ttu-id="b1b0f-124">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b1b0f-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b1b0f-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b1b0f-125">NOTES</span></span>

## <span data-ttu-id="b1b0f-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b1b0f-126">RELATED LINKS</span></span>

[<span data-ttu-id="b1b0f-127">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="b1b0f-127">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="b1b0f-128">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="b1b0f-128">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="b1b0f-129">Új – AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="b1b0f-129">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="b1b0f-130">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="b1b0f-130">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)


