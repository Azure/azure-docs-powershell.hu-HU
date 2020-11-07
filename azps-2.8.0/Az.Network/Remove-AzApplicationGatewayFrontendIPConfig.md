---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 289B761C-1A1D-46D2-8755-B6B6A4758EFC
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 72cc21b697b2dbdc05ad7106fca5687203aec870
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837133"
---
# <span data-ttu-id="cb4a4-101">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="cb4a4-101">Remove-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="cb4a4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cb4a4-102">SYNOPSIS</span></span>
<span data-ttu-id="cb4a4-103">Az előtér IP-konfigurációjának eltávolítása egy alkalmazás-átjáróról.</span><span class="sxs-lookup"><span data-stu-id="cb4a4-103">Removes a front-end IP configuration from an application gateway.</span></span>

## <span data-ttu-id="cb4a4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cb4a4-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayFrontendIPConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb4a4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cb4a4-105">DESCRIPTION</span></span>
<span data-ttu-id="cb4a4-106">A **Remove-AzApplicationGatewayFrontendIPConfig** parancsmag az Azure Application Gateway-ből eltávolítja az IP-felületet.</span><span class="sxs-lookup"><span data-stu-id="cb4a4-106">The **Remove-AzApplicationGatewayFrontendIPConfig** cmdlet removes frontend IP from an Azure application gateway.</span></span>

## <span data-ttu-id="cb4a4-107">Példák</span><span class="sxs-lookup"><span data-stu-id="cb4a4-107">EXAMPLES</span></span>

### <span data-ttu-id="cb4a4-108">Példa 1: előtér IP-konfigurációjának eltávolítása</span><span class="sxs-lookup"><span data-stu-id="cb4a4-108">Example 1: Remove a front-end IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIP02"
```

<span data-ttu-id="cb4a4-109">Az első parancs a ApplicationGateway01 nevű alkalmazás-átjárót kapja, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="cb4a4-109">The first command gets an application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="cb4a4-110">A második parancs eltávolítja a FrontEndIP02 nevű előtér-IP-konfigurációt az $AppGw-ban tárolt alkalmazás-átjáróról.</span><span class="sxs-lookup"><span data-stu-id="cb4a4-110">The second command removes the front-end IP configuration named FrontEndIP02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="cb4a4-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cb4a4-111">PARAMETERS</span></span>

### <span data-ttu-id="cb4a4-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cb4a4-112">-ApplicationGateway</span></span>
<span data-ttu-id="cb4a4-113">Annak az alkalmazásnak az átjáróját adja meg, amelyből el szeretné távolítani az előtér IP-konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="cb4a4-113">Specifies an application gateway from which to remove a front-end IP configuration.</span></span>

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

### <span data-ttu-id="cb4a4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb4a4-114">-DefaultProfile</span></span>
<span data-ttu-id="cb4a4-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cb4a4-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb4a4-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cb4a4-116">-Name</span></span>
<span data-ttu-id="cb4a4-117">Az eltávolítandó előtér IP-konfigurációjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cb4a4-117">Specifies the name of a front-end IP configuration to remove.</span></span>

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

### <span data-ttu-id="cb4a4-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb4a4-118">CommonParameters</span></span>
<span data-ttu-id="cb4a4-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cb4a4-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb4a4-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb4a4-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb4a4-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cb4a4-121">INPUTS</span></span>

### <span data-ttu-id="cb4a4-122">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cb4a4-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="cb4a4-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cb4a4-123">OUTPUTS</span></span>

### <span data-ttu-id="cb4a4-124">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cb4a4-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="cb4a4-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cb4a4-125">NOTES</span></span>

## <span data-ttu-id="cb4a4-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cb4a4-126">RELATED LINKS</span></span>

[<span data-ttu-id="cb4a4-127">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="cb4a4-127">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="cb4a4-128">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="cb4a4-128">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="cb4a4-129">Új – AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="cb4a4-129">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="cb4a4-130">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="cb4a4-130">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)


