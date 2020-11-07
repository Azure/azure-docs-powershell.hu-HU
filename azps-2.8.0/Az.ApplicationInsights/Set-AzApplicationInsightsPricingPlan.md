---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/set-azapplicationinsightspricingplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsPricingPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsPricingPlan.md
ms.openlocfilehash: 13bd076488e8bb379e3b365c6c4d7803ea650f40
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667886"
---
# <span data-ttu-id="bc4ce-101">Set-AzApplicationInsightsPricingPlan</span><span class="sxs-lookup"><span data-stu-id="bc4ce-101">Set-AzApplicationInsightsPricingPlan</span></span>

## <span data-ttu-id="bc4ce-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bc4ce-102">SYNOPSIS</span></span>
<span data-ttu-id="bc4ce-103">Árképzési terv és a napi adatmennyiség adatainak beállítása az alkalmazásbeli betekintéshez</span><span class="sxs-lookup"><span data-stu-id="bc4ce-103">Set pricing plan and daily data volume information for an application insights resource</span></span>

## <span data-ttu-id="bc4ce-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bc4ce-104">SYNTAX</span></span>

### <span data-ttu-id="bc4ce-105">ComponentNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bc4ce-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ResourceGroupName] <String> [-Name] <String> [-PricingPlan <String>]
 [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc4ce-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc4ce-106">ComponentObjectParameterSet</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-PricingPlan <String>] [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc4ce-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc4ce-107">ResourceIdParameterSet</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ResourceId] <String> [-PricingPlan <String>] [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bc4ce-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="bc4ce-108">DESCRIPTION</span></span>
<span data-ttu-id="bc4ce-109">Árképzési terv és a napi adatmennyiség adatainak beállítása az alkalmazásbeli betekintéshez</span><span class="sxs-lookup"><span data-stu-id="bc4ce-109">Set pricing plan and daily data volume information for an application insights resource</span></span>

## <span data-ttu-id="bc4ce-110">Példák</span><span class="sxs-lookup"><span data-stu-id="bc4ce-110">EXAMPLES</span></span>

### <span data-ttu-id="bc4ce-111">Példa 1 az árképzési terv és a napi adatmennyiség beállítása az alkalmazási adatokhoz</span><span class="sxs-lookup"><span data-stu-id="bc4ce-111">Example 1 Set pricing plan and daily data volume information for an application insights resource</span></span>
```
PS C:\> Set-AzApplicationInsightsDailyCap -ResourceGroupName "testgroup" -Name "test" -PricingPlan "Basic" -DailyCapGB 400

 Cap ResetTime StopSendNotificationWhenHitCap PricingPlan
--- --------- ------------------------------ -----------
400         0                           False Basic
```

<span data-ttu-id="bc4ce-112">Az árképzési terv beállítása az "egyszerű" értékre a napi adatmennyiség sapka és a 400GB közötti választás leállításához, ha a találatok között a "teszt" az erőforrás csoportban "testgroup"</span><span class="sxs-lookup"><span data-stu-id="bc4ce-112">Set the pricing plan to "Basic", set the daily data volume cap to 400GB per day and stop send notification when hit cap for resource "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="bc4ce-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bc4ce-113">PARAMETERS</span></span>

### <span data-ttu-id="bc4ce-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="bc4ce-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="bc4ce-115">Az alkalmazás betekintése összetevő-objektum.</span><span class="sxs-lookup"><span data-stu-id="bc4ce-115">Application Insights Component Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent
Parameter Sets: ComponentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bc4ce-116">-DailyCapGB</span><span class="sxs-lookup"><span data-stu-id="bc4ce-116">-DailyCapGB</span></span>
<span data-ttu-id="bc4ce-117">Napi sapka.</span><span class="sxs-lookup"><span data-stu-id="bc4ce-117">Daily Cap.</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc4ce-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc4ce-118">-DefaultProfile</span></span>
<span data-ttu-id="bc4ce-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bc4ce-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc4ce-120">-DisableNotificationWhenHitCap</span><span class="sxs-lookup"><span data-stu-id="bc4ce-120">-DisableNotificationWhenHitCap</span></span>
<span data-ttu-id="bc4ce-121">Az üzenet küldésének leállítása a találatok között.</span><span class="sxs-lookup"><span data-stu-id="bc4ce-121">Stop send notification when hit cap.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc4ce-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bc4ce-122">-Name</span></span>
<span data-ttu-id="bc4ce-123">Az alkalmazás betekintési összetevőjének neve.</span><span class="sxs-lookup"><span data-stu-id="bc4ce-123">Application Insights Component Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc4ce-124">-PricingPlan</span><span class="sxs-lookup"><span data-stu-id="bc4ce-124">-PricingPlan</span></span>
<span data-ttu-id="bc4ce-125">Árképzési terv neve</span><span class="sxs-lookup"><span data-stu-id="bc4ce-125">Pricing plan name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Application Insights Enterprise, Limited Basic

Required: False
Position: Named
Default value: "Basic"
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc4ce-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc4ce-126">-ResourceGroupName</span></span>
<span data-ttu-id="bc4ce-127">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="bc4ce-127">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc4ce-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bc4ce-128">-ResourceId</span></span>
<span data-ttu-id="bc4ce-129">Az alkalmazás betekintési összetevőjének erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="bc4ce-129">Application Insights Component Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc4ce-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="bc4ce-130">-Confirm</span></span>
<span data-ttu-id="bc4ce-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bc4ce-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc4ce-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc4ce-132">-WhatIf</span></span>
<span data-ttu-id="bc4ce-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="bc4ce-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bc4ce-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bc4ce-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc4ce-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc4ce-135">CommonParameters</span></span>
<span data-ttu-id="bc4ce-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bc4ce-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc4ce-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc4ce-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc4ce-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bc4ce-138">INPUTS</span></span>

### <span data-ttu-id="bc4ce-139">Microsoft. Azure. Command. ApplicationInsights. models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="bc4ce-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="bc4ce-140">System. String</span><span class="sxs-lookup"><span data-stu-id="bc4ce-140">System.String</span></span>

## <span data-ttu-id="bc4ce-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bc4ce-141">OUTPUTS</span></span>

### <span data-ttu-id="bc4ce-142">Microsoft. Azure. Command. ApplicationInsights. models. PSPricingPlan</span><span class="sxs-lookup"><span data-stu-id="bc4ce-142">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span></span>

## <span data-ttu-id="bc4ce-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bc4ce-143">NOTES</span></span>

## <span data-ttu-id="bc4ce-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bc4ce-144">RELATED LINKS</span></span>
