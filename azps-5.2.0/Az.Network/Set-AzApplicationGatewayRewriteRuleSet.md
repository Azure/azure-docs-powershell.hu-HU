---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 45d7fdf6a276e98ce0aca2c2a0db6989e062e42c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372160"
---
# <span data-ttu-id="8eb54-101">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8eb54-101">Set-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="8eb54-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8eb54-102">SYNOPSIS</span></span>
<span data-ttu-id="8eb54-103">Módosítja az alkalmazás-átjárók újraírási szabálykészletét.</span><span class="sxs-lookup"><span data-stu-id="8eb54-103">Modifies a rewrite rule set for an application gateway.</span></span>

## <span data-ttu-id="8eb54-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8eb54-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayRewriteRuleSet -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RewriteRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8eb54-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8eb54-105">DESCRIPTION</span></span>
<span data-ttu-id="8eb54-106">A **Set-AzApplicationGatewayRewriteRuleSet** parancsmag módosítja a kéréstovábbítási szabályt.</span><span class="sxs-lookup"><span data-stu-id="8eb54-106">The **Set-AzApplicationGatewayRewriteRuleSet** cmdlet modifies a request routing rule.</span></span>

## <span data-ttu-id="8eb54-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8eb54-107">EXAMPLES</span></span>

### <span data-ttu-id="8eb54-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="8eb54-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayRewriteRuleSet -ApplicationGateway $AppGw -Name "ruleset1" -RewriteRule $rule
```

<span data-ttu-id="8eb54-109">Az első parancs az ApplicationGateway01 nevű alkalmazás-átjárót kapja meg, és a $AppGw tárolja.</span><span class="sxs-lookup"><span data-stu-id="8eb54-109">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="8eb54-110">A második parancs módosítja az újraírási szabálykészletet ahhoz, hogy az alkalmazás-átjáró a $rule szabályokat használja.</span><span class="sxs-lookup"><span data-stu-id="8eb54-110">The second command modifies the rewrite rule set for the application gateway to use rewrite rules specified in the $rule variable.</span></span>

## <span data-ttu-id="8eb54-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8eb54-111">PARAMETERS</span></span>

### <span data-ttu-id="8eb54-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8eb54-112">-ApplicationGateway</span></span>
<span data-ttu-id="8eb54-113">Az applicationGateway</span><span class="sxs-lookup"><span data-stu-id="8eb54-113">The applicationGateway</span></span>

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

### <span data-ttu-id="8eb54-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8eb54-114">-DefaultProfile</span></span>
<span data-ttu-id="8eb54-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8eb54-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8eb54-116">-Name</span><span class="sxs-lookup"><span data-stu-id="8eb54-116">-Name</span></span>
<span data-ttu-id="8eb54-117">A RewriteRuleSet neve</span><span class="sxs-lookup"><span data-stu-id="8eb54-117">The name of the RewriteRuleSet</span></span>

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

### <span data-ttu-id="8eb54-118">-RewriteRule</span><span class="sxs-lookup"><span data-stu-id="8eb54-118">-RewriteRule</span></span>
<span data-ttu-id="8eb54-119">Az újraírási szabályok listája</span><span class="sxs-lookup"><span data-stu-id="8eb54-119">List of rewrite rules</span></span>

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

### <span data-ttu-id="8eb54-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8eb54-120">CommonParameters</span></span>
<span data-ttu-id="8eb54-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8eb54-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8eb54-122">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8eb54-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8eb54-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8eb54-123">INPUTS</span></span>

### <span data-ttu-id="8eb54-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8eb54-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8eb54-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8eb54-125">OUTPUTS</span></span>

### <span data-ttu-id="8eb54-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8eb54-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8eb54-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8eb54-127">NOTES</span></span>

## <span data-ttu-id="8eb54-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8eb54-128">RELATED LINKS</span></span>

[<span data-ttu-id="8eb54-129">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8eb54-129">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="8eb54-130">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8eb54-130">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="8eb54-131">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8eb54-131">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="8eb54-132">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8eb54-132">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="8eb54-133">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="8eb54-133">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="8eb54-134">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="8eb54-134">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="8eb54-135">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="8eb54-135">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
