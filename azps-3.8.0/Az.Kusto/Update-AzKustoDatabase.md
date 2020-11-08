---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/update-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Update-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Update-AzKustoDatabase.md
ms.openlocfilehash: 858578d36f2f913f903f86b9c556a93d30e2e3b3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011114"
---
# <span data-ttu-id="6799f-101">Update-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="6799f-101">Update-AzKustoDatabase</span></span>

## <span data-ttu-id="6799f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6799f-102">SYNOPSIS</span></span>
<span data-ttu-id="6799f-103">Meglévő Kusto-adatbázis frissítése</span><span class="sxs-lookup"><span data-stu-id="6799f-103">Update an existing Kusto database.</span></span>

## <span data-ttu-id="6799f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6799f-104">SYNTAX</span></span>

### <span data-ttu-id="6799f-105">ByNameAndResourceGroup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6799f-105">ByNameAndResourceGroup (Default)</span></span>
```
Update-AzKustoDatabase [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-SoftDeletePeriodInDays <Int32>] [-HotCachePeriodInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6799f-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6799f-106">ByResourceId</span></span>
```
Update-AzKustoDatabase [-SoftDeletePeriodInDays <Int32>] [-HotCachePeriodInDays <Int32>] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6799f-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="6799f-107">ByInputObject</span></span>
```
Update-AzKustoDatabase [-SoftDeletePeriodInDays <Int32>] [-HotCachePeriodInDays <Int32>]
 [-InputObject] <PSKustoDatabase> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6799f-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="6799f-108">DESCRIPTION</span></span>
<span data-ttu-id="6799f-109">Meglévő Kusto-adatbázis frissítése</span><span class="sxs-lookup"><span data-stu-id="6799f-109">Update an existing Kusto database.</span></span>

## <span data-ttu-id="6799f-110">Példák</span><span class="sxs-lookup"><span data-stu-id="6799f-110">EXAMPLES</span></span>

### <span data-ttu-id="6799f-111">Példa 1 – létező adatbázis frissítése név szerint</span><span class="sxs-lookup"><span data-stu-id="6799f-111">Example 1 - Update an existing database by name</span></span>

```
PS C:\> Update-AzKustoDatabase -ResourceGroupName testrg -ClusterName mykustocluster -Name mykustodatabase -SoftDeletePeriodInDays 5

Name                   : mykustocluster/mykustodatabase
SoftDeletePeriodInDays : 5
HotCachePeriodInDays   : 2
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="6799f-112">A fenti parancs frissíti a "mykustodatabase" Kusto-adatbázis Soft törlési időszakát az "testrg" erőforráscsoport "mykustocluster" csoportjában.</span><span class="sxs-lookup"><span data-stu-id="6799f-112">The above command updates the soft deletion period of the Kusto database "mykustodatabase" in the cluster "mykustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="6799f-113">2. példa: meglévő adatbázis frissítése csővezetéken</span><span class="sxs-lookup"><span data-stu-id="6799f-113">Example 2 - Update an existing database by piping</span></span>

```
PS C:\> PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName mykustocluster -Name mykustodatabase | Update-AzKustoDatabase -SoftDeletePeriodInDays 5

Name                   : mykustocluster/mykustodatabase
SoftDeletePeriodInDays : 5
HotCachePeriodInDays   : 2
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="6799f-114">A fenti parancs a "mykustodatabase" Kusto-adatbázist kapja a "mykustocluster" erőforráscsoport "testrg" `Get-AzKustoDatabase` , a parancsmag segítségével, majd a csöveket az eredmény az `Update-AzKustoDatabase` adatbázis Soft törlési időszakának öt napig történő frissítéséhez.</span><span class="sxs-lookup"><span data-stu-id="6799f-114">The above command gets the Kusto database "mykustodatabase" in the cluster "mykustocluster" found in the resource group "testrg" using the `Get-AzKustoDatabase` cmdlet, and then pipes the result to `Update-AzKustoDatabase` to update the database's soft deletion period to five days.</span></span>

## <span data-ttu-id="6799f-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6799f-115">PARAMETERS</span></span>

### <span data-ttu-id="6799f-116">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="6799f-116">-ClusterName</span></span>
<span data-ttu-id="6799f-117">Annak a fürtnek a neve, amelyben az adatbázis létezik</span><span class="sxs-lookup"><span data-stu-id="6799f-117">Name of cluster under which the database exists</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6799f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6799f-118">-DefaultProfile</span></span>
<span data-ttu-id="6799f-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6799f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6799f-120">-HotCachePeriodInDays</span><span class="sxs-lookup"><span data-stu-id="6799f-120">-HotCachePeriodInDays</span></span>
<span data-ttu-id="6799f-121">Azoknak a napoknak a száma, amelyeket az adatgyorsítótárban meg kell őrizni a Fast lekérdezésekhez</span><span class="sxs-lookup"><span data-stu-id="6799f-121">The number of days that data should be kept in cache for fast queries</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6799f-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6799f-122">-InputObject</span></span>
<span data-ttu-id="6799f-123">Kusto adatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="6799f-123">Kusto database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Kusto.Models.PSKustoDatabase
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6799f-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6799f-124">-Name</span></span>
<span data-ttu-id="6799f-125">A frissítendő adatbázis neve</span><span class="sxs-lookup"><span data-stu-id="6799f-125">Name of the database to update</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6799f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6799f-126">-ResourceGroupName</span></span>
<span data-ttu-id="6799f-127">Annak az erőforráscsoport-csoportnak a neve, amelyben a fürt létezik.</span><span class="sxs-lookup"><span data-stu-id="6799f-127">Name of resource group under which the cluster exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6799f-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6799f-128">-ResourceId</span></span>
<span data-ttu-id="6799f-129">Kusto adatbázis-ResourceID.</span><span class="sxs-lookup"><span data-stu-id="6799f-129">Kusto database ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6799f-130">-SoftDeletePeriodInDays</span><span class="sxs-lookup"><span data-stu-id="6799f-130">-SoftDeletePeriodInDays</span></span>
<span data-ttu-id="6799f-131">Azoknak a napoknak a száma, amelyeket a lekérdezések hozzáférhetősége előtt meg kell őrizni.</span><span class="sxs-lookup"><span data-stu-id="6799f-131">The number of days that data should be kept before it stops being accessible to queries</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6799f-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6799f-132">-Confirm</span></span>
<span data-ttu-id="6799f-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6799f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6799f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6799f-134">-WhatIf</span></span>
<span data-ttu-id="6799f-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6799f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6799f-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6799f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6799f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6799f-137">CommonParameters</span></span>
<span data-ttu-id="6799f-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6799f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6799f-139">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6799f-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6799f-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6799f-140">INPUTS</span></span>

### <span data-ttu-id="6799f-141">System. String</span><span class="sxs-lookup"><span data-stu-id="6799f-141">System.String</span></span>

### <span data-ttu-id="6799f-142">Microsoft. Azure. Command. Kusto. models. PSKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="6799f-142">Microsoft.Azure.Commands.Kusto.Models.PSKustoDatabase</span></span>

## <span data-ttu-id="6799f-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6799f-143">OUTPUTS</span></span>

### <span data-ttu-id="6799f-144">Microsoft. Azure. Command. Kusto. models. PSKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="6799f-144">Microsoft.Azure.Commands.Kusto.Models.PSKustoDatabase</span></span>

## <span data-ttu-id="6799f-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6799f-145">NOTES</span></span>

## <span data-ttu-id="6799f-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6799f-146">RELATED LINKS</span></span>
