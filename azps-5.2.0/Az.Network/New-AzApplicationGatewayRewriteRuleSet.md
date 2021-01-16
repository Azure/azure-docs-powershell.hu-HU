---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: b2fc00bf62b1ed147e1c7c32aa30731222a28bea
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358859"
---
# <span data-ttu-id="e9d26-101">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e9d26-101">New-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="e9d26-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9d26-102">SYNOPSIS</span></span>
<span data-ttu-id="e9d26-103">Kéréstovábbító szabályt hoz létre egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="e9d26-103">Creates a request routing rule for an application gateway.</span></span>

## <span data-ttu-id="e9d26-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e9d26-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleSet -Name <String>
 -RewriteRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e9d26-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e9d26-105">DESCRIPTION</span></span>
<span data-ttu-id="e9d26-106">**A New-AzApplicationGatewayRewriteRuleSet** parancsmag létrehoz egy újraírási szabálykészletet egy Azure-alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="e9d26-106">**The New-AzApplicationGatewayRewriteRuleSet** cmdlet creates a rewrite rule set for an Azure application gateway.</span></span>

## <span data-ttu-id="e9d26-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e9d26-107">EXAMPLES</span></span>

### <span data-ttu-id="e9d26-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="e9d26-108">Example 1</span></span>
```powershell
PS C:\> $ruleset = New-AzApplicationGatewayRewriteRuleSet -Name ruleset1 -RewriteRule $rule
```

<span data-ttu-id="e9d26-109">Ez a parancs létrehoz egy ruleset1 nevű újraírási szabálykészletet, és az eredményt a következő nevű változóban $ruleset.</span><span class="sxs-lookup"><span data-stu-id="e9d26-109">This command creates a rewrite rule set named ruleset1 and stores the result in the variable named $ruleset.</span></span>

## <span data-ttu-id="e9d26-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e9d26-110">PARAMETERS</span></span>

### <span data-ttu-id="e9d26-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9d26-111">-DefaultProfile</span></span>
<span data-ttu-id="e9d26-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e9d26-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9d26-113">-Name</span><span class="sxs-lookup"><span data-stu-id="e9d26-113">-Name</span></span>
<span data-ttu-id="e9d26-114">A RewriteRuleSet neve</span><span class="sxs-lookup"><span data-stu-id="e9d26-114">The name of the RewriteRuleSet</span></span>

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

### <span data-ttu-id="e9d26-115">-RewriteRule</span><span class="sxs-lookup"><span data-stu-id="e9d26-115">-RewriteRule</span></span>
<span data-ttu-id="e9d26-116">Az újraírási szabályok listája</span><span class="sxs-lookup"><span data-stu-id="e9d26-116">List of rewrite rules</span></span>

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

### <span data-ttu-id="e9d26-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9d26-117">CommonParameters</span></span>
<span data-ttu-id="e9d26-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9d26-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9d26-119">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9d26-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9d26-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e9d26-120">INPUTS</span></span>

### <span data-ttu-id="e9d26-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="e9d26-121">None</span></span>

## <span data-ttu-id="e9d26-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e9d26-122">OUTPUTS</span></span>

### <span data-ttu-id="e9d26-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e9d26-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="e9d26-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e9d26-124">NOTES</span></span>

## <span data-ttu-id="e9d26-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e9d26-125">RELATED LINKS</span></span>

[<span data-ttu-id="e9d26-126">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e9d26-126">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="e9d26-127">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e9d26-127">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="e9d26-128">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e9d26-128">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="e9d26-129">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e9d26-129">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="e9d26-130">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="e9d26-130">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="e9d26-131">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="e9d26-131">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="e9d26-132">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="e9d26-132">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
