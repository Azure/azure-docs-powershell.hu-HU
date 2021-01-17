---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/remove-azapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsContinuousExport.md
ms.openlocfilehash: 6138d3d454a23cdbdbaa67d7ee668c5ffa752b4a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98381288"
---
# <span data-ttu-id="2d9a2-101">Remove-AzApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="2d9a2-101">Remove-AzApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="2d9a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d9a2-102">SYNOPSIS</span></span>
<span data-ttu-id="2d9a2-103">Folyamatos exportálási konfiguráció eltávolítása egy alkalmazásstatékony erőforrásban</span><span class="sxs-lookup"><span data-stu-id="2d9a2-103">Remove a continuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="2d9a2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2d9a2-104">SYNTAX</span></span>

### <span data-ttu-id="2d9a2-105">ComponentNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2d9a2-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String>
 [-ExportId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2d9a2-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2d9a2-106">ComponentObjectParameterSet</span></span>
```
Remove-AzApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-ExportId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2d9a2-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2d9a2-107">ResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsightsContinuousExport [-ResourceId] <String> [-ExportId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d9a2-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2d9a2-108">DESCRIPTION</span></span>
<span data-ttu-id="2d9a2-109">Folyamatos exportálási konfiguráció eltávolítása egy alkalmazásstatékony erőforrásban</span><span class="sxs-lookup"><span data-stu-id="2d9a2-109">Remove a continuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="2d9a2-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2d9a2-110">EXAMPLES</span></span>

### <span data-ttu-id="2d9a2-111">1. példa: Folyamatos exportálási konfiguráció eltávolítása egy alkalmazásstatékony erőforrásban</span><span class="sxs-lookup"><span data-stu-id="2d9a2-111">Example 1 Remove a continuous export configuration in an application insights resource</span></span>
```
PS C:\> Remove-AzApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test" -ExportId "uGOoki0jQsyEs3IdQ83Q4QsNr4=" -PassThru
True
```

<span data-ttu-id="2d9a2-112">Az "uGOoki0jQsyEs3IdQ83Q4QsNr4=" exportazonosítóval eltávolíthatja az alkalmazásstatéria folyamatos exportálási konfigurációját a "tesztcsoport" erőforráscsoport "teszt" nevű erőforrásához.</span><span class="sxs-lookup"><span data-stu-id="2d9a2-112">Remove application insights continuous export configuration with export id "uGOoki0jQsyEs3IdQ83Q4QsNr4=" for resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="2d9a2-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2d9a2-113">PARAMETERS</span></span>

### <span data-ttu-id="2d9a2-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="2d9a2-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="2d9a2-115">Application Insights összetevő-objektum.</span><span class="sxs-lookup"><span data-stu-id="2d9a2-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="2d9a2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d9a2-116">-DefaultProfile</span></span>
<span data-ttu-id="2d9a2-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2d9a2-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2d9a2-118">-ExportId</span><span class="sxs-lookup"><span data-stu-id="2d9a2-118">-ExportId</span></span>
<span data-ttu-id="2d9a2-119">Application Insights folyamatos exportálási azonosító.</span><span class="sxs-lookup"><span data-stu-id="2d9a2-119">Application Insights Continuous Export ID.</span></span>

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

### <span data-ttu-id="2d9a2-120">-Name</span><span class="sxs-lookup"><span data-stu-id="2d9a2-120">-Name</span></span>
<span data-ttu-id="2d9a2-121">Application Insights összetevő neve.</span><span class="sxs-lookup"><span data-stu-id="2d9a2-121">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="2d9a2-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2d9a2-122">-PassThru</span></span>
<span data-ttu-id="2d9a2-123">Ha a megadott érték igaz értéket ad meg, akkor a művelet sikeres lesz.</span><span class="sxs-lookup"><span data-stu-id="2d9a2-123">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="2d9a2-124">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="2d9a2-124">This parameter is optional.</span></span> <span data-ttu-id="2d9a2-125">Az alapértelmezett érték hamis.</span><span class="sxs-lookup"><span data-stu-id="2d9a2-125">Default value is false.</span></span>

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

### <span data-ttu-id="2d9a2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d9a2-126">-ResourceGroupName</span></span>
<span data-ttu-id="2d9a2-127">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="2d9a2-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="2d9a2-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2d9a2-128">-ResourceId</span></span>
<span data-ttu-id="2d9a2-129">Application Insights összetevő erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="2d9a2-129">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="2d9a2-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2d9a2-130">-Confirm</span></span>
<span data-ttu-id="2d9a2-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="2d9a2-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d9a2-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d9a2-132">-WhatIf</span></span>
<span data-ttu-id="2d9a2-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="2d9a2-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d9a2-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2d9a2-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d9a2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d9a2-135">CommonParameters</span></span>
<span data-ttu-id="2d9a2-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d9a2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d9a2-137">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d9a2-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d9a2-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2d9a2-138">INPUTS</span></span>

### <span data-ttu-id="2d9a2-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="2d9a2-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="2d9a2-140">System.String</span><span class="sxs-lookup"><span data-stu-id="2d9a2-140">System.String</span></span>

## <span data-ttu-id="2d9a2-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2d9a2-141">OUTPUTS</span></span>

### <span data-ttu-id="2d9a2-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2d9a2-142">System.Boolean</span></span>

## <span data-ttu-id="2d9a2-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2d9a2-143">NOTES</span></span>

## <span data-ttu-id="2d9a2-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2d9a2-144">RELATED LINKS</span></span>
