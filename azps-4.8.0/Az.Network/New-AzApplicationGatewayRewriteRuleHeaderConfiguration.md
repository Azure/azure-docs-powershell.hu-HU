---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleheaderconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md
ms.openlocfilehash: ed8cda03debbb69c2fa65d7c209889c4cd3d2446
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183021"
---
# <span data-ttu-id="3b24a-101">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="3b24a-101">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>

## <span data-ttu-id="3b24a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3b24a-102">SYNOPSIS</span></span>
<span data-ttu-id="3b24a-103">Egy új szabály fejléc-konfigurációját hozza létre egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="3b24a-103">Creates a rewrite rule header configuration for an application gateway.</span></span>

## <span data-ttu-id="3b24a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3b24a-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleHeaderConfiguration -HeaderName <String> [-HeaderValue <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3b24a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3b24a-105">DESCRIPTION</span></span>
<span data-ttu-id="3b24a-106">**Az AzApplicationGatewayRewriteRuleHeaderConfiguration** parancsmag létrehoz egy átírási szabályt az Azure Application átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="3b24a-106">**The AzApplicationGatewayRewriteRuleHeaderConfiguration** cmdlet creates a rewrite rule action set for an Azure application gateway.</span></span>

## <span data-ttu-id="3b24a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3b24a-107">EXAMPLES</span></span>

### <span data-ttu-id="3b24a-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3b24a-108">Example 1</span></span>
```powershell
PS C:\> $hc = New-AzApplicationGatewayRewriteRuleHeaderConfiguration -HeaderName abc -HeaderValue def
```

<span data-ttu-id="3b24a-109">Ez a parancs átírják a szabály fejlécének konfigurációját, és az eredményt az $hc nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="3b24a-109">This command creates a rewrite rule header configuration and stores the result in the variable named $hc.</span></span>

## <span data-ttu-id="3b24a-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3b24a-110">PARAMETERS</span></span>

### <span data-ttu-id="3b24a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b24a-111">-DefaultProfile</span></span>
<span data-ttu-id="3b24a-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3b24a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b24a-113">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="3b24a-113">-HeaderName</span></span>
<span data-ttu-id="3b24a-114">Az átírni kívánt fejléc neve</span><span class="sxs-lookup"><span data-stu-id="3b24a-114">Name of the Header to rewrite</span></span>

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

### <span data-ttu-id="3b24a-115">-HeaderValue</span><span class="sxs-lookup"><span data-stu-id="3b24a-115">-HeaderValue</span></span>
<span data-ttu-id="3b24a-116">A fejléc értéke a megadott fejléc-név halmazához.</span><span class="sxs-lookup"><span data-stu-id="3b24a-116">Header value to the set for the given header name.</span></span>
<span data-ttu-id="3b24a-117">A fejléc törlődik, ha nincs megadva</span><span class="sxs-lookup"><span data-stu-id="3b24a-117">Header will be deleted if this is omitted</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b24a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b24a-118">CommonParameters</span></span>
<span data-ttu-id="3b24a-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3b24a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b24a-120">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b24a-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b24a-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3b24a-121">INPUTS</span></span>

### <span data-ttu-id="3b24a-122">Nincs</span><span class="sxs-lookup"><span data-stu-id="3b24a-122">None</span></span>

## <span data-ttu-id="3b24a-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3b24a-123">OUTPUTS</span></span>

### <span data-ttu-id="3b24a-124">Microsoft. Azure. commands. Network. models. PSApplicationGatewayHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="3b24a-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration</span></span>

## <span data-ttu-id="3b24a-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3b24a-125">NOTES</span></span>

## <span data-ttu-id="3b24a-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3b24a-126">RELATED LINKS</span></span>

[<span data-ttu-id="3b24a-127">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3b24a-127">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="3b24a-128">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3b24a-128">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="3b24a-129">Új – AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3b24a-129">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="3b24a-130">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3b24a-130">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="3b24a-131">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3b24a-131">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="3b24a-132">Új – AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="3b24a-132">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="3b24a-133">Új – AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="3b24a-133">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)
