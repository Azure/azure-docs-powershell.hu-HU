---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityPricing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityPricing.md
ms.openlocfilehash: e9dfe0e7ed4612ca99a2decf3aa91b521a7e9664
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187997"
---
# <span data-ttu-id="9ca97-101">Set-AzSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="9ca97-101">Set-AzSecurityPricing</span></span>

## <span data-ttu-id="9ca97-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9ca97-102">SYNOPSIS</span></span>
<span data-ttu-id="9ca97-103">Az Azure Security Center-szint díjszabását határozza meg egy hatókörben.</span><span class="sxs-lookup"><span data-stu-id="9ca97-103">Sets the pricing of Azure Security Center tier for a scope.</span></span>

## <span data-ttu-id="9ca97-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9ca97-104">SYNTAX</span></span>

### <span data-ttu-id="9ca97-105">SubscriptionLevelResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9ca97-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzSecurityPricing -Name <String> -PricingTier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ca97-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="9ca97-106">InputObject</span></span>
```
Set-AzSecurityPricing -InputObject <PSSecurityPricing> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ca97-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="9ca97-107">DESCRIPTION</span></span>
<span data-ttu-id="9ca97-108">Az Azure Security Center-szint díjszabását határozza meg egy hatókörben.</span><span class="sxs-lookup"><span data-stu-id="9ca97-108">Sets the pricing of Azure Security Center tier for a scope.</span></span>

## <span data-ttu-id="9ca97-109">Példák</span><span class="sxs-lookup"><span data-stu-id="9ca97-109">EXAMPLES</span></span>

### <span data-ttu-id="9ca97-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9ca97-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityPricing -Name "virtualmachines" -PricingTier "Standard"
```

<span data-ttu-id="9ca97-111">Az előfizetés Azure Security Center árazási rétegének "normál" értékre állítása</span><span class="sxs-lookup"><span data-stu-id="9ca97-111">Sets the subscription Azure Security Center pricing tier to "Standard"</span></span>


## <span data-ttu-id="9ca97-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9ca97-112">PARAMETERS</span></span>

### <span data-ttu-id="9ca97-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ca97-113">-DefaultProfile</span></span>
<span data-ttu-id="9ca97-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9ca97-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ca97-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9ca97-115">-InputObject</span></span>
<span data-ttu-id="9ca97-116">Beviteli objektum</span><span class="sxs-lookup"><span data-stu-id="9ca97-116">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9ca97-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9ca97-117">-Name</span></span>
<span data-ttu-id="9ca97-118">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="9ca97-118">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ca97-119">-PricingTier</span><span class="sxs-lookup"><span data-stu-id="9ca97-119">-PricingTier</span></span>
<span data-ttu-id="9ca97-120">Árazási szint</span><span class="sxs-lookup"><span data-stu-id="9ca97-120">Pricing Tier.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ca97-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9ca97-121">-Confirm</span></span>
<span data-ttu-id="9ca97-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9ca97-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ca97-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ca97-123">-WhatIf</span></span>
<span data-ttu-id="9ca97-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9ca97-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9ca97-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9ca97-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ca97-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ca97-126">CommonParameters</span></span>
<span data-ttu-id="9ca97-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9ca97-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ca97-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="9ca97-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ca97-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9ca97-129">INPUTS</span></span>

### <span data-ttu-id="9ca97-130">Microsoft. Azure. commands. Security. models. árak. PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="9ca97-130">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="9ca97-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9ca97-131">OUTPUTS</span></span>

### <span data-ttu-id="9ca97-132">Microsoft. Azure. commands. Security. models. árak. PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="9ca97-132">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="9ca97-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9ca97-133">NOTES</span></span>

## <span data-ttu-id="9ca97-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9ca97-134">RELATED LINKS</span></span>