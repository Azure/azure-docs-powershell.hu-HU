---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/New-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/New-AzKustoDatabase.md
ms.openlocfilehash: ed039eefe46a1527948e7fffc3030f209a91b0c7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011131"
---
# <span data-ttu-id="f45ac-101">New-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="f45ac-101">New-AzKustoDatabase</span></span>

## <span data-ttu-id="f45ac-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f45ac-102">SYNOPSIS</span></span>
<span data-ttu-id="f45ac-103">Új Kusto-adatbázis létrehozása meglévő fürtben.</span><span class="sxs-lookup"><span data-stu-id="f45ac-103">Creates a new Kusto database in an existing cluster.</span></span>

## <span data-ttu-id="f45ac-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f45ac-104">SYNTAX</span></span>

### <span data-ttu-id="f45ac-105">ByNameAndResourceGroup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f45ac-105">ByNameAndResourceGroup (Default)</span></span>
```
New-AzKustoDatabase [-ResourceGroupName] <String> [-ClusterName] <String> -Name <String>
 -SoftDeletePeriodInDays <Int32> -HotCachePeriodInDays <Int32> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f45ac-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f45ac-106">ByResourceId</span></span>
```
New-AzKustoDatabase -Name <String> -SoftDeletePeriodInDays <Int32> -HotCachePeriodInDays <Int32>
 [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f45ac-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="f45ac-107">ByInputObject</span></span>
```
New-AzKustoDatabase -Name <String> -SoftDeletePeriodInDays <Int32> -HotCachePeriodInDays <Int32>
 [-InputObject] <PSKustoCluster> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f45ac-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="f45ac-108">DESCRIPTION</span></span>
<span data-ttu-id="f45ac-109">Új Kusto-adatbázis létrehozása meglévő fürtben.</span><span class="sxs-lookup"><span data-stu-id="f45ac-109">Creates a new Kusto database in an existing cluster.</span></span>

## <span data-ttu-id="f45ac-110">Példák</span><span class="sxs-lookup"><span data-stu-id="f45ac-110">EXAMPLES</span></span>

### <span data-ttu-id="f45ac-111">Példa 1 – új Kusto-adatbázis létrehozása név szerint</span><span class="sxs-lookup"><span data-stu-id="f45ac-111">Example 1 - Create a new Kusto database by name</span></span>

```
PS C:\> New-AzKustoDatabase -ResourceGroupName testrg -ClusterName mykustocluster -Name mykustodatabase -SoftDeletePeriodInDays 4 -HotCachePeriodInDays 2

Name                   : mykustocluster/mykustodatabase
SoftDeletePeriodInDays : 4
HotCachePeriodInDays   : 2
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="f45ac-112">A fenti parancs létrehoz egy "mykustodatabase" nevű új Kusto-adatbázist a meglévő, "mykustocluster" nevű "" nevű "testrg" erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="f45ac-112">The above command creates a new Kusto database named "mykustodatabase" in the existing cluster "mykustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="f45ac-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f45ac-113">PARAMETERS</span></span>

### <span data-ttu-id="f45ac-114">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="f45ac-114">-ClusterName</span></span>
<span data-ttu-id="f45ac-115">Annak a fürtnek a neve, amelyből az adatbázist létre szeretné hozni.</span><span class="sxs-lookup"><span data-stu-id="f45ac-115">Name of cluster under which you want to create the database.</span></span>

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

### <span data-ttu-id="f45ac-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f45ac-116">-DefaultProfile</span></span>
<span data-ttu-id="f45ac-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f45ac-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f45ac-118">-HotCachePeriodInDays</span><span class="sxs-lookup"><span data-stu-id="f45ac-118">-HotCachePeriodInDays</span></span>
<span data-ttu-id="f45ac-119">Azoknak az adatnapoknak a száma, amelyeknek gyorsítótárban kell tartaniuk a gyors lekérdezésekhez.</span><span class="sxs-lookup"><span data-stu-id="f45ac-119">The number of days of data that should be kept in cache for fast queries.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f45ac-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f45ac-120">-InputObject</span></span>
<span data-ttu-id="f45ac-121">Kusto.</span><span class="sxs-lookup"><span data-stu-id="f45ac-121">Kusto cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f45ac-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f45ac-122">-Name</span></span>
<span data-ttu-id="f45ac-123">A létrehozandó adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="f45ac-123">Name of the database to be created.</span></span>

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

### <span data-ttu-id="f45ac-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f45ac-124">-ResourceGroupName</span></span>
<span data-ttu-id="f45ac-125">Annak az erőforráscsoport-csoportnak a neve, amelyben a fürt létezik.</span><span class="sxs-lookup"><span data-stu-id="f45ac-125">Name of resource group under which the cluster exists.</span></span>

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

### <span data-ttu-id="f45ac-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f45ac-126">-ResourceId</span></span>
<span data-ttu-id="f45ac-127">Kusto a cluster ResourceID.</span><span class="sxs-lookup"><span data-stu-id="f45ac-127">Kusto cluster ResourceID.</span></span>

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

### <span data-ttu-id="f45ac-128">-SoftDeletePeriodInDays</span><span class="sxs-lookup"><span data-stu-id="f45ac-128">-SoftDeletePeriodInDays</span></span>
<span data-ttu-id="f45ac-129">A napok számát meg kell őrizni, mielőtt a lekérdezések hozzáférhetővé válnak.</span><span class="sxs-lookup"><span data-stu-id="f45ac-129">The number of days data should be kept before it stops being accessible to queries.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f45ac-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f45ac-130">-Confirm</span></span>
<span data-ttu-id="f45ac-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f45ac-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f45ac-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f45ac-132">-WhatIf</span></span>
<span data-ttu-id="f45ac-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f45ac-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f45ac-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f45ac-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f45ac-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f45ac-135">CommonParameters</span></span>
<span data-ttu-id="f45ac-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f45ac-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f45ac-137">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f45ac-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f45ac-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f45ac-138">INPUTS</span></span>

### <span data-ttu-id="f45ac-139">System. String</span><span class="sxs-lookup"><span data-stu-id="f45ac-139">System.String</span></span>

### <span data-ttu-id="f45ac-140">Microsoft. Azure. Command. Kusto. models. PSKustoCluster</span><span class="sxs-lookup"><span data-stu-id="f45ac-140">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="f45ac-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f45ac-141">OUTPUTS</span></span>

### <span data-ttu-id="f45ac-142">Microsoft. Azure. Command. Kusto. models. PSKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="f45ac-142">Microsoft.Azure.Commands.Kusto.Models.PSKustoDatabase</span></span>

## <span data-ttu-id="f45ac-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f45ac-143">NOTES</span></span>

## <span data-ttu-id="f45ac-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f45ac-144">RELATED LINKS</span></span>
