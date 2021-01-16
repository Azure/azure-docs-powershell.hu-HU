---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 57A6DB40-43EC-402C-9784-06817ECD99B8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 75666d2f897adeda4031b03309979366949a0040
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98351882"
---
# <span data-ttu-id="4459c-101">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="4459c-101">Get-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="4459c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4459c-102">SYNOPSIS</span></span>
<span data-ttu-id="4459c-103">Egy alkalmazás-átjáró kéréstovábbító szabályát kéri le.</span><span class="sxs-lookup"><span data-stu-id="4459c-103">Gets the request routing rule of an application gateway.</span></span>

## <span data-ttu-id="4459c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4459c-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayRequestRoutingRule [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4459c-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4459c-105">DESCRIPTION</span></span>
<span data-ttu-id="4459c-106">A **Get-AzApplicationGatewayRequestRoutingRule** parancsmag egy alkalmazás-átjáró kéréstovábbítási szabályát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="4459c-106">The **Get-AzApplicationGatewayRequestRoutingRule** cmdlet gets the request routing rule of an application gateway.</span></span>

## <span data-ttu-id="4459c-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4459c-107">EXAMPLES</span></span>

### <span data-ttu-id="4459c-108">1. példa: Konkrét kéréstovábbirányítási szabály kérése</span><span class="sxs-lookup"><span data-stu-id="4459c-108">Example 1: Get a specific request routing rule</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rule = Get-AzApplicationGatewayRequestRoutingRule -"Rule01" -ApplicationGateway $AppGW
```

<span data-ttu-id="4459c-109">Az első parancs az ApplicationGateway01 nevű Alkalmazás-átjárót kapja meg, és az eredményt a következő nevű változóban $AppGW.</span><span class="sxs-lookup"><span data-stu-id="4459c-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="4459c-110">A második parancs a Szabály01 nevű kéréstovábbítási szabályt az adott változóban tárolt alkalmazás-átjáróból $AppGW.</span><span class="sxs-lookup"><span data-stu-id="4459c-110">The second command gets the request routing rule named Rule01 from the Application Gateway stored in the variable named $AppGW.</span></span>

### <span data-ttu-id="4459c-111">2. példa: Kéréstovább kiszolgálói szabályok listájának lekérése</span><span class="sxs-lookup"><span data-stu-id="4459c-111">Example 2: Get a list of request routing rules</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rules = Get-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGW
```

<span data-ttu-id="4459c-112">Az első parancs az ApplicationGateway01 nevű Alkalmazás-átjárót kapja meg, és az eredményt a következő nevű változóban $AppGW.</span><span class="sxs-lookup"><span data-stu-id="4459c-112">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="4459c-113">A második parancs a kéréstovábbítási szabályok listáját kapja meg a $AppGW.</span><span class="sxs-lookup"><span data-stu-id="4459c-113">The second command gets a list of request routing rules from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="4459c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4459c-114">PARAMETERS</span></span>

### <span data-ttu-id="4459c-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4459c-115">-ApplicationGateway</span></span>
<span data-ttu-id="4459c-116">Megadja azt az alkalmazás-átjáróobjektumot, amely kéréstovábbító szabályt tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="4459c-116">Specifies the application gateway object that contains request routing rule.</span></span>

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

### <span data-ttu-id="4459c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4459c-117">-DefaultProfile</span></span>
<span data-ttu-id="4459c-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4459c-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4459c-119">-Name</span><span class="sxs-lookup"><span data-stu-id="4459c-119">-Name</span></span>
<span data-ttu-id="4459c-120">Megadja annak a kérés-útválasztási szabálynak a nevét, amelyet ez a parancsmag kap.</span><span class="sxs-lookup"><span data-stu-id="4459c-120">Specifies the name of the request routing rule which this cmdlet gets.</span></span>

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

### <span data-ttu-id="4459c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4459c-121">CommonParameters</span></span>
<span data-ttu-id="4459c-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4459c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4459c-123">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4459c-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4459c-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4459c-124">INPUTS</span></span>

### <span data-ttu-id="4459c-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4459c-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4459c-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4459c-126">OUTPUTS</span></span>

### <span data-ttu-id="4459c-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="4459c-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="4459c-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4459c-128">NOTES</span></span>

## <span data-ttu-id="4459c-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4459c-129">RELATED LINKS</span></span>

[<span data-ttu-id="4459c-130">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="4459c-130">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="4459c-131">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="4459c-131">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="4459c-132">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="4459c-132">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="4459c-133">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="4459c-133">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


