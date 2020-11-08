---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: b2fc00bf62b1ed147e1c7c32aa30731222a28bea
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014774"
---
# <span data-ttu-id="e3b51-101">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e3b51-101">New-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="e3b51-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e3b51-102">SYNOPSIS</span></span>
<span data-ttu-id="e3b51-103">Kérés-útválasztási szabályt hoz létre egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="e3b51-103">Creates a request routing rule for an application gateway.</span></span>

## <span data-ttu-id="e3b51-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e3b51-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleSet -Name <String>
 -RewriteRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3b51-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e3b51-105">DESCRIPTION</span></span>
<span data-ttu-id="e3b51-106">**A New-AzApplicationGatewayRewriteRuleSet** parancsmag átírási szabályt hoz létre egy Azure Application Gateway-nek.</span><span class="sxs-lookup"><span data-stu-id="e3b51-106">**The New-AzApplicationGatewayRewriteRuleSet** cmdlet creates a rewrite rule set for an Azure application gateway.</span></span>

## <span data-ttu-id="e3b51-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e3b51-107">EXAMPLES</span></span>

### <span data-ttu-id="e3b51-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e3b51-108">Example 1</span></span>
```powershell
PS C:\> $ruleset = New-AzApplicationGatewayRewriteRuleSet -Name ruleset1 -RewriteRule $rule
```

<span data-ttu-id="e3b51-109">A parancs létrehoz egy ruleset1 nevű szabályt, és az eredményt az $ruleset nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="e3b51-109">This command creates a rewrite rule set named ruleset1 and stores the result in the variable named $ruleset.</span></span>

## <span data-ttu-id="e3b51-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e3b51-110">PARAMETERS</span></span>

### <span data-ttu-id="e3b51-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3b51-111">-DefaultProfile</span></span>
<span data-ttu-id="e3b51-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e3b51-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3b51-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e3b51-113">-Name</span></span>
<span data-ttu-id="e3b51-114">A RewriteRuleSet neve</span><span class="sxs-lookup"><span data-stu-id="e3b51-114">The name of the RewriteRuleSet</span></span>

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

### <span data-ttu-id="e3b51-115">-RewriteRule</span><span class="sxs-lookup"><span data-stu-id="e3b51-115">-RewriteRule</span></span>
<span data-ttu-id="e3b51-116">Az átírási szabályok listája</span><span class="sxs-lookup"><span data-stu-id="e3b51-116">List of rewrite rules</span></span>

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

### <span data-ttu-id="e3b51-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3b51-117">CommonParameters</span></span>
<span data-ttu-id="e3b51-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e3b51-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3b51-119">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3b51-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3b51-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e3b51-120">INPUTS</span></span>

### <span data-ttu-id="e3b51-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="e3b51-121">None</span></span>

## <span data-ttu-id="e3b51-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e3b51-122">OUTPUTS</span></span>

### <span data-ttu-id="e3b51-123">Microsoft. Azure. commands. Network. models. PSApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e3b51-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="e3b51-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e3b51-124">NOTES</span></span>

## <span data-ttu-id="e3b51-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e3b51-125">RELATED LINKS</span></span>

[<span data-ttu-id="e3b51-126">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e3b51-126">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="e3b51-127">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e3b51-127">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="e3b51-128">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e3b51-128">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="e3b51-129">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e3b51-129">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="e3b51-130">Új – AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="e3b51-130">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="e3b51-131">Új – AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="e3b51-131">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="e3b51-132">Új – AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="e3b51-132">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
