---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/remove-azapplicationinsightsapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsApiKey.md
ms.openlocfilehash: 53ebb6d1a7bcfc35dafb09c377b2a4a023e327d8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194833"
---
# <span data-ttu-id="64b9c-101">Remove-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="64b9c-101">Remove-AzApplicationInsightsApiKey</span></span>

## <span data-ttu-id="64b9c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="64b9c-102">SYNOPSIS</span></span>
<span data-ttu-id="64b9c-103">A betekintést használó erőforráshoz tartozó alkalmazás-ismertető API-kulcs eltávolítása</span><span class="sxs-lookup"><span data-stu-id="64b9c-103">Remove an application insights api key for an application insights resource</span></span>

## <span data-ttu-id="64b9c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="64b9c-104">SYNTAX</span></span>

### <span data-ttu-id="64b9c-105">ComponentNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="64b9c-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsightsApiKey [-ResourceGroupName] <String> [-Name] <String> [-ApiKeyId] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64b9c-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="64b9c-106">ComponentObjectParameterSet</span></span>
```
Remove-AzApplicationInsightsApiKey [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-ApiKeyId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="64b9c-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="64b9c-107">ResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsightsApiKey [-ResourceId] <String> [-ApiKeyId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64b9c-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="64b9c-108">DESCRIPTION</span></span>
<span data-ttu-id="64b9c-109">A betekintést használó erőforráshoz tartozó alkalmazás-ismertető API-kulcs eltávolítása</span><span class="sxs-lookup"><span data-stu-id="64b9c-109">Remove an application insights api key for an application insights resource</span></span>

## <span data-ttu-id="64b9c-110">Példák</span><span class="sxs-lookup"><span data-stu-id="64b9c-110">EXAMPLES</span></span>

### <span data-ttu-id="64b9c-111">Példa 1 az alkalmazás-elemzések API-kulcsának eltávolítása egy betekintést használó erőforráshoz</span><span class="sxs-lookup"><span data-stu-id="64b9c-111">Example 1 Remove an application insights api key for an application insights resource</span></span>
```
Remove-AzApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test"  -ApiKeyId dd173f38-4fd1-4c75-8af5-9
9c29aa0f867 -PassThru
True
```

<span data-ttu-id="64b9c-112">A "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867" erőforrás "teszt" az erőforráscsoport "testGroup" című csoportjának eltávolítása</span><span class="sxs-lookup"><span data-stu-id="64b9c-112">Remove specific application insights api key that id is "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867" for resource "test" in resource group "testGroup".</span></span>

## <span data-ttu-id="64b9c-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="64b9c-113">PARAMETERS</span></span>

### <span data-ttu-id="64b9c-114">-ApiKeyId</span><span class="sxs-lookup"><span data-stu-id="64b9c-114">-ApiKeyId</span></span>
<span data-ttu-id="64b9c-115">Az alkalmazás betekintési API-kulcs azonosítója.</span><span class="sxs-lookup"><span data-stu-id="64b9c-115">Application Insights API Key ID.</span></span>

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

### <span data-ttu-id="64b9c-116">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="64b9c-116">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="64b9c-117">Az alkalmazás betekintése összetevő-objektum.</span><span class="sxs-lookup"><span data-stu-id="64b9c-117">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="64b9c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64b9c-118">-DefaultProfile</span></span>
<span data-ttu-id="64b9c-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="64b9c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64b9c-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="64b9c-120">-Name</span></span>
<span data-ttu-id="64b9c-121">Az alkalmazás betekintési összetevőjének neve.</span><span class="sxs-lookup"><span data-stu-id="64b9c-121">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="64b9c-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="64b9c-122">-PassThru</span></span>
<span data-ttu-id="64b9c-123">Ha a megadott művelet sikeres, akkor a True Write True értékre vált.</span><span class="sxs-lookup"><span data-stu-id="64b9c-123">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="64b9c-124">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="64b9c-124">This parameter is optional.</span></span> <span data-ttu-id="64b9c-125">Az alapértelmezett érték a hamis.</span><span class="sxs-lookup"><span data-stu-id="64b9c-125">Default value is false.</span></span>

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

### <span data-ttu-id="64b9c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64b9c-126">-ResourceGroupName</span></span>
<span data-ttu-id="64b9c-127">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="64b9c-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="64b9c-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="64b9c-128">-ResourceId</span></span>
<span data-ttu-id="64b9c-129">Az alkalmazás betekintési összetevőjének erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="64b9c-129">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="64b9c-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="64b9c-130">-Confirm</span></span>
<span data-ttu-id="64b9c-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="64b9c-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64b9c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64b9c-132">-WhatIf</span></span>
<span data-ttu-id="64b9c-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="64b9c-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64b9c-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="64b9c-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64b9c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64b9c-135">CommonParameters</span></span>
<span data-ttu-id="64b9c-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="64b9c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64b9c-137">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64b9c-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64b9c-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="64b9c-138">INPUTS</span></span>

### <span data-ttu-id="64b9c-139">Microsoft. Azure. Command. ApplicationInsights. models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="64b9c-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="64b9c-140">System. String</span><span class="sxs-lookup"><span data-stu-id="64b9c-140">System.String</span></span>

## <span data-ttu-id="64b9c-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="64b9c-141">OUTPUTS</span></span>

### <span data-ttu-id="64b9c-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="64b9c-142">System.Boolean</span></span>

## <span data-ttu-id="64b9c-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="64b9c-143">NOTES</span></span>

## <span data-ttu-id="64b9c-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="64b9c-144">RELATED LINKS</span></span>
