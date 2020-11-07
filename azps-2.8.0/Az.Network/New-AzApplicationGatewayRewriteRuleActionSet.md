---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleactionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleActionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleActionSet.md
ms.openlocfilehash: 84be6aa60ede19e88b98ca9517fa3cbce3872c8b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837495"
---
# <span data-ttu-id="8cfdf-101">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="8cfdf-101">New-AzApplicationGatewayRewriteRuleActionSet</span></span>

## <span data-ttu-id="8cfdf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8cfdf-102">SYNOPSIS</span></span>
<span data-ttu-id="8cfdf-103">Egy alkalmazás-átjáróhoz tartozó átírási szabály műveleti beállítását hozza létre.</span><span class="sxs-lookup"><span data-stu-id="8cfdf-103">Creates a rewrite rule action set for an application gateway.</span></span>

## <span data-ttu-id="8cfdf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8cfdf-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleActionSet
 [-RequestHeaderConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]>]
 [-ResponseHeaderConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8cfdf-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8cfdf-105">DESCRIPTION</span></span>
<span data-ttu-id="8cfdf-106">**A New-AzApplicationGatewayRewriteRuleActionSet** parancsmag az Azure Application Gateway-hez létrehozott átírási szabályhoz.</span><span class="sxs-lookup"><span data-stu-id="8cfdf-106">**The New-AzApplicationGatewayRewriteRuleActionSet** cmdlet creates a rewrite rule action set for an Azure application gateway.</span></span>

## <span data-ttu-id="8cfdf-107">Példák</span><span class="sxs-lookup"><span data-stu-id="8cfdf-107">EXAMPLES</span></span>

### <span data-ttu-id="8cfdf-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="8cfdf-108">Example 1</span></span>
```powershell
PS C:\> $action = New-AzApplicationGatewayRewriteRuleActionSet -ResponseHeaderConfiguration $hc
```

<span data-ttu-id="8cfdf-109">Ez a parancs létrehoz egy új szabály-műveleti halmazt, és az eredményt az $action nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="8cfdf-109">This command creates a rewrite rule action set and stores the result in the variable named $action.</span></span>

## <span data-ttu-id="8cfdf-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8cfdf-110">PARAMETERS</span></span>

### <span data-ttu-id="8cfdf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cfdf-111">-DefaultProfile</span></span>
<span data-ttu-id="8cfdf-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8cfdf-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8cfdf-113">-RequestHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="8cfdf-113">-RequestHeaderConfiguration</span></span>
<span data-ttu-id="8cfdf-114">A kérés fejléc-konfigurációjának listája</span><span class="sxs-lookup"><span data-stu-id="8cfdf-114">List of request header configurations</span></span>

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

### <span data-ttu-id="8cfdf-115">-ResponseHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="8cfdf-115">-ResponseHeaderConfiguration</span></span>
<span data-ttu-id="8cfdf-116">A válasz fejléc-konfigurációinak listája</span><span class="sxs-lookup"><span data-stu-id="8cfdf-116">List of response header configurations</span></span>

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

### <span data-ttu-id="8cfdf-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cfdf-117">CommonParameters</span></span>
<span data-ttu-id="8cfdf-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8cfdf-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cfdf-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8cfdf-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cfdf-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8cfdf-120">INPUTS</span></span>

### <span data-ttu-id="8cfdf-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="8cfdf-121">None</span></span>

## <span data-ttu-id="8cfdf-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8cfdf-122">OUTPUTS</span></span>

### <span data-ttu-id="8cfdf-123">Microsoft. Azure. commands. Network. models. PSApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="8cfdf-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleActionSet</span></span>

## <span data-ttu-id="8cfdf-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8cfdf-124">NOTES</span></span>

## <span data-ttu-id="8cfdf-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8cfdf-125">RELATED LINKS</span></span>

[<span data-ttu-id="8cfdf-126">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8cfdf-126">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="8cfdf-127">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8cfdf-127">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="8cfdf-128">Új – AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8cfdf-128">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="8cfdf-129">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8cfdf-129">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="8cfdf-130">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8cfdf-130">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="8cfdf-131">Új – AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="8cfdf-131">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="8cfdf-132">Új – AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="8cfdf-132">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
