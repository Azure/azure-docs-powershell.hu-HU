---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDatabase.md
ms.openlocfilehash: fe976ed4e5d34e4b10fb8bba0a5e5397173417b8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466355"
---
# <span data-ttu-id="74b96-101">New-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="74b96-101">New-AzKustoDatabase</span></span>

## <span data-ttu-id="74b96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74b96-102">SYNOPSIS</span></span>
<span data-ttu-id="74b96-103">Létrehoz vagy frissíti az adatbázist.</span><span class="sxs-lookup"><span data-stu-id="74b96-103">Creates or updates a database.</span></span>

## <span data-ttu-id="74b96-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="74b96-104">SYNTAX</span></span>

```
New-AzKustoDatabase -ClusterName <String> -Name <String> -ResourceGroupName <String> -Kind <Kind>
 [-SubscriptionId <String>] [-HotCachePeriod <TimeSpan>] [-Location <String>] [-SoftDeletePeriod <TimeSpan>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="74b96-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="74b96-105">DESCRIPTION</span></span>
<span data-ttu-id="74b96-106">Létrehoz vagy frissíti az adatbázist.</span><span class="sxs-lookup"><span data-stu-id="74b96-106">Creates or updates a database.</span></span>

## <span data-ttu-id="74b96-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="74b96-107">EXAMPLES</span></span>

### <span data-ttu-id="74b96-108">1. példa: Új Kusto-adatbázis létrehozása név szerint</span><span class="sxs-lookup"><span data-stu-id="74b96-108">Example 1: Create a new Kusto database by name</span></span>
```powershell
PS C:\> New-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase -Kind ReadWrite -Location 'East US'

Kind      Location Name                                Type
----      -------- ----                                ----
ReadWrite East US  testnewkustocluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="74b96-109">A fenti parancs létrehoz egy "mykustodatabase" nevű új Kusto-adatbázist a meglévő "testnewkustocluster" fürtben, amely a "testrg" erőforráscsoportban található.</span><span class="sxs-lookup"><span data-stu-id="74b96-109">The above command creates a new Kusto database named "mykustodatabase" in the existing cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="74b96-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="74b96-110">PARAMETERS</span></span>

### <span data-ttu-id="74b96-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="74b96-111">-AsJob</span></span>
<span data-ttu-id="74b96-112">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="74b96-112">Run the command as a job</span></span>

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

### <span data-ttu-id="74b96-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="74b96-113">-ClusterName</span></span>
<span data-ttu-id="74b96-114">A Kusto-fürt neve.</span><span class="sxs-lookup"><span data-stu-id="74b96-114">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="74b96-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74b96-115">-DefaultProfile</span></span>
<span data-ttu-id="74b96-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="74b96-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74b96-117">-HotCachePeriod</span><span class="sxs-lookup"><span data-stu-id="74b96-117">-HotCachePeriod</span></span>
<span data-ttu-id="74b96-118">A Gyors lekérdezések időkorlában való gyorsítótárazása a TimeSpanban.</span><span class="sxs-lookup"><span data-stu-id="74b96-118">The time the data should be kept in cache for fast queries in TimeSpan.</span></span>

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

### <span data-ttu-id="74b96-119">-Kind</span><span class="sxs-lookup"><span data-stu-id="74b96-119">-Kind</span></span>
<span data-ttu-id="74b96-120">Az adatbázis fajtája</span><span class="sxs-lookup"><span data-stu-id="74b96-120">Kind of the database</span></span>

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

### <span data-ttu-id="74b96-121">-Location</span><span class="sxs-lookup"><span data-stu-id="74b96-121">-Location</span></span>
<span data-ttu-id="74b96-122">Erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="74b96-122">Resource location.</span></span>

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

### <span data-ttu-id="74b96-123">-Name</span><span class="sxs-lookup"><span data-stu-id="74b96-123">-Name</span></span>
<span data-ttu-id="74b96-124">A Kusto-fürtben található adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="74b96-124">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="74b96-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="74b96-125">-NoWait</span></span>
<span data-ttu-id="74b96-126">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="74b96-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="74b96-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74b96-127">-ResourceGroupName</span></span>
<span data-ttu-id="74b96-128">A Kusto-fürtöt tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="74b96-128">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="74b96-129">-SoftDeletePeriod</span><span class="sxs-lookup"><span data-stu-id="74b96-129">-SoftDeletePeriod</span></span>
<span data-ttu-id="74b96-130">A TimeSpan lekérdezései számára elérhetővé tétele előtt meg kell tartani az adatokat.</span><span class="sxs-lookup"><span data-stu-id="74b96-130">The time the data should be kept before it stops being accessible to queries in TimeSpan.</span></span>

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

### <span data-ttu-id="74b96-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="74b96-131">-SubscriptionId</span></span>
<span data-ttu-id="74b96-132">Az előfizetéshez olyan hitelesítő adatokat kap, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="74b96-132">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="74b96-133">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="74b96-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="74b96-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="74b96-134">-Confirm</span></span>
<span data-ttu-id="74b96-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="74b96-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74b96-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74b96-136">-WhatIf</span></span>
<span data-ttu-id="74b96-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="74b96-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74b96-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="74b96-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74b96-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74b96-139">CommonParameters</span></span>
<span data-ttu-id="74b96-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74b96-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74b96-141">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="74b96-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74b96-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="74b96-142">INPUTS</span></span>

## <span data-ttu-id="74b96-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="74b96-143">OUTPUTS</span></span>

### <span data-ttu-id="74b96-144">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabase</span><span class="sxs-lookup"><span data-stu-id="74b96-144">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabase</span></span>

## <span data-ttu-id="74b96-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="74b96-145">NOTES</span></span>

<span data-ttu-id="74b96-146">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="74b96-146">ALIASES</span></span>

## <span data-ttu-id="74b96-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="74b96-147">RELATED LINKS</span></span>

