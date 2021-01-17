---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/remove-azapplicationinsightsapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsApiKey.md
ms.openlocfilehash: 53ebb6d1a7bcfc35dafb09c377b2a4a023e327d8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98381274"
---
# <span data-ttu-id="7a0ae-101">Remove-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="7a0ae-101">Remove-AzApplicationInsightsApiKey</span></span>

## <span data-ttu-id="7a0ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a0ae-102">SYNOPSIS</span></span>
<span data-ttu-id="7a0ae-103">Alkalmazásstatektúra api-kulcsának eltávolítása egy alkalmazásstatékony erőforráshoz</span><span class="sxs-lookup"><span data-stu-id="7a0ae-103">Remove an application insights api key for an application insights resource</span></span>

## <span data-ttu-id="7a0ae-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7a0ae-104">SYNTAX</span></span>

### <span data-ttu-id="7a0ae-105">ComponentNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7a0ae-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsightsApiKey [-ResourceGroupName] <String> [-Name] <String> [-ApiKeyId] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a0ae-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a0ae-106">ComponentObjectParameterSet</span></span>
```
Remove-AzApplicationInsightsApiKey [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-ApiKeyId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7a0ae-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a0ae-107">ResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsightsApiKey [-ResourceId] <String> [-ApiKeyId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a0ae-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7a0ae-108">DESCRIPTION</span></span>
<span data-ttu-id="7a0ae-109">Alkalmazásstatektúra api-kulcsának eltávolítása egy alkalmazásstatékony erőforráshoz</span><span class="sxs-lookup"><span data-stu-id="7a0ae-109">Remove an application insights api key for an application insights resource</span></span>

## <span data-ttu-id="7a0ae-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7a0ae-110">EXAMPLES</span></span>

### <span data-ttu-id="7a0ae-111">1. példa egy alkalmazásstatékony api-kulcs eltávolítása egy alkalmazásstatékony erőforráshoz</span><span class="sxs-lookup"><span data-stu-id="7a0ae-111">Example 1 Remove an application insights api key for an application insights resource</span></span>
```
Remove-AzApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test"  -ApiKeyId dd173f38-4fd1-4c75-8af5-9
9c29aa0f867 -PassThru
True
```

<span data-ttu-id="7a0ae-112">Távolítsa el a "testGroup" erőforráscsoport "teszt" erőforráscsoportjában a "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867" azonosítójú alkalmazásstatéria-kulcsot.</span><span class="sxs-lookup"><span data-stu-id="7a0ae-112">Remove specific application insights api key that id is "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867" for resource "test" in resource group "testGroup".</span></span>

## <span data-ttu-id="7a0ae-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7a0ae-113">PARAMETERS</span></span>

### <span data-ttu-id="7a0ae-114">-ApiKeyId</span><span class="sxs-lookup"><span data-stu-id="7a0ae-114">-ApiKeyId</span></span>
<span data-ttu-id="7a0ae-115">Application Insights API-kulcsazonosító.</span><span class="sxs-lookup"><span data-stu-id="7a0ae-115">Application Insights API Key ID.</span></span>

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

### <span data-ttu-id="7a0ae-116">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="7a0ae-116">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="7a0ae-117">Application Insights összetevő-objektum.</span><span class="sxs-lookup"><span data-stu-id="7a0ae-117">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="7a0ae-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a0ae-118">-DefaultProfile</span></span>
<span data-ttu-id="7a0ae-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7a0ae-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7a0ae-120">-Name</span><span class="sxs-lookup"><span data-stu-id="7a0ae-120">-Name</span></span>
<span data-ttu-id="7a0ae-121">Application Insights összetevő neve.</span><span class="sxs-lookup"><span data-stu-id="7a0ae-121">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="7a0ae-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7a0ae-122">-PassThru</span></span>
<span data-ttu-id="7a0ae-123">Ha a megadott érték igaz értéket ad meg, akkor a művelet sikeres lesz.</span><span class="sxs-lookup"><span data-stu-id="7a0ae-123">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="7a0ae-124">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="7a0ae-124">This parameter is optional.</span></span> <span data-ttu-id="7a0ae-125">Az alapértelmezett érték hamis.</span><span class="sxs-lookup"><span data-stu-id="7a0ae-125">Default value is false.</span></span>

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

### <span data-ttu-id="7a0ae-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a0ae-126">-ResourceGroupName</span></span>
<span data-ttu-id="7a0ae-127">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="7a0ae-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="7a0ae-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7a0ae-128">-ResourceId</span></span>
<span data-ttu-id="7a0ae-129">Application Insights összetevő erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="7a0ae-129">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="7a0ae-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7a0ae-130">-Confirm</span></span>
<span data-ttu-id="7a0ae-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7a0ae-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a0ae-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a0ae-132">-WhatIf</span></span>
<span data-ttu-id="7a0ae-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7a0ae-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a0ae-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7a0ae-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a0ae-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a0ae-135">CommonParameters</span></span>
<span data-ttu-id="7a0ae-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a0ae-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a0ae-137">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a0ae-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a0ae-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7a0ae-138">INPUTS</span></span>

### <span data-ttu-id="7a0ae-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="7a0ae-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="7a0ae-140">System.String</span><span class="sxs-lookup"><span data-stu-id="7a0ae-140">System.String</span></span>

## <span data-ttu-id="7a0ae-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7a0ae-141">OUTPUTS</span></span>

### <span data-ttu-id="7a0ae-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7a0ae-142">System.Boolean</span></span>

## <span data-ttu-id="7a0ae-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7a0ae-143">NOTES</span></span>

## <span data-ttu-id="7a0ae-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7a0ae-144">RELATED LINKS</span></span>
