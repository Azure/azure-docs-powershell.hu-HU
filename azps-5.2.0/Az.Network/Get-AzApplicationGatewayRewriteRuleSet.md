---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: dc3019154d4041396d46f3c9f6dbdbdd3deb22a7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98322794"
---
# <span data-ttu-id="6b35e-101">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6b35e-101">Get-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="6b35e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b35e-102">SYNOPSIS</span></span>
<span data-ttu-id="6b35e-103">Egy alkalmazás-átjáró újraírási szabálykészletét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="6b35e-103">Gets the rewrite rule set of an application gateway.</span></span>

## <span data-ttu-id="6b35e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6b35e-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayRewriteRuleSet [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b35e-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6b35e-105">DESCRIPTION</span></span>
<span data-ttu-id="6b35e-106">Egy alkalmazás-átjáró újraírási szabálykészletét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="6b35e-106">Gets the rewrite rule set of an application gateway.</span></span>

## <span data-ttu-id="6b35e-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6b35e-107">EXAMPLES</span></span>

### <span data-ttu-id="6b35e-108">1. példa: Adott átírási szabálykészlet lekérte</span><span class="sxs-lookup"><span data-stu-id="6b35e-108">Example 1 : Get a specific rewrite rule set</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rule = Get-AzApplicationGatewayRewriteRuleSet -Name "RuleSet01" -ApplicationGateway $AppGW
```

<span data-ttu-id="6b35e-109">Az első parancs az ApplicationGateway01 nevű Alkalmazás-átjárót kapja meg, és az eredményt a következő nevű változóban $AppGW.</span><span class="sxs-lookup"><span data-stu-id="6b35e-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="6b35e-110">A második parancs a RuleSet01 nevű újraírási szabálykészletet az $AppGW nevű változóban tárolt alkalmazás-átjáróból $AppGW.</span><span class="sxs-lookup"><span data-stu-id="6b35e-110">The second command gets the rewrite rule set named RuleSet01 from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="6b35e-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6b35e-111">PARAMETERS</span></span>

### <span data-ttu-id="6b35e-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6b35e-112">-ApplicationGateway</span></span>
<span data-ttu-id="6b35e-113">Az applicationGateway</span><span class="sxs-lookup"><span data-stu-id="6b35e-113">The applicationGateway</span></span>

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

### <span data-ttu-id="6b35e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b35e-114">-DefaultProfile</span></span>
<span data-ttu-id="6b35e-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6b35e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b35e-116">-Name</span><span class="sxs-lookup"><span data-stu-id="6b35e-116">-Name</span></span>
<span data-ttu-id="6b35e-117">Az alkalmazás-átjáró rewriteRuleSet neve</span><span class="sxs-lookup"><span data-stu-id="6b35e-117">The name of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="6b35e-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b35e-118">CommonParameters</span></span>
<span data-ttu-id="6b35e-119">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b35e-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b35e-120">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6b35e-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b35e-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6b35e-121">INPUTS</span></span>

### <span data-ttu-id="6b35e-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6b35e-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6b35e-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6b35e-123">OUTPUTS</span></span>

### <span data-ttu-id="6b35e-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6b35e-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="6b35e-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6b35e-125">NOTES</span></span>

## <span data-ttu-id="6b35e-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6b35e-126">RELATED LINKS</span></span>

[<span data-ttu-id="6b35e-127">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6b35e-127">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="6b35e-128">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6b35e-128">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="6b35e-129">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6b35e-129">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="6b35e-130">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6b35e-130">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="6b35e-131">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="6b35e-131">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="6b35e-132">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="6b35e-132">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="6b35e-133">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="6b35e-133">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
