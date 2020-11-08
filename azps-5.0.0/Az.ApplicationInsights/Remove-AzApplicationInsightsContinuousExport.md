---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/remove-azapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsContinuousExport.md
ms.openlocfilehash: 6138d3d454a23cdbdbaa67d7ee668c5ffa752b4a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195430"
---
# <span data-ttu-id="6cbf1-101">Remove-AzApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="6cbf1-101">Remove-AzApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="6cbf1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6cbf1-102">SYNOPSIS</span></span>
<span data-ttu-id="6cbf1-103">A folyamatos exportálási konfiguráció eltávolítása egy alkalmazás-erőforrásban</span><span class="sxs-lookup"><span data-stu-id="6cbf1-103">Remove a continuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="6cbf1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6cbf1-104">SYNTAX</span></span>

### <span data-ttu-id="6cbf1-105">ComponentNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6cbf1-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String>
 [-ExportId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6cbf1-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6cbf1-106">ComponentObjectParameterSet</span></span>
```
Remove-AzApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-ExportId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6cbf1-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6cbf1-107">ResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsightsContinuousExport [-ResourceId] <String> [-ExportId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6cbf1-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="6cbf1-108">DESCRIPTION</span></span>
<span data-ttu-id="6cbf1-109">A folyamatos exportálási konfiguráció eltávolítása egy alkalmazás-erőforrásban</span><span class="sxs-lookup"><span data-stu-id="6cbf1-109">Remove a continuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="6cbf1-110">Példák</span><span class="sxs-lookup"><span data-stu-id="6cbf1-110">EXAMPLES</span></span>

### <span data-ttu-id="6cbf1-111">Példa 1 a folyamatos exportálási konfiguráció eltávolítása egy alkalmazásbeli betekintést tartalmazó erőforrásból</span><span class="sxs-lookup"><span data-stu-id="6cbf1-111">Example 1 Remove a continuous export configuration in an application insights resource</span></span>
```
PS C:\> Remove-AzApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test" -ExportId "uGOoki0jQsyEs3IdQ83Q4QsNr4=" -PassThru
True
```

<span data-ttu-id="6cbf1-112">A folyamatos exportálási konfiguráció eltávolítása a "teszt" erőforráscsoport "testgroup" erőforráscsoporthoz tartozó "uGOoki0jQsyEs3IdQ83Q4QsNr4 =" exportálási azonosítóval</span><span class="sxs-lookup"><span data-stu-id="6cbf1-112">Remove application insights continuous export configuration with export id "uGOoki0jQsyEs3IdQ83Q4QsNr4=" for resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="6cbf1-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6cbf1-113">PARAMETERS</span></span>

### <span data-ttu-id="6cbf1-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="6cbf1-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="6cbf1-115">Az alkalmazás betekintése összetevő-objektum.</span><span class="sxs-lookup"><span data-stu-id="6cbf1-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="6cbf1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cbf1-116">-DefaultProfile</span></span>
<span data-ttu-id="6cbf1-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6cbf1-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6cbf1-118">-ExportId</span><span class="sxs-lookup"><span data-stu-id="6cbf1-118">-ExportId</span></span>
<span data-ttu-id="6cbf1-119">Az alkalmazás betekintést nyújt a folyamatos exportálási AZONOSÍTÓra.</span><span class="sxs-lookup"><span data-stu-id="6cbf1-119">Application Insights Continuous Export ID.</span></span>

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

### <span data-ttu-id="6cbf1-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6cbf1-120">-Name</span></span>
<span data-ttu-id="6cbf1-121">Az alkalmazás betekintési összetevőjének neve.</span><span class="sxs-lookup"><span data-stu-id="6cbf1-121">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="6cbf1-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6cbf1-122">-PassThru</span></span>
<span data-ttu-id="6cbf1-123">Ha a megadott művelet sikeres, akkor a True Write True értékre vált.</span><span class="sxs-lookup"><span data-stu-id="6cbf1-123">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="6cbf1-124">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="6cbf1-124">This parameter is optional.</span></span> <span data-ttu-id="6cbf1-125">Az alapértelmezett érték a hamis.</span><span class="sxs-lookup"><span data-stu-id="6cbf1-125">Default value is false.</span></span>

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

### <span data-ttu-id="6cbf1-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cbf1-126">-ResourceGroupName</span></span>
<span data-ttu-id="6cbf1-127">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="6cbf1-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="6cbf1-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6cbf1-128">-ResourceId</span></span>
<span data-ttu-id="6cbf1-129">Az alkalmazás betekintési összetevőjének erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="6cbf1-129">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="6cbf1-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6cbf1-130">-Confirm</span></span>
<span data-ttu-id="6cbf1-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6cbf1-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6cbf1-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6cbf1-132">-WhatIf</span></span>
<span data-ttu-id="6cbf1-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6cbf1-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6cbf1-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6cbf1-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6cbf1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cbf1-135">CommonParameters</span></span>
<span data-ttu-id="6cbf1-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6cbf1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cbf1-137">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6cbf1-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cbf1-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6cbf1-138">INPUTS</span></span>

### <span data-ttu-id="6cbf1-139">Microsoft. Azure. Command. ApplicationInsights. models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="6cbf1-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="6cbf1-140">System. String</span><span class="sxs-lookup"><span data-stu-id="6cbf1-140">System.String</span></span>

## <span data-ttu-id="6cbf1-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6cbf1-141">OUTPUTS</span></span>

### <span data-ttu-id="6cbf1-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6cbf1-142">System.Boolean</span></span>

## <span data-ttu-id="6cbf1-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6cbf1-143">NOTES</span></span>

## <span data-ttu-id="6cbf1-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6cbf1-144">RELATED LINKS</span></span>
