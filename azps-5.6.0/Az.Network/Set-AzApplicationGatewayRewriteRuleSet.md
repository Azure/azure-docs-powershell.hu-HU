---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 934c69071e90ebb1a38bf4e1fda5e631364ab87b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003462"
---
# <span data-ttu-id="2b317-101">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2b317-101">Set-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="2b317-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b317-102">SYNOPSIS</span></span>
<span data-ttu-id="2b317-103">Módosítja az alkalmazás-átjárók újraírási szabálykészletét.</span><span class="sxs-lookup"><span data-stu-id="2b317-103">Modifies a rewrite rule set for an application gateway.</span></span>

## <span data-ttu-id="2b317-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2b317-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayRewriteRuleSet -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RewriteRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b317-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2b317-105">DESCRIPTION</span></span>
<span data-ttu-id="2b317-106">A **Set-AzApplicationGatewayRewriteRuleSet** parancsmag módosítja a kéréstovábbítási szabályt.</span><span class="sxs-lookup"><span data-stu-id="2b317-106">The **Set-AzApplicationGatewayRewriteRuleSet** cmdlet modifies a request routing rule.</span></span>

## <span data-ttu-id="2b317-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2b317-107">EXAMPLES</span></span>

### <span data-ttu-id="2b317-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="2b317-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayRewriteRuleSet -ApplicationGateway $AppGw -Name "ruleset1" -RewriteRule $rule
```

<span data-ttu-id="2b317-109">Az első parancs az ApplicationGateway01 nevű alkalmazás-átjárót kapja meg, és a $AppGw tárolja.</span><span class="sxs-lookup"><span data-stu-id="2b317-109">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="2b317-110">A második parancs módosítja az újraírási szabálykészletet ahhoz, hogy az alkalmazás-átjáró a módosított változóban megadott újraírási szabályokat $rule használva.</span><span class="sxs-lookup"><span data-stu-id="2b317-110">The second command modifies the rewrite rule set for the application gateway to use rewrite rules specified in the $rule variable.</span></span>

## <span data-ttu-id="2b317-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2b317-111">PARAMETERS</span></span>

### <span data-ttu-id="2b317-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2b317-112">-ApplicationGateway</span></span>
<span data-ttu-id="2b317-113">Az applicationGateway</span><span class="sxs-lookup"><span data-stu-id="2b317-113">The applicationGateway</span></span>

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

### <span data-ttu-id="2b317-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b317-114">-DefaultProfile</span></span>
<span data-ttu-id="2b317-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2b317-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b317-116">-Name</span><span class="sxs-lookup"><span data-stu-id="2b317-116">-Name</span></span>
<span data-ttu-id="2b317-117">A RewriteRuleSet neve</span><span class="sxs-lookup"><span data-stu-id="2b317-117">The name of the RewriteRuleSet</span></span>

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

### <span data-ttu-id="2b317-118">-RewriteRule</span><span class="sxs-lookup"><span data-stu-id="2b317-118">-RewriteRule</span></span>
<span data-ttu-id="2b317-119">Az újraírási szabályok listája</span><span class="sxs-lookup"><span data-stu-id="2b317-119">List of rewrite rules</span></span>

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

### <span data-ttu-id="2b317-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b317-120">CommonParameters</span></span>
<span data-ttu-id="2b317-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b317-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b317-122">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b317-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b317-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2b317-123">INPUTS</span></span>

### <span data-ttu-id="2b317-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2b317-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2b317-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2b317-125">OUTPUTS</span></span>

### <span data-ttu-id="2b317-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2b317-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2b317-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2b317-127">NOTES</span></span>

## <span data-ttu-id="2b317-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2b317-128">RELATED LINKS</span></span>

[<span data-ttu-id="2b317-129">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2b317-129">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="2b317-130">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2b317-130">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="2b317-131">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2b317-131">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="2b317-132">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2b317-132">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="2b317-133">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="2b317-133">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="2b317-134">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="2b317-134">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="2b317-135">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="2b317-135">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
