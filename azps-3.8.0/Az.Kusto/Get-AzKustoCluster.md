---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Get-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Get-AzKustoCluster.md
ms.openlocfilehash: 6e24eaee77e8965ea34cbfcd8c169d675bce56d8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011134"
---
# <span data-ttu-id="339d7-101">Get-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="339d7-101">Get-AzKustoCluster</span></span>

## <span data-ttu-id="339d7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="339d7-102">SYNOPSIS</span></span>
<span data-ttu-id="339d7-103">Megtekintheti egy erőforráscsoport összes Kusto-szektorcsoportját, vagy egy bizonyos Kusto-fürtöt.</span><span class="sxs-lookup"><span data-stu-id="339d7-103">List all Kusto clusters in a resource group or get a specific Kusto cluster.</span></span>

## <span data-ttu-id="339d7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="339d7-104">SYNTAX</span></span>

### <span data-ttu-id="339d7-105">ByClusterOrResourceGroupOrSubscription (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="339d7-105">ByClusterOrResourceGroupOrSubscription (Default)</span></span>
```
Get-AzKustoCluster -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="339d7-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="339d7-106">ByResourceId</span></span>
```
Get-AzKustoCluster -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="339d7-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="339d7-107">DESCRIPTION</span></span>
<span data-ttu-id="339d7-108">Megtekintheti egy erőforráscsoport összes Kusto-szektorcsoportját, vagy egy bizonyos Kusto-fürtöt.</span><span class="sxs-lookup"><span data-stu-id="339d7-108">List all Kusto clusters in a resource group or get a specific Kusto cluster.</span></span>

## <span data-ttu-id="339d7-109">Példák</span><span class="sxs-lookup"><span data-stu-id="339d7-109">EXAMPLES</span></span>

### <span data-ttu-id="339d7-110">Példa 1 – egy erőforráscsoport összes Kusto listája</span><span class="sxs-lookup"><span data-stu-id="339d7-110">Example 1 - List all Kusto clusters in a resource group</span></span>

<span data-ttu-id="339d7-111">Írja be a következőt: Microsoft. Kusto/Clusters ID:/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster1 ResourceGroup: testrg név: mykustocluster1 hely: Közép-amerikai kapacitás: 3 SKU: D13_v2 ProvisioningState: sikeres állapot: futó címke: {} URI: https://mykustocluster1.centralus.kusto.windows.net DataIngestionUri: https://ingest-mykustocluster1.centralus.kusto.windows.net</span><span class="sxs-lookup"><span data-stu-id="339d7-111">Type              : Microsoft.Kusto/Clusters Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster1 ResourceGroup     : testrg Name              : mykustocluster1 Location          : Central US Capacity          : 3 Sku               : D13_v2 ProvisioningState : Succeeded State             : Running Tag               : {} Uri               : https://mykustocluster1.centralus.kusto.windows.net DataIngestionUri  : https://ingest-mykustocluster1.centralus.kusto.windows.net</span></span>

<span data-ttu-id="339d7-112">Írja be a következőt: Microsoft. Kusto/Clusters ID:/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster2 ResourceGroup: testrg név: mykustocluster2 hely: Közép-amerikai kapacitás: 5 SKU: D13_v2 ProvisioningState: sikeres állapot: futó címke: {} URI: https://mykustocluster2.centralus.kusto.windows.net DataIngestionUri: https://ingest-mykustocluster2.centralus.kusto.windows.net</span><span class="sxs-lookup"><span data-stu-id="339d7-112">Type              : Microsoft.Kusto/Clusters Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster2 ResourceGroup     : testrg Name              : mykustocluster2 Location          : Central US Capacity          : 5 Sku               : D13_v2 ProvisioningState : Succeeded State             : Running Tag               : {} Uri               : https://mykustocluster2.centralus.kusto.windows.net DataIngestionUri  : https://ingest-mykustocluster2.centralus.kusto.windows.net</span></span>


```
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg
```

<span data-ttu-id="339d7-113">A fenti parancs felsorolja az összes Kusto-szektorcsoportot az "testrg" erőforráscsoport csoportjában.</span><span class="sxs-lookup"><span data-stu-id="339d7-113">The above command lists all Kusto clusters in the resource group "testrg".</span></span>

### <span data-ttu-id="339d7-114">2 példa – adott Kusto-fürt beszerzése név alapján</span><span class="sxs-lookup"><span data-stu-id="339d7-114">Example 2 - Get a specific Kusto cluster by name</span></span>

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

<span data-ttu-id="339d7-115">A fenti parancs az "testrg" erőforráscsoport "mykustocluster" nevű Kusto-fürtöt számítja ki.</span><span class="sxs-lookup"><span data-stu-id="339d7-115">The above command returns the Kusto cluster named "mykustocluster" in the resource group "testrg".</span></span>

### <span data-ttu-id="339d7-116">3 példa – adott Kusto-fürt beszerzése erőforrás-azonosítóval</span><span class="sxs-lookup"><span data-stu-id="339d7-116">Example 3 - Get a specific Kusto cluster by resource id</span></span>

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

<span data-ttu-id="339d7-117">A fenti parancs az "testrg" erőforráscsoport "mykustocluster" nevű Kusto-fürtöt számítja ki.</span><span class="sxs-lookup"><span data-stu-id="339d7-117">The above command returns the Kusto cluster named "mykustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="339d7-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="339d7-118">PARAMETERS</span></span>

### <span data-ttu-id="339d7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="339d7-119">-DefaultProfile</span></span>
<span data-ttu-id="339d7-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="339d7-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="339d7-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="339d7-121">-Name</span></span>
<span data-ttu-id="339d7-122">Egy adott fürt neve.</span><span class="sxs-lookup"><span data-stu-id="339d7-122">Name of a specific cluster.</span></span>

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

### <span data-ttu-id="339d7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="339d7-123">-ResourceGroupName</span></span>
<span data-ttu-id="339d7-124">Annak az erőforráscsoportnek a neve, amelyben a felhasználó a fürtöt szeretné beolvasni.</span><span class="sxs-lookup"><span data-stu-id="339d7-124">Name of resource group under which the user wants to retrieve the cluster.</span></span>

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

### <span data-ttu-id="339d7-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="339d7-125">-ResourceId</span></span>
<span data-ttu-id="339d7-126">Kusto a cluster ResourceID.</span><span class="sxs-lookup"><span data-stu-id="339d7-126">Kusto cluster ResourceID.</span></span>

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

### <span data-ttu-id="339d7-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="339d7-127">CommonParameters</span></span>
<span data-ttu-id="339d7-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="339d7-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="339d7-129">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="339d7-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="339d7-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="339d7-130">INPUTS</span></span>

### <span data-ttu-id="339d7-131">System. String</span><span class="sxs-lookup"><span data-stu-id="339d7-131">System.String</span></span>

## <span data-ttu-id="339d7-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="339d7-132">OUTPUTS</span></span>

### <span data-ttu-id="339d7-133">Microsoft. Azure. Command. Kusto. models. PSKustoCluster</span><span class="sxs-lookup"><span data-stu-id="339d7-133">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="339d7-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="339d7-134">NOTES</span></span>

## <span data-ttu-id="339d7-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="339d7-135">RELATED LINKS</span></span>
