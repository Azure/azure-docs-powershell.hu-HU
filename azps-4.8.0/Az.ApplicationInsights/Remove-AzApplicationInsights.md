---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/remove-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsights.md
ms.openlocfilehash: b63f1b350daad55a26dc91f46e89b28675622fbb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94180657"
---
# <span data-ttu-id="81e92-101">Remove-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="81e92-101">Remove-AzApplicationInsights</span></span>

## <span data-ttu-id="81e92-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="81e92-102">SYNOPSIS</span></span>
<span data-ttu-id="81e92-103">Alkalmazás-betekintési erőforrás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="81e92-103">Remove an application insights resource</span></span>

## <span data-ttu-id="81e92-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="81e92-104">SYNTAX</span></span>

### <span data-ttu-id="81e92-105">ComponentNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="81e92-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81e92-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="81e92-106">ComponentObjectParameterSet</span></span>
```
Remove-AzApplicationInsights [-ApplicationInsightsComponent] <PSApplicationInsightsComponent> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81e92-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="81e92-107">ResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsights [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81e92-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="81e92-108">DESCRIPTION</span></span>
<span data-ttu-id="81e92-109">Alkalmazás-betekintési erőforrás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="81e92-109">Remove an application insights resource</span></span>

## <span data-ttu-id="81e92-110">Példák</span><span class="sxs-lookup"><span data-stu-id="81e92-110">EXAMPLES</span></span>

### <span data-ttu-id="81e92-111">Példa 1 alkalmazás-betekintési erőforrás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="81e92-111">Example 1 Remove an application insights resource</span></span>
```
PS C:\> Remove-AzApplicationInsights -ResourceGroupName "testgroup" -Name "test" -PassThru
True
```

<span data-ttu-id="81e92-112">A "teszt" nevű, az "testgroup" erőforráscsoporthoz tartozó "teszt" nevű erőforrás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="81e92-112">Remove an application insights resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="81e92-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="81e92-113">PARAMETERS</span></span>

### <span data-ttu-id="81e92-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="81e92-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="81e92-115">Az alkalmazás betekintése összetevő-objektum.</span><span class="sxs-lookup"><span data-stu-id="81e92-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="81e92-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81e92-116">-DefaultProfile</span></span>
<span data-ttu-id="81e92-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="81e92-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81e92-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="81e92-118">-Name</span></span>
<span data-ttu-id="81e92-119">Az alkalmazás betekintési összetevőjének neve.</span><span class="sxs-lookup"><span data-stu-id="81e92-119">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="81e92-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="81e92-120">-PassThru</span></span>
<span data-ttu-id="81e92-121">Ha a megadott művelet sikeres, akkor a True Write True értékre vált.</span><span class="sxs-lookup"><span data-stu-id="81e92-121">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="81e92-122">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="81e92-122">This parameter is optional.</span></span> <span data-ttu-id="81e92-123">Az alapértelmezett érték a hamis.</span><span class="sxs-lookup"><span data-stu-id="81e92-123">Default value is false.</span></span>

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

### <span data-ttu-id="81e92-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81e92-124">-ResourceGroupName</span></span>
<span data-ttu-id="81e92-125">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="81e92-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="81e92-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="81e92-126">-ResourceId</span></span>
<span data-ttu-id="81e92-127">Az alkalmazás betekintési összetevőjének erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="81e92-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="81e92-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="81e92-128">-Confirm</span></span>
<span data-ttu-id="81e92-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="81e92-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81e92-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81e92-130">-WhatIf</span></span>
<span data-ttu-id="81e92-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="81e92-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81e92-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="81e92-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81e92-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81e92-133">CommonParameters</span></span>
<span data-ttu-id="81e92-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="81e92-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81e92-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="81e92-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81e92-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="81e92-136">INPUTS</span></span>

### <span data-ttu-id="81e92-137">Microsoft. Azure. Command. ApplicationInsights. models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="81e92-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="81e92-138">System. String</span><span class="sxs-lookup"><span data-stu-id="81e92-138">System.String</span></span>

## <span data-ttu-id="81e92-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="81e92-139">OUTPUTS</span></span>

### <span data-ttu-id="81e92-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="81e92-140">System.Boolean</span></span>

## <span data-ttu-id="81e92-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="81e92-141">NOTES</span></span>

## <span data-ttu-id="81e92-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="81e92-142">RELATED LINKS</span></span>
