---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayrewriteruleactionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleActionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleActionSet.md
ms.openlocfilehash: 2c5fa5f4c12a44d1efc12e75dfa3901dce061f8e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008773"
---
# <span data-ttu-id="bba55-101">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="bba55-101">New-AzApplicationGatewayRewriteRuleActionSet</span></span>

## <span data-ttu-id="bba55-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bba55-102">SYNOPSIS</span></span>
<span data-ttu-id="bba55-103">Újraírási szabály műveletkészletet hoz létre egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="bba55-103">Creates a rewrite rule action set for an application gateway.</span></span>

## <span data-ttu-id="bba55-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="bba55-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleActionSet
 [-RequestHeaderConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]>]
 [-ResponseHeaderConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]>]
 [-UrlConfiguration [Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlConfiguration]]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bba55-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="bba55-105">DESCRIPTION</span></span>
<span data-ttu-id="bba55-106">**A New-AzApplicationGatewayRewriteRuleActionSet** parancsmag létrehoz egy újraírási szabály műveletkészletet egy Azure-alkalmazás átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="bba55-106">**The New-AzApplicationGatewayRewriteRuleActionSet** cmdlet creates a rewrite rule action set for an Azure application gateway.</span></span>

## <span data-ttu-id="bba55-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="bba55-107">EXAMPLES</span></span>

### <span data-ttu-id="bba55-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="bba55-108">Example 1</span></span>
```powershell
PS C:\> $action = New-AzApplicationGatewayRewriteRuleActionSet -ResponseHeaderConfiguration $hc -UrlConfiguration $urlConfiguration
```

<span data-ttu-id="bba55-109">Ez a parancs egy újraírási szabály-műveletkészletet hoz létre, és az eredményt a következő nevű változóban $action.</span><span class="sxs-lookup"><span data-stu-id="bba55-109">This command creates a rewrite rule action set and stores the result in the variable named $action.</span></span>

## <span data-ttu-id="bba55-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bba55-110">PARAMETERS</span></span>

### <span data-ttu-id="bba55-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bba55-111">-DefaultProfile</span></span>
<span data-ttu-id="bba55-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bba55-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bba55-113">-RequestHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="bba55-113">-RequestHeaderConfiguration</span></span>
<span data-ttu-id="bba55-114">Kérésfejléc-konfigurációk listája</span><span class="sxs-lookup"><span data-stu-id="bba55-114">List of request header configurations</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bba55-115">-ResponseHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="bba55-115">-ResponseHeaderConfiguration</span></span>
<span data-ttu-id="bba55-116">Válaszfejléc-konfigurációk listája</span><span class="sxs-lookup"><span data-stu-id="bba55-116">List of response header configurations</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bba55-117">-UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="bba55-117">-UrlConfiguration</span></span>
<span data-ttu-id="bba55-118">Url Configuration for action set</span><span class="sxs-lookup"><span data-stu-id="bba55-118">Url Configuration for action set</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlConfiguration
Parameter Sets: (All)
Aliases:
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bba55-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bba55-119">CommonParameters</span></span>
<span data-ttu-id="bba55-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bba55-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bba55-121">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bba55-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bba55-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bba55-122">INPUTS</span></span>

### <span data-ttu-id="bba55-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="bba55-123">None</span></span>

## <span data-ttu-id="bba55-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bba55-124">OUTPUTS</span></span>

### <span data-ttu-id="bba55-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="bba55-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleActionSet</span></span>

## <span data-ttu-id="bba55-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="bba55-126">NOTES</span></span>

## <span data-ttu-id="bba55-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bba55-127">RELATED LINKS</span></span>

[<span data-ttu-id="bba55-128">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="bba55-128">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="bba55-129">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="bba55-129">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="bba55-130">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="bba55-130">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="bba55-131">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="bba55-131">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="bba55-132">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="bba55-132">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="bba55-133">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="bba55-133">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="bba55-134">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="bba55-134">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)

[<span data-ttu-id="bba55-135">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="bba55-135">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleUrlConfiguration.md)