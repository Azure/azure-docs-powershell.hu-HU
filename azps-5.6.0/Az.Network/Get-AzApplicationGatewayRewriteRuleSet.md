---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 935e2df3de68d9ab8444cd1037d5c48951d6a335
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940345"
---
# <span data-ttu-id="13392-101">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="13392-101">Get-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="13392-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13392-102">SYNOPSIS</span></span>
<span data-ttu-id="13392-103">Egy alkalmazás-átjáró újraírási szabálykészletét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="13392-103">Gets the rewrite rule set of an application gateway.</span></span>

## <span data-ttu-id="13392-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="13392-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayRewriteRuleSet [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13392-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="13392-105">DESCRIPTION</span></span>
<span data-ttu-id="13392-106">Egy alkalmazás-átjáró újraírási szabálykészletét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="13392-106">Gets the rewrite rule set of an application gateway.</span></span>

## <span data-ttu-id="13392-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="13392-107">EXAMPLES</span></span>

### <span data-ttu-id="13392-108">1. példa: Adott átírási szabálykészlet lekérte</span><span class="sxs-lookup"><span data-stu-id="13392-108">Example 1 : Get a specific rewrite rule set</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rule = Get-AzApplicationGatewayRewriteRuleSet -Name "RuleSet01" -ApplicationGateway $AppGW
```

<span data-ttu-id="13392-109">Az első parancs az ApplicationGateway01 nevű Alkalmazás-átjárót kapja meg, és az eredményt a következő nevű változóban $AppGW.</span><span class="sxs-lookup"><span data-stu-id="13392-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="13392-110">A második parancs a RuleSet01 nevű újraírási szabálykészletet az $AppGW nevű változóban tárolt alkalmazás-átjáróból $AppGW.</span><span class="sxs-lookup"><span data-stu-id="13392-110">The second command gets the rewrite rule set named RuleSet01 from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="13392-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="13392-111">PARAMETERS</span></span>

### <span data-ttu-id="13392-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="13392-112">-ApplicationGateway</span></span>
<span data-ttu-id="13392-113">Az applicationGateway</span><span class="sxs-lookup"><span data-stu-id="13392-113">The applicationGateway</span></span>

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

### <span data-ttu-id="13392-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13392-114">-DefaultProfile</span></span>
<span data-ttu-id="13392-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="13392-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13392-116">-Name</span><span class="sxs-lookup"><span data-stu-id="13392-116">-Name</span></span>
<span data-ttu-id="13392-117">Az alkalmazás-átjáró rewriteRuleSet neve</span><span class="sxs-lookup"><span data-stu-id="13392-117">The name of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="13392-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13392-118">CommonParameters</span></span>
<span data-ttu-id="13392-119">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13392-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13392-120">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="13392-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13392-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="13392-121">INPUTS</span></span>

### <span data-ttu-id="13392-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="13392-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="13392-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="13392-123">OUTPUTS</span></span>

### <span data-ttu-id="13392-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="13392-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="13392-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="13392-125">NOTES</span></span>

## <span data-ttu-id="13392-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="13392-126">RELATED LINKS</span></span>

[<span data-ttu-id="13392-127">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="13392-127">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="13392-128">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="13392-128">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="13392-129">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="13392-129">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="13392-130">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="13392-130">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="13392-131">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="13392-131">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="13392-132">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="13392-132">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="13392-133">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="13392-133">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
