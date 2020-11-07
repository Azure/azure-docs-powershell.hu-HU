---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 3587005559849072d973242eb6af221c0b8b0557
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837039"
---
# <span data-ttu-id="54374-101">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="54374-101">Set-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="54374-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="54374-102">SYNOPSIS</span></span>
<span data-ttu-id="54374-103">Módosítja az alkalmazás-átjárók átírási szabályát.</span><span class="sxs-lookup"><span data-stu-id="54374-103">Modifies a rewrite rule set for an application gateway.</span></span>

## <span data-ttu-id="54374-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="54374-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayRewriteRuleSet -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RewriteRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54374-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="54374-105">DESCRIPTION</span></span>
<span data-ttu-id="54374-106">A **set-AzApplicationGatewayRewriteRuleSet** parancsmag módosítja a kérések útválasztási szabályát.</span><span class="sxs-lookup"><span data-stu-id="54374-106">The **Set-AzApplicationGatewayRewriteRuleSet** cmdlet modifies a request routing rule.</span></span>

## <span data-ttu-id="54374-107">Példák</span><span class="sxs-lookup"><span data-stu-id="54374-107">EXAMPLES</span></span>

### <span data-ttu-id="54374-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="54374-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayRewriteRuleSet -ApplicationGateway $AppGw -Name "ruleset1" -RewriteRule $rule
```

<span data-ttu-id="54374-109">Az első parancs a ApplicationGateway01 nevű alkalmazás-átjárót kapja meg, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="54374-109">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="54374-110">A második parancs a $rule változóban megadott átírási szabályok használatához módosította az alkalmazás átjárójának átírási szabályát.</span><span class="sxs-lookup"><span data-stu-id="54374-110">The second command modifies the rewrite rule set for the application gateway to use rewrite rules specified in the $rule variable.</span></span>

## <span data-ttu-id="54374-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="54374-111">PARAMETERS</span></span>

### <span data-ttu-id="54374-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="54374-112">-ApplicationGateway</span></span>
<span data-ttu-id="54374-113">A applicationGateway</span><span class="sxs-lookup"><span data-stu-id="54374-113">The applicationGateway</span></span>

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

### <span data-ttu-id="54374-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54374-114">-DefaultProfile</span></span>
<span data-ttu-id="54374-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="54374-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54374-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="54374-116">-Name</span></span>
<span data-ttu-id="54374-117">A RewriteRuleSet neve</span><span class="sxs-lookup"><span data-stu-id="54374-117">The name of the RewriteRuleSet</span></span>

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

### <span data-ttu-id="54374-118">-RewriteRule</span><span class="sxs-lookup"><span data-stu-id="54374-118">-RewriteRule</span></span>
<span data-ttu-id="54374-119">Az átírási szabályok listája</span><span class="sxs-lookup"><span data-stu-id="54374-119">List of rewrite rules</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54374-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54374-120">CommonParameters</span></span>
<span data-ttu-id="54374-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="54374-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54374-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54374-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54374-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="54374-123">INPUTS</span></span>

### <span data-ttu-id="54374-124">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="54374-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="54374-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="54374-125">OUTPUTS</span></span>

### <span data-ttu-id="54374-126">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="54374-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="54374-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="54374-127">NOTES</span></span>

## <span data-ttu-id="54374-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="54374-128">RELATED LINKS</span></span>

[<span data-ttu-id="54374-129">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="54374-129">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="54374-130">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="54374-130">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="54374-131">Új – AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="54374-131">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="54374-132">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="54374-132">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="54374-133">Új – AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="54374-133">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="54374-134">Új – AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="54374-134">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="54374-135">Új – AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="54374-135">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
