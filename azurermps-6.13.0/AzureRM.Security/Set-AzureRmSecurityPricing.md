---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityPricing.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityPricing.md
ms.openlocfilehash: f5b23c9221fe8d344e9220590283ab7799a0a3fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495656"
---
# <span data-ttu-id="fb392-101">Set-AzureRmSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="fb392-101">Set-AzureRmSecurityPricing</span></span>

## <span data-ttu-id="fb392-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fb392-102">SYNOPSIS</span></span>
<span data-ttu-id="fb392-103">Az Azure Security Center-szint díjszabását határozza meg egy hatókörben.</span><span class="sxs-lookup"><span data-stu-id="fb392-103">Sets the pricing of Azure Security Center tier for a scope.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb392-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fb392-104">SYNTAX</span></span>

### <span data-ttu-id="fb392-105">SubscriptionLevelResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fb392-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzureRmSecurityPricing -Name <String> -PricingTier <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb392-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="fb392-106">ResourceGroupLevelResource</span></span>
```
Set-AzureRmSecurityPricing -ResourceGroupName <String> -Name <String> -PricingTier <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb392-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="fb392-107">InputObject</span></span>
```
Set-AzureRmSecurityPricing -InputObject <PSAddPricingInputObject> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb392-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="fb392-108">DESCRIPTION</span></span>
<span data-ttu-id="fb392-109">Az Azure Security Center-szint díjszabását határozza meg egy hatókörben.</span><span class="sxs-lookup"><span data-stu-id="fb392-109">Sets the pricing of Azure Security Center tier for a scope.</span></span>

## <span data-ttu-id="fb392-110">Példák</span><span class="sxs-lookup"><span data-stu-id="fb392-110">EXAMPLES</span></span>

### <span data-ttu-id="fb392-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="fb392-111">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmSecurityPricing -Name "default" -PricingTier "Standard"
Id                                                                                                 Name    PricingTier
--                                                                                                 ----    -----------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/pricings/default default Standard
```

<span data-ttu-id="fb392-112">Az előfizetés Azure Security Center árazási rétegének "normál" értékre állítása</span><span class="sxs-lookup"><span data-stu-id="fb392-112">Sets the subscription Azure Security Center pricing tier to "Standard"</span></span>

### <span data-ttu-id="fb392-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="fb392-113">Example 2</span></span>
```powershell
PS C:\> Set-AzureRmSecurityPricing -Name "myService1" -ResourceGroupName "myService1" -PricingTier "Standard"

Id                                                                                                                     
--                                                                                                                     
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/pricings/...
```

<span data-ttu-id="fb392-114">A "myService1" erőforráscsoporthoz az Azure Security Center árazási rétegét "normál" értékre állítja.</span><span class="sxs-lookup"><span data-stu-id="fb392-114">Sets the "myService1" resource group Azure Security Center pricing tier to "Standard"</span></span>

## <span data-ttu-id="fb392-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fb392-115">PARAMETERS</span></span>

### <span data-ttu-id="fb392-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb392-116">-DefaultProfile</span></span>
<span data-ttu-id="fb392-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fb392-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb392-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fb392-118">-InputObject</span></span>
<span data-ttu-id="fb392-119">Beviteli objektum</span><span class="sxs-lookup"><span data-stu-id="fb392-119">Input Object.</span></span>

```yaml
Type: PSAddPricingInputObject
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fb392-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fb392-120">-Name</span></span>
<span data-ttu-id="fb392-121">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="fb392-121">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb392-122">-PricingTier</span><span class="sxs-lookup"><span data-stu-id="fb392-122">-PricingTier</span></span>
<span data-ttu-id="fb392-123">Árazási szint</span><span class="sxs-lookup"><span data-stu-id="fb392-123">Pricing Tier.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb392-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb392-124">-ResourceGroupName</span></span>
<span data-ttu-id="fb392-125">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="fb392-125">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb392-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fb392-126">-Confirm</span></span>
<span data-ttu-id="fb392-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fb392-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb392-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb392-128">-WhatIf</span></span>
<span data-ttu-id="fb392-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fb392-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fb392-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fb392-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb392-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb392-131">CommonParameters</span></span>
<span data-ttu-id="fb392-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fb392-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb392-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb392-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb392-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fb392-134">INPUTS</span></span>

### <span data-ttu-id="fb392-135">System. String</span><span class="sxs-lookup"><span data-stu-id="fb392-135">System.String</span></span>
<span data-ttu-id="fb392-136">Microsoft. Azure. Command. Security. parancsmagok. árak. PSAddPricingInputObject</span><span class="sxs-lookup"><span data-stu-id="fb392-136">Microsoft.Azure.Commands.Security.Cmdlets.Pricings.PSAddPricingInputObject</span></span>

## <span data-ttu-id="fb392-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fb392-137">OUTPUTS</span></span>

### <span data-ttu-id="fb392-138">Microsoft. Azure. commands. Security. models. árak. PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="fb392-138">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="fb392-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fb392-139">NOTES</span></span>

## <span data-ttu-id="fb392-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fb392-140">RELATED LINKS</span></span>
