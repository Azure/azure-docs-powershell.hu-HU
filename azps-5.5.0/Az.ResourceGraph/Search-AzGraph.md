---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.dll-Help.xml
Module Name: Az.ResourceGraph
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcegraph/search-azgraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Search-AzGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Search-AzGraph.md
ms.openlocfilehash: e1d9aa5c9bf2538f20d37a23b35dec4d7a850cbc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100143579"
---
# <span data-ttu-id="adad9-101">Search-AzGraph</span><span class="sxs-lookup"><span data-stu-id="adad9-101">Search-AzGraph</span></span>

## <span data-ttu-id="adad9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="adad9-102">SYNOPSIS</span></span>
<span data-ttu-id="adad9-103">Lekérdezi az Azure Resource Manager által kezelt erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="adad9-103">Queries the resources managed by Azure Resource Manager.</span></span>

## <span data-ttu-id="adad9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="adad9-104">SYNTAX</span></span>

```
Search-AzGraph [-Query] <String> [-Subscription <String[]>] [-First <Int32>] [-Skip <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="adad9-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="adad9-105">DESCRIPTION</span></span>
<span data-ttu-id="adad9-106">További információ a lekérdezés szintaxisával kapcsolatban: https://aka.ms/resource-graph/learntoquery</span><span class="sxs-lookup"><span data-stu-id="adad9-106">Learn more about the query syntax here: https://aka.ms/resource-graph/learntoquery</span></span>

## <span data-ttu-id="adad9-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="adad9-107">EXAMPLES</span></span>

### <span data-ttu-id="adad9-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="adad9-108">Example 1</span></span>
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

<span data-ttu-id="adad9-109">Egyszerű erőforráslekérdezés, amely az erőforrásmezők egy részkészletét kéri.</span><span class="sxs-lookup"><span data-stu-id="adad9-109">Simple resources query requesting a subset of resource fields.</span></span>

### <span data-ttu-id="adad9-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="adad9-110">Example 2</span></span>
```powershell
PS C:\> Search-AzGraph "project id, name, type, location | where type =~ 'Microsoft.Compute/virtualMachines' | summarize count() by location | top 3 by count_"

location      count_
--------      ------
eastus            66
westcentralus     32
westus            26
```

<span data-ttu-id="adad9-111">Összetett lekérdezés az erőforrásokról, amelyek mezőkijelölést, szűrést és összegzést tartalmaznak.</span><span class="sxs-lookup"><span data-stu-id="adad9-111">A complex query on resources featuring field selection, filtering and summarizing.</span></span>

### <span data-ttu-id="adad9-112">3. példa</span><span class="sxs-lookup"><span data-stu-id="adad9-112">Example 3</span></span>
```powershell
PS C:\> Search-AzGraph -Include DisplayName -Query 'where type =~ "Microsoft.Compute/virtualMachines"| where properties.storageProfile.osDisk.managedDisk == "" | project name, resourceGroup, subscriptionDisplayName'

name         resourceGroup      subscriptionDisplayName
----         -------------      -----------------------
ContosoVM    RG-Contoso         Contoso Production Subscription                                               

```
<span data-ttu-id="adad9-113">Lekérdezés az összes olyan virtuális gépről, amely nem használ felügyelt lemezeket, és tartalmazza az előfizetés megjelenítendő nevét.</span><span class="sxs-lookup"><span data-stu-id="adad9-113">A query featuring all virtual machines which are not using Managed Disks and includes subscription display names.</span></span>

### <span data-ttu-id="adad9-114">4. példa</span><span class="sxs-lookup"><span data-stu-id="adad9-114">Example 4</span></span>
```powershell
PS C:\> Search-AzGraph -Include DisplayName -Query 'summarize count() by tenantDisplayName, subscriptionDisplayName'

tenantDisplayName   subscriptionDisplayName              count_
-----------------   -----------------------              ------
ContosoTenant       Contoso Production Subscription      118                                           
```
<span data-ttu-id="adad9-115">Egy lekérdezés, amely az erőforrások számát jeleníti meg bérlő és előfizetés megjelenítendő neve szerint.</span><span class="sxs-lookup"><span data-stu-id="adad9-115">A query displaying the count of resources by tenant and subscription display names.</span></span>

## <span data-ttu-id="adad9-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="adad9-116">PARAMETERS</span></span>

### <span data-ttu-id="adad9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adad9-117">-DefaultProfile</span></span>
<span data-ttu-id="adad9-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="adad9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="adad9-119">-Query</span><span class="sxs-lookup"><span data-stu-id="adad9-119">-Query</span></span>
<span data-ttu-id="adad9-120">Resource Graph-lekérdezés.</span><span class="sxs-lookup"><span data-stu-id="adad9-120">Resource Graph query.</span></span>

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

### <span data-ttu-id="adad9-121">-Előfizetés</span><span class="sxs-lookup"><span data-stu-id="adad9-121">-Subscription</span></span>
<span data-ttu-id="adad9-122">A lekérdezés futtatásához szükséges előfizetések.</span><span class="sxs-lookup"><span data-stu-id="adad9-122">Subscription(s) to run query against.</span></span>

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

### <span data-ttu-id="adad9-123">-Skip</span><span class="sxs-lookup"><span data-stu-id="adad9-123">-Skip</span></span>
<span data-ttu-id="adad9-124">Figyelmen kívül hagyja az első N objektumot, majd beveszi a fennmaradó objektumokat.</span><span class="sxs-lookup"><span data-stu-id="adad9-124">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="adad9-125">-First</span><span class="sxs-lookup"><span data-stu-id="adad9-125">-First</span></span>
<span data-ttu-id="adad9-126">A vissza nem térhet objektumok maximális száma.</span><span class="sxs-lookup"><span data-stu-id="adad9-126">The maximum number of objects to return.</span></span> <span data-ttu-id="adad9-127">Engedélyezett értékek: 1-5000.</span><span class="sxs-lookup"><span data-stu-id="adad9-127">Allowed values: 1-5000.</span></span>
<span data-ttu-id="adad9-128">Az alapértelmezett érték 100.</span><span class="sxs-lookup"><span data-stu-id="adad9-128">Default value is 100.</span></span>

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

### <span data-ttu-id="adad9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adad9-129">CommonParameters</span></span>
<span data-ttu-id="adad9-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="adad9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adad9-131">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="adad9-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adad9-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="adad9-132">INPUTS</span></span>

### <span data-ttu-id="adad9-133">Nincs</span><span class="sxs-lookup"><span data-stu-id="adad9-133">None</span></span>

## <span data-ttu-id="adad9-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="adad9-134">OUTPUTS</span></span>

### <span data-ttu-id="adad9-135">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="adad9-135">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="adad9-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="adad9-136">NOTES</span></span>

## <span data-ttu-id="adad9-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="adad9-137">RELATED LINKS</span></span>
