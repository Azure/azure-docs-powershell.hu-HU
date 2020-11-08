---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: dc3019154d4041396d46f3c9f6dbdbdd3deb22a7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195694"
---
# <span data-ttu-id="b81a7-101">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b81a7-101">Get-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="b81a7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b81a7-102">SYNOPSIS</span></span>
<span data-ttu-id="b81a7-103">Beolvassa az alkalmazás-átjáró átírási szabályát.</span><span class="sxs-lookup"><span data-stu-id="b81a7-103">Gets the rewrite rule set of an application gateway.</span></span>

## <span data-ttu-id="b81a7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b81a7-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayRewriteRuleSet [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b81a7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b81a7-105">DESCRIPTION</span></span>
<span data-ttu-id="b81a7-106">Beolvassa az alkalmazás-átjáró átírási szabályát.</span><span class="sxs-lookup"><span data-stu-id="b81a7-106">Gets the rewrite rule set of an application gateway.</span></span>

## <span data-ttu-id="b81a7-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b81a7-107">EXAMPLES</span></span>

### <span data-ttu-id="b81a7-108">Példa 1: speciális átírási szabály beállítása</span><span class="sxs-lookup"><span data-stu-id="b81a7-108">Example 1 : Get a specific rewrite rule set</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rule = Get-AzApplicationGatewayRewriteRuleSet -Name "RuleSet01" -ApplicationGateway $AppGW
```

<span data-ttu-id="b81a7-109">Az első parancs beolvassa a ApplicationGateway01 nevű alkalmazás-átjárót, és az eredményt az $AppGW nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="b81a7-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="b81a7-110">A második parancs a $AppGW nevű változóban tárolt RuleSet01-os átírási szabályt kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b81a7-110">The second command gets the rewrite rule set named RuleSet01 from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="b81a7-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b81a7-111">PARAMETERS</span></span>

### <span data-ttu-id="b81a7-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b81a7-112">-ApplicationGateway</span></span>
<span data-ttu-id="b81a7-113">A applicationGateway</span><span class="sxs-lookup"><span data-stu-id="b81a7-113">The applicationGateway</span></span>

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

### <span data-ttu-id="b81a7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b81a7-114">-DefaultProfile</span></span>
<span data-ttu-id="b81a7-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b81a7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b81a7-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b81a7-116">-Name</span></span>
<span data-ttu-id="b81a7-117">Az alkalmazás-átjáró RewriteRuleSet neve</span><span class="sxs-lookup"><span data-stu-id="b81a7-117">The name of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="b81a7-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b81a7-118">CommonParameters</span></span>
<span data-ttu-id="b81a7-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b81a7-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b81a7-120">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b81a7-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b81a7-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b81a7-121">INPUTS</span></span>

### <span data-ttu-id="b81a7-122">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b81a7-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b81a7-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b81a7-123">OUTPUTS</span></span>

### <span data-ttu-id="b81a7-124">Microsoft. Azure. commands. Network. models. PSApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b81a7-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="b81a7-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b81a7-125">NOTES</span></span>

## <span data-ttu-id="b81a7-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b81a7-126">RELATED LINKS</span></span>

[<span data-ttu-id="b81a7-127">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b81a7-127">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="b81a7-128">Új – AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b81a7-128">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="b81a7-129">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b81a7-129">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="b81a7-130">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b81a7-130">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="b81a7-131">Új – AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="b81a7-131">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="b81a7-132">Új – AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="b81a7-132">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="b81a7-133">Új – AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="b81a7-133">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)