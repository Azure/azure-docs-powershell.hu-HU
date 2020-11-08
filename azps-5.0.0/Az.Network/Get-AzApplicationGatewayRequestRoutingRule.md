---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 57A6DB40-43EC-402C-9784-06817ECD99B8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 75666d2f897adeda4031b03309979366949a0040
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195697"
---
# <span data-ttu-id="b46b5-101">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="b46b5-101">Get-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="b46b5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b46b5-102">SYNOPSIS</span></span>
<span data-ttu-id="b46b5-103">Az alkalmazás-átjáró kérése útválasztási szabályát kapja.</span><span class="sxs-lookup"><span data-stu-id="b46b5-103">Gets the request routing rule of an application gateway.</span></span>

## <span data-ttu-id="b46b5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b46b5-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayRequestRoutingRule [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b46b5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b46b5-105">DESCRIPTION</span></span>
<span data-ttu-id="b46b5-106">A **Get-AzApplicationGatewayRequestRoutingRule** parancsmag az alkalmazás-átjárók kérése útválasztási szabályát kapja.</span><span class="sxs-lookup"><span data-stu-id="b46b5-106">The **Get-AzApplicationGatewayRequestRoutingRule** cmdlet gets the request routing rule of an application gateway.</span></span>

## <span data-ttu-id="b46b5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b46b5-107">EXAMPLES</span></span>

### <span data-ttu-id="b46b5-108">Példa 1: adott kérés útválasztási szabályának beszerzése</span><span class="sxs-lookup"><span data-stu-id="b46b5-108">Example 1: Get a specific request routing rule</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rule = Get-AzApplicationGatewayRequestRoutingRule -"Rule01" -ApplicationGateway $AppGW
```

<span data-ttu-id="b46b5-109">Az első parancs beolvassa a ApplicationGateway01 nevű alkalmazás-átjárót, és az eredményt az $AppGW nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="b46b5-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="b46b5-110">A második parancs a Rule01 nevű útválasztási szabályt a $AppGW nevű változóban tárolt alkalmazás-átjáróról kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b46b5-110">The second command gets the request routing rule named Rule01 from the Application Gateway stored in the variable named $AppGW.</span></span>

### <span data-ttu-id="b46b5-111">2. példa: a kérési útválasztási szabályok listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="b46b5-111">Example 2: Get a list of request routing rules</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rules = Get-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGW
```

<span data-ttu-id="b46b5-112">Az első parancs beolvassa a ApplicationGateway01 nevű alkalmazás-átjárót, és az eredményt az $AppGW nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="b46b5-112">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="b46b5-113">A második parancs a $AppGW nevű változóban tárolt alkalmazás-útválasztási szabályok listáját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b46b5-113">The second command gets a list of request routing rules from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="b46b5-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b46b5-114">PARAMETERS</span></span>

### <span data-ttu-id="b46b5-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b46b5-115">-ApplicationGateway</span></span>
<span data-ttu-id="b46b5-116">A kérés útválasztási szabályát tartalmazó Application Gateway-objektum.</span><span class="sxs-lookup"><span data-stu-id="b46b5-116">Specifies the application gateway object that contains request routing rule.</span></span>

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

### <span data-ttu-id="b46b5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b46b5-117">-DefaultProfile</span></span>
<span data-ttu-id="b46b5-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b46b5-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b46b5-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b46b5-119">-Name</span></span>
<span data-ttu-id="b46b5-120">Annak a kérési művelettervi szabálynak a nevét adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="b46b5-120">Specifies the name of the request routing rule which this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b46b5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b46b5-121">CommonParameters</span></span>
<span data-ttu-id="b46b5-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b46b5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b46b5-123">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b46b5-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b46b5-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b46b5-124">INPUTS</span></span>

### <span data-ttu-id="b46b5-125">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b46b5-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b46b5-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b46b5-126">OUTPUTS</span></span>

### <span data-ttu-id="b46b5-127">Microsoft. Azure. commands. Network. models. PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="b46b5-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="b46b5-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b46b5-128">NOTES</span></span>

## <span data-ttu-id="b46b5-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b46b5-129">RELATED LINKS</span></span>

[<span data-ttu-id="b46b5-130">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="b46b5-130">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="b46b5-131">Új – AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="b46b5-131">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="b46b5-132">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="b46b5-132">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="b46b5-133">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="b46b5-133">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)

