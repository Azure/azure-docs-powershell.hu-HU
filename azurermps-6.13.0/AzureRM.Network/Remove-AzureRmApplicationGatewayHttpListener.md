---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6C90AF6C-3193-4D75-A78F-3EC315C6D7DF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayHttpListener.md
ms.openlocfilehash: 4079d8b6859a2860116520c52928d13c7e3fa29e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680634"
---
# <span data-ttu-id="72da2-101">Remove-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="72da2-101">Remove-AzureRmApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="72da2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="72da2-102">SYNOPSIS</span></span>
<span data-ttu-id="72da2-103">A HTTP-figyelők eltávolítása egy alkalmazás-átjáróról.</span><span class="sxs-lookup"><span data-stu-id="72da2-103">Removes an HTTP listener from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72da2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="72da2-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayHttpListener -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72da2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="72da2-105">DESCRIPTION</span></span>
<span data-ttu-id="72da2-106">A **Remove-AzureRmApplicationGatewayHttpListener** parancsmag ELTÁVOLÍTJA a http-figyelőt egy Azure Application Gateway-webhelyről.</span><span class="sxs-lookup"><span data-stu-id="72da2-106">The **Remove-AzureRmApplicationGatewayHttpListener** cmdlet removes an HTTP listener from an Azure application gateway.</span></span>

## <span data-ttu-id="72da2-107">Példák</span><span class="sxs-lookup"><span data-stu-id="72da2-107">EXAMPLES</span></span>

### <span data-ttu-id="72da2-108">1. példa: az alkalmazás-átjárók HTTP-figyelésének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="72da2-108">Example 1: Remove an application gateway HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener02"
```

<span data-ttu-id="72da2-109">Az első parancs beolvassa az Application Gatewayt, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="72da2-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="72da2-110">A második parancs eltávolítja a Listener02 nevű HTTP-figyelőt a $AppGwban tárolt alkalmazás-átjáróról.</span><span class="sxs-lookup"><span data-stu-id="72da2-110">The second command removes the HTTP listener named Listener02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="72da2-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="72da2-111">PARAMETERS</span></span>

### <span data-ttu-id="72da2-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="72da2-112">-ApplicationGateway</span></span>
<span data-ttu-id="72da2-113">Annak az alkalmazásnak az átjáróját adja meg, amelyből el szeretné távolítani a HTTP-figyelőt.</span><span class="sxs-lookup"><span data-stu-id="72da2-113">Specifies the application gateway from which to remove an HTTP listener.</span></span>

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

### <span data-ttu-id="72da2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72da2-114">-DefaultProfile</span></span>
<span data-ttu-id="72da2-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="72da2-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72da2-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="72da2-116">-Name</span></span>
<span data-ttu-id="72da2-117">Megadja annak a HTTP-figyelőnek a nevét, amely a parancsmag eltávolítását okozta.</span><span class="sxs-lookup"><span data-stu-id="72da2-117">Specifies the name of the HTTP listener that this cmdlet removes.</span></span>

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

### <span data-ttu-id="72da2-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72da2-118">CommonParameters</span></span>
<span data-ttu-id="72da2-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="72da2-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72da2-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72da2-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72da2-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="72da2-121">INPUTS</span></span>

### <span data-ttu-id="72da2-122">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="72da2-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="72da2-123">Paraméterek: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="72da2-123">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="72da2-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="72da2-124">OUTPUTS</span></span>

### <span data-ttu-id="72da2-125">Microsoft. Azure. commands. Network. models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="72da2-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="72da2-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="72da2-126">NOTES</span></span>

## <span data-ttu-id="72da2-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="72da2-127">RELATED LINKS</span></span>

[<span data-ttu-id="72da2-128">Add-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="72da2-128">Add-AzureRmApplicationGatewayHttpListener</span></span>](./Add-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="72da2-129">Get-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="72da2-129">Get-AzureRmApplicationGatewayHttpListener</span></span>](./Get-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="72da2-130">Új – AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="72da2-130">New-AzureRmApplicationGatewayHttpListener</span></span>](./New-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="72da2-131">Set-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="72da2-131">Set-AzureRmApplicationGatewayHttpListener</span></span>](./Set-AzureRmApplicationGatewayHttpListener.md)


