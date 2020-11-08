---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/set-azapplicationinsightspricingplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsPricingPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsPricingPlan.md
ms.openlocfilehash: e044d8a086833ad94ed01267adf08469941a32a7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183728"
---
# <span data-ttu-id="9f10b-101">Set-AzApplicationInsightsPricingPlan</span><span class="sxs-lookup"><span data-stu-id="9f10b-101">Set-AzApplicationInsightsPricingPlan</span></span>

## <span data-ttu-id="9f10b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9f10b-102">SYNOPSIS</span></span>
<span data-ttu-id="9f10b-103">Árképzési terv és a napi adatmennyiség adatainak beállítása az alkalmazásbeli betekintéshez</span><span class="sxs-lookup"><span data-stu-id="9f10b-103">Set pricing plan and daily data volume information for an application insights resource</span></span>

## <span data-ttu-id="9f10b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9f10b-104">SYNTAX</span></span>

### <span data-ttu-id="9f10b-105">ComponentNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9f10b-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ResourceGroupName] <String> [-Name] <String> [-PricingPlan <String>]
 [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f10b-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f10b-106">ComponentObjectParameterSet</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-PricingPlan <String>] [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f10b-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f10b-107">ResourceIdParameterSet</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ResourceId] <String> [-PricingPlan <String>] [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9f10b-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="9f10b-108">DESCRIPTION</span></span>
<span data-ttu-id="9f10b-109">Árképzési terv és a napi adatmennyiség adatainak beállítása az alkalmazásbeli betekintéshez</span><span class="sxs-lookup"><span data-stu-id="9f10b-109">Set pricing plan and daily data volume information for an application insights resource</span></span>

## <span data-ttu-id="9f10b-110">Példák</span><span class="sxs-lookup"><span data-stu-id="9f10b-110">EXAMPLES</span></span>

### <span data-ttu-id="9f10b-111">Példa 1 az árképzési terv és a napi adatmennyiség beállítása az alkalmazási adatokhoz</span><span class="sxs-lookup"><span data-stu-id="9f10b-111">Example 1 Set pricing plan and daily data volume information for an application insights resource</span></span>
```
PS C:\> Set-AzApplicationInsightsDailyCap -ResourceGroupName "testgroup" -Name "test" -PricingPlan "Basic" -DailyCapGB 400

 Cap ResetTime StopSendNotificationWhenHitCap PricingPlan
--- --------- ------------------------------ -----------
400         0                           False Basic
```

<span data-ttu-id="9f10b-112">Az árképzési terv beállítása az "egyszerű" értékre a napi adatmennyiség sapka és a 400GB közötti választás leállításához, ha a találatok között a "teszt" az erőforrás csoportban "testgroup"</span><span class="sxs-lookup"><span data-stu-id="9f10b-112">Set the pricing plan to "Basic", set the daily data volume cap to 400GB per day and stop send notification when hit cap for resource "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="9f10b-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9f10b-113">PARAMETERS</span></span>

### <span data-ttu-id="9f10b-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="9f10b-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="9f10b-115">Az alkalmazás betekintése összetevő-objektum.</span><span class="sxs-lookup"><span data-stu-id="9f10b-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="9f10b-116">-DailyCapGB</span><span class="sxs-lookup"><span data-stu-id="9f10b-116">-DailyCapGB</span></span>
<span data-ttu-id="9f10b-117">Napi sapka.</span><span class="sxs-lookup"><span data-stu-id="9f10b-117">Daily Cap.</span></span>

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

### <span data-ttu-id="9f10b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f10b-118">-DefaultProfile</span></span>
<span data-ttu-id="9f10b-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9f10b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9f10b-120">-DisableNotificationWhenHitCap</span><span class="sxs-lookup"><span data-stu-id="9f10b-120">-DisableNotificationWhenHitCap</span></span>
<span data-ttu-id="9f10b-121">Az üzenet küldésének leállítása a találatok között.</span><span class="sxs-lookup"><span data-stu-id="9f10b-121">Stop send notification when hit cap.</span></span>

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

### <span data-ttu-id="9f10b-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9f10b-122">-Name</span></span>
<span data-ttu-id="9f10b-123">Az alkalmazás betekintési összetevőjének neve.</span><span class="sxs-lookup"><span data-stu-id="9f10b-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="9f10b-124">-PricingPlan</span><span class="sxs-lookup"><span data-stu-id="9f10b-124">-PricingPlan</span></span>
<span data-ttu-id="9f10b-125">Árképzési terv neve</span><span class="sxs-lookup"><span data-stu-id="9f10b-125">Pricing plan name.</span></span>

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

### <span data-ttu-id="9f10b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f10b-126">-ResourceGroupName</span></span>
<span data-ttu-id="9f10b-127">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="9f10b-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="9f10b-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9f10b-128">-ResourceId</span></span>
<span data-ttu-id="9f10b-129">Az alkalmazás betekintési összetevőjének erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="9f10b-129">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="9f10b-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9f10b-130">-Confirm</span></span>
<span data-ttu-id="9f10b-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9f10b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f10b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f10b-132">-WhatIf</span></span>
<span data-ttu-id="9f10b-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9f10b-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9f10b-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9f10b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f10b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f10b-135">CommonParameters</span></span>
<span data-ttu-id="9f10b-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9f10b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f10b-137">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f10b-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f10b-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9f10b-138">INPUTS</span></span>

### <span data-ttu-id="9f10b-139">Microsoft. Azure. Command. ApplicationInsights. models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="9f10b-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="9f10b-140">System. String</span><span class="sxs-lookup"><span data-stu-id="9f10b-140">System.String</span></span>

## <span data-ttu-id="9f10b-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9f10b-141">OUTPUTS</span></span>

### <span data-ttu-id="9f10b-142">Microsoft. Azure. Command. ApplicationInsights. models. PSPricingPlan</span><span class="sxs-lookup"><span data-stu-id="9f10b-142">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span></span>

## <span data-ttu-id="9f10b-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9f10b-143">NOTES</span></span>

## <span data-ttu-id="9f10b-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9f10b-144">RELATED LINKS</span></span>
