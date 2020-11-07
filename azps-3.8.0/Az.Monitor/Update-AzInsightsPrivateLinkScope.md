---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/update-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: 93e97906fc7e985d522f5af9d678392741a9022b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845081"
---
# <span data-ttu-id="b5ee1-101">Update-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="b5ee1-101">Update-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="b5ee1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b5ee1-102">SYNOPSIS</span></span>
<span data-ttu-id="b5ee1-103">A magánjellegű hivatkozás hatókörének frissítése</span><span class="sxs-lookup"><span data-stu-id="b5ee1-103">Update for private link scope</span></span>

## <span data-ttu-id="b5ee1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b5ee1-104">SYNTAX</span></span>

### <span data-ttu-id="b5ee1-105">ByResourceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b5ee1-105">ByResourceNameParameterSet (Default)</span></span>
```
Update-AzInsightsPrivateLinkScope -ResourceGroupName <String> -Name <String> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5ee1-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5ee1-106">ByResourceIdParameterSet</span></span>
```
Update-AzInsightsPrivateLinkScope -ResourceId <String> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5ee1-107">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5ee1-107">ByInputObjectParameterSet</span></span>
```
Update-AzInsightsPrivateLinkScope -InputObject <PSMonitorPrivateLinkScope> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5ee1-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="b5ee1-108">DESCRIPTION</span></span>
<span data-ttu-id="b5ee1-109">A magánjellegű hivatkozás hatókörének frissítése</span><span class="sxs-lookup"><span data-stu-id="b5ee1-109">Update for private link scope</span></span>

## <span data-ttu-id="b5ee1-110">Példák</span><span class="sxs-lookup"><span data-stu-id="b5ee1-110">EXAMPLES</span></span>

### <span data-ttu-id="b5ee1-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b5ee1-111">Example 1</span></span>
```powershell
Update-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name" -Tags "key:value"
```

<span data-ttu-id="b5ee1-112">a privát hivatkozás hatókörének frissítése "scope_name" névvel a "kulcs: érték" nevű erőforráscsoport "rg_name" csoportjában</span><span class="sxs-lookup"><span data-stu-id="b5ee1-112">update private link scope with name "scope_name" under resource group "rg_name" to use tag "key:value"</span></span>

### <span data-ttu-id="b5ee1-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="b5ee1-113">Example 2</span></span>
```powershell
Update-AzInsightsPrivateLinkScope -ResourceId "/subscriptions/{subscriptionId}/resourceGroups/rg_name/providers/microsoft.insights/privateLinkScopes/scope_name" -Tags "key:value"
```

<span data-ttu-id="b5ee1-114">a privát hivatkozás hatókörének frissítése erőforrás-azonosítóval a "kulcs: érték" címke használatához</span><span class="sxs-lookup"><span data-stu-id="b5ee1-114">update private link scope with resource Id to use tag "key:value"</span></span>

### <span data-ttu-id="b5ee1-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="b5ee1-115">Example 3</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name" | Update-AzInsightsPrivateLinkScope -Tags "key:value"
```

<span data-ttu-id="b5ee1-116">a privát hivatkozás hatókörének frissítése a bemeneti privát hivatkozás hatóköre objektummal a "kulcs: érték" címke használatára</span><span class="sxs-lookup"><span data-stu-id="b5ee1-116">update private link scope with input private link scope object to use tag "key:value"</span></span>

## <span data-ttu-id="b5ee1-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b5ee1-117">PARAMETERS</span></span>

### <span data-ttu-id="b5ee1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5ee1-118">-DefaultProfile</span></span>
<span data-ttu-id="b5ee1-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b5ee1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5ee1-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b5ee1-120">-InputObject</span></span>
<span data-ttu-id="b5ee1-121">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="b5ee1-121">PSMonitorPrivateLinkScope</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b5ee1-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b5ee1-122">-Name</span></span>
<span data-ttu-id="b5ee1-123">Magánjellegű hivatkozás hatókörének neve</span><span class="sxs-lookup"><span data-stu-id="b5ee1-123">Private Link Scope Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5ee1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5ee1-124">-ResourceGroupName</span></span>
<span data-ttu-id="b5ee1-125">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="b5ee1-125">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5ee1-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b5ee1-126">-ResourceId</span></span>
<span data-ttu-id="b5ee1-127">Erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="b5ee1-127">Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5ee1-128">-Címkék</span><span class="sxs-lookup"><span data-stu-id="b5ee1-128">-Tags</span></span>
<span data-ttu-id="b5ee1-129">Címkék</span><span class="sxs-lookup"><span data-stu-id="b5ee1-129">Tags</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5ee1-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b5ee1-130">-Confirm</span></span>
<span data-ttu-id="b5ee1-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b5ee1-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5ee1-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5ee1-132">-WhatIf</span></span>
<span data-ttu-id="b5ee1-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b5ee1-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5ee1-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b5ee1-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5ee1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5ee1-135">CommonParameters</span></span>
<span data-ttu-id="b5ee1-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b5ee1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5ee1-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b5ee1-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5ee1-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b5ee1-138">INPUTS</span></span>

### <span data-ttu-id="b5ee1-139">Microsoft. Azure. commands. OutputClasses. PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="b5ee1-139">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="b5ee1-140">System. String</span><span class="sxs-lookup"><span data-stu-id="b5ee1-140">System.String</span></span>

## <span data-ttu-id="b5ee1-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b5ee1-141">OUTPUTS</span></span>

### <span data-ttu-id="b5ee1-142">Microsoft. Azure. commands. OutputClasses. PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="b5ee1-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

## <span data-ttu-id="b5ee1-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b5ee1-143">NOTES</span></span>

## <span data-ttu-id="b5ee1-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b5ee1-144">RELATED LINKS</span></span>
