---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 57A6DB40-43EC-402C-9784-06817ECD99B8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 7657b9e10a17ea53ad39594dc4013383d96f311c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837627"
---
# <span data-ttu-id="a0784-101">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="a0784-101">Get-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="a0784-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a0784-102">SYNOPSIS</span></span>
<span data-ttu-id="a0784-103">Az alkalmazás-átjáró kérése útválasztási szabályát kapja.</span><span class="sxs-lookup"><span data-stu-id="a0784-103">Gets the request routing rule of an application gateway.</span></span>

## <span data-ttu-id="a0784-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a0784-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayRequestRoutingRule [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a0784-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a0784-105">DESCRIPTION</span></span>
<span data-ttu-id="a0784-106">A **Get-AzApplicationGatewayRequestRoutingRule** parancsmag az alkalmazás-átjárók kérése útválasztási szabályát kapja.</span><span class="sxs-lookup"><span data-stu-id="a0784-106">The **Get-AzApplicationGatewayRequestRoutingRule** cmdlet gets the request routing rule of an application gateway.</span></span>

## <span data-ttu-id="a0784-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a0784-107">EXAMPLES</span></span>

### <span data-ttu-id="a0784-108">Példa 1: adott kérés útválasztási szabályának beszerzése</span><span class="sxs-lookup"><span data-stu-id="a0784-108">Example 1: Get a specific request routing rule</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rule = Get-AzApplicationGatewayRequestRoutingRule -"Rule01" -ApplicationGateway $AppGW
```

<span data-ttu-id="a0784-109">Az első parancs beolvassa a ApplicationGateway01 nevű alkalmazás-átjárót, és az eredményt az $AppGW nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="a0784-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="a0784-110">A második parancs a Rule01 nevű útválasztási szabályt a $AppGW nevű változóban tárolt alkalmazás-átjáróról kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a0784-110">The second command gets the request routing rule named Rule01 from the Application Gateway stored in the variable named $AppGW.</span></span>

### <span data-ttu-id="a0784-111">2. példa: a kérési útválasztási szabályok listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="a0784-111">Example 2: Get a list of request routing rules</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rules = Get-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGW
```

<span data-ttu-id="a0784-112">Az első parancs beolvassa a ApplicationGateway01 nevű alkalmazás-átjárót, és az eredményt az $AppGW nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="a0784-112">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="a0784-113">A második parancs a $AppGW nevű változóban tárolt alkalmazás-útválasztási szabályok listáját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a0784-113">The second command gets a list of request routing rules from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="a0784-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a0784-114">PARAMETERS</span></span>

### <span data-ttu-id="a0784-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a0784-115">-ApplicationGateway</span></span>
<span data-ttu-id="a0784-116">A kérés útválasztási szabályát tartalmazó Application Gateway-objektum.</span><span class="sxs-lookup"><span data-stu-id="a0784-116">Specifies the application gateway object that contains request routing rule.</span></span>

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

### <span data-ttu-id="a0784-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0784-117">-DefaultProfile</span></span>
<span data-ttu-id="a0784-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a0784-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a0784-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a0784-119">-Name</span></span>
<span data-ttu-id="a0784-120">Annak a kérési művelettervi szabálynak a nevét adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="a0784-120">Specifies the name of the request routing rule which this cmdlet gets.</span></span>

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

### <span data-ttu-id="a0784-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0784-121">CommonParameters</span></span>
<span data-ttu-id="a0784-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a0784-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0784-123">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a0784-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0784-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a0784-124">INPUTS</span></span>

### <span data-ttu-id="a0784-125">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a0784-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a0784-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a0784-126">OUTPUTS</span></span>

### <span data-ttu-id="a0784-127">Microsoft. Azure. commands. Network. models. PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="a0784-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="a0784-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a0784-128">NOTES</span></span>

## <span data-ttu-id="a0784-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a0784-129">RELATED LINKS</span></span>

[<span data-ttu-id="a0784-130">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="a0784-130">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="a0784-131">Új – AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="a0784-131">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="a0784-132">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="a0784-132">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="a0784-133">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="a0784-133">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


