---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 1ed5c90d4c53769d53cd645b2e5bced7bdec4ce8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670383"
---
# <span data-ttu-id="2598d-101">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2598d-101">New-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="2598d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2598d-102">SYNOPSIS</span></span>
<span data-ttu-id="2598d-103">Kérés-útválasztási szabályt hoz létre egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="2598d-103">Creates a request routing rule for an application gateway.</span></span>

## <span data-ttu-id="2598d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2598d-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleSet -Name <String>
 -RewriteRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2598d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2598d-105">DESCRIPTION</span></span>
<span data-ttu-id="2598d-106">**A New-AzApplicationGatewayRewriteRuleSet** parancsmag átírási szabályt hoz létre egy Azure Application Gateway-nek.</span><span class="sxs-lookup"><span data-stu-id="2598d-106">**The New-AzApplicationGatewayRewriteRuleSet** cmdlet creates a rewrite rule set for an Azure application gateway.</span></span>

## <span data-ttu-id="2598d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2598d-107">EXAMPLES</span></span>

### <span data-ttu-id="2598d-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="2598d-108">Example 1</span></span>
```powershell
PS C:\> $ruleset = New-AzApplicationGatewayRewriteRuleSet -Name ruleset1 -RewriteRule $rule
```

<span data-ttu-id="2598d-109">A parancs létrehoz egy ruleset1 nevű szabályt, és az eredményt az $ruleset nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="2598d-109">This command creates a rewrite rule set named ruleset1 and stores the result in the variable named $ruleset.</span></span>

## <span data-ttu-id="2598d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2598d-110">PARAMETERS</span></span>

### <span data-ttu-id="2598d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2598d-111">-DefaultProfile</span></span>
<span data-ttu-id="2598d-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2598d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2598d-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2598d-113">-Name</span></span>
<span data-ttu-id="2598d-114">A RewriteRuleSet neve</span><span class="sxs-lookup"><span data-stu-id="2598d-114">The name of the RewriteRuleSet</span></span>

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

### <span data-ttu-id="2598d-115">-RewriteRule</span><span class="sxs-lookup"><span data-stu-id="2598d-115">-RewriteRule</span></span>
<span data-ttu-id="2598d-116">Az átírási szabályok listája</span><span class="sxs-lookup"><span data-stu-id="2598d-116">List of rewrite rules</span></span>

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

### <span data-ttu-id="2598d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2598d-117">CommonParameters</span></span>
<span data-ttu-id="2598d-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2598d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2598d-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2598d-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2598d-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2598d-120">INPUTS</span></span>

### <span data-ttu-id="2598d-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="2598d-121">None</span></span>

## <span data-ttu-id="2598d-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2598d-122">OUTPUTS</span></span>

### <span data-ttu-id="2598d-123">Microsoft. Azure. commands. Network. models. PSApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2598d-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="2598d-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2598d-124">NOTES</span></span>

## <span data-ttu-id="2598d-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2598d-125">RELATED LINKS</span></span>

[<span data-ttu-id="2598d-126">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2598d-126">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="2598d-127">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2598d-127">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="2598d-128">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2598d-128">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="2598d-129">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2598d-129">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="2598d-130">Új – AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="2598d-130">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="2598d-131">Új – AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="2598d-131">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="2598d-132">Új – AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="2598d-132">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
