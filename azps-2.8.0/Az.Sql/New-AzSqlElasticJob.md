---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJob.md
ms.openlocfilehash: 29ae424807b8648238e2cc855fb90734773e870d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839147"
---
# <span data-ttu-id="bfcb1-101">New-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="bfcb1-101">New-AzSqlElasticJob</span></span>

## <span data-ttu-id="bfcb1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bfcb1-102">SYNOPSIS</span></span>
<span data-ttu-id="bfcb1-103">Új feladat létrehozása</span><span class="sxs-lookup"><span data-stu-id="bfcb1-103">Creates a new job</span></span>

## <span data-ttu-id="bfcb1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bfcb1-104">SYNTAX</span></span>

### <span data-ttu-id="bfcb1-105">DefaultSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bfcb1-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bfcb1-106">Túlfolyás</span><span class="sxs-lookup"><span data-stu-id="bfcb1-106">RunOnce</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-RunOnce] [-StartTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfcb1-107">Ismétlődő</span><span class="sxs-lookup"><span data-stu-id="bfcb1-107">Recurring</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 -IntervalType <String> -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>]
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bfcb1-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="bfcb1-108">ObjectSet</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> [-Description <String>]
 [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfcb1-109">RunOnceUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="bfcb1-109">RunOnceUsingParentObject</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> [-RunOnce]
 [-StartTime <DateTime>] [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfcb1-110">RecurringUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="bfcb1-110">RecurringUsingParentObject</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> -IntervalType <String>
 -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfcb1-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="bfcb1-111">ResourceIdSet</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfcb1-112">RunOnceUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="bfcb1-112">RunOnceUsingParentResourceId</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> [-RunOnce] [-StartTime <DateTime>]
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bfcb1-113">RecurringUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="bfcb1-113">RecurringUsingParentResourceId</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> -IntervalType <String>
 -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bfcb1-114">Leírás</span><span class="sxs-lookup"><span data-stu-id="bfcb1-114">DESCRIPTION</span></span>
<span data-ttu-id="bfcb1-115">A New-AzSqlElasticJob parancsmag új feladatot hoz létre</span><span class="sxs-lookup"><span data-stu-id="bfcb1-115">The New-AzSqlElasticJob cmdlet creates a new job</span></span>

## <span data-ttu-id="bfcb1-116">Példák</span><span class="sxs-lookup"><span data-stu-id="bfcb1-116">EXAMPLES</span></span>

### <span data-ttu-id="bfcb1-117">Példa 1 – új feladat létrehozása</span><span class="sxs-lookup"><span data-stu-id="bfcb1-117">Example 1 - Creates a new job</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | New-AzSqlElasticJob -Name job1

JobName Version Description StartTime           EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------           -------                ------------ -------- -------
job1    0                   6/1/2018 9:46:29 PM 12/31/9999 11:59:59 AM Once                  False
```

<span data-ttu-id="bfcb1-118">Új feladat létrehozása</span><span class="sxs-lookup"><span data-stu-id="bfcb1-118">Creates a new job</span></span>

## <span data-ttu-id="bfcb1-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bfcb1-119">PARAMETERS</span></span>

### <span data-ttu-id="bfcb1-120">-AgentName</span><span class="sxs-lookup"><span data-stu-id="bfcb1-120">-AgentName</span></span>
<span data-ttu-id="bfcb1-121">Az ügynök neve</span><span class="sxs-lookup"><span data-stu-id="bfcb1-121">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, RunOnce, Recurring
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfcb1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfcb1-122">-DefaultProfile</span></span>
<span data-ttu-id="bfcb1-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bfcb1-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bfcb1-124">-Leírás</span><span class="sxs-lookup"><span data-stu-id="bfcb1-124">-Description</span></span>
<span data-ttu-id="bfcb1-125">A munkakör leírása</span><span class="sxs-lookup"><span data-stu-id="bfcb1-125">The job description</span></span>

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

### <span data-ttu-id="bfcb1-126">– Engedélyezés</span><span class="sxs-lookup"><span data-stu-id="bfcb1-126">-Enable</span></span>
<span data-ttu-id="bfcb1-127">Annak jelzése, hogy az ügyfél szeretné-e engedélyezni ezt a feladatot.</span><span class="sxs-lookup"><span data-stu-id="bfcb1-127">The flag to indicate customer wants this job to be enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfcb1-128">-A befejezési időpont</span><span class="sxs-lookup"><span data-stu-id="bfcb1-128">-EndTime</span></span>
<span data-ttu-id="bfcb1-129">A projekt ütemtervének befejezési időpontja</span><span class="sxs-lookup"><span data-stu-id="bfcb1-129">The job schedule end time</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: Recurring, RecurringUsingParentObject, RecurringUsingParentResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfcb1-130">-IntervalCount</span><span class="sxs-lookup"><span data-stu-id="bfcb1-130">-IntervalCount</span></span>
<span data-ttu-id="bfcb1-131">Az ismétlődő ütemezési intervallumok száma</span><span class="sxs-lookup"><span data-stu-id="bfcb1-131">The recurring schedule interval count</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: Recurring, RecurringUsingParentObject, RecurringUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfcb1-132">-IntervalType</span><span class="sxs-lookup"><span data-stu-id="bfcb1-132">-IntervalType</span></span>
<span data-ttu-id="bfcb1-133">Az ismétlődő ütemezési intervallum típusa lehet perc, óra, nap, hét, hónap</span><span class="sxs-lookup"><span data-stu-id="bfcb1-133">The recurring schedule interval type - Can be Minute, Hour, Day, Week, Month</span></span>

```yaml
Type: System.String
Parameter Sets: Recurring, RecurringUsingParentObject, RecurringUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfcb1-134">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bfcb1-134">-Name</span></span>
<span data-ttu-id="bfcb1-135">A feladat neve</span><span class="sxs-lookup"><span data-stu-id="bfcb1-135">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: JobName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfcb1-136">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="bfcb1-136">-ParentObject</span></span>
<span data-ttu-id="bfcb1-137">Ügynök beviteli objektuma</span><span class="sxs-lookup"><span data-stu-id="bfcb1-137">The agent input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel
Parameter Sets: ObjectSet, RunOnceUsingParentObject, RecurringUsingParentObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bfcb1-138">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="bfcb1-138">-ParentResourceId</span></span>
<span data-ttu-id="bfcb1-139">Az ügynök erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="bfcb1-139">The agent resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet, RunOnceUsingParentResourceId, RecurringUsingParentResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfcb1-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfcb1-140">-ResourceGroupName</span></span>
<span data-ttu-id="bfcb1-141">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="bfcb1-141">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, RunOnce, Recurring
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfcb1-142">-Túlfolyás</span><span class="sxs-lookup"><span data-stu-id="bfcb1-142">-RunOnce</span></span>
<span data-ttu-id="bfcb1-143">A feladat megjelölésére szolgáló jelölő egyszer fog futni</span><span class="sxs-lookup"><span data-stu-id="bfcb1-143">The flag to indicate job will be run once</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RunOnce, RunOnceUsingParentObject, RunOnceUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfcb1-144">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="bfcb1-144">-ServerName</span></span>
<span data-ttu-id="bfcb1-145">A kiszolgáló neve</span><span class="sxs-lookup"><span data-stu-id="bfcb1-145">The server name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, RunOnce, Recurring
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfcb1-146">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="bfcb1-146">-StartTime</span></span>
<span data-ttu-id="bfcb1-147">A projekt ütemtervének kezdési időpontja</span><span class="sxs-lookup"><span data-stu-id="bfcb1-147">The job schedule start time</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: RunOnce, Recurring, RunOnceUsingParentObject, RecurringUsingParentObject, RunOnceUsingParentResourceId, RecurringUsingParentResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfcb1-148">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="bfcb1-148">-Confirm</span></span>
<span data-ttu-id="bfcb1-149">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bfcb1-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfcb1-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bfcb1-150">-WhatIf</span></span>
<span data-ttu-id="bfcb1-151">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="bfcb1-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bfcb1-152">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bfcb1-152">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfcb1-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfcb1-153">CommonParameters</span></span>
<span data-ttu-id="bfcb1-154">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bfcb1-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfcb1-155">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="bfcb1-155">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfcb1-156">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bfcb1-156">INPUTS</span></span>

### <span data-ttu-id="bfcb1-157">Microsoft. Azure. Command. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="bfcb1-157">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="bfcb1-158">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bfcb1-158">OUTPUTS</span></span>

### <span data-ttu-id="bfcb1-159">Microsoft. Azure. Command. SQL. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="bfcb1-159">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="bfcb1-160">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bfcb1-160">NOTES</span></span>

## <span data-ttu-id="bfcb1-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bfcb1-161">RELATED LINKS</span></span>
