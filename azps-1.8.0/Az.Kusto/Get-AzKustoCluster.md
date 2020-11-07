---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Get-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Get-AzKustoCluster.md
ms.openlocfilehash: a68604e9701a6ae2c251edf3f2a0935df5ffa94f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835582"
---
# <span data-ttu-id="af7a4-101">Get-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="af7a4-101">Get-AzKustoCluster</span></span>

## <span data-ttu-id="af7a4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="af7a4-102">SYNOPSIS</span></span>
<span data-ttu-id="af7a4-103">Megtekintheti egy erőforráscsoport összes Kusto-szektorcsoportját, vagy egy bizonyos Kusto-fürtöt.</span><span class="sxs-lookup"><span data-stu-id="af7a4-103">List all Kusto clusters in a resource group or get a specific Kusto cluster.</span></span>

## <span data-ttu-id="af7a4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="af7a4-104">SYNTAX</span></span>

### <span data-ttu-id="af7a4-105">ByClusterOrResourceGroupOrSubscription (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="af7a4-105">ByClusterOrResourceGroupOrSubscription (Default)</span></span>
```
Get-AzKustoCluster -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="af7a4-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="af7a4-106">ByResourceId</span></span>
```
Get-AzKustoCluster -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af7a4-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="af7a4-107">DESCRIPTION</span></span>
<span data-ttu-id="af7a4-108">Megtekintheti egy erőforráscsoport összes Kusto-szektorcsoportját, vagy egy bizonyos Kusto-fürtöt.</span><span class="sxs-lookup"><span data-stu-id="af7a4-108">List all Kusto clusters in a resource group or get a specific Kusto cluster.</span></span>

## <span data-ttu-id="af7a4-109">Példák</span><span class="sxs-lookup"><span data-stu-id="af7a4-109">EXAMPLES</span></span>

### <span data-ttu-id="af7a4-110">Példa 1 – egy erőforráscsoport összes Kusto listája</span><span class="sxs-lookup"><span data-stu-id="af7a4-110">Example 1 - List all Kusto clusters in a resource group</span></span>

<span data-ttu-id="af7a4-111">Írja be a következőt: Microsoft. Kusto/Clusters ID:/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster1 ResourceGroup: testrg név: mykustocluster1 hely: Közép-amerikai kapacitás: 3 SKU: D13_v2 ProvisioningState: sikeres állapot: futó címke: {} URI: https://mykustocluster1.centralus.kusto.windows.net DataIngestionUri: https://ingest-mykustocluster1.centralus.kusto.windows.net</span><span class="sxs-lookup"><span data-stu-id="af7a4-111">Type              : Microsoft.Kusto/Clusters Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster1 ResourceGroup     : testrg Name              : mykustocluster1 Location          : Central US Capacity          : 3 Sku               : D13_v2 ProvisioningState : Succeeded State             : Running Tag               : {} Uri               : https://mykustocluster1.centralus.kusto.windows.net DataIngestionUri  : https://ingest-mykustocluster1.centralus.kusto.windows.net</span></span>

<span data-ttu-id="af7a4-112">Írja be a következőt: Microsoft. Kusto/Clusters ID:/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster2 ResourceGroup: testrg név: mykustocluster2 hely: Közép-amerikai kapacitás: 5 SKU: D13_v2 ProvisioningState: sikeres állapot: futó címke: {} URI: https://mykustocluster2.centralus.kusto.windows.net DataIngestionUri: https://ingest-mykustocluster2.centralus.kusto.windows.net</span><span class="sxs-lookup"><span data-stu-id="af7a4-112">Type              : Microsoft.Kusto/Clusters Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster2 ResourceGroup     : testrg Name              : mykustocluster2 Location          : Central US Capacity          : 5 Sku               : D13_v2 ProvisioningState : Succeeded State             : Running Tag               : {} Uri               : https://mykustocluster2.centralus.kusto.windows.net DataIngestionUri  : https://ingest-mykustocluster2.centralus.kusto.windows.net</span></span>


```
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg
```

<span data-ttu-id="af7a4-113">A fenti parancs felsorolja az összes Kusto-szektorcsoportot az "testrg" erőforráscsoport csoportjában.</span><span class="sxs-lookup"><span data-stu-id="af7a4-113">The above command lists all Kusto clusters in the resource group "testrg".</span></span>

### <span data-ttu-id="af7a4-114">2 példa – adott Kusto-fürt beszerzése név alapján</span><span class="sxs-lookup"><span data-stu-id="af7a4-114">Example 2 - Get a specific Kusto cluster by name</span></span>

```
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster

Type              : Microsoft.Kusto/Clusters
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster
ResourceGroup     : testrg
Name              : mykustocluster
Location          : Central US
Capacity          : 5
Sku               : D13_v2
ProvisioningState : Succeeded
State             : Running
Tag               : {}
Uri               : https://mykustocluster.centralus.kusto.windows.net
DataIngestionUri  : https://ingest-mykustocluster.centralus.kusto.windows.net
```

<span data-ttu-id="af7a4-115">A fenti parancs az "testrg" erőforráscsoport "mykustocluster" nevű Kusto-fürtöt számítja ki.</span><span class="sxs-lookup"><span data-stu-id="af7a4-115">The above command returns the Kusto cluster named "mykustocluster" in the resource group "testrg".</span></span>

### <span data-ttu-id="af7a4-116">3 példa – adott Kusto-fürt beszerzése erőforrás-azonosítóval</span><span class="sxs-lookup"><span data-stu-id="af7a4-116">Example 3 - Get a specific Kusto cluster by resource id</span></span>

```
PS C:\> Get-AzKustoCluster -ResourceId /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/clusters/mykustocluster
Type              : Microsoft.Kusto/Clusters
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster
ResourceGroup     : testrg
Name              : mykustocluster
Location          : Central US
Capacity          : 5
Sku               : D13_v2
ProvisioningState : Succeeded
State             : Running
Tag               : {}
Uri               : https://mykustocluster.centralus.kusto.windows.net
DataIngestionUri  : https://ingest-mykustocluster.centralus.kusto.windows.net
```

<span data-ttu-id="af7a4-117">A fenti parancs az "testrg" erőforráscsoport "mykustocluster" nevű Kusto-fürtöt számítja ki.</span><span class="sxs-lookup"><span data-stu-id="af7a4-117">The above command returns the Kusto cluster named "mykustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="af7a4-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="af7a4-118">PARAMETERS</span></span>

### <span data-ttu-id="af7a4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af7a4-119">-DefaultProfile</span></span>
<span data-ttu-id="af7a4-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="af7a4-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af7a4-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="af7a4-121">-Name</span></span>
<span data-ttu-id="af7a4-122">Egy adott fürt neve.</span><span class="sxs-lookup"><span data-stu-id="af7a4-122">Name of a specific cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByClusterOrResourceGroupOrSubscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af7a4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af7a4-123">-ResourceGroupName</span></span>
<span data-ttu-id="af7a4-124">Annak az erőforráscsoportnek a neve, amelyben a felhasználó a fürtöt szeretné beolvasni.</span><span class="sxs-lookup"><span data-stu-id="af7a4-124">Name of resource group under which the user wants to retrieve the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByClusterOrResourceGroupOrSubscription
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af7a4-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="af7a4-125">-ResourceId</span></span>
<span data-ttu-id="af7a4-126">Kusto a cluster ResourceID.</span><span class="sxs-lookup"><span data-stu-id="af7a4-126">Kusto cluster ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af7a4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af7a4-127">CommonParameters</span></span>
<span data-ttu-id="af7a4-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="af7a4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af7a4-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af7a4-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af7a4-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="af7a4-130">INPUTS</span></span>

### <span data-ttu-id="af7a4-131">System. String</span><span class="sxs-lookup"><span data-stu-id="af7a4-131">System.String</span></span>

## <span data-ttu-id="af7a4-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="af7a4-132">OUTPUTS</span></span>

### <span data-ttu-id="af7a4-133">Microsoft. Azure. Command. Kusto. models. PSKustoCluster</span><span class="sxs-lookup"><span data-stu-id="af7a4-133">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="af7a4-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="af7a4-134">NOTES</span></span>

## <span data-ttu-id="af7a4-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="af7a4-135">RELATED LINKS</span></span>
