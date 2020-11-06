---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 289B761C-1A1D-46D2-8755-B6B6A4758EFC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 94cb9e07bc5d4b8d59e543c39ddada5386ebcb27
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493637"
---
# <span data-ttu-id="3907a-101">Remove-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="3907a-101">Remove-AzureRmApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="3907a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3907a-102">SYNOPSIS</span></span>
<span data-ttu-id="3907a-103">Az előtér IP-konfigurációjának eltávolítása egy alkalmazás-átjáróról.</span><span class="sxs-lookup"><span data-stu-id="3907a-103">Removes a front-end IP configuration from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3907a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3907a-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayFrontendIPConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3907a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3907a-105">DESCRIPTION</span></span>
<span data-ttu-id="3907a-106">A **Remove-AzureRmApplicationGatewayFrontendIPConfig** parancsmag az Azure Application Gateway-ből eltávolítja az IP-felületet.</span><span class="sxs-lookup"><span data-stu-id="3907a-106">The **Remove-AzureRmApplicationGatewayFrontendIPConfig** cmdlet removes frontend IP from an Azure application gateway.</span></span>

## <span data-ttu-id="3907a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3907a-107">EXAMPLES</span></span>

### <span data-ttu-id="3907a-108">Példa 1: előtér IP-konfigurációjának eltávolítása</span><span class="sxs-lookup"><span data-stu-id="3907a-108">Example 1: Remove a front-end IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIP02"
```

<span data-ttu-id="3907a-109">Az első parancs a ApplicationGateway01 nevű alkalmazás-átjárót kapja, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="3907a-109">The first command gets an application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="3907a-110">A második parancs eltávolítja a FrontEndIP02 nevű előtér-IP-konfigurációt az $AppGw-ban tárolt alkalmazás-átjáróról.</span><span class="sxs-lookup"><span data-stu-id="3907a-110">The second command removes the front-end IP configuration named FrontEndIP02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="3907a-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3907a-111">PARAMETERS</span></span>

### <span data-ttu-id="3907a-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3907a-112">-ApplicationGateway</span></span>
<span data-ttu-id="3907a-113">Annak az alkalmazásnak az átjáróját adja meg, amelyből el szeretné távolítani az előtér IP-konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="3907a-113">Specifies an application gateway from which to remove a front-end IP configuration.</span></span>

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

### <span data-ttu-id="3907a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3907a-114">-DefaultProfile</span></span>
<span data-ttu-id="3907a-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3907a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3907a-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3907a-116">-Name</span></span>
<span data-ttu-id="3907a-117">Az eltávolítandó előtér IP-konfigurációjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3907a-117">Specifies the name of a front-end IP configuration to remove.</span></span>

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

### <span data-ttu-id="3907a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3907a-118">CommonParameters</span></span>
<span data-ttu-id="3907a-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3907a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3907a-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3907a-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3907a-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3907a-121">INPUTS</span></span>

### <span data-ttu-id="3907a-122">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3907a-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="3907a-123">Paraméterek: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3907a-123">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="3907a-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3907a-124">OUTPUTS</span></span>

### <span data-ttu-id="3907a-125">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3907a-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3907a-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3907a-126">NOTES</span></span>

## <span data-ttu-id="3907a-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3907a-127">RELATED LINKS</span></span>

[<span data-ttu-id="3907a-128">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="3907a-128">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Add-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="3907a-129">Get-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="3907a-129">Get-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Get-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="3907a-130">Új – AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="3907a-130">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./New-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="3907a-131">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="3907a-131">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Set-AzureRmApplicationGatewayFrontendIPConfig.md)


