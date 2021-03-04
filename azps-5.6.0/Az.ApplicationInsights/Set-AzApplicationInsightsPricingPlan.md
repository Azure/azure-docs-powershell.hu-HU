---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/powershell/module/az.applicationinsights/set-azapplicationinsightspricingplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsPricingPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsPricingPlan.md
ms.openlocfilehash: 7f730a59b740b061406f2ba14ccf76fe660aea14
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935410"
---
# <span data-ttu-id="f2234-101">Set-AzApplicationInsightsPricingPlan</span><span class="sxs-lookup"><span data-stu-id="f2234-101">Set-AzApplicationInsightsPricingPlan</span></span>

## <span data-ttu-id="f2234-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2234-102">SYNOPSIS</span></span>
<span data-ttu-id="f2234-103">Árazási csomag és napi adatmennyiség-információk beállítása alkalmazásstatószám-erőforráshoz</span><span class="sxs-lookup"><span data-stu-id="f2234-103">Set pricing plan and daily data volume information for an application insights resource</span></span>

## <span data-ttu-id="f2234-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f2234-104">SYNTAX</span></span>

### <span data-ttu-id="f2234-105">ComponentNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f2234-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ResourceGroupName] <String> [-Name] <String> [-PricingPlan <String>]
 [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2234-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f2234-106">ComponentObjectParameterSet</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-PricingPlan <String>] [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2234-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f2234-107">ResourceIdParameterSet</span></span>
```
Set-AzApplicationInsightsPricingPlan [-ResourceId] <String> [-PricingPlan <String>] [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f2234-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f2234-108">DESCRIPTION</span></span>
<span data-ttu-id="f2234-109">Megszabhat árcsomagot és napi adatmennyiség-adatokat egy alkalmazásstatószám-erőforráshoz.</span><span class="sxs-lookup"><span data-stu-id="f2234-109">Set pricing plan and daily data volume information for an application insights resource.</span></span>
<span data-ttu-id="f2234-110">A 2018 áprilisa után létrehozott alkalmazásstatikát a következő parancsmag nem tudja beállítani: https://docs.microsoft.com/azure/azure-monitor/app/pricing#legacy-enterprise-per-node-pricing-tier</span><span class="sxs-lookup"><span data-stu-id="f2234-110">Pricing plan of application insights created after April 2018 cannot be set by this cmdlet: https://docs.microsoft.com/azure/azure-monitor/app/pricing#legacy-enterprise-per-node-pricing-tier</span></span>

## <span data-ttu-id="f2234-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f2234-111">EXAMPLES</span></span>

### <span data-ttu-id="f2234-112">1. példa: Az árcsomag és a napi adatok mennyiségének beállítása egy alkalmazásstatószám-erőforráshoz</span><span class="sxs-lookup"><span data-stu-id="f2234-112">Example 1 Set pricing plan and daily data volume information for an application insights resource</span></span>
```
PS C:\> Set-AzApplicationInsightsDailyCap -ResourceGroupName "testgroup" -Name "test" -PricingPlan "Basic" -DailyCapGB 400

 Cap ResetTime StopSendNotificationWhenHitCap PricingPlan
--- --------- ------------------------------ -----------
400         0                           False Basic
```

<span data-ttu-id="f2234-113">Állítsa az árcsomagot "Alapszintű" csomagra, állítsa a napi adatmennyiség-kapacitást 400 GB/nap-ra, és állítsa le az értesítés elküldését, amikor a "test" erőforráscsoport "teszt" erőforráscsoportban a "tesztcsoport" erőforrás-kapacitást nyomja le.</span><span class="sxs-lookup"><span data-stu-id="f2234-113">Set the pricing plan to "Basic", set the daily data volume cap to 400GB per day and stop send notification when hit cap for resource "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="f2234-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f2234-114">PARAMETERS</span></span>

### <span data-ttu-id="f2234-115">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="f2234-115">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="f2234-116">Application Insights összetevő-objektum.</span><span class="sxs-lookup"><span data-stu-id="f2234-116">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="f2234-117">-DailyCapGB</span><span class="sxs-lookup"><span data-stu-id="f2234-117">-DailyCapGB</span></span>
<span data-ttu-id="f2234-118">Napi cap.</span><span class="sxs-lookup"><span data-stu-id="f2234-118">Daily Cap.</span></span>

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

### <span data-ttu-id="f2234-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2234-119">-DefaultProfile</span></span>
<span data-ttu-id="f2234-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f2234-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2234-121">-DisableNotificationWhenTiltásaCap</span><span class="sxs-lookup"><span data-stu-id="f2234-121">-DisableNotificationWhenHitCap</span></span>
<span data-ttu-id="f2234-122">A küldésről szóló értesítés leállítása, ha a találati nagybetű megjelenik.</span><span class="sxs-lookup"><span data-stu-id="f2234-122">Stop send notification when hit cap.</span></span>

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

### <span data-ttu-id="f2234-123">-Name</span><span class="sxs-lookup"><span data-stu-id="f2234-123">-Name</span></span>
<span data-ttu-id="f2234-124">Application Insights összetevő neve.</span><span class="sxs-lookup"><span data-stu-id="f2234-124">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="f2234-125">-PricingPlan</span><span class="sxs-lookup"><span data-stu-id="f2234-125">-PricingPlan</span></span>
<span data-ttu-id="f2234-126">Árazási csomag neve.</span><span class="sxs-lookup"><span data-stu-id="f2234-126">Pricing plan name.</span></span>

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

### <span data-ttu-id="f2234-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2234-127">-ResourceGroupName</span></span>
<span data-ttu-id="f2234-128">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f2234-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="f2234-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f2234-129">-ResourceId</span></span>
<span data-ttu-id="f2234-130">Application Insights összetevő erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f2234-130">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="f2234-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f2234-131">-Confirm</span></span>
<span data-ttu-id="f2234-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f2234-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2234-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2234-133">-WhatIf</span></span>
<span data-ttu-id="f2234-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f2234-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f2234-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f2234-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2234-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2234-136">CommonParameters</span></span>
<span data-ttu-id="f2234-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2234-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2234-138">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2234-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2234-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f2234-139">INPUTS</span></span>

### <span data-ttu-id="f2234-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="f2234-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="f2234-141">System.String</span><span class="sxs-lookup"><span data-stu-id="f2234-141">System.String</span></span>

## <span data-ttu-id="f2234-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f2234-142">OUTPUTS</span></span>

### <span data-ttu-id="f2234-143">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span><span class="sxs-lookup"><span data-stu-id="f2234-143">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span></span>

## <span data-ttu-id="f2234-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f2234-144">NOTES</span></span>

## <span data-ttu-id="f2234-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f2234-145">RELATED LINKS</span></span>
