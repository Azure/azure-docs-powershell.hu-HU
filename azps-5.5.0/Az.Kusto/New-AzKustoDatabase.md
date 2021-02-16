---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDatabase.md
ms.openlocfilehash: fe976ed4e5d34e4b10fb8bba0a5e5397173417b8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203783"
---
# <span data-ttu-id="92fe5-101">New-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="92fe5-101">New-AzKustoDatabase</span></span>

## <span data-ttu-id="92fe5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92fe5-102">SYNOPSIS</span></span>
<span data-ttu-id="92fe5-103">Létrehoz vagy frissíti az adatbázist.</span><span class="sxs-lookup"><span data-stu-id="92fe5-103">Creates or updates a database.</span></span>

## <span data-ttu-id="92fe5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="92fe5-104">SYNTAX</span></span>

```
New-AzKustoDatabase -ClusterName <String> -Name <String> -ResourceGroupName <String> -Kind <Kind>
 [-SubscriptionId <String>] [-HotCachePeriod <TimeSpan>] [-Location <String>] [-SoftDeletePeriod <TimeSpan>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="92fe5-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="92fe5-105">DESCRIPTION</span></span>
<span data-ttu-id="92fe5-106">Létrehoz vagy frissíti az adatbázist.</span><span class="sxs-lookup"><span data-stu-id="92fe5-106">Creates or updates a database.</span></span>

## <span data-ttu-id="92fe5-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="92fe5-107">EXAMPLES</span></span>

### <span data-ttu-id="92fe5-108">1. példa: Új Kusto-adatbázis létrehozása név szerint</span><span class="sxs-lookup"><span data-stu-id="92fe5-108">Example 1: Create a new Kusto database by name</span></span>
```powershell
PS C:\> New-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase -Kind ReadWrite -Location 'East US'

Kind      Location Name                                Type
----      -------- ----                                ----
ReadWrite East US  testnewkustocluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="92fe5-109">A fenti parancs létrehoz egy "mykustodatabase" nevű új Kusto-adatbázist a meglévő "testnewkustocluster" fürtben, amely a "testrg" erőforráscsoportban található.</span><span class="sxs-lookup"><span data-stu-id="92fe5-109">The above command creates a new Kusto database named "mykustodatabase" in the existing cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="92fe5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="92fe5-110">PARAMETERS</span></span>

### <span data-ttu-id="92fe5-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="92fe5-111">-AsJob</span></span>
<span data-ttu-id="92fe5-112">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="92fe5-112">Run the command as a job</span></span>

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

### <span data-ttu-id="92fe5-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="92fe5-113">-ClusterName</span></span>
<span data-ttu-id="92fe5-114">A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="92fe5-114">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="92fe5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92fe5-115">-DefaultProfile</span></span>
<span data-ttu-id="92fe5-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="92fe5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92fe5-117">-HotCachePeriod</span><span class="sxs-lookup"><span data-stu-id="92fe5-117">-HotCachePeriod</span></span>
<span data-ttu-id="92fe5-118">A Gyors lekérdezések időkorlában való gyorsítótárazása a TimeSpanban.</span><span class="sxs-lookup"><span data-stu-id="92fe5-118">The time the data should be kept in cache for fast queries in TimeSpan.</span></span>

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

### <span data-ttu-id="92fe5-119">-Kind</span><span class="sxs-lookup"><span data-stu-id="92fe5-119">-Kind</span></span>
<span data-ttu-id="92fe5-120">Az adatbázis fajtája</span><span class="sxs-lookup"><span data-stu-id="92fe5-120">Kind of the database</span></span>

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

### <span data-ttu-id="92fe5-121">-Location</span><span class="sxs-lookup"><span data-stu-id="92fe5-121">-Location</span></span>
<span data-ttu-id="92fe5-122">Erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="92fe5-122">Resource location.</span></span>

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

### <span data-ttu-id="92fe5-123">-Name</span><span class="sxs-lookup"><span data-stu-id="92fe5-123">-Name</span></span>
<span data-ttu-id="92fe5-124">A Kusto-fürtben található adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="92fe5-124">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="92fe5-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="92fe5-125">-NoWait</span></span>
<span data-ttu-id="92fe5-126">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="92fe5-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="92fe5-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92fe5-127">-ResourceGroupName</span></span>
<span data-ttu-id="92fe5-128">A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="92fe5-128">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="92fe5-129">-SoftDeletePeriod</span><span class="sxs-lookup"><span data-stu-id="92fe5-129">-SoftDeletePeriod</span></span>
<span data-ttu-id="92fe5-130">A TimeSpan lekérdezései számára elérhetővé tétele előtt meg kell tartani az adatokat.</span><span class="sxs-lookup"><span data-stu-id="92fe5-130">The time the data should be kept before it stops being accessible to queries in TimeSpan.</span></span>

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

### <span data-ttu-id="92fe5-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="92fe5-131">-SubscriptionId</span></span>
<span data-ttu-id="92fe5-132">Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="92fe5-132">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="92fe5-133">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="92fe5-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="92fe5-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="92fe5-134">-Confirm</span></span>
<span data-ttu-id="92fe5-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="92fe5-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92fe5-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92fe5-136">-WhatIf</span></span>
<span data-ttu-id="92fe5-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="92fe5-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92fe5-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="92fe5-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92fe5-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92fe5-139">CommonParameters</span></span>
<span data-ttu-id="92fe5-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92fe5-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92fe5-141">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="92fe5-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92fe5-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="92fe5-142">INPUTS</span></span>

## <span data-ttu-id="92fe5-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="92fe5-143">OUTPUTS</span></span>

### <span data-ttu-id="92fe5-144">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabase</span><span class="sxs-lookup"><span data-stu-id="92fe5-144">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabase</span></span>

## <span data-ttu-id="92fe5-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="92fe5-145">NOTES</span></span>

<span data-ttu-id="92fe5-146">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="92fe5-146">ALIASES</span></span>

## <span data-ttu-id="92fe5-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="92fe5-147">RELATED LINKS</span></span>

