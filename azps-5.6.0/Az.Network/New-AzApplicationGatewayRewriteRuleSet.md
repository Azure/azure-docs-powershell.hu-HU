---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 8bd540c30551451bd729126c35c4d778c700591f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001125"
---
# <span data-ttu-id="328a4-101">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="328a4-101">New-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="328a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="328a4-102">SYNOPSIS</span></span>
<span data-ttu-id="328a4-103">Kéréstovábbító szabályt hoz létre egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="328a4-103">Creates a request routing rule for an application gateway.</span></span>

## <span data-ttu-id="328a4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="328a4-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleSet -Name <String>
 -RewriteRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="328a4-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="328a4-105">DESCRIPTION</span></span>
<span data-ttu-id="328a4-106">**A New-AzApplicationGatewayRewriteRuleSet** parancsmag létrehoz egy újraírási szabálykészletet egy Azure-alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="328a4-106">**The New-AzApplicationGatewayRewriteRuleSet** cmdlet creates a rewrite rule set for an Azure application gateway.</span></span>

## <span data-ttu-id="328a4-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="328a4-107">EXAMPLES</span></span>

### <span data-ttu-id="328a4-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="328a4-108">Example 1</span></span>
```powershell
PS C:\> $ruleset = New-AzApplicationGatewayRewriteRuleSet -Name ruleset1 -RewriteRule $rule
```

<span data-ttu-id="328a4-109">Ez a parancs létrehoz egy ruleset1 nevű újraírási szabálykészletet, és az eredményt a következő nevű változóban $ruleset.</span><span class="sxs-lookup"><span data-stu-id="328a4-109">This command creates a rewrite rule set named ruleset1 and stores the result in the variable named $ruleset.</span></span>

## <span data-ttu-id="328a4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="328a4-110">PARAMETERS</span></span>

### <span data-ttu-id="328a4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="328a4-111">-DefaultProfile</span></span>
<span data-ttu-id="328a4-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="328a4-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="328a4-113">-Name</span><span class="sxs-lookup"><span data-stu-id="328a4-113">-Name</span></span>
<span data-ttu-id="328a4-114">A RewriteRuleSet neve</span><span class="sxs-lookup"><span data-stu-id="328a4-114">The name of the RewriteRuleSet</span></span>

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

### <span data-ttu-id="328a4-115">-RewriteRule</span><span class="sxs-lookup"><span data-stu-id="328a4-115">-RewriteRule</span></span>
<span data-ttu-id="328a4-116">Az újraírási szabályok listája</span><span class="sxs-lookup"><span data-stu-id="328a4-116">List of rewrite rules</span></span>

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

### <span data-ttu-id="328a4-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="328a4-117">CommonParameters</span></span>
<span data-ttu-id="328a4-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="328a4-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="328a4-119">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="328a4-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="328a4-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="328a4-120">INPUTS</span></span>

### <span data-ttu-id="328a4-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="328a4-121">None</span></span>

## <span data-ttu-id="328a4-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="328a4-122">OUTPUTS</span></span>

### <span data-ttu-id="328a4-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="328a4-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="328a4-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="328a4-124">NOTES</span></span>

## <span data-ttu-id="328a4-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="328a4-125">RELATED LINKS</span></span>

[<span data-ttu-id="328a4-126">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="328a4-126">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="328a4-127">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="328a4-127">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="328a4-128">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="328a4-128">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="328a4-129">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="328a4-129">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="328a4-130">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="328a4-130">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="328a4-131">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="328a4-131">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="328a4-132">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="328a4-132">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
