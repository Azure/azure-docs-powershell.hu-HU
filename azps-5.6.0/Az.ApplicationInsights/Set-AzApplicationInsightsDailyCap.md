---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/powershell/module/az.applicationinsights/set-azapplicationinsightsdailycap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsDailyCap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsDailyCap.md
ms.openlocfilehash: ce4c9d8fd297b53eb628ffcc32ad9479e0647dd6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014326"
---
# <span data-ttu-id="406ac-101">Set-AzApplicationInsightsDailyCap</span><span class="sxs-lookup"><span data-stu-id="406ac-101">Set-AzApplicationInsightsDailyCap</span></span>

## <span data-ttu-id="406ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="406ac-102">SYNOPSIS</span></span>
<span data-ttu-id="406ac-103">Napi adatmennyiség-mennyiség beállítása alkalmazásstatószám-erőforráshoz</span><span class="sxs-lookup"><span data-stu-id="406ac-103">Set daily data volume cap for an application insights resource</span></span>

## <span data-ttu-id="406ac-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="406ac-104">SYNTAX</span></span>

### <span data-ttu-id="406ac-105">ComponentNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="406ac-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzApplicationInsightsDailyCap [-ResourceGroupName] <String> [-Name] <String> [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="406ac-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="406ac-106">ComponentObjectParameterSet</span></span>
```
Set-AzApplicationInsightsDailyCap [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="406ac-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="406ac-107">ResourceIdParameterSet</span></span>
```
Set-AzApplicationInsightsDailyCap [-ResourceId] <String> [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="406ac-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="406ac-108">DESCRIPTION</span></span>
<span data-ttu-id="406ac-109">Napi adatmennyiség-mennyiség beállítása alkalmazásstatószám-erőforráshoz</span><span class="sxs-lookup"><span data-stu-id="406ac-109">Set daily data volume cap for an application insights resource</span></span>

## <span data-ttu-id="406ac-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="406ac-110">EXAMPLES</span></span>

### <span data-ttu-id="406ac-111">1. példa: Napi adatmennyiség-mennyiség beállítása alkalmazásstatószám-erőforráshoz</span><span class="sxs-lookup"><span data-stu-id="406ac-111">Example 1 Set daily data volume cap for an application insights resource</span></span>
```
PS C:\> Set-AzApplicationInsightsDailyCap -ResourceGroupName "testgroup" -Name "test" -DailyCapGB 400
 -DisableNotificationWhenHitCap

 Cap ResetTime StopSendNotificationWhenHitCap
--- --------- ------------------------------
400         0                           True
```

<span data-ttu-id="406ac-112">Állítsa a napi adatmennyiség-kapacitást 400 GB-ra naponta, és állítsa le az értesítés elküldését, amikor az erőforrás"teszt" beállításnál az erőforráscsoport "tesztcsoport" beállításában leállítja az értesítés elküldését.</span><span class="sxs-lookup"><span data-stu-id="406ac-112">Set the daily data volume cap to 400GB per day and stop send notification when hit cap for resource "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="406ac-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="406ac-113">PARAMETERS</span></span>

### <span data-ttu-id="406ac-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="406ac-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="406ac-115">Application Insights összetevő-objektum.</span><span class="sxs-lookup"><span data-stu-id="406ac-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="406ac-116">-DailyCapGB</span><span class="sxs-lookup"><span data-stu-id="406ac-116">-DailyCapGB</span></span>
<span data-ttu-id="406ac-117">Napi cap.</span><span class="sxs-lookup"><span data-stu-id="406ac-117">Daily Cap.</span></span>

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

### <span data-ttu-id="406ac-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="406ac-118">-DefaultProfile</span></span>
<span data-ttu-id="406ac-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="406ac-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="406ac-120">-DisableNotificationWhenTiltásaCap</span><span class="sxs-lookup"><span data-stu-id="406ac-120">-DisableNotificationWhenHitCap</span></span>
<span data-ttu-id="406ac-121">A küldésről szóló értesítés leállítása, ha a találati nagybetű megjelenik.</span><span class="sxs-lookup"><span data-stu-id="406ac-121">Stop send notification when hit cap.</span></span>

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

### <span data-ttu-id="406ac-122">-Name</span><span class="sxs-lookup"><span data-stu-id="406ac-122">-Name</span></span>
<span data-ttu-id="406ac-123">Application Insights összetevő neve.</span><span class="sxs-lookup"><span data-stu-id="406ac-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="406ac-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="406ac-124">-ResourceGroupName</span></span>
<span data-ttu-id="406ac-125">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="406ac-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="406ac-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="406ac-126">-ResourceId</span></span>
<span data-ttu-id="406ac-127">Application Insights összetevő erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="406ac-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="406ac-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="406ac-128">-Confirm</span></span>
<span data-ttu-id="406ac-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="406ac-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="406ac-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="406ac-130">-WhatIf</span></span>
<span data-ttu-id="406ac-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="406ac-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="406ac-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="406ac-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="406ac-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="406ac-133">CommonParameters</span></span>
<span data-ttu-id="406ac-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="406ac-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="406ac-135">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="406ac-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="406ac-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="406ac-136">INPUTS</span></span>

### <span data-ttu-id="406ac-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="406ac-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="406ac-138">System.String</span><span class="sxs-lookup"><span data-stu-id="406ac-138">System.String</span></span>

## <span data-ttu-id="406ac-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="406ac-139">OUTPUTS</span></span>

### <span data-ttu-id="406ac-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span><span class="sxs-lookup"><span data-stu-id="406ac-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span></span>

## <span data-ttu-id="406ac-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="406ac-141">NOTES</span></span>

## <span data-ttu-id="406ac-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="406ac-142">RELATED LINKS</span></span>
