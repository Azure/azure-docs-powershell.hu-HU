---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Get-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Get-AzKustoCluster.md
ms.openlocfilehash: c5c7cdffc8b329fdff426f48f60869ca6821f32d
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100401351"
---
# <span data-ttu-id="c5fec-101">Get-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="c5fec-101">Get-AzKustoCluster</span></span>

## <span data-ttu-id="c5fec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5fec-102">SYNOPSIS</span></span>
<span data-ttu-id="c5fec-103">List all Kusto clusters in a resource group or get a specific Kusto cluster.</span><span class="sxs-lookup"><span data-stu-id="c5fec-103">List all Kusto clusters in a resource group or get a specific Kusto cluster.</span></span>

## <span data-ttu-id="c5fec-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c5fec-104">SYNTAX</span></span>

### <span data-ttu-id="c5fec-105">ByClusterOrResourceGroupOrSubscription (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c5fec-105">ByClusterOrResourceGroupOrSubscription (Default)</span></span>
```
Get-AzKustoCluster -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c5fec-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c5fec-106">ByResourceId</span></span>
```
Get-AzKustoCluster -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c5fec-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c5fec-107">DESCRIPTION</span></span>
<span data-ttu-id="c5fec-108">List all Kusto clusters in a resource group or get a specific Kusto cluster.</span><span class="sxs-lookup"><span data-stu-id="c5fec-108">List all Kusto clusters in a resource group or get a specific Kusto cluster.</span></span>

## <span data-ttu-id="c5fec-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c5fec-109">EXAMPLES</span></span>

### <span data-ttu-id="c5fec-110">1. példa : Egy erőforráscsoport összes Kusto-fürtének felsorolása</span><span class="sxs-lookup"><span data-stu-id="c5fec-110">Example 1 - List all Kusto clusters in a resource group</span></span>

<span data-ttu-id="c5fec-111">Típus: Microsoft.Kusto/Clusters Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster1 ResourceGroup: testrg Name: mykustocluster1 Location: Central US Capacity: 3 Termékváltozat: D13_v2 ProvisioningState: Sikeres állam: Running Tag : {} Uri : `https://mykustocluster1.centralus.kusto.windows.net` DataIngestionUri : `https://ingest-mykustocluster1.centralus.kusto.windows.net`</span><span class="sxs-lookup"><span data-stu-id="c5fec-111">Type              : Microsoft.Kusto/Clusters Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster1 ResourceGroup     : testrg Name              : mykustocluster1 Location          : Central US Capacity          : 3 Sku               : D13_v2 ProvisioningState : Succeeded State             : Running Tag               : {} Uri               : `https://mykustocluster1.centralus.kusto.windows.net` DataIngestionUri  : `https://ingest-mykustocluster1.centralus.kusto.windows.net`</span></span>

<span data-ttu-id="c5fec-112">Típus: Microsoft.Kusto/Clusters Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster2 ResourceGroup: testrg Name: mykustocluster2 Location: Central US Capacity : 5 Termékváltozat: D13_v2 ProvisioningState: Sikeres állam: Running Tag : {} Uri : `https://mykustocluster2.centralus.kusto.windows.net` DataIngestionUri : `https://ingest-mykustocluster2.centralus.kusto.windows.net`</span><span class="sxs-lookup"><span data-stu-id="c5fec-112">Type              : Microsoft.Kusto/Clusters Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster2 ResourceGroup     : testrg Name              : mykustocluster2 Location          : Central US Capacity          : 5 Sku               : D13_v2 ProvisioningState : Succeeded State             : Running Tag               : {} Uri               : `https://mykustocluster2.centralus.kusto.windows.net` DataIngestionUri  : `https://ingest-mykustocluster2.centralus.kusto.windows.net`</span></span>


```
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg
```

<span data-ttu-id="c5fec-113">A fenti parancs felsorolja a "testrg" erőforráscsoport összes Kusto-fürtöt.</span><span class="sxs-lookup"><span data-stu-id="c5fec-113">The above command lists all Kusto clusters in the resource group "testrg".</span></span>

### <span data-ttu-id="c5fec-114">2. példa : Adott Kusto-fürt lekérte név szerint</span><span class="sxs-lookup"><span data-stu-id="c5fec-114">Example 2 - Get a specific Kusto cluster by name</span></span>

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

<span data-ttu-id="c5fec-115">A fenti parancs a "testrg" erőforráscsoportban a "mykustocluster" nevű Kusto-fürtöt adja vissza.</span><span class="sxs-lookup"><span data-stu-id="c5fec-115">The above command returns the Kusto cluster named "mykustocluster" in the resource group "testrg".</span></span>

### <span data-ttu-id="c5fec-116">3. példa: Adott Kusto-fürt lekérte erőforrás-azonosító szerint</span><span class="sxs-lookup"><span data-stu-id="c5fec-116">Example 3 - Get a specific Kusto cluster by resource id</span></span>

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

<span data-ttu-id="c5fec-117">A fenti parancs a "testrg" erőforráscsoportban a "mykustocluster" nevű Kusto-fürtöt adja vissza.</span><span class="sxs-lookup"><span data-stu-id="c5fec-117">The above command returns the Kusto cluster named "mykustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="c5fec-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c5fec-118">PARAMETERS</span></span>

### <span data-ttu-id="c5fec-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5fec-119">-DefaultProfile</span></span>
<span data-ttu-id="c5fec-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c5fec-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5fec-121">-Name</span><span class="sxs-lookup"><span data-stu-id="c5fec-121">-Name</span></span>
<span data-ttu-id="c5fec-122">Egy adott fürt neve.</span><span class="sxs-lookup"><span data-stu-id="c5fec-122">Name of a specific cluster.</span></span>

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

### <span data-ttu-id="c5fec-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5fec-123">-ResourceGroupName</span></span>
<span data-ttu-id="c5fec-124">Annak az erőforráscsoportnak a neve, amely alatt a felhasználó le szeretné kéri a fürtöt.</span><span class="sxs-lookup"><span data-stu-id="c5fec-124">Name of resource group under which the user wants to retrieve the cluster.</span></span>

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

### <span data-ttu-id="c5fec-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c5fec-125">-ResourceId</span></span>
<span data-ttu-id="c5fec-126">Kusto cluster ResourceID.</span><span class="sxs-lookup"><span data-stu-id="c5fec-126">Kusto cluster ResourceID.</span></span>

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

### <span data-ttu-id="c5fec-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5fec-127">CommonParameters</span></span>
<span data-ttu-id="c5fec-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5fec-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5fec-129">További információt a about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5fec-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5fec-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c5fec-130">INPUTS</span></span>

### <span data-ttu-id="c5fec-131">System.String</span><span class="sxs-lookup"><span data-stu-id="c5fec-131">System.String</span></span>

## <span data-ttu-id="c5fec-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c5fec-132">OUTPUTS</span></span>

### <span data-ttu-id="c5fec-133">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span><span class="sxs-lookup"><span data-stu-id="c5fec-133">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="c5fec-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c5fec-134">NOTES</span></span>

## <span data-ttu-id="c5fec-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c5fec-135">RELATED LINKS</span></span>
