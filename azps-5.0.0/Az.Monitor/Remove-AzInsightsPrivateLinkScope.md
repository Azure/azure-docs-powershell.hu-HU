---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: 358eb796a156949520cf8cf0c073ee08a6537e2f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195615"
---
# <span data-ttu-id="344bb-101">Remove-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="344bb-101">Remove-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="344bb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="344bb-102">SYNOPSIS</span></span>
<span data-ttu-id="344bb-103">a magánjellegű hivatkozás törlése hatókör</span><span class="sxs-lookup"><span data-stu-id="344bb-103">delete private link scope</span></span>

## <span data-ttu-id="344bb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="344bb-104">SYNTAX</span></span>

### <span data-ttu-id="344bb-105">ByResourceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="344bb-105">ByResourceNameParameterSet (Default)</span></span>
```
Remove-AzInsightsPrivateLinkScope -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="344bb-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="344bb-106">ByResourceIdParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScope -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="344bb-107">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="344bb-107">ByInputObjectParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScope -InputObject <PSMonitorPrivateLinkScope>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="344bb-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="344bb-108">DESCRIPTION</span></span>
<span data-ttu-id="344bb-109">a magánjellegű hivatkozás törlése hatókör</span><span class="sxs-lookup"><span data-stu-id="344bb-109">delete private link scope</span></span>

## <span data-ttu-id="344bb-110">Példák</span><span class="sxs-lookup"><span data-stu-id="344bb-110">EXAMPLES</span></span>

### <span data-ttu-id="344bb-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="344bb-111">Example 1</span></span>
```powershell
Remove-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name"
```

<span data-ttu-id="344bb-112">a privát hivatkozás törlése "scope_name" névvel az erőforráscsoport "rg_name" csoportjában</span><span class="sxs-lookup"><span data-stu-id="344bb-112">delete private link scope with name "scope_name" under resource group "rg_name"</span></span>

### <span data-ttu-id="344bb-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="344bb-113">Example 2</span></span>
```powershell
Remove-AzInsightsPrivateLinkScope -ResourceId "/subscriptions/{subscriptionId}/resourceGroups/rg_name/providers/microsoft.insights/privateLinkScopes/scope_name"
```

<span data-ttu-id="344bb-114">a magánjellegű hivatkozás hatókörének törlése az erőforrás-azonosítóval</span><span class="sxs-lookup"><span data-stu-id="344bb-114">delete private link scope with resource Id</span></span>

### <span data-ttu-id="344bb-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="344bb-115">Example 3</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name" | Remove-AzInsightsPrivateLinkScope
```

<span data-ttu-id="344bb-116">a magánjellegű hivatkozás hatókörének törlése az input Private link scope objektummal</span><span class="sxs-lookup"><span data-stu-id="344bb-116">delete private link scope with input private link scope object</span></span>

## <span data-ttu-id="344bb-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="344bb-117">PARAMETERS</span></span>

### <span data-ttu-id="344bb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="344bb-118">-DefaultProfile</span></span>
<span data-ttu-id="344bb-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="344bb-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="344bb-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="344bb-120">-InputObject</span></span>
<span data-ttu-id="344bb-121">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="344bb-121">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="344bb-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="344bb-122">-Name</span></span>
<span data-ttu-id="344bb-123">Magánjellegű hivatkozás hatókörének neve</span><span class="sxs-lookup"><span data-stu-id="344bb-123">Private Link Scope Name</span></span>

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

### <span data-ttu-id="344bb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="344bb-124">-ResourceGroupName</span></span>
<span data-ttu-id="344bb-125">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="344bb-125">Resource Group Name</span></span>

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

### <span data-ttu-id="344bb-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="344bb-126">-ResourceId</span></span>
<span data-ttu-id="344bb-127">Erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="344bb-127">Resource Id</span></span>

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

### <span data-ttu-id="344bb-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="344bb-128">-Confirm</span></span>
<span data-ttu-id="344bb-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="344bb-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="344bb-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="344bb-130">-WhatIf</span></span>
<span data-ttu-id="344bb-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="344bb-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="344bb-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="344bb-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="344bb-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="344bb-133">CommonParameters</span></span>
<span data-ttu-id="344bb-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="344bb-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="344bb-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="344bb-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="344bb-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="344bb-136">INPUTS</span></span>

### <span data-ttu-id="344bb-137">Microsoft. Azure. commands. OutputClasses. PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="344bb-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="344bb-138">System. String</span><span class="sxs-lookup"><span data-stu-id="344bb-138">System.String</span></span>

## <span data-ttu-id="344bb-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="344bb-139">OUTPUTS</span></span>

### <span data-ttu-id="344bb-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="344bb-140">System.Boolean</span></span>

## <span data-ttu-id="344bb-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="344bb-141">NOTES</span></span>

## <span data-ttu-id="344bb-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="344bb-142">RELATED LINKS</span></span>
