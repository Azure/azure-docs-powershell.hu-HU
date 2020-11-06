---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/set-azurermapplicationinsightsdailycap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Set-AzureRmApplicationInsightsDailyCap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Set-AzureRmApplicationInsightsDailyCap.md
ms.openlocfilehash: 7b47576c0fd506831d8e48201d39bd66fec72032
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494204"
---
# <span data-ttu-id="d15f2-101">Set-AzureRmApplicationInsightsDailyCap</span><span class="sxs-lookup"><span data-stu-id="d15f2-101">Set-AzureRmApplicationInsightsDailyCap</span></span>

## <span data-ttu-id="d15f2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d15f2-102">SYNOPSIS</span></span>
<span data-ttu-id="d15f2-103">A Daily Data Volume Cap beállítása az alkalmazásbeli betekintések erőforrásához</span><span class="sxs-lookup"><span data-stu-id="d15f2-103">Set daily data volume cap for an application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d15f2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d15f2-104">SYNTAX</span></span>

### <span data-ttu-id="d15f2-105">ComponentNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d15f2-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzureRmApplicationInsightsDailyCap [-ResourceGroupName] <String> [-Name] <String> [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d15f2-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d15f2-106">ComponentObjectParameterSet</span></span>
```
Set-AzureRmApplicationInsightsDailyCap [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d15f2-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d15f2-107">ResourceIdParameterSet</span></span>
```
Set-AzureRmApplicationInsightsDailyCap [-ResourceId] <String> [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d15f2-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="d15f2-108">DESCRIPTION</span></span>
<span data-ttu-id="d15f2-109">A Daily Data Volume Cap beállítása az alkalmazásbeli betekintések erőforrásához</span><span class="sxs-lookup"><span data-stu-id="d15f2-109">Set daily data volume cap for an application insights resource</span></span>

## <span data-ttu-id="d15f2-110">Példák</span><span class="sxs-lookup"><span data-stu-id="d15f2-110">EXAMPLES</span></span>

### <span data-ttu-id="d15f2-111">Példa 1 a napi adatmennyiség sapka beállítása az alkalmazásbeli betekintések erőforráshoz</span><span class="sxs-lookup"><span data-stu-id="d15f2-111">Example 1 Set daily data volume cap for an application insights resource</span></span>
```
PS C:\> Set-AzureRmApplicationInsightsDailyCap -ResourceGroupName "testgroup" -Name "test" -DailyCapGB 400
 -DisableNotificationWhenHitCap

 Cap ResetTime StopSendNotificationWhenHitCap
--- --------- ------------------------------
400         0                           True
```

<span data-ttu-id="d15f2-112">A napi adatvolumeni sapka beállítása napi 400GB és az üzenet küldésének leállítása az "ellenőrzés" erőforráscsoport "testgroup" erőforráscsoport esetén</span><span class="sxs-lookup"><span data-stu-id="d15f2-112">Set the daily data volumen cap to 400GB per day and stop send notification when hit cap for resource "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="d15f2-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d15f2-113">PARAMETERS</span></span>

### <span data-ttu-id="d15f2-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="d15f2-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="d15f2-115">Az alkalmazás betekintése összetevő-objektum.</span><span class="sxs-lookup"><span data-stu-id="d15f2-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="d15f2-116">-DailyCapGB</span><span class="sxs-lookup"><span data-stu-id="d15f2-116">-DailyCapGB</span></span>
<span data-ttu-id="d15f2-117">Napi sapka.</span><span class="sxs-lookup"><span data-stu-id="d15f2-117">Daily Cap.</span></span>

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

### <span data-ttu-id="d15f2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d15f2-118">-DefaultProfile</span></span>
<span data-ttu-id="d15f2-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d15f2-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d15f2-120">-DisableNotificationWhenHitCap</span><span class="sxs-lookup"><span data-stu-id="d15f2-120">-DisableNotificationWhenHitCap</span></span>
<span data-ttu-id="d15f2-121">Az üzenet küldésének leállítása a találatok között.</span><span class="sxs-lookup"><span data-stu-id="d15f2-121">Stop send notification when hit cap.</span></span>

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

### <span data-ttu-id="d15f2-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d15f2-122">-Name</span></span>
<span data-ttu-id="d15f2-123">Az alkalmazás betekintési összetevőjének neve.</span><span class="sxs-lookup"><span data-stu-id="d15f2-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="d15f2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d15f2-124">-ResourceGroupName</span></span>
<span data-ttu-id="d15f2-125">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="d15f2-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="d15f2-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d15f2-126">-ResourceId</span></span>
<span data-ttu-id="d15f2-127">Az alkalmazás betekintési összetevőjének erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d15f2-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="d15f2-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d15f2-128">-Confirm</span></span>
<span data-ttu-id="d15f2-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d15f2-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d15f2-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d15f2-130">-WhatIf</span></span>
<span data-ttu-id="d15f2-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d15f2-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d15f2-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d15f2-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d15f2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d15f2-133">CommonParameters</span></span>
<span data-ttu-id="d15f2-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d15f2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d15f2-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d15f2-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d15f2-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d15f2-136">INPUTS</span></span>

### <span data-ttu-id="d15f2-137">Microsoft. Azure. Command. ApplicationInsights. models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="d15f2-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>
<span data-ttu-id="d15f2-138">Paraméterek: ApplicationInsightsComponent (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d15f2-138">Parameters: ApplicationInsightsComponent (ByValue)</span></span>

### <span data-ttu-id="d15f2-139">System. String</span><span class="sxs-lookup"><span data-stu-id="d15f2-139">System.String</span></span>

## <span data-ttu-id="d15f2-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d15f2-140">OUTPUTS</span></span>

### <span data-ttu-id="d15f2-141">Microsoft. Azure. Command. ApplicationInsights. models. PSPricingPlan</span><span class="sxs-lookup"><span data-stu-id="d15f2-141">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span></span>

## <span data-ttu-id="d15f2-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d15f2-142">NOTES</span></span>

## <span data-ttu-id="d15f2-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d15f2-143">RELATED LINKS</span></span>
