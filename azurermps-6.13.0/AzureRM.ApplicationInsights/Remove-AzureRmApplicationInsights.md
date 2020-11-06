---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/remove-azurermapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Remove-AzureRmApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Remove-AzureRmApplicationInsights.md
ms.openlocfilehash: 72a5affb91cbd2c1dfbe78cc7ee86da799b6ae50
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492057"
---
# <span data-ttu-id="abdfe-101">Remove-AzureRmApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="abdfe-101">Remove-AzureRmApplicationInsights</span></span>

## <span data-ttu-id="abdfe-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="abdfe-102">SYNOPSIS</span></span>
<span data-ttu-id="abdfe-103">Alkalmazás-betekintési erőforrás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="abdfe-103">Remove an application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="abdfe-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="abdfe-104">SYNTAX</span></span>

### <span data-ttu-id="abdfe-105">ComponentNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="abdfe-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzureRmApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="abdfe-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="abdfe-106">ComponentObjectParameterSet</span></span>
```
Remove-AzureRmApplicationInsights [-ApplicationInsightsComponent] <PSApplicationInsightsComponent> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="abdfe-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="abdfe-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmApplicationInsights [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="abdfe-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="abdfe-108">DESCRIPTION</span></span>
<span data-ttu-id="abdfe-109">Alkalmazás-betekintési erőforrás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="abdfe-109">Remove an application insights resource</span></span>

## <span data-ttu-id="abdfe-110">Példák</span><span class="sxs-lookup"><span data-stu-id="abdfe-110">EXAMPLES</span></span>

### <span data-ttu-id="abdfe-111">Példa 1 alkalmazás-betekintési erőforrás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="abdfe-111">Example 1 Remove an application insights resource</span></span>
```
PS C:\> Remove-AzureRmApplicationInsights -ResourceGroupName "testgroup" -Name "test" -PassThru
True
```

<span data-ttu-id="abdfe-112">A "teszt" nevű applciation-betekintési erőforrás eltávolítása a "testgroup" erőforráscsoporthoz</span><span class="sxs-lookup"><span data-stu-id="abdfe-112">Remove an applciation insights resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="abdfe-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="abdfe-113">PARAMETERS</span></span>

### <span data-ttu-id="abdfe-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="abdfe-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="abdfe-115">Az alkalmazás betekintése összetevő-objektum.</span><span class="sxs-lookup"><span data-stu-id="abdfe-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="abdfe-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abdfe-116">-DefaultProfile</span></span>
<span data-ttu-id="abdfe-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="abdfe-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="abdfe-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="abdfe-118">-Name</span></span>
<span data-ttu-id="abdfe-119">Az alkalmazás betekintési összetevőjének neve.</span><span class="sxs-lookup"><span data-stu-id="abdfe-119">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="abdfe-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="abdfe-120">-PassThru</span></span>
<span data-ttu-id="abdfe-121">Ha a megadott művelet sikeres, akkor a True Write True értékre vált.</span><span class="sxs-lookup"><span data-stu-id="abdfe-121">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="abdfe-122">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="abdfe-122">This parameter is optional.</span></span> <span data-ttu-id="abdfe-123">Az alapértelmezett érték a hamis.</span><span class="sxs-lookup"><span data-stu-id="abdfe-123">Default value is false.</span></span>

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

### <span data-ttu-id="abdfe-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abdfe-124">-ResourceGroupName</span></span>
<span data-ttu-id="abdfe-125">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="abdfe-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="abdfe-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="abdfe-126">-ResourceId</span></span>
<span data-ttu-id="abdfe-127">Az alkalmazás betekintési összetevőjének erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="abdfe-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="abdfe-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="abdfe-128">-Confirm</span></span>
<span data-ttu-id="abdfe-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="abdfe-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="abdfe-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abdfe-130">-WhatIf</span></span>
<span data-ttu-id="abdfe-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="abdfe-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="abdfe-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="abdfe-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="abdfe-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abdfe-133">CommonParameters</span></span>
<span data-ttu-id="abdfe-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="abdfe-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abdfe-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abdfe-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abdfe-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="abdfe-136">INPUTS</span></span>

### <span data-ttu-id="abdfe-137">Microsoft. Azure. Command. ApplicationInsights. models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="abdfe-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>
<span data-ttu-id="abdfe-138">Paraméterek: ApplicationInsightsComponent (ByValue)</span><span class="sxs-lookup"><span data-stu-id="abdfe-138">Parameters: ApplicationInsightsComponent (ByValue)</span></span>

### <span data-ttu-id="abdfe-139">System. String</span><span class="sxs-lookup"><span data-stu-id="abdfe-139">System.String</span></span>

## <span data-ttu-id="abdfe-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="abdfe-140">OUTPUTS</span></span>

### <span data-ttu-id="abdfe-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="abdfe-141">System.Boolean</span></span>

## <span data-ttu-id="abdfe-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="abdfe-142">NOTES</span></span>

## <span data-ttu-id="abdfe-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="abdfe-143">RELATED LINKS</span></span>
