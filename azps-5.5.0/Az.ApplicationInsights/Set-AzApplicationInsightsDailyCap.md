---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/set-azapplicationinsightsdailycap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsDailyCap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsDailyCap.md
ms.openlocfilehash: f13408e23dcf8f1db9de2e19fc05d899b712a783
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100168474"
---
# <span data-ttu-id="18dc0-101">Set-AzApplicationInsightsDailyCap</span><span class="sxs-lookup"><span data-stu-id="18dc0-101">Set-AzApplicationInsightsDailyCap</span></span>

## <span data-ttu-id="18dc0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18dc0-102">SYNOPSIS</span></span>
<span data-ttu-id="18dc0-103">Napi adatmennyiség-mennyiség beállítása alkalmazásstatószám-erőforráshoz</span><span class="sxs-lookup"><span data-stu-id="18dc0-103">Set daily data volume cap for an application insights resource</span></span>

## <span data-ttu-id="18dc0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="18dc0-104">SYNTAX</span></span>

### <span data-ttu-id="18dc0-105">ComponentNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="18dc0-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzApplicationInsightsDailyCap [-ResourceGroupName] <String> [-Name] <String> [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="18dc0-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="18dc0-106">ComponentObjectParameterSet</span></span>
```
Set-AzApplicationInsightsDailyCap [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18dc0-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="18dc0-107">ResourceIdParameterSet</span></span>
```
Set-AzApplicationInsightsDailyCap [-ResourceId] <String> [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="18dc0-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="18dc0-108">DESCRIPTION</span></span>
<span data-ttu-id="18dc0-109">Napi adatmennyiség-mennyiség beállítása alkalmazásstatószám-erőforráshoz</span><span class="sxs-lookup"><span data-stu-id="18dc0-109">Set daily data volume cap for an application insights resource</span></span>

## <span data-ttu-id="18dc0-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="18dc0-110">EXAMPLES</span></span>

### <span data-ttu-id="18dc0-111">1. példa: Napi adatmennyiség-mennyiség beállítása alkalmazásstatószám-erőforráshoz</span><span class="sxs-lookup"><span data-stu-id="18dc0-111">Example 1 Set daily data volume cap for an application insights resource</span></span>
```
PS C:\> Set-AzApplicationInsightsDailyCap -ResourceGroupName "testgroup" -Name "test" -DailyCapGB 400
 -DisableNotificationWhenHitCap

 Cap ResetTime StopSendNotificationWhenHitCap
--- --------- ------------------------------
400         0                           True
```

<span data-ttu-id="18dc0-112">Állítsa a napi adatmennyiség-kapacitást napi 400 GB-osra, és állítsa le az értesítés elküldését, amikor az erőforrás"teszt" beállításnál az erőforráscsoport "tesztcsoport" beállításában az erőforrás-kapacitást nyomja le.</span><span class="sxs-lookup"><span data-stu-id="18dc0-112">Set the daily data volume cap to 400GB per day and stop send notification when hit cap for resource "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="18dc0-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="18dc0-113">PARAMETERS</span></span>

### <span data-ttu-id="18dc0-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="18dc0-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="18dc0-115">Application Insights összetevő-objektum.</span><span class="sxs-lookup"><span data-stu-id="18dc0-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="18dc0-116">-DailyCapGB</span><span class="sxs-lookup"><span data-stu-id="18dc0-116">-DailyCapGB</span></span>
<span data-ttu-id="18dc0-117">Napi cap.</span><span class="sxs-lookup"><span data-stu-id="18dc0-117">Daily Cap.</span></span>

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

### <span data-ttu-id="18dc0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18dc0-118">-DefaultProfile</span></span>
<span data-ttu-id="18dc0-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="18dc0-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18dc0-120">-DisableNotificationWhenTiltásaCap</span><span class="sxs-lookup"><span data-stu-id="18dc0-120">-DisableNotificationWhenHitCap</span></span>
<span data-ttu-id="18dc0-121">A küldésről szóló értesítés leállítása, ha a találati nagybetű megjelenik.</span><span class="sxs-lookup"><span data-stu-id="18dc0-121">Stop send notification when hit cap.</span></span>

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

### <span data-ttu-id="18dc0-122">-Name</span><span class="sxs-lookup"><span data-stu-id="18dc0-122">-Name</span></span>
<span data-ttu-id="18dc0-123">Application Insights összetevő neve.</span><span class="sxs-lookup"><span data-stu-id="18dc0-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="18dc0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18dc0-124">-ResourceGroupName</span></span>
<span data-ttu-id="18dc0-125">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="18dc0-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="18dc0-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="18dc0-126">-ResourceId</span></span>
<span data-ttu-id="18dc0-127">Application Insights összetevő erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="18dc0-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="18dc0-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="18dc0-128">-Confirm</span></span>
<span data-ttu-id="18dc0-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="18dc0-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18dc0-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18dc0-130">-WhatIf</span></span>
<span data-ttu-id="18dc0-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="18dc0-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="18dc0-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="18dc0-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18dc0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18dc0-133">CommonParameters</span></span>
<span data-ttu-id="18dc0-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18dc0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18dc0-135">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18dc0-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18dc0-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="18dc0-136">INPUTS</span></span>

### <span data-ttu-id="18dc0-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="18dc0-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="18dc0-138">System.String</span><span class="sxs-lookup"><span data-stu-id="18dc0-138">System.String</span></span>

## <span data-ttu-id="18dc0-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="18dc0-139">OUTPUTS</span></span>

### <span data-ttu-id="18dc0-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span><span class="sxs-lookup"><span data-stu-id="18dc0-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span></span>

## <span data-ttu-id="18dc0-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="18dc0-141">NOTES</span></span>

## <span data-ttu-id="18dc0-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="18dc0-142">RELATED LINKS</span></span>
