---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleactionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleActionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleActionSet.md
ms.openlocfilehash: f20647613a6e484d46a8785cfebea304b6a7ff23
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358229"
---
# <span data-ttu-id="ada92-101">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="ada92-101">New-AzApplicationGatewayRewriteRuleActionSet</span></span>

## <span data-ttu-id="ada92-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ada92-102">SYNOPSIS</span></span>
<span data-ttu-id="ada92-103">Újraírási szabály műveletkészletet hoz létre egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="ada92-103">Creates a rewrite rule action set for an application gateway.</span></span>

## <span data-ttu-id="ada92-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ada92-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleActionSet
 [-RequestHeaderConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]>]
 [-ResponseHeaderConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]>]
 [-UrlConfiguration [Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlConfiguration]]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ada92-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ada92-105">DESCRIPTION</span></span>
<span data-ttu-id="ada92-106">**A New-AzApplicationGatewayRewriteRuleActionSet** parancsmag létrehoz egy újraírási szabály műveletkészletet egy Azure-alkalmazás átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="ada92-106">**The New-AzApplicationGatewayRewriteRuleActionSet** cmdlet creates a rewrite rule action set for an Azure application gateway.</span></span>

## <span data-ttu-id="ada92-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ada92-107">EXAMPLES</span></span>

### <span data-ttu-id="ada92-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="ada92-108">Example 1</span></span>
```powershell
PS C:\> $action = New-AzApplicationGatewayRewriteRuleActionSet -ResponseHeaderConfiguration $hc -UrlConfiguration $urlConfiguration
```

<span data-ttu-id="ada92-109">Ez a parancs egy újraírási szabály-műveletkészletet hoz létre, és az eredményt a következő nevű változóban $action.</span><span class="sxs-lookup"><span data-stu-id="ada92-109">This command creates a rewrite rule action set and stores the result in the variable named $action.</span></span>

## <span data-ttu-id="ada92-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ada92-110">PARAMETERS</span></span>

### <span data-ttu-id="ada92-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ada92-111">-DefaultProfile</span></span>
<span data-ttu-id="ada92-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ada92-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ada92-113">-RequestHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="ada92-113">-RequestHeaderConfiguration</span></span>
<span data-ttu-id="ada92-114">Kérésfejléc-konfigurációk listája</span><span class="sxs-lookup"><span data-stu-id="ada92-114">List of request header configurations</span></span>

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

### <span data-ttu-id="ada92-115">-ResponseHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="ada92-115">-ResponseHeaderConfiguration</span></span>
<span data-ttu-id="ada92-116">Válaszfejléc-konfigurációk listája</span><span class="sxs-lookup"><span data-stu-id="ada92-116">List of response header configurations</span></span>

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

### <span data-ttu-id="ada92-117">-UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="ada92-117">-UrlConfiguration</span></span>
<span data-ttu-id="ada92-118">Url Configuration for action set</span><span class="sxs-lookup"><span data-stu-id="ada92-118">Url Configuration for action set</span></span>

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

### <span data-ttu-id="ada92-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ada92-119">CommonParameters</span></span>
<span data-ttu-id="ada92-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ada92-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ada92-121">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ada92-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ada92-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ada92-122">INPUTS</span></span>

### <span data-ttu-id="ada92-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="ada92-123">None</span></span>

## <span data-ttu-id="ada92-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ada92-124">OUTPUTS</span></span>

### <span data-ttu-id="ada92-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="ada92-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleActionSet</span></span>

## <span data-ttu-id="ada92-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ada92-126">NOTES</span></span>

## <span data-ttu-id="ada92-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ada92-127">RELATED LINKS</span></span>

[<span data-ttu-id="ada92-128">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ada92-128">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="ada92-129">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ada92-129">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="ada92-130">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ada92-130">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="ada92-131">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ada92-131">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="ada92-132">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ada92-132">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="ada92-133">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="ada92-133">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="ada92-134">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="ada92-134">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)

[<span data-ttu-id="ada92-135">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="ada92-135">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleUrlConfiguration.md)