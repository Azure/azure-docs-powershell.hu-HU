---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: CC033DA8-FACC-44E2-82F9-E30FADBF8926
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 635e1377c5120fcfb1c623634bf857e3f33bd162
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499728"
---
# <span data-ttu-id="2d140-101">Remove-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="2d140-101">Remove-AzureRmApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="2d140-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2d140-102">SYNOPSIS</span></span>
<span data-ttu-id="2d140-103">Request útválasztási szabály eltávolítása egy alkalmazás-átjáróról.</span><span class="sxs-lookup"><span data-stu-id="2d140-103">Removes a request routing rule from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2d140-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2d140-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayRequestRoutingRule -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2d140-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2d140-105">DESCRIPTION</span></span>
<span data-ttu-id="2d140-106">A **Remove-AzureRmApplicationGatewayRequestRoutingRule** parancsmag eltávolítja a kérések útválasztási szabályát egy Azure Application Gateway-ből.</span><span class="sxs-lookup"><span data-stu-id="2d140-106">The **Remove-AzureRmApplicationGatewayRequestRoutingRule** cmdlet removes a request routing rule from an Azure application gateway.</span></span>

## <span data-ttu-id="2d140-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2d140-107">EXAMPLES</span></span>

### <span data-ttu-id="2d140-108">1. példa: a Request Routing Rule eltávolítása egy alkalmazás-átjáróról</span><span class="sxs-lookup"><span data-stu-id="2d140-108">Example 1: Remove a request routing rule from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule02"
```

<span data-ttu-id="2d140-109">Az első parancs beolvassa az Application Gatewayt, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="2d140-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="2d140-110">A második parancs eltávolítja a Rule02 nevű "Request Routing" szabályt a $AppGw-ban tárolt alkalmazás-átjáróról.</span><span class="sxs-lookup"><span data-stu-id="2d140-110">The second command removes the request routing rule named Rule02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="2d140-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2d140-111">PARAMETERS</span></span>

### <span data-ttu-id="2d140-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2d140-112">-ApplicationGateway</span></span>
<span data-ttu-id="2d140-113">Annak az alkalmazásnak az átjáróját adja meg, amelyből el szeretné távolítani a kérések útválasztási szabályát.</span><span class="sxs-lookup"><span data-stu-id="2d140-113">Specifies the application gateway from which to remove a request routing rule.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2d140-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d140-114">-DefaultProfile</span></span>
<span data-ttu-id="2d140-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2d140-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d140-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2d140-116">-Name</span></span>
<span data-ttu-id="2d140-117">Annak a kérési művelettervi szabálynak a neve, amelyhez a parancsmag törlődik.</span><span class="sxs-lookup"><span data-stu-id="2d140-117">Specifies the name of the request routing rule for which this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d140-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d140-118">CommonParameters</span></span>
<span data-ttu-id="2d140-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2d140-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d140-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d140-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d140-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2d140-121">INPUTS</span></span>

### <span data-ttu-id="2d140-122">System. String</span><span class="sxs-lookup"><span data-stu-id="2d140-122">System.String</span></span>

## <span data-ttu-id="2d140-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2d140-123">OUTPUTS</span></span>

### <span data-ttu-id="2d140-124">Microsoft. Azure. commands. Network. models. PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="2d140-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="2d140-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2d140-125">NOTES</span></span>

## <span data-ttu-id="2d140-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2d140-126">RELATED LINKS</span></span>

[<span data-ttu-id="2d140-127">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="2d140-127">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Add-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="2d140-128">Get-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="2d140-128">Get-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Get-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="2d140-129">Új – AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="2d140-129">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./New-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="2d140-130">Set-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="2d140-130">Set-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Set-AzureRmApplicationGatewayRequestRoutingRule.md)


