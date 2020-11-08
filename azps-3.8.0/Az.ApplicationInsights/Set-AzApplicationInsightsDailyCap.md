---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/set-azapplicationinsightsdailycap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsDailyCap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsDailyCap.md
ms.openlocfilehash: f13408e23dcf8f1db9de2e19fc05d899b712a783
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012805"
---
# <span data-ttu-id="74bcc-101">Set-AzApplicationInsightsDailyCap</span><span class="sxs-lookup"><span data-stu-id="74bcc-101">Set-AzApplicationInsightsDailyCap</span></span>

## <span data-ttu-id="74bcc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="74bcc-102">SYNOPSIS</span></span>
<span data-ttu-id="74bcc-103">A Daily Data Volume Cap beállítása az alkalmazásbeli betekintések erőforrásához</span><span class="sxs-lookup"><span data-stu-id="74bcc-103">Set daily data volume cap for an application insights resource</span></span>

## <span data-ttu-id="74bcc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="74bcc-104">SYNTAX</span></span>

### <span data-ttu-id="74bcc-105">ComponentNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="74bcc-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzApplicationInsightsDailyCap [-ResourceGroupName] <String> [-Name] <String> [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="74bcc-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="74bcc-106">ComponentObjectParameterSet</span></span>
```
Set-AzApplicationInsightsDailyCap [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-DailyCapGB <Double>] [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74bcc-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="74bcc-107">ResourceIdParameterSet</span></span>
```
Set-AzApplicationInsightsDailyCap [-ResourceId] <String> [-DailyCapGB <Double>]
 [-DisableNotificationWhenHitCap] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="74bcc-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="74bcc-108">DESCRIPTION</span></span>
<span data-ttu-id="74bcc-109">A Daily Data Volume Cap beállítása az alkalmazásbeli betekintések erőforrásához</span><span class="sxs-lookup"><span data-stu-id="74bcc-109">Set daily data volume cap for an application insights resource</span></span>

## <span data-ttu-id="74bcc-110">Példák</span><span class="sxs-lookup"><span data-stu-id="74bcc-110">EXAMPLES</span></span>

### <span data-ttu-id="74bcc-111">Példa 1 a napi adatmennyiség sapka beállítása az alkalmazásbeli betekintések erőforráshoz</span><span class="sxs-lookup"><span data-stu-id="74bcc-111">Example 1 Set daily data volume cap for an application insights resource</span></span>
```
PS C:\> Set-AzApplicationInsightsDailyCap -ResourceGroupName "testgroup" -Name "test" -DailyCapGB 400
 -DisableNotificationWhenHitCap

 Cap ResetTime StopSendNotificationWhenHitCap
--- --------- ------------------------------
400         0                           True
```

<span data-ttu-id="74bcc-112">Állítsa be a napi adatmennyiség kupakját 400GB naponta, és az üzenet elküldése "teszt" az erőforrás csoport "testgroup" erőforráscsoport esetén</span><span class="sxs-lookup"><span data-stu-id="74bcc-112">Set the daily data volume cap to 400GB per day and stop send notification when hit cap for resource "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="74bcc-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="74bcc-113">PARAMETERS</span></span>

### <span data-ttu-id="74bcc-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="74bcc-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="74bcc-115">Az alkalmazás betekintése összetevő-objektum.</span><span class="sxs-lookup"><span data-stu-id="74bcc-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="74bcc-116">-DailyCapGB</span><span class="sxs-lookup"><span data-stu-id="74bcc-116">-DailyCapGB</span></span>
<span data-ttu-id="74bcc-117">Napi sapka.</span><span class="sxs-lookup"><span data-stu-id="74bcc-117">Daily Cap.</span></span>

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

### <span data-ttu-id="74bcc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74bcc-118">-DefaultProfile</span></span>
<span data-ttu-id="74bcc-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="74bcc-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74bcc-120">-DisableNotificationWhenHitCap</span><span class="sxs-lookup"><span data-stu-id="74bcc-120">-DisableNotificationWhenHitCap</span></span>
<span data-ttu-id="74bcc-121">Az üzenet küldésének leállítása a találatok között.</span><span class="sxs-lookup"><span data-stu-id="74bcc-121">Stop send notification when hit cap.</span></span>

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

### <span data-ttu-id="74bcc-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="74bcc-122">-Name</span></span>
<span data-ttu-id="74bcc-123">Az alkalmazás betekintési összetevőjének neve.</span><span class="sxs-lookup"><span data-stu-id="74bcc-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="74bcc-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74bcc-124">-ResourceGroupName</span></span>
<span data-ttu-id="74bcc-125">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="74bcc-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="74bcc-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="74bcc-126">-ResourceId</span></span>
<span data-ttu-id="74bcc-127">Az alkalmazás betekintési összetevőjének erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="74bcc-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="74bcc-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="74bcc-128">-Confirm</span></span>
<span data-ttu-id="74bcc-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="74bcc-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74bcc-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74bcc-130">-WhatIf</span></span>
<span data-ttu-id="74bcc-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="74bcc-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="74bcc-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="74bcc-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74bcc-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74bcc-133">CommonParameters</span></span>
<span data-ttu-id="74bcc-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="74bcc-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74bcc-135">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74bcc-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74bcc-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="74bcc-136">INPUTS</span></span>

### <span data-ttu-id="74bcc-137">Microsoft. Azure. Command. ApplicationInsights. models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="74bcc-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="74bcc-138">System. String</span><span class="sxs-lookup"><span data-stu-id="74bcc-138">System.String</span></span>

## <span data-ttu-id="74bcc-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="74bcc-139">OUTPUTS</span></span>

### <span data-ttu-id="74bcc-140">Microsoft. Azure. Command. ApplicationInsights. models. PSPricingPlan</span><span class="sxs-lookup"><span data-stu-id="74bcc-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSPricingPlan</span></span>

## <span data-ttu-id="74bcc-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="74bcc-141">NOTES</span></span>

## <span data-ttu-id="74bcc-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="74bcc-142">RELATED LINKS</span></span>
