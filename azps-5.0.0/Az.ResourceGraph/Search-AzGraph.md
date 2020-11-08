---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.dll-Help.xml
Module Name: Az.ResourceGraph
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcegraph/search-azgraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Search-AzGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Search-AzGraph.md
ms.openlocfilehash: e1d9aa5c9bf2538f20d37a23b35dec4d7a850cbc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194185"
---
# <span data-ttu-id="19b3f-101">Search-AzGraph</span><span class="sxs-lookup"><span data-stu-id="19b3f-101">Search-AzGraph</span></span>

## <span data-ttu-id="19b3f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="19b3f-102">SYNOPSIS</span></span>
<span data-ttu-id="19b3f-103">Lekérdezi az Azure Resource Manager által kezelt erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="19b3f-103">Queries the resources managed by Azure Resource Manager.</span></span>

## <span data-ttu-id="19b3f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="19b3f-104">SYNTAX</span></span>

```
Search-AzGraph [-Query] <String> [-Subscription <String[]>] [-First <Int32>] [-Skip <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19b3f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="19b3f-105">DESCRIPTION</span></span>
<span data-ttu-id="19b3f-106">További információ a lekérdezési szintaxisról: https://aka.ms/resource-graph/learntoquery</span><span class="sxs-lookup"><span data-stu-id="19b3f-106">Learn more about the query syntax here: https://aka.ms/resource-graph/learntoquery</span></span>

## <span data-ttu-id="19b3f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="19b3f-107">EXAMPLES</span></span>

### <span data-ttu-id="19b3f-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="19b3f-108">Example 1</span></span>
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

<span data-ttu-id="19b3f-109">Egyszerű erőforrások lekérdezése: az erőforrásmezők egy alcsoportját kéri.</span><span class="sxs-lookup"><span data-stu-id="19b3f-109">Simple resources query requesting a subset of resource fields.</span></span>

### <span data-ttu-id="19b3f-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="19b3f-110">Example 2</span></span>
```powershell
PS C:\> Search-AzGraph "project id, name, type, location | where type =~ 'Microsoft.Compute/virtualMachines' | summarize count() by location | top 3 by count_"

location      count_
--------      ------
eastus            66
westcentralus     32
westus            26
```

<span data-ttu-id="19b3f-111">Komplex lekérdezés a mezők kijelöléséről, szűréséről és összegzéséről.</span><span class="sxs-lookup"><span data-stu-id="19b3f-111">A complex query on resources featuring field selection, filtering and summarizing.</span></span>

### <span data-ttu-id="19b3f-112">3. példa</span><span class="sxs-lookup"><span data-stu-id="19b3f-112">Example 3</span></span>
```powershell
PS C:\> Search-AzGraph -Include DisplayName -Query 'where type =~ "Microsoft.Compute/virtualMachines"| where properties.storageProfile.osDisk.managedDisk == "" | project name, resourceGroup, subscriptionDisplayName'

name         resourceGroup      subscriptionDisplayName
----         -------------      -----------------------
ContosoVM    RG-Contoso         Contoso Production Subscription                                               

```
<span data-ttu-id="19b3f-113">Egy olyan lekérdezés, amely minden olyan virtuális gépet tartalmaz, amely nem használ kezelt lemezeket, és tartalmazza az előfizetés megjelenítendő nevét.</span><span class="sxs-lookup"><span data-stu-id="19b3f-113">A query featuring all virtual machines which are not using Managed Disks and includes subscription display names.</span></span>

### <span data-ttu-id="19b3f-114">4. példa</span><span class="sxs-lookup"><span data-stu-id="19b3f-114">Example 4</span></span>
```powershell
PS C:\> Search-AzGraph -Include DisplayName -Query 'summarize count() by tenantDisplayName, subscriptionDisplayName'

tenantDisplayName   subscriptionDisplayName              count_
-----------------   -----------------------              ------
ContosoTenant       Contoso Production Subscription      118                                           
```
<span data-ttu-id="19b3f-115">Egy lekérdezés, amely az erőforrások számát jeleníti meg a bérlői és az előfizetéses megjelenítendő nevek alapján.</span><span class="sxs-lookup"><span data-stu-id="19b3f-115">A query displaying the count of resources by tenant and subscription display names.</span></span>

## <span data-ttu-id="19b3f-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="19b3f-116">PARAMETERS</span></span>

### <span data-ttu-id="19b3f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19b3f-117">-DefaultProfile</span></span>
<span data-ttu-id="19b3f-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="19b3f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19b3f-119">-Query</span><span class="sxs-lookup"><span data-stu-id="19b3f-119">-Query</span></span>
<span data-ttu-id="19b3f-120">Erőforrás-grafikon lekérdezése</span><span class="sxs-lookup"><span data-stu-id="19b3f-120">Resource Graph query.</span></span>

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

### <span data-ttu-id="19b3f-121">-Előfizetés</span><span class="sxs-lookup"><span data-stu-id="19b3f-121">-Subscription</span></span>
<span data-ttu-id="19b3f-122">Előfizetés (ek) a lekérdezés futtatásához.</span><span class="sxs-lookup"><span data-stu-id="19b3f-122">Subscription(s) to run query against.</span></span>

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

### <span data-ttu-id="19b3f-123">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="19b3f-123">-Skip</span></span>
<span data-ttu-id="19b3f-124">Figyelmen kívül hagyja az első N objektumokat, és a fennmaradó objektumokat kapja.</span><span class="sxs-lookup"><span data-stu-id="19b3f-124">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="19b3f-125">– Első</span><span class="sxs-lookup"><span data-stu-id="19b3f-125">-First</span></span>
<span data-ttu-id="19b3f-126">A visszaadni kívánt objektumok maximális száma.</span><span class="sxs-lookup"><span data-stu-id="19b3f-126">The maximum number of objects to return.</span></span> <span data-ttu-id="19b3f-127">Engedélyezett értékek: 1-5000.</span><span class="sxs-lookup"><span data-stu-id="19b3f-127">Allowed values: 1-5000.</span></span>
<span data-ttu-id="19b3f-128">Az alapértelmezett érték a 100.</span><span class="sxs-lookup"><span data-stu-id="19b3f-128">Default value is 100.</span></span>

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

### <span data-ttu-id="19b3f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19b3f-129">CommonParameters</span></span>
<span data-ttu-id="19b3f-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="19b3f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19b3f-131">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19b3f-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19b3f-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="19b3f-132">INPUTS</span></span>

### <span data-ttu-id="19b3f-133">Nincs</span><span class="sxs-lookup"><span data-stu-id="19b3f-133">None</span></span>

## <span data-ttu-id="19b3f-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="19b3f-134">OUTPUTS</span></span>

### <span data-ttu-id="19b3f-135">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="19b3f-135">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="19b3f-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="19b3f-136">NOTES</span></span>

## <span data-ttu-id="19b3f-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="19b3f-137">RELATED LINKS</span></span>