---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/powershell/module/az.applicationinsights/remove-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsights.md
ms.openlocfilehash: 089561268233876976598f3cf74cd0a52fef8402
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004853"
---
# <span data-ttu-id="ebc5b-101">Remove-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="ebc5b-101">Remove-AzApplicationInsights</span></span>

## <span data-ttu-id="ebc5b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ebc5b-102">SYNOPSIS</span></span>
<span data-ttu-id="ebc5b-103">Alkalmazáselemzési erőforrás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="ebc5b-103">Remove an application insights resource</span></span>

## <span data-ttu-id="ebc5b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ebc5b-104">SYNTAX</span></span>

### <span data-ttu-id="ebc5b-105">ComponentNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ebc5b-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ebc5b-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ebc5b-106">ComponentObjectParameterSet</span></span>
```
Remove-AzApplicationInsights [-ApplicationInsightsComponent] <PSApplicationInsightsComponent> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ebc5b-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ebc5b-107">ResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsights [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ebc5b-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ebc5b-108">DESCRIPTION</span></span>
<span data-ttu-id="ebc5b-109">Alkalmazáselemzési erőforrás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="ebc5b-109">Remove an application insights resource</span></span>

## <span data-ttu-id="ebc5b-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ebc5b-110">EXAMPLES</span></span>

### <span data-ttu-id="ebc5b-111">1. példa egy alkalmazásstatstatékony erőforrás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="ebc5b-111">Example 1 Remove an application insights resource</span></span>
```
PS C:\> Remove-AzApplicationInsights -ResourceGroupName "testgroup" -Name "test" -PassThru
True
```

<span data-ttu-id="ebc5b-112">A "teszt" nevű alkalmazáselemzési erőforrás eltávolítása a "tesztcsoport" erőforráscsoportban</span><span class="sxs-lookup"><span data-stu-id="ebc5b-112">Remove an application insights resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="ebc5b-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ebc5b-113">PARAMETERS</span></span>

### <span data-ttu-id="ebc5b-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="ebc5b-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="ebc5b-115">Application Insights összetevő-objektum.</span><span class="sxs-lookup"><span data-stu-id="ebc5b-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="ebc5b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebc5b-116">-DefaultProfile</span></span>
<span data-ttu-id="ebc5b-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ebc5b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ebc5b-118">-Name</span><span class="sxs-lookup"><span data-stu-id="ebc5b-118">-Name</span></span>
<span data-ttu-id="ebc5b-119">Application Insights összetevő neve.</span><span class="sxs-lookup"><span data-stu-id="ebc5b-119">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="ebc5b-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ebc5b-120">-PassThru</span></span>
<span data-ttu-id="ebc5b-121">Ha a megadott érték igaz értéket ad meg, akkor a művelet sikeres lesz.</span><span class="sxs-lookup"><span data-stu-id="ebc5b-121">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="ebc5b-122">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="ebc5b-122">This parameter is optional.</span></span> <span data-ttu-id="ebc5b-123">Az alapértelmezett érték hamis.</span><span class="sxs-lookup"><span data-stu-id="ebc5b-123">Default value is false.</span></span>

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

### <span data-ttu-id="ebc5b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebc5b-124">-ResourceGroupName</span></span>
<span data-ttu-id="ebc5b-125">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ebc5b-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="ebc5b-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ebc5b-126">-ResourceId</span></span>
<span data-ttu-id="ebc5b-127">Application Insights összetevő erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ebc5b-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="ebc5b-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ebc5b-128">-Confirm</span></span>
<span data-ttu-id="ebc5b-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ebc5b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ebc5b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ebc5b-130">-WhatIf</span></span>
<span data-ttu-id="ebc5b-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="ebc5b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ebc5b-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ebc5b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ebc5b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebc5b-133">CommonParameters</span></span>
<span data-ttu-id="ebc5b-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ebc5b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebc5b-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ebc5b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebc5b-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ebc5b-136">INPUTS</span></span>

### <span data-ttu-id="ebc5b-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="ebc5b-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="ebc5b-138">System.String</span><span class="sxs-lookup"><span data-stu-id="ebc5b-138">System.String</span></span>

## <span data-ttu-id="ebc5b-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ebc5b-139">OUTPUTS</span></span>

### <span data-ttu-id="ebc5b-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ebc5b-140">System.Boolean</span></span>

## <span data-ttu-id="ebc5b-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ebc5b-141">NOTES</span></span>

## <span data-ttu-id="ebc5b-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ebc5b-142">RELATED LINKS</span></span>
