---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Get-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Get-AzKustoDatabase.md
ms.openlocfilehash: f78dd41283312434f8a3ea833f9c96df6527cb95
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011133"
---
# <span data-ttu-id="9b919-101">Get-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="9b919-101">Get-AzKustoDatabase</span></span>

## <span data-ttu-id="9b919-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9b919-102">SYNOPSIS</span></span>
<span data-ttu-id="9b919-103">Az összes Kusto-adatbázis listázása egy fürtben vagy egy bizonyos Kusto-adatbázis beszerzése.</span><span class="sxs-lookup"><span data-stu-id="9b919-103">List all Kusto databases in a cluster or get a specific Kusto database.</span></span>

## <span data-ttu-id="9b919-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9b919-104">SYNTAX</span></span>

### <span data-ttu-id="9b919-105">ByClusterOrResourceGroupOrSubscription (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9b919-105">ByClusterOrResourceGroupOrSubscription (Default)</span></span>
```
Get-AzKustoDatabase -ResourceGroupName <String> -ClusterName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b919-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="9b919-106">ByResourceId</span></span>
```
Get-AzKustoDatabase [-Name <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9b919-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="9b919-107">ByInputObject</span></span>
```
Get-AzKustoDatabase [-Name <String>] -InputObject <PSKustoCluster> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9b919-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="9b919-108">DESCRIPTION</span></span>
<span data-ttu-id="9b919-109">Az összes Kusto-adatbázis listázása egy fürtben vagy egy bizonyos Kusto-adatbázis beszerzése.</span><span class="sxs-lookup"><span data-stu-id="9b919-109">List all Kusto databases in a cluster or get a specific Kusto database.</span></span>

## <span data-ttu-id="9b919-110">Példák</span><span class="sxs-lookup"><span data-stu-id="9b919-110">EXAMPLES</span></span>

### <span data-ttu-id="9b919-111">Példa 1 – az összes Kusto-adatbázis listázása egy fürtben név szerint</span><span class="sxs-lookup"><span data-stu-id="9b919-111">Example 1 - List all Kusto databases in a cluster by name</span></span>

```
PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName mykustocluster

Name                   : mykustocluster/mykustodatabase1
SoftDeletePeriodInDays : 3650
HotCachePeriodInDays   : 31
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase1
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases

Name                   : mykustocluster/mykustodatabase2
SoftDeletePeriodInDays : 3650
HotCachePeriodInDays   : 31
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase2
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="9b919-112">A fenti parancs visszaadott minden Kusto-adatbázist a "mykustocluster" ("") szektorcsoportban, az "testrg" erőforráscsoport nevében.</span><span class="sxs-lookup"><span data-stu-id="9b919-112">The above command returns all Kusto databases in the cluster "mykustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="9b919-113">Példa: 2 – a fürtökben lévő összes Kusto-adatbázis listázása</span><span class="sxs-lookup"><span data-stu-id="9b919-113">Example 2 - List all Kusto databases in a cluster by piping</span></span>

```
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster | Get-AzKustoDatabase
Name                   : mykustocluster/mykustodatabase1
SoftDeletePeriodInDays : 3650
HotCachePeriodInDays   : 31
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase1
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases

Name                   : mykustocluster/mykustodatabase2
SoftDeletePeriodInDays : 3650
HotCachePeriodInDays   : 31
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase2
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="9b919-114">A fenti parancs a mykustocluster "testrg" nevű erőforráscsoport "" nevű Kusto-fürtöt jeleníti meg a `Get-AzKustoCluster` parancsmag használatával, és az eredményt a `Get-AzKustoDatabase` parancsmagot használva a fürt összes adatbázisát listázhatja.</span><span class="sxs-lookup"><span data-stu-id="9b919-114">The above command will get the Kusto cluster named "mykustocluster" found in the resource group "testrg" using the `Get-AzKustoCluster` cmdlet, and pipe the result to the `Get-AzKustoDatabase` cmdlet to list all databases in that cluster.</span></span>

### <span data-ttu-id="9b919-115">3 példa – adott Kusto-adatbázis beszerzése név alapján</span><span class="sxs-lookup"><span data-stu-id="9b919-115">Example 3 - Get a specific Kusto database by name</span></span>

```
PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName mykustocluster -Name mykustodatabase

Name                   : mykustocluster/mykustodatabase
SoftDeletePeriodInDays : 3650
HotCachePeriodInDays   : 31
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="9b919-116">A fenti parancs az "testrg" erőforráscsoport "mykustocluster" nevű "mykustodatabase" nevű Kusto-adatbázisát jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="9b919-116">The above command returns the Kusto database named "mykustodatabase" in the cluster "mykustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="9b919-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9b919-117">PARAMETERS</span></span>

### <span data-ttu-id="9b919-118">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="9b919-118">-ClusterName</span></span>
<span data-ttu-id="9b919-119">Annak a fürtnek a neve, amelyben az adatbázis létezik.</span><span class="sxs-lookup"><span data-stu-id="9b919-119">Name of cluster under which the database exists.</span></span>

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

### <span data-ttu-id="9b919-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b919-120">-DefaultProfile</span></span>
<span data-ttu-id="9b919-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9b919-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b919-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9b919-122">-InputObject</span></span>
<span data-ttu-id="9b919-123">Kusto.</span><span class="sxs-lookup"><span data-stu-id="9b919-123">Kusto cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9b919-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9b919-124">-Name</span></span>
<span data-ttu-id="9b919-125">az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="9b919-125">the name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b919-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b919-126">-ResourceGroupName</span></span>
<span data-ttu-id="9b919-127">Annak az erőforráscsoportnek a neve, amelyben a felhasználó a fürtöt szeretné beolvasni.</span><span class="sxs-lookup"><span data-stu-id="9b919-127">Name of resource group under which the user wants to retrieve the cluster.</span></span>

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

### <span data-ttu-id="9b919-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9b919-128">-ResourceId</span></span>
<span data-ttu-id="9b919-129">Kusto a cluster ResourceID.</span><span class="sxs-lookup"><span data-stu-id="9b919-129">Kusto cluster ResourceID.</span></span>

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

### <span data-ttu-id="9b919-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b919-130">CommonParameters</span></span>
<span data-ttu-id="9b919-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9b919-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b919-132">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b919-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b919-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9b919-133">INPUTS</span></span>

### <span data-ttu-id="9b919-134">System. String</span><span class="sxs-lookup"><span data-stu-id="9b919-134">System.String</span></span>

### <span data-ttu-id="9b919-135">Microsoft. Azure. Command. Kusto. models. PSKustoCluster</span><span class="sxs-lookup"><span data-stu-id="9b919-135">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="9b919-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9b919-136">OUTPUTS</span></span>

### <span data-ttu-id="9b919-137">Microsoft. Azure. Command. Kusto. models. PSKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="9b919-137">Microsoft.Azure.Commands.Kusto.Models.PSKustoDatabase</span></span>

## <span data-ttu-id="9b919-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9b919-138">NOTES</span></span>

## <span data-ttu-id="9b919-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9b919-139">RELATED LINKS</span></span>
