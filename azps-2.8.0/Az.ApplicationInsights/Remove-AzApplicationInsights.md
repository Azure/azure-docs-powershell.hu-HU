---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/remove-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsights.md
ms.openlocfilehash: 5665b85a680411910513663d782791f56b7c1081
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667899"
---
# <span data-ttu-id="70733-101">Remove-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="70733-101">Remove-AzApplicationInsights</span></span>

## <span data-ttu-id="70733-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="70733-102">SYNOPSIS</span></span>
<span data-ttu-id="70733-103">Alkalmazás-betekintési erőforrás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="70733-103">Remove an application insights resource</span></span>

## <span data-ttu-id="70733-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="70733-104">SYNTAX</span></span>

### <span data-ttu-id="70733-105">ComponentNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="70733-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70733-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="70733-106">ComponentObjectParameterSet</span></span>
```
Remove-AzApplicationInsights [-ApplicationInsightsComponent] <PSApplicationInsightsComponent> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70733-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="70733-107">ResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsights [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70733-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="70733-108">DESCRIPTION</span></span>
<span data-ttu-id="70733-109">Alkalmazás-betekintési erőforrás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="70733-109">Remove an application insights resource</span></span>

## <span data-ttu-id="70733-110">Példák</span><span class="sxs-lookup"><span data-stu-id="70733-110">EXAMPLES</span></span>

### <span data-ttu-id="70733-111">Példa 1 alkalmazás-betekintési erőforrás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="70733-111">Example 1 Remove an application insights resource</span></span>
```
PS C:\> Remove-AzApplicationInsights -ResourceGroupName "testgroup" -Name "test" -PassThru
True
```

<span data-ttu-id="70733-112">A "teszt" nevű, az "testgroup" erőforráscsoporthoz tartozó "teszt" nevű erőforrás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="70733-112">Remove an application insights resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="70733-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="70733-113">PARAMETERS</span></span>

### <span data-ttu-id="70733-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="70733-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="70733-115">Az alkalmazás betekintése összetevő-objektum.</span><span class="sxs-lookup"><span data-stu-id="70733-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="70733-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70733-116">-DefaultProfile</span></span>
<span data-ttu-id="70733-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="70733-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="70733-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="70733-118">-Name</span></span>
<span data-ttu-id="70733-119">Az alkalmazás betekintési összetevőjének neve.</span><span class="sxs-lookup"><span data-stu-id="70733-119">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="70733-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="70733-120">-PassThru</span></span>
<span data-ttu-id="70733-121">Ha a megadott művelet sikeres, akkor a True Write True értékre vált.</span><span class="sxs-lookup"><span data-stu-id="70733-121">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="70733-122">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="70733-122">This parameter is optional.</span></span> <span data-ttu-id="70733-123">Az alapértelmezett érték a hamis.</span><span class="sxs-lookup"><span data-stu-id="70733-123">Default value is false.</span></span>

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

### <span data-ttu-id="70733-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70733-124">-ResourceGroupName</span></span>
<span data-ttu-id="70733-125">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="70733-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="70733-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="70733-126">-ResourceId</span></span>
<span data-ttu-id="70733-127">Az alkalmazás betekintési összetevőjének erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="70733-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="70733-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="70733-128">-Confirm</span></span>
<span data-ttu-id="70733-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="70733-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70733-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70733-130">-WhatIf</span></span>
<span data-ttu-id="70733-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="70733-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70733-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="70733-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70733-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70733-133">CommonParameters</span></span>
<span data-ttu-id="70733-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="70733-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70733-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70733-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70733-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="70733-136">INPUTS</span></span>

### <span data-ttu-id="70733-137">Microsoft. Azure. Command. ApplicationInsights. models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="70733-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="70733-138">System. String</span><span class="sxs-lookup"><span data-stu-id="70733-138">System.String</span></span>

## <span data-ttu-id="70733-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="70733-139">OUTPUTS</span></span>

### <span data-ttu-id="70733-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="70733-140">System.Boolean</span></span>

## <span data-ttu-id="70733-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="70733-141">NOTES</span></span>

## <span data-ttu-id="70733-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="70733-142">RELATED LINKS</span></span>
