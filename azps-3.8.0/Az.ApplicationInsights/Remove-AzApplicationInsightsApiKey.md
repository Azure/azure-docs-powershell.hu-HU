---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/remove-azapplicationinsightsapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsApiKey.md
ms.openlocfilehash: 53ebb6d1a7bcfc35dafb09c377b2a4a023e327d8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012808"
---
# <span data-ttu-id="90e5f-101">Remove-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="90e5f-101">Remove-AzApplicationInsightsApiKey</span></span>

## <span data-ttu-id="90e5f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="90e5f-102">SYNOPSIS</span></span>
<span data-ttu-id="90e5f-103">A betekintést használó erőforráshoz tartozó alkalmazás-ismertető API-kulcs eltávolítása</span><span class="sxs-lookup"><span data-stu-id="90e5f-103">Remove an application insights api key for an application insights resource</span></span>

## <span data-ttu-id="90e5f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="90e5f-104">SYNTAX</span></span>

### <span data-ttu-id="90e5f-105">ComponentNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="90e5f-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsightsApiKey [-ResourceGroupName] <String> [-Name] <String> [-ApiKeyId] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90e5f-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="90e5f-106">ComponentObjectParameterSet</span></span>
```
Remove-AzApplicationInsightsApiKey [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-ApiKeyId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="90e5f-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="90e5f-107">ResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsightsApiKey [-ResourceId] <String> [-ApiKeyId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90e5f-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="90e5f-108">DESCRIPTION</span></span>
<span data-ttu-id="90e5f-109">A betekintést használó erőforráshoz tartozó alkalmazás-ismertető API-kulcs eltávolítása</span><span class="sxs-lookup"><span data-stu-id="90e5f-109">Remove an application insights api key for an application insights resource</span></span>

## <span data-ttu-id="90e5f-110">Példák</span><span class="sxs-lookup"><span data-stu-id="90e5f-110">EXAMPLES</span></span>

### <span data-ttu-id="90e5f-111">Példa 1 az alkalmazás-elemzések API-kulcsának eltávolítása egy betekintést használó erőforráshoz</span><span class="sxs-lookup"><span data-stu-id="90e5f-111">Example 1 Remove an application insights api key for an application insights resource</span></span>
```
Remove-AzApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test"  -ApiKeyId dd173f38-4fd1-4c75-8af5-9
9c29aa0f867 -PassThru
True
```

<span data-ttu-id="90e5f-112">A "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867" erőforrás "teszt" az erőforráscsoport "testGroup" című csoportjának eltávolítása</span><span class="sxs-lookup"><span data-stu-id="90e5f-112">Remove specific application insights api key that id is "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867" for resource "test" in resource group "testGroup".</span></span>

## <span data-ttu-id="90e5f-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="90e5f-113">PARAMETERS</span></span>

### <span data-ttu-id="90e5f-114">-ApiKeyId</span><span class="sxs-lookup"><span data-stu-id="90e5f-114">-ApiKeyId</span></span>
<span data-ttu-id="90e5f-115">Az alkalmazás betekintési API-kulcs azonosítója.</span><span class="sxs-lookup"><span data-stu-id="90e5f-115">Application Insights API Key ID.</span></span>

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

### <span data-ttu-id="90e5f-116">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="90e5f-116">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="90e5f-117">Az alkalmazás betekintése összetevő-objektum.</span><span class="sxs-lookup"><span data-stu-id="90e5f-117">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="90e5f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90e5f-118">-DefaultProfile</span></span>
<span data-ttu-id="90e5f-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="90e5f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90e5f-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="90e5f-120">-Name</span></span>
<span data-ttu-id="90e5f-121">Az alkalmazás betekintési összetevőjének neve.</span><span class="sxs-lookup"><span data-stu-id="90e5f-121">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="90e5f-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="90e5f-122">-PassThru</span></span>
<span data-ttu-id="90e5f-123">Ha a megadott művelet sikeres, akkor a True Write True értékre vált.</span><span class="sxs-lookup"><span data-stu-id="90e5f-123">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="90e5f-124">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="90e5f-124">This parameter is optional.</span></span> <span data-ttu-id="90e5f-125">Az alapértelmezett érték a hamis.</span><span class="sxs-lookup"><span data-stu-id="90e5f-125">Default value is false.</span></span>

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

### <span data-ttu-id="90e5f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90e5f-126">-ResourceGroupName</span></span>
<span data-ttu-id="90e5f-127">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="90e5f-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="90e5f-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="90e5f-128">-ResourceId</span></span>
<span data-ttu-id="90e5f-129">Az alkalmazás betekintési összetevőjének erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="90e5f-129">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="90e5f-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="90e5f-130">-Confirm</span></span>
<span data-ttu-id="90e5f-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="90e5f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90e5f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90e5f-132">-WhatIf</span></span>
<span data-ttu-id="90e5f-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="90e5f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90e5f-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="90e5f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90e5f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90e5f-135">CommonParameters</span></span>
<span data-ttu-id="90e5f-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="90e5f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90e5f-137">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90e5f-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90e5f-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="90e5f-138">INPUTS</span></span>

### <span data-ttu-id="90e5f-139">Microsoft. Azure. Command. ApplicationInsights. models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="90e5f-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="90e5f-140">System. String</span><span class="sxs-lookup"><span data-stu-id="90e5f-140">System.String</span></span>

## <span data-ttu-id="90e5f-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="90e5f-141">OUTPUTS</span></span>

### <span data-ttu-id="90e5f-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="90e5f-142">System.Boolean</span></span>

## <span data-ttu-id="90e5f-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="90e5f-143">NOTES</span></span>

## <span data-ttu-id="90e5f-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="90e5f-144">RELATED LINKS</span></span>
