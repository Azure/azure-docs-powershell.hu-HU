---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 01f1dc89257088c053cdd6003384c31c708d6b04
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341646"
---
# <span data-ttu-id="47ee5-101">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="47ee5-101">Remove-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="47ee5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47ee5-102">SYNOPSIS</span></span>
<span data-ttu-id="47ee5-103">Eltávolít egy újraírási szabálykészletet egy alkalmazás-átjáróból.</span><span class="sxs-lookup"><span data-stu-id="47ee5-103">Removes a rewrite rule set from an application gateway.</span></span>

## <span data-ttu-id="47ee5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="47ee5-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayRewriteRuleSet -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47ee5-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="47ee5-105">DESCRIPTION</span></span>
<span data-ttu-id="47ee5-106">A **Remove-AzApplicationGatewayRewriteRuleSet** parancsmag eltávolít egy újraírási szabálykészletet egy Azure-alkalmazás-átjáróból.</span><span class="sxs-lookup"><span data-stu-id="47ee5-106">The **Remove-AzApplicationGatewayRewriteRuleSet** cmdlet removes a rewrite rule set from an Azure application gateway.</span></span>

## <span data-ttu-id="47ee5-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="47ee5-107">EXAMPLES</span></span>

### <span data-ttu-id="47ee5-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="47ee5-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayRewriteRuleSet -ApplicationGateway $AppGw -Name "RuleSet02"
```

<span data-ttu-id="47ee5-109">Az első parancs egy alkalmazás-átjárót kap, és a $AppGw tárolja.</span><span class="sxs-lookup"><span data-stu-id="47ee5-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="47ee5-110">A második parancs eltávolítja a RuleSet02 nevű átírási szabálykészletet a $AppGw.</span><span class="sxs-lookup"><span data-stu-id="47ee5-110">The second command removes the rewrite rule set named RuleSet02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="47ee5-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="47ee5-111">PARAMETERS</span></span>

### <span data-ttu-id="47ee5-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="47ee5-112">-ApplicationGateway</span></span>
<span data-ttu-id="47ee5-113">Az applicationGateway</span><span class="sxs-lookup"><span data-stu-id="47ee5-113">The applicationGateway</span></span>

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

### <span data-ttu-id="47ee5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47ee5-114">-DefaultProfile</span></span>
<span data-ttu-id="47ee5-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="47ee5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47ee5-116">-Name</span><span class="sxs-lookup"><span data-stu-id="47ee5-116">-Name</span></span>
<span data-ttu-id="47ee5-117">Az alkalmazás-átjáró rewriteRuleSet neve</span><span class="sxs-lookup"><span data-stu-id="47ee5-117">The name of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="47ee5-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47ee5-118">CommonParameters</span></span>
<span data-ttu-id="47ee5-119">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47ee5-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47ee5-120">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47ee5-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47ee5-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="47ee5-121">INPUTS</span></span>

### <span data-ttu-id="47ee5-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="47ee5-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="47ee5-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="47ee5-123">OUTPUTS</span></span>

### <span data-ttu-id="47ee5-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="47ee5-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="47ee5-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="47ee5-125">NOTES</span></span>

## <span data-ttu-id="47ee5-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="47ee5-126">RELATED LINKS</span></span>

[<span data-ttu-id="47ee5-127">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="47ee5-127">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="47ee5-128">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="47ee5-128">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="47ee5-129">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="47ee5-129">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="47ee5-130">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="47ee5-130">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="47ee5-131">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="47ee5-131">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="47ee5-132">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="47ee5-132">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="47ee5-133">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="47ee5-133">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
