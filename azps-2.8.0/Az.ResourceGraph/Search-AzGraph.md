---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.dll-Help.xml
Module Name: Az.ResourceGraph
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcegraph/search-azgraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Search-AzGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Search-AzGraph.md
ms.openlocfilehash: 5a9a47ff6f4a329d3e48ec54df85ade3be5ae84d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838185"
---
# <span data-ttu-id="474d0-101">Search-AzGraph</span><span class="sxs-lookup"><span data-stu-id="474d0-101">Search-AzGraph</span></span>

## <span data-ttu-id="474d0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="474d0-102">SYNOPSIS</span></span>
<span data-ttu-id="474d0-103">Lekérdezi az Azure Resource Manager által kezelt erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="474d0-103">Queries the resources managed by Azure Resource Manager.</span></span>

## <span data-ttu-id="474d0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="474d0-104">SYNTAX</span></span>

```
Search-AzGraph [-Query] <String> [-Subscription <String[]>] [-First <Int32>] [-Skip <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="474d0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="474d0-105">DESCRIPTION</span></span>
<span data-ttu-id="474d0-106">További információ a lekérdezési szintaxisról: https://aka.ms/resource-graph/learntoquery</span><span class="sxs-lookup"><span data-stu-id="474d0-106">Learn more about the query syntax here: https://aka.ms/resource-graph/learntoquery</span></span>

## <span data-ttu-id="474d0-107">Példák</span><span class="sxs-lookup"><span data-stu-id="474d0-107">EXAMPLES</span></span>

### <span data-ttu-id="474d0-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="474d0-108">Example 1</span></span>
```powershell
PS C:\> Search-AzGraph "project id, name, type, location, tags" -First 3


id         : /subscriptions/1ef51df4-f8a9-4b69-9919-1ef51df4eff6/resourceGroups/Service-INT-a/providers/Microsoft.Compute/virtualMachineScaleSets/nt
name       : nt
type       : microsoft.compute/virtualmachinescalesets
location   : eastus
tags       : @{resourceType=Service Fabric; clusterName=gov-art-int-nt-a}

id         : /subscriptions/1ef51df4-f8a9-4b69-9919-1ef51df4eff6/resourceGroups/Service-INT-a/providers/Microsoft.EventGrid/topics/egtopic-1
name       : egtopic-1
type       : microsoft.eventgrid/topics
location   : westus2
tags       :
```

<span data-ttu-id="474d0-109">Egyszerű erőforrások lekérdezése: az erőforrásmezők egy alcsoportját kéri.</span><span class="sxs-lookup"><span data-stu-id="474d0-109">Simple resources query requesting a subset of resource fields.</span></span>

### <span data-ttu-id="474d0-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="474d0-110">Example 2</span></span>
```powershell
PS C:\> Search-AzGraph "project id, name, type, location | where type =~ 'Microsoft.Compute/virtualMachines' | summarize count() by location | top 3 by count_"

location      count_
--------      ------
eastus            66
westcentralus     32
westus            26
```

<span data-ttu-id="474d0-111">Komplex lekérdezés a mezők kijelöléséről, szűréséről és összegzéséről.</span><span class="sxs-lookup"><span data-stu-id="474d0-111">A complex query on resources featuring field selection, filtering and summarizing.</span></span>

## <span data-ttu-id="474d0-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="474d0-112">PARAMETERS</span></span>

### <span data-ttu-id="474d0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="474d0-113">-DefaultProfile</span></span>
<span data-ttu-id="474d0-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="474d0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="474d0-115">-Query</span><span class="sxs-lookup"><span data-stu-id="474d0-115">-Query</span></span>
<span data-ttu-id="474d0-116">Erőforrás-grafikon lekérdezése</span><span class="sxs-lookup"><span data-stu-id="474d0-116">Resource Graph query.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="474d0-117">-Előfizetés</span><span class="sxs-lookup"><span data-stu-id="474d0-117">-Subscription</span></span>
<span data-ttu-id="474d0-118">Előfizetés (ek) a lekérdezés futtatásához.</span><span class="sxs-lookup"><span data-stu-id="474d0-118">Subscription(s) to run query against.</span></span>

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

### <span data-ttu-id="474d0-119">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="474d0-119">-Skip</span></span>
<span data-ttu-id="474d0-120">Figyelmen kívül hagyja az első N objektumokat, és a fennmaradó objektumokat kapja.</span><span class="sxs-lookup"><span data-stu-id="474d0-120">Ignores the first N objects and then gets the remaining objects.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="474d0-121">– Első</span><span class="sxs-lookup"><span data-stu-id="474d0-121">-First</span></span>
<span data-ttu-id="474d0-122">A visszaadni kívánt objektumok maximális száma.</span><span class="sxs-lookup"><span data-stu-id="474d0-122">The maximum number of objects to return.</span></span> <span data-ttu-id="474d0-123">Engedélyezett értékek: 1-5000.</span><span class="sxs-lookup"><span data-stu-id="474d0-123">Allowed values: 1-5000.</span></span>
<span data-ttu-id="474d0-124">Az alapértelmezett érték a 100.</span><span class="sxs-lookup"><span data-stu-id="474d0-124">Default value is 100.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="474d0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="474d0-125">CommonParameters</span></span>
<span data-ttu-id="474d0-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="474d0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="474d0-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="474d0-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="474d0-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="474d0-128">INPUTS</span></span>

### <span data-ttu-id="474d0-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="474d0-129">None</span></span>

## <span data-ttu-id="474d0-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="474d0-130">OUTPUTS</span></span>

### <span data-ttu-id="474d0-131">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="474d0-131">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="474d0-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="474d0-132">NOTES</span></span>

## <span data-ttu-id="474d0-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="474d0-133">RELATED LINKS</span></span>
