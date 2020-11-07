---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityPricing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityPricing.md
ms.openlocfilehash: a52ae3b59cc7cbf99bf7f4751a36f271bc9610de
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669222"
---
# <span data-ttu-id="2f414-101">Set-AzSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="2f414-101">Set-AzSecurityPricing</span></span>

## <span data-ttu-id="2f414-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2f414-102">SYNOPSIS</span></span>
<span data-ttu-id="2f414-103">Az Azure Security Center-szint díjszabását határozza meg egy hatókörben.</span><span class="sxs-lookup"><span data-stu-id="2f414-103">Sets the pricing of Azure Security Center tier for a scope.</span></span>

## <span data-ttu-id="2f414-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2f414-104">SYNTAX</span></span>

### <span data-ttu-id="2f414-105">SubscriptionLevelResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2f414-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzSecurityPricing -Name <String> -PricingTier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f414-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="2f414-106">InputObject</span></span>
```
Set-AzSecurityPricing -InputObject <PSSecurityPricing> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f414-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="2f414-107">DESCRIPTION</span></span>
<span data-ttu-id="2f414-108">Az Azure Security Center-szint díjszabását határozza meg egy hatókörben.</span><span class="sxs-lookup"><span data-stu-id="2f414-108">Sets the pricing of Azure Security Center tier for a scope.</span></span>

## <span data-ttu-id="2f414-109">Példák</span><span class="sxs-lookup"><span data-stu-id="2f414-109">EXAMPLES</span></span>

### <span data-ttu-id="2f414-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="2f414-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityPricing -Name "default" -PricingTier "Standard"
Id                                                                                                 Name    PricingTier
--                                                                                                 ----    -----------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/pricings/default default Standard
```

<span data-ttu-id="2f414-111">Az előfizetés Azure Security Center árazási rétegének "normál" értékre állítása</span><span class="sxs-lookup"><span data-stu-id="2f414-111">Sets the subscription Azure Security Center pricing tier to "Standard"</span></span>

### <span data-ttu-id="2f414-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="2f414-112">Example 2</span></span>
```powershell
PS C:\> Set-AzSecurityPricing -Name "myService1" -ResourceGroupName "myService1" -PricingTier "Standard"

Id                                                                                                                     
--                                                                                                                     
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/pricings/...
```

<span data-ttu-id="2f414-113">A "myService1" erőforráscsoporthoz az Azure Security Center árazási rétegét "normál" értékre állítja.</span><span class="sxs-lookup"><span data-stu-id="2f414-113">Sets the "myService1" resource group Azure Security Center pricing tier to "Standard"</span></span>

## <span data-ttu-id="2f414-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2f414-114">PARAMETERS</span></span>

### <span data-ttu-id="2f414-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f414-115">-DefaultProfile</span></span>
<span data-ttu-id="2f414-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2f414-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f414-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2f414-117">-InputObject</span></span>
<span data-ttu-id="2f414-118">Beviteli objektum</span><span class="sxs-lookup"><span data-stu-id="2f414-118">Input Object.</span></span>

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

### <span data-ttu-id="2f414-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2f414-119">-Name</span></span>
<span data-ttu-id="2f414-120">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="2f414-120">Resource name.</span></span>

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

### <span data-ttu-id="2f414-121">-PricingTier</span><span class="sxs-lookup"><span data-stu-id="2f414-121">-PricingTier</span></span>
<span data-ttu-id="2f414-122">Árazási szint</span><span class="sxs-lookup"><span data-stu-id="2f414-122">Pricing Tier.</span></span>

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

### <span data-ttu-id="2f414-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2f414-123">-Confirm</span></span>
<span data-ttu-id="2f414-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2f414-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f414-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f414-125">-WhatIf</span></span>
<span data-ttu-id="2f414-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2f414-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2f414-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2f414-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f414-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f414-128">CommonParameters</span></span>
<span data-ttu-id="2f414-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2f414-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f414-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f414-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f414-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2f414-131">INPUTS</span></span>

### <span data-ttu-id="2f414-132">Microsoft. Azure. commands. Security. models. árak. PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="2f414-132">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="2f414-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2f414-133">OUTPUTS</span></span>

### <span data-ttu-id="2f414-134">Microsoft. Azure. commands. Security. models. árak. PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="2f414-134">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="2f414-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2f414-135">NOTES</span></span>

## <span data-ttu-id="2f414-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2f414-136">RELATED LINKS</span></span>
