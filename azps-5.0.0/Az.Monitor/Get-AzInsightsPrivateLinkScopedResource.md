---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azinsightsprivatelinkscopedresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScopedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScopedResource.md
ms.openlocfilehash: f3d00ba82bbafce42cca49c60d443cd244f83df3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195763"
---
# <span data-ttu-id="4620c-101">Get-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="4620c-101">Get-AzInsightsPrivateLinkScopedResource</span></span>

## <span data-ttu-id="4620c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4620c-102">SYNOPSIS</span></span>
<span data-ttu-id="4620c-103">A magánjellegű kapcsolat hatókörű erőforrásának beszerzése</span><span class="sxs-lookup"><span data-stu-id="4620c-103">Get for private link scoped resource</span></span>

## <span data-ttu-id="4620c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4620c-104">SYNTAX</span></span>

### <span data-ttu-id="4620c-105">ByScopeParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4620c-105">ByScopeParameterSet (Default)</span></span>
```
Get-AzInsightsPrivateLinkScopedResource -ResourceGroupName <String> -ScopeName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4620c-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4620c-106">ByInputObjectParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScopedResource [-Name <String>] -InputObject <PSMonitorPrivateLinkScope>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4620c-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4620c-107">ByResourceIdParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScopedResource -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4620c-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="4620c-108">DESCRIPTION</span></span>
<span data-ttu-id="4620c-109">A magánjellegű kapcsolat hatókörű erőforrásának beolvasása vagy listázása, a hatókörben lévő erőforrás lehet naplózási Analytics munkaterületet vagy alkalmazás-keresési összetevőt.</span><span class="sxs-lookup"><span data-stu-id="4620c-109">Get or list for private link scoped resource, scoped resource could be Log Analytics workspace or Application Insights component</span></span>

## <span data-ttu-id="4620c-110">Példák</span><span class="sxs-lookup"><span data-stu-id="4620c-110">EXAMPLES</span></span>

### <span data-ttu-id="4620c-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4620c-111">Example 1</span></span>
```powershell
Get-AzInsightsPrivateLinkScopedResource -ResourceGroupName "rg_name" -ScopeName "scope_name"
```

<span data-ttu-id="4620c-112">Lista hatókörű erőforrás a privát hivatkozás hatóköre "scope_name"</span><span class="sxs-lookup"><span data-stu-id="4620c-112">List scoped resource under private link scope "scope_name"</span></span>

### <span data-ttu-id="4620c-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="4620c-113">Example 2</span></span>
```powershell
Get-AzInsightsPrivateLinkScopedResource -ResourceGroupName "rg_name" -ScopeName "scope_name" -Name "scoped_resource_name"
```

<span data-ttu-id="4620c-114">A "scope_name" név "scoped_resource_name" nevű "a magánjellegű hivatkozás hatóköre" területének beolvasása</span><span class="sxs-lookup"><span data-stu-id="4620c-114">Get scoped resource under private link scope "scope_name" with name "scoped_resource_name"</span></span>

## <span data-ttu-id="4620c-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4620c-115">PARAMETERS</span></span>

### <span data-ttu-id="4620c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4620c-116">-DefaultProfile</span></span>
<span data-ttu-id="4620c-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4620c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4620c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4620c-118">-InputObject</span></span>
<span data-ttu-id="4620c-119">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="4620c-119">PSMonitorPrivateLinkScope</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4620c-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4620c-120">-Name</span></span>
<span data-ttu-id="4620c-121">Hatókörben lévő erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="4620c-121">Scoped resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByScopeParameterSet, ByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4620c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4620c-122">-ResourceGroupName</span></span>
<span data-ttu-id="4620c-123">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="4620c-123">Resource Group Name</span></span>

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

### <span data-ttu-id="4620c-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4620c-124">-ResourceId</span></span>
<span data-ttu-id="4620c-125">Erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="4620c-125">Resource Id</span></span>

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

### <span data-ttu-id="4620c-126">-ScopeName</span><span class="sxs-lookup"><span data-stu-id="4620c-126">-ScopeName</span></span>
<span data-ttu-id="4620c-127">Magánjellegű hivatkozás hatókörének neve</span><span class="sxs-lookup"><span data-stu-id="4620c-127">Private Link Scope Name</span></span>

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

### <span data-ttu-id="4620c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4620c-128">CommonParameters</span></span>
<span data-ttu-id="4620c-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4620c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4620c-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4620c-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4620c-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4620c-131">INPUTS</span></span>

### <span data-ttu-id="4620c-132">System. String</span><span class="sxs-lookup"><span data-stu-id="4620c-132">System.String</span></span>

## <span data-ttu-id="4620c-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4620c-133">OUTPUTS</span></span>

### <span data-ttu-id="4620c-134">icrosoft. Azure. Command. detekintést. OutputClasses. PSMonitorPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="4620c-134">icrosoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScopedResource</span></span>

## <span data-ttu-id="4620c-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4620c-135">NOTES</span></span>

## <span data-ttu-id="4620c-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4620c-136">RELATED LINKS</span></span>
