---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/remove-azurermapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Remove-AzureRmApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Remove-AzureRmApplicationInsights.md
ms.openlocfilehash: a440dd37d26bf65f4deb8c7e4c4535f6460f76be
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679302"
---
# <span data-ttu-id="3ca80-101">Remove-AzureRmApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="3ca80-101">Remove-AzureRmApplicationInsights</span></span>

## <span data-ttu-id="3ca80-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3ca80-102">SYNOPSIS</span></span>
<span data-ttu-id="3ca80-103">Alkalmazás-betekintési erőforrás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="3ca80-103">Remove an application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3ca80-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3ca80-104">SYNTAX</span></span>

### <span data-ttu-id="3ca80-105">ComponentNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3ca80-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzureRmApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ca80-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ca80-106">ComponentObjectParameterSet</span></span>
```
Remove-AzureRmApplicationInsights [-ApplicationInsightsComponent] <PSApplicationInsightsComponent> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ca80-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ca80-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmApplicationInsights [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ca80-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="3ca80-108">DESCRIPTION</span></span>
<span data-ttu-id="3ca80-109">Alkalmazás-betekintési erőforrás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="3ca80-109">Remove an application insights resource</span></span>

## <span data-ttu-id="3ca80-110">Példák</span><span class="sxs-lookup"><span data-stu-id="3ca80-110">EXAMPLES</span></span>

### <span data-ttu-id="3ca80-111">Példa 1 alkalmazás-betekintési erőforrás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="3ca80-111">Example 1 Remove an application insights resource</span></span>
```
PS C:\> Remove-AzureRmApplicationInsights -ResourceGroupName "testgroup" -Name "test" -PassThru
True
```

<span data-ttu-id="3ca80-112">A "teszt" nevű applciation-betekintési erőforrás eltávolítása a "testgroup" erőforráscsoporthoz</span><span class="sxs-lookup"><span data-stu-id="3ca80-112">Remove an applciation insights resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="3ca80-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3ca80-113">PARAMETERS</span></span>

### <span data-ttu-id="3ca80-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="3ca80-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="3ca80-115">Az alkalmazás betekintése összetevő-objektum.</span><span class="sxs-lookup"><span data-stu-id="3ca80-115">Application Insights Component Object.</span></span>

```yaml
Type: PSApplicationInsightsComponent
Parameter Sets: ComponentObjectParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3ca80-116">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3ca80-116">-Confirm</span></span>
<span data-ttu-id="3ca80-117">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3ca80-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ca80-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ca80-118">-DefaultProfile</span></span>
<span data-ttu-id="3ca80-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3ca80-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ca80-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3ca80-120">-Name</span></span>
<span data-ttu-id="3ca80-121">Az alkalmazás betekintési összetevőjének neve.</span><span class="sxs-lookup"><span data-stu-id="3ca80-121">Application Insights Component Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ca80-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3ca80-122">-PassThru</span></span>
<span data-ttu-id="3ca80-123">Ha a megadott művelet sikeres, akkor a True Write True értékre vált.</span><span class="sxs-lookup"><span data-stu-id="3ca80-123">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="3ca80-124">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="3ca80-124">This parameter is optional.</span></span> <span data-ttu-id="3ca80-125">Az alapértelmezett érték a hamis.</span><span class="sxs-lookup"><span data-stu-id="3ca80-125">Default value is false.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ca80-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ca80-126">-ResourceGroupName</span></span>
<span data-ttu-id="3ca80-127">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="3ca80-127">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ca80-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3ca80-128">-ResourceId</span></span>
<span data-ttu-id="3ca80-129">Az alkalmazás betekintési összetevőjének erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="3ca80-129">Application Insights Component Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ca80-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ca80-130">-WhatIf</span></span>
<span data-ttu-id="3ca80-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3ca80-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ca80-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3ca80-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ca80-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ca80-133">CommonParameters</span></span>
<span data-ttu-id="3ca80-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3ca80-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ca80-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ca80-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ca80-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3ca80-136">INPUTS</span></span>

### <span data-ttu-id="3ca80-137">System. String</span><span class="sxs-lookup"><span data-stu-id="3ca80-137">System.String</span></span>

## <span data-ttu-id="3ca80-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3ca80-138">OUTPUTS</span></span>

### <span data-ttu-id="3ca80-139">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="3ca80-139">System.Object</span></span>

## <span data-ttu-id="3ca80-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3ca80-140">NOTES</span></span>

## <span data-ttu-id="3ca80-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3ca80-141">RELATED LINKS</span></span>

