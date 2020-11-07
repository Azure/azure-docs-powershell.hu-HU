---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/remove-azapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsContinuousExport.md
ms.openlocfilehash: 0265a273cb575d2cc3a165afae8f7a2090499cdc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671655"
---
# <span data-ttu-id="f64aa-101">Remove-AzApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="f64aa-101">Remove-AzApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="f64aa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f64aa-102">SYNOPSIS</span></span>
<span data-ttu-id="f64aa-103">Cotinuous-exportálási konfiguráció eltávolítása egy alkalmazásbeli betekintést tartalmazó erőforrásban</span><span class="sxs-lookup"><span data-stu-id="f64aa-103">Remove a cotinuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="f64aa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f64aa-104">SYNTAX</span></span>

### <span data-ttu-id="f64aa-105">ComponentNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f64aa-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String>
 [-ExportId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f64aa-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f64aa-106">ComponentObjectParameterSet</span></span>
```
Remove-AzApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-ExportId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f64aa-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f64aa-107">ResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsightsContinuousExport [-ResourceId] <String> [-ExportId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f64aa-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="f64aa-108">DESCRIPTION</span></span>
<span data-ttu-id="f64aa-109">Cotinuous-exportálási konfiguráció eltávolítása egy alkalmazásbeli betekintést tartalmazó erőforrásban</span><span class="sxs-lookup"><span data-stu-id="f64aa-109">Remove a cotinuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="f64aa-110">Példák</span><span class="sxs-lookup"><span data-stu-id="f64aa-110">EXAMPLES</span></span>

### <span data-ttu-id="f64aa-111">Példa 1 cotinuous-exportálási konfiguráció eltávolítása egy alkalmazásbeli betekintést tartalmazó erőforrásban</span><span class="sxs-lookup"><span data-stu-id="f64aa-111">Example 1 Remove a cotinuous export configuration in an application insights resource</span></span>
```
PS C:\> Remove-AzApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test" -ExportId "uGOoki0jQsyEs3IdQ83Q4QsNr4=" -PassThru
True
```

<span data-ttu-id="f64aa-112">A folyamatos exportálási konfiguráció eltávolítása a "teszt" erőforráscsoport "testgroup" erőforráscsoporthoz tartozó "uGOoki0jQsyEs3IdQ83Q4QsNr4 =" exportálási azonosítóval</span><span class="sxs-lookup"><span data-stu-id="f64aa-112">Remove application insights continuous export configuration with export id "uGOoki0jQsyEs3IdQ83Q4QsNr4=" for resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="f64aa-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f64aa-113">PARAMETERS</span></span>

### <span data-ttu-id="f64aa-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="f64aa-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="f64aa-115">Az alkalmazás betekintése összetevő-objektum.</span><span class="sxs-lookup"><span data-stu-id="f64aa-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="f64aa-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f64aa-116">-DefaultProfile</span></span>
<span data-ttu-id="f64aa-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f64aa-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f64aa-118">-ExportId</span><span class="sxs-lookup"><span data-stu-id="f64aa-118">-ExportId</span></span>
<span data-ttu-id="f64aa-119">Az alkalmazás betekintést nyújt a folyamatos exportálási AZONOSÍTÓra.</span><span class="sxs-lookup"><span data-stu-id="f64aa-119">Application Insights Continuous Export ID.</span></span>

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

### <span data-ttu-id="f64aa-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f64aa-120">-Name</span></span>
<span data-ttu-id="f64aa-121">Az alkalmazás betekintési összetevőjének neve.</span><span class="sxs-lookup"><span data-stu-id="f64aa-121">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="f64aa-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f64aa-122">-PassThru</span></span>
<span data-ttu-id="f64aa-123">Ha a megadott művelet sikeres, akkor a True Write True értékre vált.</span><span class="sxs-lookup"><span data-stu-id="f64aa-123">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="f64aa-124">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="f64aa-124">This parameter is optional.</span></span> <span data-ttu-id="f64aa-125">Az alapértelmezett érték a hamis.</span><span class="sxs-lookup"><span data-stu-id="f64aa-125">Default value is false.</span></span>

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

### <span data-ttu-id="f64aa-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f64aa-126">-ResourceGroupName</span></span>
<span data-ttu-id="f64aa-127">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="f64aa-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="f64aa-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f64aa-128">-ResourceId</span></span>
<span data-ttu-id="f64aa-129">Az alkalmazás betekintési összetevőjének erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f64aa-129">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="f64aa-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f64aa-130">-Confirm</span></span>
<span data-ttu-id="f64aa-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f64aa-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f64aa-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f64aa-132">-WhatIf</span></span>
<span data-ttu-id="f64aa-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f64aa-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f64aa-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f64aa-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f64aa-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f64aa-135">CommonParameters</span></span>
<span data-ttu-id="f64aa-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f64aa-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f64aa-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f64aa-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f64aa-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f64aa-138">INPUTS</span></span>

### <span data-ttu-id="f64aa-139">Microsoft. Azure. Command. ApplicationInsights. models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="f64aa-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="f64aa-140">System. String</span><span class="sxs-lookup"><span data-stu-id="f64aa-140">System.String</span></span>

## <span data-ttu-id="f64aa-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f64aa-141">OUTPUTS</span></span>

### <span data-ttu-id="f64aa-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f64aa-142">System.Boolean</span></span>

## <span data-ttu-id="f64aa-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f64aa-143">NOTES</span></span>

## <span data-ttu-id="f64aa-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f64aa-144">RELATED LINKS</span></span>
