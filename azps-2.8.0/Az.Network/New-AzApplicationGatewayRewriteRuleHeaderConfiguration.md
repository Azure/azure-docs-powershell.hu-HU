---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleheaderconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md
ms.openlocfilehash: d003bd63813fa1b3b0b7d4ffc63b591655b3ff09
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837491"
---
# <span data-ttu-id="65b0c-101">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="65b0c-101">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>

## <span data-ttu-id="65b0c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="65b0c-102">SYNOPSIS</span></span>
<span data-ttu-id="65b0c-103">Egy új szabály fejléc-konfigurációját hozza létre egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="65b0c-103">Creates a rewrite rule header configuration for an application gateway.</span></span>

## <span data-ttu-id="65b0c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="65b0c-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleHeaderConfiguration -HeaderName <String> [-HeaderValue <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65b0c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="65b0c-105">DESCRIPTION</span></span>
<span data-ttu-id="65b0c-106">**Az AzApplicationGatewayRewriteRuleHeaderConfiguration** parancsmag létrehoz egy átírási szabályt az Azure Application átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="65b0c-106">**The AzApplicationGatewayRewriteRuleHeaderConfiguration** cmdlet creates a rewrite rule action set for an Azure application gateway.</span></span>

## <span data-ttu-id="65b0c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="65b0c-107">EXAMPLES</span></span>

### <span data-ttu-id="65b0c-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="65b0c-108">Example 1</span></span>
```powershell
PS C:\> $hc = New-AzApplicationGatewayRewriteRuleHeaderConfiguration -HeaderName abc -HeaderValue def
```

<span data-ttu-id="65b0c-109">Ez a parancs átírják a szabály fejlécének konfigurációját, és az eredményt az $hc nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="65b0c-109">This command creates a rewrite rule header configuration and stores the result in the variable named $hc.</span></span>

## <span data-ttu-id="65b0c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="65b0c-110">PARAMETERS</span></span>

### <span data-ttu-id="65b0c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65b0c-111">-DefaultProfile</span></span>
<span data-ttu-id="65b0c-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="65b0c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65b0c-113">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="65b0c-113">-HeaderName</span></span>
<span data-ttu-id="65b0c-114">Az átírni kívánt fejléc neve</span><span class="sxs-lookup"><span data-stu-id="65b0c-114">Name of the Header to rewrite</span></span>

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

### <span data-ttu-id="65b0c-115">-HeaderValue</span><span class="sxs-lookup"><span data-stu-id="65b0c-115">-HeaderValue</span></span>
<span data-ttu-id="65b0c-116">A fejléc értéke a megadott fejléc-név halmazához.</span><span class="sxs-lookup"><span data-stu-id="65b0c-116">Header value to the set for the given header name.</span></span>
<span data-ttu-id="65b0c-117">A fejléc törlődik, ha nincs megadva</span><span class="sxs-lookup"><span data-stu-id="65b0c-117">Header will be deleted if this is omitted</span></span>

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

### <span data-ttu-id="65b0c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65b0c-118">CommonParameters</span></span>
<span data-ttu-id="65b0c-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="65b0c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65b0c-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65b0c-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65b0c-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="65b0c-121">INPUTS</span></span>

### <span data-ttu-id="65b0c-122">Nincs</span><span class="sxs-lookup"><span data-stu-id="65b0c-122">None</span></span>

## <span data-ttu-id="65b0c-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="65b0c-123">OUTPUTS</span></span>

### <span data-ttu-id="65b0c-124">Microsoft. Azure. commands. Network. models. PSApplicationGatewayHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="65b0c-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration</span></span>

## <span data-ttu-id="65b0c-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="65b0c-125">NOTES</span></span>

## <span data-ttu-id="65b0c-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="65b0c-126">RELATED LINKS</span></span>

[<span data-ttu-id="65b0c-127">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="65b0c-127">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="65b0c-128">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="65b0c-128">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="65b0c-129">Új – AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="65b0c-129">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="65b0c-130">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="65b0c-130">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="65b0c-131">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="65b0c-131">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="65b0c-132">Új – AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="65b0c-132">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="65b0c-133">Új – AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="65b0c-133">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)
