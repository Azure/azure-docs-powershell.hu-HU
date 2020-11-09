---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleactionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleActionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleActionSet.md
ms.openlocfilehash: f20647613a6e484d46a8785cfebea304b6a7ff23
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302763"
---
# <span data-ttu-id="33ae3-101">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="33ae3-101">New-AzApplicationGatewayRewriteRuleActionSet</span></span>

## <span data-ttu-id="33ae3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="33ae3-102">SYNOPSIS</span></span>
<span data-ttu-id="33ae3-103">Egy alkalmazás-átjáróhoz tartozó átírási szabály műveleti beállítását hozza létre.</span><span class="sxs-lookup"><span data-stu-id="33ae3-103">Creates a rewrite rule action set for an application gateway.</span></span>

## <span data-ttu-id="33ae3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="33ae3-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleActionSet
 [-RequestHeaderConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]>]
 [-ResponseHeaderConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]>]
 [-UrlConfiguration [Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlConfiguration]]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="33ae3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="33ae3-105">DESCRIPTION</span></span>
<span data-ttu-id="33ae3-106">**A New-AzApplicationGatewayRewriteRuleActionSet** parancsmag az Azure Application Gateway-hez létrehozott átírási szabályhoz.</span><span class="sxs-lookup"><span data-stu-id="33ae3-106">**The New-AzApplicationGatewayRewriteRuleActionSet** cmdlet creates a rewrite rule action set for an Azure application gateway.</span></span>

## <span data-ttu-id="33ae3-107">Példák</span><span class="sxs-lookup"><span data-stu-id="33ae3-107">EXAMPLES</span></span>

### <span data-ttu-id="33ae3-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="33ae3-108">Example 1</span></span>
```powershell
PS C:\> $action = New-AzApplicationGatewayRewriteRuleActionSet -ResponseHeaderConfiguration $hc -UrlConfiguration $urlConfiguration
```

<span data-ttu-id="33ae3-109">Ez a parancs létrehoz egy új szabály-műveleti halmazt, és az eredményt az $action nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="33ae3-109">This command creates a rewrite rule action set and stores the result in the variable named $action.</span></span>

## <span data-ttu-id="33ae3-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="33ae3-110">PARAMETERS</span></span>

### <span data-ttu-id="33ae3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33ae3-111">-DefaultProfile</span></span>
<span data-ttu-id="33ae3-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="33ae3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33ae3-113">-RequestHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="33ae3-113">-RequestHeaderConfiguration</span></span>
<span data-ttu-id="33ae3-114">A kérés fejléc-konfigurációjának listája</span><span class="sxs-lookup"><span data-stu-id="33ae3-114">List of request header configurations</span></span>

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

### <span data-ttu-id="33ae3-115">-ResponseHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="33ae3-115">-ResponseHeaderConfiguration</span></span>
<span data-ttu-id="33ae3-116">A válasz fejléc-konfigurációinak listája</span><span class="sxs-lookup"><span data-stu-id="33ae3-116">List of response header configurations</span></span>

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

### <span data-ttu-id="33ae3-117">-UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="33ae3-117">-UrlConfiguration</span></span>
<span data-ttu-id="33ae3-118">A műveletsor URL-beállítása</span><span class="sxs-lookup"><span data-stu-id="33ae3-118">Url Configuration for action set</span></span>

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

### <span data-ttu-id="33ae3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33ae3-119">CommonParameters</span></span>
<span data-ttu-id="33ae3-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="33ae3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33ae3-121">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33ae3-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33ae3-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="33ae3-122">INPUTS</span></span>

### <span data-ttu-id="33ae3-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="33ae3-123">None</span></span>

## <span data-ttu-id="33ae3-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="33ae3-124">OUTPUTS</span></span>

### <span data-ttu-id="33ae3-125">Microsoft. Azure. commands. Network. models. PSApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="33ae3-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleActionSet</span></span>

## <span data-ttu-id="33ae3-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="33ae3-126">NOTES</span></span>

## <span data-ttu-id="33ae3-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="33ae3-127">RELATED LINKS</span></span>

[<span data-ttu-id="33ae3-128">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="33ae3-128">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="33ae3-129">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="33ae3-129">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="33ae3-130">Új – AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="33ae3-130">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="33ae3-131">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="33ae3-131">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="33ae3-132">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="33ae3-132">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="33ae3-133">Új – AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="33ae3-133">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="33ae3-134">Új – AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="33ae3-134">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)

[<span data-ttu-id="33ae3-135">Új – AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="33ae3-135">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleUrlConfiguration.md)