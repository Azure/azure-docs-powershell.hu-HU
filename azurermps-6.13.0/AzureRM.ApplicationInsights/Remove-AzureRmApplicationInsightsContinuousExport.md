---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/remove-azurermapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Remove-AzureRmApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Remove-AzureRmApplicationInsightsContinuousExport.md
ms.openlocfilehash: b9a26a1279b89609728837def1997ac5735ddaea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494206"
---
# <span data-ttu-id="c7022-101">Remove-AzureRmApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="c7022-101">Remove-AzureRmApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="c7022-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c7022-102">SYNOPSIS</span></span>
<span data-ttu-id="c7022-103">Cotinuous-exportálási konfiguráció eltávolítása egy alkalmazásbeli betekintést tartalmazó erőforrásban</span><span class="sxs-lookup"><span data-stu-id="c7022-103">Remove a cotinuous export configuration in an application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7022-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c7022-104">SYNTAX</span></span>

### <span data-ttu-id="c7022-105">ComponentNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c7022-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzureRmApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String>
 [-ExportId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c7022-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7022-106">ComponentObjectParameterSet</span></span>
```
Remove-AzureRmApplicationInsightsContinuousExport
 [-ApplicationInsightsComponent] <PSApplicationInsightsComponent> [-ExportId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7022-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7022-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmApplicationInsightsContinuousExport [-ResourceId] <String> [-ExportId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7022-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="c7022-108">DESCRIPTION</span></span>
<span data-ttu-id="c7022-109">Cotinuous-exportálási konfiguráció eltávolítása egy alkalmazásbeli betekintést tartalmazó erőforrásban</span><span class="sxs-lookup"><span data-stu-id="c7022-109">Remove a cotinuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="c7022-110">Példák</span><span class="sxs-lookup"><span data-stu-id="c7022-110">EXAMPLES</span></span>

### <span data-ttu-id="c7022-111">Példa 1 cotinuous-exportálási konfiguráció eltávolítása egy alkalmazásbeli betekintést tartalmazó erőforrásban</span><span class="sxs-lookup"><span data-stu-id="c7022-111">Example 1 Remove a cotinuous export configuration in an application insights resource</span></span>
```
PS C:\> Remove-AzureRmApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test" -ExportId "uGOoki0jQsyEs3IdQ83Q4QsNr4=" -PassThru
True
```

<span data-ttu-id="c7022-112">A folyamatos exportálási konfiguráció eltávolítása a "teszt" erőforráscsoport "testgroup" erőforráscsoporthoz tartozó "uGOoki0jQsyEs3IdQ83Q4QsNr4 =" exportálási azonosítóval</span><span class="sxs-lookup"><span data-stu-id="c7022-112">Remove application insights continuous export configuration with export id "uGOoki0jQsyEs3IdQ83Q4QsNr4=" for resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="c7022-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c7022-113">PARAMETERS</span></span>

### <span data-ttu-id="c7022-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="c7022-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="c7022-115">Az alkalmazás betekintése összetevő-objektum.</span><span class="sxs-lookup"><span data-stu-id="c7022-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="c7022-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7022-116">-DefaultProfile</span></span>
<span data-ttu-id="c7022-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c7022-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7022-118">-ExportId</span><span class="sxs-lookup"><span data-stu-id="c7022-118">-ExportId</span></span>
<span data-ttu-id="c7022-119">Az alkalmazás betekintést nyújt a folyamatos exportálási AZONOSÍTÓra.</span><span class="sxs-lookup"><span data-stu-id="c7022-119">Application Insights Continuous Export ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7022-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c7022-120">-Name</span></span>
<span data-ttu-id="c7022-121">Az alkalmazás betekintési összetevőjének neve.</span><span class="sxs-lookup"><span data-stu-id="c7022-121">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="c7022-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c7022-122">-PassThru</span></span>
<span data-ttu-id="c7022-123">Ha a megadott művelet sikeres, akkor a True Write True értékre vált.</span><span class="sxs-lookup"><span data-stu-id="c7022-123">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="c7022-124">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="c7022-124">This parameter is optional.</span></span> <span data-ttu-id="c7022-125">Az alapértelmezett érték a hamis.</span><span class="sxs-lookup"><span data-stu-id="c7022-125">Default value is false.</span></span>

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

### <span data-ttu-id="c7022-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7022-126">-ResourceGroupName</span></span>
<span data-ttu-id="c7022-127">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="c7022-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="c7022-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c7022-128">-ResourceId</span></span>
<span data-ttu-id="c7022-129">Az alkalmazás betekintési összetevőjének erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="c7022-129">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="c7022-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c7022-130">-Confirm</span></span>
<span data-ttu-id="c7022-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c7022-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7022-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7022-132">-WhatIf</span></span>
<span data-ttu-id="c7022-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c7022-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7022-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c7022-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7022-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7022-135">CommonParameters</span></span>
<span data-ttu-id="c7022-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c7022-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7022-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7022-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7022-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c7022-138">INPUTS</span></span>

### <span data-ttu-id="c7022-139">Microsoft. Azure. Command. ApplicationInsights. models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="c7022-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>
<span data-ttu-id="c7022-140">Paraméterek: ApplicationInsightsComponent (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c7022-140">Parameters: ApplicationInsightsComponent (ByValue)</span></span>

### <span data-ttu-id="c7022-141">System. String</span><span class="sxs-lookup"><span data-stu-id="c7022-141">System.String</span></span>

## <span data-ttu-id="c7022-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c7022-142">OUTPUTS</span></span>

### <span data-ttu-id="c7022-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c7022-143">System.Boolean</span></span>

## <span data-ttu-id="c7022-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c7022-144">NOTES</span></span>

## <span data-ttu-id="c7022-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c7022-145">RELATED LINKS</span></span>
