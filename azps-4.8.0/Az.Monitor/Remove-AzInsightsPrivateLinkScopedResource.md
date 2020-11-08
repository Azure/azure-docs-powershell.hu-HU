---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azinsightsprivatelinkscopedresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScopedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScopedResource.md
ms.openlocfilehash: cd71f1561525f166736b708caf4905fdefd443ce
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181617"
---
# <span data-ttu-id="658c6-101">Remove-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="658c6-101">Remove-AzInsightsPrivateLinkScopedResource</span></span>

## <span data-ttu-id="658c6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="658c6-102">SYNOPSIS</span></span>
<span data-ttu-id="658c6-103">a magánjellegű kapcsolat hatókörű erőforrásának törlése</span><span class="sxs-lookup"><span data-stu-id="658c6-103">delete for private link scoped resource</span></span>

## <span data-ttu-id="658c6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="658c6-104">SYNTAX</span></span>

### <span data-ttu-id="658c6-105">ByScopeParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="658c6-105">ByScopeParameterSet (Default)</span></span>
```
Remove-AzInsightsPrivateLinkScopedResource -ResourceGroupName <String> -ScopeName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="658c6-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="658c6-106">ByInputObjectParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScopedResource -Name <String> -InputObject <PSMonitorPrivateLinkScope>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="658c6-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="658c6-107">ByResourceIdParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScopedResource -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="658c6-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="658c6-108">DESCRIPTION</span></span>
<span data-ttu-id="658c6-109">a magánjellegű kapcsolat hatókörű erőforrásának törlése</span><span class="sxs-lookup"><span data-stu-id="658c6-109">delete for private link scoped resource</span></span>

## <span data-ttu-id="658c6-110">Példák</span><span class="sxs-lookup"><span data-stu-id="658c6-110">EXAMPLES</span></span>

### <span data-ttu-id="658c6-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="658c6-111">Example 1</span></span>
```powershell
Remove-AzInsightsPrivateLinkScopedResource -ResourceGroupName "rg_name" -ScopeName "scope_name" -Name "scoped_resource_name"
```

<span data-ttu-id="658c6-112">a magánjellegű kapcsolat hatókörű erőforrás törlése</span><span class="sxs-lookup"><span data-stu-id="658c6-112">delete private link scoped resource</span></span>

## <span data-ttu-id="658c6-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="658c6-113">PARAMETERS</span></span>

### <span data-ttu-id="658c6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="658c6-114">-DefaultProfile</span></span>
<span data-ttu-id="658c6-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="658c6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="658c6-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="658c6-116">-InputObject</span></span>
<span data-ttu-id="658c6-117">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="658c6-117">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="658c6-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="658c6-118">-Name</span></span>
<span data-ttu-id="658c6-119">Hatókörben lévő erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="658c6-119">Scoped resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByScopeParameterSet, ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="658c6-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="658c6-120">-ResourceGroupName</span></span>
<span data-ttu-id="658c6-121">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="658c6-121">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByScopeParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="658c6-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="658c6-122">-ResourceId</span></span>
<span data-ttu-id="658c6-123">Erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="658c6-123">Resource Id</span></span>

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

### <span data-ttu-id="658c6-124">-ScopeName</span><span class="sxs-lookup"><span data-stu-id="658c6-124">-ScopeName</span></span>
<span data-ttu-id="658c6-125">Magánjellegű hivatkozás hatókörének neve</span><span class="sxs-lookup"><span data-stu-id="658c6-125">Private Link Scope Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByScopeParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="658c6-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="658c6-126">-Confirm</span></span>
<span data-ttu-id="658c6-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="658c6-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="658c6-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="658c6-128">-WhatIf</span></span>
<span data-ttu-id="658c6-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="658c6-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="658c6-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="658c6-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="658c6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="658c6-131">CommonParameters</span></span>
<span data-ttu-id="658c6-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="658c6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="658c6-133">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="658c6-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="658c6-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="658c6-134">INPUTS</span></span>

### <span data-ttu-id="658c6-135">Microsoft. Azure. commands. OutputClasses. PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="658c6-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="658c6-136">System. String</span><span class="sxs-lookup"><span data-stu-id="658c6-136">System.String</span></span>

## <span data-ttu-id="658c6-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="658c6-137">OUTPUTS</span></span>

### <span data-ttu-id="658c6-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="658c6-138">System.Boolean</span></span>

## <span data-ttu-id="658c6-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="658c6-139">NOTES</span></span>

## <span data-ttu-id="658c6-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="658c6-140">RELATED LINKS</span></span>
