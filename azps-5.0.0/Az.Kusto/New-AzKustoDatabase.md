---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDatabase.md
ms.openlocfilehash: dc0b4ea1616c916edacaf4d5a4a2b431e7f7d113
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194702"
---
# <span data-ttu-id="720a6-101">New-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="720a6-101">New-AzKustoDatabase</span></span>

## <span data-ttu-id="720a6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="720a6-102">SYNOPSIS</span></span>
<span data-ttu-id="720a6-103">Adatbázist hoz létre vagy frissít.</span><span class="sxs-lookup"><span data-stu-id="720a6-103">Creates or updates a database.</span></span>

## <span data-ttu-id="720a6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="720a6-104">SYNTAX</span></span>

```
New-AzKustoDatabase -ClusterName <String> -Name <String> -ResourceGroupName <String> -Kind <Kind>
 [-SubscriptionId <String>] [-HotCachePeriod <TimeSpan>] [-Location <String>] [-SoftDeletePeriod <TimeSpan>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="720a6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="720a6-105">DESCRIPTION</span></span>
<span data-ttu-id="720a6-106">Adatbázist hoz létre vagy frissít.</span><span class="sxs-lookup"><span data-stu-id="720a6-106">Creates or updates a database.</span></span>

## <span data-ttu-id="720a6-107">Példák</span><span class="sxs-lookup"><span data-stu-id="720a6-107">EXAMPLES</span></span>

### <span data-ttu-id="720a6-108">Példa 1: új Kusto-adatbázis létrehozása név szerint</span><span class="sxs-lookup"><span data-stu-id="720a6-108">Example 1: Create a new Kusto database by name</span></span>
```powershell
PS C:\> New-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase -Kind ReadWrite -Location 'East US'

Kind      Location Name                                Type
----      -------- ----                                ----
ReadWrite East US  testnewkustocluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="720a6-109">A fenti parancs létrehoz egy "mykustodatabase" nevű új Kusto-adatbázist a meglévő, "testnewkustocluster" nevű "" nevű "testrg" erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="720a6-109">The above command creates a new Kusto database named "mykustodatabase" in the existing cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="720a6-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="720a6-110">PARAMETERS</span></span>

### <span data-ttu-id="720a6-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="720a6-111">-AsJob</span></span>
<span data-ttu-id="720a6-112">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="720a6-112">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="720a6-113">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="720a6-113">-ClusterName</span></span>
<span data-ttu-id="720a6-114">A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="720a6-114">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="720a6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="720a6-115">-DefaultProfile</span></span>
<span data-ttu-id="720a6-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="720a6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="720a6-117">-HotCachePeriod</span><span class="sxs-lookup"><span data-stu-id="720a6-117">-HotCachePeriod</span></span>
<span data-ttu-id="720a6-118">Az az időpont, amikor az adatgyorsítótárban meg kell őrizni a gyors lekérdezéseket a időszak-ban.</span><span class="sxs-lookup"><span data-stu-id="720a6-118">The time the data should be kept in cache for fast queries in TimeSpan.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="720a6-119">-Kind</span><span class="sxs-lookup"><span data-stu-id="720a6-119">-Kind</span></span>
<span data-ttu-id="720a6-120">Az adatbázis típusa</span><span class="sxs-lookup"><span data-stu-id="720a6-120">Kind of the database</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Kind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="720a6-121">-Hely</span><span class="sxs-lookup"><span data-stu-id="720a6-121">-Location</span></span>
<span data-ttu-id="720a6-122">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="720a6-122">Resource location.</span></span>

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

### <span data-ttu-id="720a6-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="720a6-123">-Name</span></span>
<span data-ttu-id="720a6-124">Az adatbázis neve a Kusto-fürtben.</span><span class="sxs-lookup"><span data-stu-id="720a6-124">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="720a6-125">-Várva</span><span class="sxs-lookup"><span data-stu-id="720a6-125">-NoWait</span></span>
<span data-ttu-id="720a6-126">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="720a6-126">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="720a6-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="720a6-127">-ResourceGroupName</span></span>
<span data-ttu-id="720a6-128">A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="720a6-128">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="720a6-129">-SoftDeletePeriod</span><span class="sxs-lookup"><span data-stu-id="720a6-129">-SoftDeletePeriod</span></span>
<span data-ttu-id="720a6-130">Az az időpont, amikor az adatot meg kell őrizni, mielőtt a időszak-ban a lekérdezések elérhetővé válnak.</span><span class="sxs-lookup"><span data-stu-id="720a6-130">The time the data should be kept before it stops being accessible to queries in TimeSpan.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="720a6-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="720a6-131">-SubscriptionId</span></span>
<span data-ttu-id="720a6-132">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="720a6-132">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="720a6-133">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="720a6-133">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="720a6-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="720a6-134">-Confirm</span></span>
<span data-ttu-id="720a6-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="720a6-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="720a6-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="720a6-136">-WhatIf</span></span>
<span data-ttu-id="720a6-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="720a6-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="720a6-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="720a6-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="720a6-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="720a6-139">CommonParameters</span></span>
<span data-ttu-id="720a6-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="720a6-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="720a6-141">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="720a6-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="720a6-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="720a6-142">INPUTS</span></span>

## <span data-ttu-id="720a6-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="720a6-143">OUTPUTS</span></span>

### <span data-ttu-id="720a6-144">Microsoft. Azure. PowerShell. parancsmagok. Kusto. modellek. Api20200614. IDatabase</span><span class="sxs-lookup"><span data-stu-id="720a6-144">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabase</span></span>

## <span data-ttu-id="720a6-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="720a6-145">NOTES</span></span>

<span data-ttu-id="720a6-146">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="720a6-146">ALIASES</span></span>

## <span data-ttu-id="720a6-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="720a6-147">RELATED LINKS</span></span>
