---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 099abbe1f8c2a536cebff59f1c21b664bb284e8b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938026"
---
# <span data-ttu-id="96a5d-101">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="96a5d-101">Remove-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="96a5d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96a5d-102">SYNOPSIS</span></span>
<span data-ttu-id="96a5d-103">Eltávolít egy újraírási szabálykészletet egy alkalmazás-átjáróból.</span><span class="sxs-lookup"><span data-stu-id="96a5d-103">Removes a rewrite rule set from an application gateway.</span></span>

## <span data-ttu-id="96a5d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="96a5d-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayRewriteRuleSet -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96a5d-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="96a5d-105">DESCRIPTION</span></span>
<span data-ttu-id="96a5d-106">A **Remove-AzApplicationGatewayRewriteRuleSet** parancsmag eltávolít egy újraírási szabálykészletet egy Azure-alkalmazás-átjáróból.</span><span class="sxs-lookup"><span data-stu-id="96a5d-106">The **Remove-AzApplicationGatewayRewriteRuleSet** cmdlet removes a rewrite rule set from an Azure application gateway.</span></span>

## <span data-ttu-id="96a5d-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="96a5d-107">EXAMPLES</span></span>

### <span data-ttu-id="96a5d-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="96a5d-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayRewriteRuleSet -ApplicationGateway $AppGw -Name "RuleSet02"
```

<span data-ttu-id="96a5d-109">Az első parancs egy alkalmazás-átjárót kap, és a $AppGw tárolja.</span><span class="sxs-lookup"><span data-stu-id="96a5d-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="96a5d-110">A második parancs eltávolítja a RuleSet02 nevű átírási szabálykészletet a $AppGw.</span><span class="sxs-lookup"><span data-stu-id="96a5d-110">The second command removes the rewrite rule set named RuleSet02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="96a5d-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="96a5d-111">PARAMETERS</span></span>

### <span data-ttu-id="96a5d-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="96a5d-112">-ApplicationGateway</span></span>
<span data-ttu-id="96a5d-113">Az applicationGateway</span><span class="sxs-lookup"><span data-stu-id="96a5d-113">The applicationGateway</span></span>

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

### <span data-ttu-id="96a5d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96a5d-114">-DefaultProfile</span></span>
<span data-ttu-id="96a5d-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="96a5d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96a5d-116">-Name</span><span class="sxs-lookup"><span data-stu-id="96a5d-116">-Name</span></span>
<span data-ttu-id="96a5d-117">Az alkalmazás-átjáró rewriteRuleSet neve</span><span class="sxs-lookup"><span data-stu-id="96a5d-117">The name of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="96a5d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96a5d-118">CommonParameters</span></span>
<span data-ttu-id="96a5d-119">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96a5d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96a5d-120">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96a5d-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96a5d-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="96a5d-121">INPUTS</span></span>

### <span data-ttu-id="96a5d-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="96a5d-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="96a5d-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="96a5d-123">OUTPUTS</span></span>

### <span data-ttu-id="96a5d-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="96a5d-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="96a5d-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="96a5d-125">NOTES</span></span>

## <span data-ttu-id="96a5d-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="96a5d-126">RELATED LINKS</span></span>

[<span data-ttu-id="96a5d-127">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="96a5d-127">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="96a5d-128">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="96a5d-128">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="96a5d-129">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="96a5d-129">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="96a5d-130">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="96a5d-130">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="96a5d-131">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="96a5d-131">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="96a5d-132">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="96a5d-132">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="96a5d-133">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="96a5d-133">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
