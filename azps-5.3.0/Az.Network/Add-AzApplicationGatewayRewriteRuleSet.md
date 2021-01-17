---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 6e45f0bc0eaab8316d0534e1f73a1543175e1144
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469321"
---
# <span data-ttu-id="67d7a-101">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="67d7a-101">Add-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="67d7a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67d7a-102">SYNOPSIS</span></span>
<span data-ttu-id="67d7a-103">Újraírási szabálykészletet ad hozzá egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="67d7a-103">Adds a rewrite rule set to an application gateway.</span></span>

## <span data-ttu-id="67d7a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="67d7a-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayRewriteRuleSet -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RewriteRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67d7a-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="67d7a-105">DESCRIPTION</span></span>
<span data-ttu-id="67d7a-106">Az **Add-AzApplicationGatewayRewriteRuleSet** parancsmag hozzáad egy újraírási szabálykészletet egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="67d7a-106">The **Add-AzApplicationGatewayRewriteRuleSet** cmdlet adds a rewrite rule set to an application gateway.</span></span>

## <span data-ttu-id="67d7a-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="67d7a-107">EXAMPLES</span></span>

### <span data-ttu-id="67d7a-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="67d7a-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayRewriteRuleSet -ApplicationGateway $AppGw -Name "ruleset1" -RewriteRule $rule
```

<span data-ttu-id="67d7a-109">Az első parancs az alkalmazás átjáróját a $AppGw tárolja.</span><span class="sxs-lookup"><span data-stu-id="67d7a-109">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="67d7a-110">A második parancs hozzáadja az újraírási szabálykészletet az alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="67d7a-110">The second command adds the rewrite rule set to the application gateway.</span></span>

## <span data-ttu-id="67d7a-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="67d7a-111">PARAMETERS</span></span>

### <span data-ttu-id="67d7a-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="67d7a-112">-ApplicationGateway</span></span>
<span data-ttu-id="67d7a-113">Az applicationGateway</span><span class="sxs-lookup"><span data-stu-id="67d7a-113">The applicationGateway</span></span>

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

### <span data-ttu-id="67d7a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67d7a-114">-DefaultProfile</span></span>
<span data-ttu-id="67d7a-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="67d7a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67d7a-116">-Name</span><span class="sxs-lookup"><span data-stu-id="67d7a-116">-Name</span></span>
<span data-ttu-id="67d7a-117">A RewriteRuleSet neve</span><span class="sxs-lookup"><span data-stu-id="67d7a-117">The name of the RewriteRuleSet</span></span>

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

### <span data-ttu-id="67d7a-118">-RewriteRule</span><span class="sxs-lookup"><span data-stu-id="67d7a-118">-RewriteRule</span></span>
<span data-ttu-id="67d7a-119">Az újraírási szabályok listája</span><span class="sxs-lookup"><span data-stu-id="67d7a-119">List of rewrite rules</span></span>

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

### <span data-ttu-id="67d7a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67d7a-120">CommonParameters</span></span>
<span data-ttu-id="67d7a-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67d7a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67d7a-122">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67d7a-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67d7a-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="67d7a-123">INPUTS</span></span>

### <span data-ttu-id="67d7a-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="67d7a-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="67d7a-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="67d7a-125">OUTPUTS</span></span>

### <span data-ttu-id="67d7a-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="67d7a-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="67d7a-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="67d7a-127">NOTES</span></span>

## <span data-ttu-id="67d7a-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="67d7a-128">RELATED LINKS</span></span>

[<span data-ttu-id="67d7a-129">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="67d7a-129">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="67d7a-130">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="67d7a-130">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="67d7a-131">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="67d7a-131">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="67d7a-132">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="67d7a-132">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="67d7a-133">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="67d7a-133">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="67d7a-134">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="67d7a-134">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="67d7a-135">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="67d7a-135">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
