---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/powershell/module/az.applicationinsights/remove-azapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsContinuousExport.md
ms.openlocfilehash: b2ada8c4a58b38eee9ab235bbcd88429934ac00c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920650"
---
# <span data-ttu-id="40798-101">Remove-AzApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="40798-101">Remove-AzApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="40798-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40798-102">SYNOPSIS</span></span>
<span data-ttu-id="40798-103">Folyamatos exportálási konfiguráció eltávolítása egy alkalmazásstatékony erőforrásban</span><span class="sxs-lookup"><span data-stu-id="40798-103">Remove a continuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="40798-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="40798-104">SYNTAX</span></span>

### <span data-ttu-id="40798-105">ComponentNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="40798-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String>
 [-ExportId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="40798-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="40798-106">ComponentObjectParameterSet</span></span>
```
Remove-AzApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-ExportId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="40798-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="40798-107">ResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsightsContinuousExport [-ResourceId] <String> [-ExportId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40798-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="40798-108">DESCRIPTION</span></span>
<span data-ttu-id="40798-109">Folyamatos exportálási konfiguráció eltávolítása egy alkalmazásstatékony erőforrásban</span><span class="sxs-lookup"><span data-stu-id="40798-109">Remove a continuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="40798-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="40798-110">EXAMPLES</span></span>

### <span data-ttu-id="40798-111">1. példa: Folyamatos exportálási konfiguráció eltávolítása egy alkalmazásstatékony erőforrásban</span><span class="sxs-lookup"><span data-stu-id="40798-111">Example 1 Remove a continuous export configuration in an application insights resource</span></span>
```
PS C:\> Remove-AzApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test" -ExportId "uGOoki0jQsyEs3IdQ83Q4QsNr4=" -PassThru
True
```

<span data-ttu-id="40798-112">Az "uGOoki0jQsyEs3IdQ83Q4QsNr4=" exportazonosítóval eltávolíthatja az alkalmazásstatéria folyamatos exportálási konfigurációját a "tesztcsoport" erőforráscsoport "teszt" nevű erőforrásához.</span><span class="sxs-lookup"><span data-stu-id="40798-112">Remove application insights continuous export configuration with export id "uGOoki0jQsyEs3IdQ83Q4QsNr4=" for resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="40798-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="40798-113">PARAMETERS</span></span>

### <span data-ttu-id="40798-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="40798-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="40798-115">Application Insights összetevő-objektum.</span><span class="sxs-lookup"><span data-stu-id="40798-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="40798-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40798-116">-DefaultProfile</span></span>
<span data-ttu-id="40798-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="40798-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40798-118">-ExportId</span><span class="sxs-lookup"><span data-stu-id="40798-118">-ExportId</span></span>
<span data-ttu-id="40798-119">Application Insights folyamatos exportálási azonosító.</span><span class="sxs-lookup"><span data-stu-id="40798-119">Application Insights Continuous Export ID.</span></span>

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

### <span data-ttu-id="40798-120">-Name</span><span class="sxs-lookup"><span data-stu-id="40798-120">-Name</span></span>
<span data-ttu-id="40798-121">Application Insights összetevő neve.</span><span class="sxs-lookup"><span data-stu-id="40798-121">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="40798-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="40798-122">-PassThru</span></span>
<span data-ttu-id="40798-123">Ha a megadott érték igaz értéket ad meg, akkor a művelet sikeres lesz.</span><span class="sxs-lookup"><span data-stu-id="40798-123">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="40798-124">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="40798-124">This parameter is optional.</span></span> <span data-ttu-id="40798-125">Az alapértelmezett érték hamis.</span><span class="sxs-lookup"><span data-stu-id="40798-125">Default value is false.</span></span>

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

### <span data-ttu-id="40798-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40798-126">-ResourceGroupName</span></span>
<span data-ttu-id="40798-127">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="40798-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="40798-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="40798-128">-ResourceId</span></span>
<span data-ttu-id="40798-129">Application Insights összetevő erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="40798-129">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="40798-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="40798-130">-Confirm</span></span>
<span data-ttu-id="40798-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="40798-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40798-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40798-132">-WhatIf</span></span>
<span data-ttu-id="40798-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="40798-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40798-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="40798-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40798-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40798-135">CommonParameters</span></span>
<span data-ttu-id="40798-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40798-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40798-137">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40798-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40798-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="40798-138">INPUTS</span></span>

### <span data-ttu-id="40798-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="40798-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="40798-140">System.String</span><span class="sxs-lookup"><span data-stu-id="40798-140">System.String</span></span>

## <span data-ttu-id="40798-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="40798-141">OUTPUTS</span></span>

### <span data-ttu-id="40798-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="40798-142">System.Boolean</span></span>

## <span data-ttu-id="40798-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="40798-143">NOTES</span></span>

## <span data-ttu-id="40798-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="40798-144">RELATED LINKS</span></span>
