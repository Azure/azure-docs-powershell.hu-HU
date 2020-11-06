---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/set-azurermapplicationinsightspricingplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Set-AzureRmApplicationInsightsPricingPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Set-AzureRmApplicationInsightsPricingPlan.md
ms.openlocfilehash: 03c1a556f6b3fc207fbbb612f31d172705e4f42b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494202"
---
# <span data-ttu-id="b967b-101">Set-AzureRmApplicationInsightsPricingPlan</span><span class="sxs-lookup"><span data-stu-id="b967b-101">Set-AzureRmApplicationInsightsPricingPlan</span></span>

## <span data-ttu-id="b967b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b967b-102">SYNOPSIS</span></span>
<span data-ttu-id="b967b-103">Árképzési terv és a napi adatmennyiség adatainak beállítása az alkalmazásbeli betekintéshez</span><span class="sxs-lookup"><span data-stu-id="b967b-103">Set pricing plan and daily data volume information for an applicaiton insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b967b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b967b-104">SYNTAX</span></span>

### <span data-ttu-id="b967b-105">ComponentNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b967b-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzureRmApplicationInsightsPricingPlan [-ResourceGroupName] <String> [-Name] <String>
 [-PricingPlan <String>] [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b967b-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b967b-106">ComponentObjectParameterSet</span></span>
```
Set-AzureRmApplicationInsightsPricingPlan [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-PricingPlan <String>] [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b967b-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b967b-107">ResourceIdParameterSet</span></span>
```
Set-AzureRmApplicationInsightsPricingPlan [-ResourceId] <String> [-PricingPlan <String>] [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b967b-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="b967b-108">DESCRIPTION</span></span>
<span data-ttu-id="b967b-109">Árképzési terv és a napi adatmennyiség adatainak beállítása az alkalmazásbeli betekintéshez</span><span class="sxs-lookup"><span data-stu-id="b967b-109">Set pricing plan and daily data volume information for an applicaiton insights resource</span></span>

## <span data-ttu-id="b967b-110">Példák</span><span class="sxs-lookup"><span data-stu-id="b967b-110">EXAMPLES</span></span>

### <span data-ttu-id="b967b-111">Példa 1 az árképzési terv és a napi adatmennyiség beállítása az alkalmazási adatokhoz</span><span class="sxs-lookup"><span data-stu-id="b967b-111">Example 1 Set pricing plan and daily data volume information for an applicaiton insights resource</span></span>
```
PS C:\> Set-AzureRmApplicationInsightsDailyCap -ResourceGroupName "testgroup" -Name "test" -PricingPlan "Basic" -DailyCapGB 400

 Cap ResetTime StopSendNotificationWhenHitCap PricingPlan
--- --------- ------------------------------ -----------
400         0                           False Basic
```

<span data-ttu-id="b967b-112">Az árképzési terv beállítása az "alap" értékre a napi adatok volumen a 400GB naponta és a küldési értesítés kikapcsolása az erőforrás "teszt" erőforráscsoport "testgroup" erőforráscsoport esetén</span><span class="sxs-lookup"><span data-stu-id="b967b-112">Set the pricing plan to "Basic", set the daily data volumen cap to 400GB per day and stop send notification when hit cap for resource "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="b967b-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b967b-113">PARAMETERS</span></span>

### <span data-ttu-id="b967b-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="b967b-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="b967b-115">Az alkalmazás betekintése összetevő-objektum.</span><span class="sxs-lookup"><span data-stu-id="b967b-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="b967b-116">-DailyCapGB</span><span class="sxs-lookup"><span data-stu-id="b967b-116">-DailyCapGB</span></span>
<span data-ttu-id="b967b-117">Napi sapka.</span><span class="sxs-lookup"><span data-stu-id="b967b-117">Daily Cap.</span></span>

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

### <span data-ttu-id="b967b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b967b-118">-DefaultProfile</span></span>
<span data-ttu-id="b967b-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b967b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b967b-120">-DisableNotificationWhenHitCap</span><span class="sxs-lookup"><span data-stu-id="b967b-120">-DisableNotificationWhenHitCap</span></span>
<span data-ttu-id="b967b-121">Az üzenet küldésének leállítása a találatok között.</span><span class="sxs-lookup"><span data-stu-id="b967b-121">Stop send notification when hit cap.</span></span>

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

### <span data-ttu-id="b967b-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b967b-122">-Name</span></span>
<span data-ttu-id="b967b-123">Az alkalmazás betekintési összetevőjének neve.</span><span class="sxs-lookup"><span data-stu-id="b967b-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="b967b-124">-PricingPlan</span><span class="sxs-lookup"><span data-stu-id="b967b-124">-PricingPlan</span></span>
<span data-ttu-id="b967b-125">Árképzési terv neve</span><span class="sxs-lookup"><span data-stu-id="b967b-125">Pricing plan name.</span></span>

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

### <span data-ttu-id="b967b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b967b-126">-ResourceGroupName</span></span>
<span data-ttu-id="b967b-127">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="b967b-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="b967b-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b967b-128">-ResourceId</span></span>
<span data-ttu-id="b967b-129">Az alkalmazás betekintési összetevőjének erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b967b-129">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="b967b-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b967b-130">-Confirm</span></span>
<span data-ttu-id="b967b-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b967b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b967b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b967b-132">-WhatIf</span></span>
<span data-ttu-id="b967b-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b967b-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b967b-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b967b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b967b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b967b-135">CommonParameters</span></span>
<span data-ttu-id="b967b-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b967b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b967b-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b967b-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b967b-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b967b-138">INPUTS</span></span>

### <span data-ttu-id="b967b-139">Microsoft. Azure. Command. ApplicationInsights. models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="b967b-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>
<span data-ttu-id="b967b-140">Paraméterek: ApplicationInsightsComponent (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b967b-140">Parameters: ApplicationInsightsComponent (ByValue)</span></span>

### <span data-ttu-id="b967b-141">System. String</span><span class="sxs-lookup"><span data-stu-id="b967b-141">System.String</span></span>

## <span data-ttu-id="b967b-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b967b-142">OUTPUTS</span></span>

### <span data-ttu-id="b967b-143">Microsoft. Azure. Command. ApplicationInsights. models. PSPricingPlan</span><span class="sxs-lookup"><span data-stu-id="b967b-143">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span></span>

## <span data-ttu-id="b967b-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b967b-144">NOTES</span></span>

## <span data-ttu-id="b967b-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b967b-145">RELATED LINKS</span></span>
