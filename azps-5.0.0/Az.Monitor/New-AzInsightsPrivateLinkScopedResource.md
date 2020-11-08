---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azinsightsprivatelinkscopedresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScopedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScopedResource.md
ms.openlocfilehash: fd4dc0dd771029951da4ae375141cc526301de34
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194570"
---
# <span data-ttu-id="4c1fa-101">New-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="4c1fa-101">New-AzInsightsPrivateLinkScopedResource</span></span>

## <span data-ttu-id="4c1fa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4c1fa-102">SYNOPSIS</span></span>
<span data-ttu-id="4c1fa-103">létrehozás a magánjellegű kapcsolat hatókörű erőforráshoz</span><span class="sxs-lookup"><span data-stu-id="4c1fa-103">create for private link scoped resource</span></span>

## <span data-ttu-id="4c1fa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4c1fa-104">SYNTAX</span></span>

### <span data-ttu-id="4c1fa-105">ByResourceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4c1fa-105">ByResourceNameParameterSet (Default)</span></span>
```
New-AzInsightsPrivateLinkScopedResource -LinkedResourceId <String> -ResourceGroupName <String>
 -ScopeName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4c1fa-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4c1fa-106">ByInputObjectParameterSet</span></span>
```
New-AzInsightsPrivateLinkScopedResource -LinkedResourceId <String> -Name <String>
 -InputObject <PSMonitorPrivateLinkScope> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4c1fa-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="4c1fa-107">DESCRIPTION</span></span>
<span data-ttu-id="4c1fa-108">Create for Private link scoped Resource, scope-erőforrás lehet naplózni az elemzési munkaterületet vagy az alkalmazási elemzések összetevőt.</span><span class="sxs-lookup"><span data-stu-id="4c1fa-108">create for private link scoped resource, scoped resource could be Log Analytics workspace or Application Insights component</span></span>

## <span data-ttu-id="4c1fa-109">Példák</span><span class="sxs-lookup"><span data-stu-id="4c1fa-109">EXAMPLES</span></span>

### <span data-ttu-id="4c1fa-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4c1fa-110">Example 1</span></span>
```powershell
$ai = Get-AzApplicationInsights -ResourceGroupName "rg_name" -Name "ai_name"

New-AzInsightsPrivateLinkScopedResource -LinkedResourceId $ai.Id -ResourceGroupName "rg_name" -ScopeName "scope_name" -Name "scoped_resource_name"
```

<span data-ttu-id="4c1fa-111">"scoped_resource_name" hatókörű erőforrás létrehozása az alkalmazás-betekintési összetevőhöz "ai_name" hivatkozással</span><span class="sxs-lookup"><span data-stu-id="4c1fa-111">create scoped resource "scoped_resource_name" linked to application insights component "ai_name"</span></span>

## <span data-ttu-id="4c1fa-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4c1fa-112">PARAMETERS</span></span>

### <span data-ttu-id="4c1fa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c1fa-113">-DefaultProfile</span></span>
<span data-ttu-id="4c1fa-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4c1fa-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c1fa-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4c1fa-115">-InputObject</span></span>
<span data-ttu-id="4c1fa-116">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="4c1fa-116">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="4c1fa-117">-LinkedResourceId</span><span class="sxs-lookup"><span data-stu-id="4c1fa-117">-LinkedResourceId</span></span>
<span data-ttu-id="4c1fa-118">Hivatkozás a LA/AI erőforrás-azonosítóra</span><span class="sxs-lookup"><span data-stu-id="4c1fa-118">LA/AI Resource Id to Link</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c1fa-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4c1fa-119">-Name</span></span>
<span data-ttu-id="4c1fa-120">Hatókörben lévő erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="4c1fa-120">Scoped resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c1fa-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c1fa-121">-ResourceGroupName</span></span>
<span data-ttu-id="4c1fa-122">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="4c1fa-122">Resource Group Name</span></span>

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

### <span data-ttu-id="4c1fa-123">-ScopeName</span><span class="sxs-lookup"><span data-stu-id="4c1fa-123">-ScopeName</span></span>
<span data-ttu-id="4c1fa-124">Magánjellegű hivatkozás hatókörének neve</span><span class="sxs-lookup"><span data-stu-id="4c1fa-124">Private Link Scope Name</span></span>

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

### <span data-ttu-id="4c1fa-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4c1fa-125">-Confirm</span></span>
<span data-ttu-id="4c1fa-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4c1fa-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c1fa-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c1fa-127">-WhatIf</span></span>
<span data-ttu-id="4c1fa-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4c1fa-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c1fa-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4c1fa-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c1fa-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c1fa-130">CommonParameters</span></span>
<span data-ttu-id="4c1fa-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4c1fa-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c1fa-132">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4c1fa-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c1fa-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4c1fa-133">INPUTS</span></span>

### <span data-ttu-id="4c1fa-134">Microsoft. Azure. commands. OutputClasses. PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="4c1fa-134">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="4c1fa-135">System. String</span><span class="sxs-lookup"><span data-stu-id="4c1fa-135">System.String</span></span>

## <span data-ttu-id="4c1fa-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4c1fa-136">OUTPUTS</span></span>

### <span data-ttu-id="4c1fa-137">Microsoft. Azure. commands. OutputClasses. PSMonitorPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="4c1fa-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScopedResource</span></span>

## <span data-ttu-id="4c1fa-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4c1fa-138">NOTES</span></span>

## <span data-ttu-id="4c1fa-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4c1fa-139">RELATED LINKS</span></span>