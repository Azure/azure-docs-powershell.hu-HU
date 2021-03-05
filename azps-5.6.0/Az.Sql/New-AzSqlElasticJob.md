---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJob.md
ms.openlocfilehash: 961f37db94cff87952b2811a528a94cc71ffabff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010165"
---
# <span data-ttu-id="a149d-101">New-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="a149d-101">New-AzSqlElasticJob</span></span>

## <span data-ttu-id="a149d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a149d-102">SYNOPSIS</span></span>
<span data-ttu-id="a149d-103">Új feladat létrehozása</span><span class="sxs-lookup"><span data-stu-id="a149d-103">Creates a new job</span></span>

## <span data-ttu-id="a149d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a149d-104">SYNTAX</span></span>

### <span data-ttu-id="a149d-105">DefaultSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a149d-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a149d-106">RunOnce</span><span class="sxs-lookup"><span data-stu-id="a149d-106">RunOnce</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-RunOnce] [-StartTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a149d-107">Ismétlődő</span><span class="sxs-lookup"><span data-stu-id="a149d-107">Recurring</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 -IntervalType <String> -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>]
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a149d-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="a149d-108">ObjectSet</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> [-Description <String>]
 [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a149d-109">RunOnceUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="a149d-109">RunOnceUsingParentObject</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> [-RunOnce]
 [-StartTime <DateTime>] [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a149d-110">RecurringUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="a149d-110">RecurringUsingParentObject</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> -IntervalType <String>
 -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a149d-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a149d-111">ResourceIdSet</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a149d-112">RunOnceUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="a149d-112">RunOnceUsingParentResourceId</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> [-RunOnce] [-StartTime <DateTime>]
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a149d-113">RecurringUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="a149d-113">RecurringUsingParentResourceId</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> -IntervalType <String>
 -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a149d-114">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a149d-114">DESCRIPTION</span></span>
<span data-ttu-id="a149d-115">A New-AzSqlElasticJob parancsmag létrehoz egy új feladatot</span><span class="sxs-lookup"><span data-stu-id="a149d-115">The New-AzSqlElasticJob cmdlet creates a new job</span></span>

## <span data-ttu-id="a149d-116">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a149d-116">EXAMPLES</span></span>

### <span data-ttu-id="a149d-117">1. példa: Új feladat létrehozása</span><span class="sxs-lookup"><span data-stu-id="a149d-117">Example 1: Creates a new job</span></span>
```powershell
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | New-AzSqlElasticJob -Name job1

JobName Version Description StartTime           EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------           -------                ------------ -------- -------
job1    0                   6/1/2018 9:46:29 PM 12/31/9999 11:59:59 AM Once                  False
```

<span data-ttu-id="a149d-118">Új feladat létrehozása</span><span class="sxs-lookup"><span data-stu-id="a149d-118">Creates a new job</span></span>

### <span data-ttu-id="a149d-119">2. példa</span><span class="sxs-lookup"><span data-stu-id="a149d-119">Example 2</span></span>

<span data-ttu-id="a149d-120">Létrehoz egy új feladatot.</span><span class="sxs-lookup"><span data-stu-id="a149d-120">Creates a new job.</span></span> <span data-ttu-id="a149d-121">(automatikusan generált)</span><span class="sxs-lookup"><span data-stu-id="a149d-121">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzSqlElasticJob -Name job1 -RunOnce
```

## <span data-ttu-id="a149d-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a149d-122">PARAMETERS</span></span>

### <span data-ttu-id="a149d-123">-AgentName</span><span class="sxs-lookup"><span data-stu-id="a149d-123">-AgentName</span></span>
<span data-ttu-id="a149d-124">Az ügynök neve</span><span class="sxs-lookup"><span data-stu-id="a149d-124">The agent name</span></span>

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

### <span data-ttu-id="a149d-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a149d-125">-DefaultProfile</span></span>
<span data-ttu-id="a149d-126">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a149d-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a149d-127">-Leírás</span><span class="sxs-lookup"><span data-stu-id="a149d-127">-Description</span></span>
<span data-ttu-id="a149d-128">A feladat leírása</span><span class="sxs-lookup"><span data-stu-id="a149d-128">The job description</span></span>

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

### <span data-ttu-id="a149d-129">-Enable</span><span class="sxs-lookup"><span data-stu-id="a149d-129">-Enable</span></span>
<span data-ttu-id="a149d-130">Az ügyfeleket jelző jelölő engedélyezi ezt a feladatot.</span><span class="sxs-lookup"><span data-stu-id="a149d-130">The flag to indicate customer wants this job to be enabled.</span></span>

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

### <span data-ttu-id="a149d-131">-EndTime</span><span class="sxs-lookup"><span data-stu-id="a149d-131">-EndTime</span></span>
<span data-ttu-id="a149d-132">A munkabeosztás záró ideje</span><span class="sxs-lookup"><span data-stu-id="a149d-132">The job schedule end time</span></span>

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

### <span data-ttu-id="a149d-133">-IntervalCount</span><span class="sxs-lookup"><span data-stu-id="a149d-133">-IntervalCount</span></span>
<span data-ttu-id="a149d-134">Az ismétlődő ütemezési intervallumok száma</span><span class="sxs-lookup"><span data-stu-id="a149d-134">The recurring schedule interval count</span></span>

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

### <span data-ttu-id="a149d-135">-IntervalType</span><span class="sxs-lookup"><span data-stu-id="a149d-135">-IntervalType</span></span>
<span data-ttu-id="a149d-136">Az ismétlődő ütemezési intervallum típusa – Lehet perc, óra, nap, hét, hónap</span><span class="sxs-lookup"><span data-stu-id="a149d-136">The recurring schedule interval type - Can be Minute, Hour, Day, Week, Month</span></span>

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

### <span data-ttu-id="a149d-137">-Name</span><span class="sxs-lookup"><span data-stu-id="a149d-137">-Name</span></span>
<span data-ttu-id="a149d-138">A feladat neve</span><span class="sxs-lookup"><span data-stu-id="a149d-138">The job name</span></span>

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

### <span data-ttu-id="a149d-139">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="a149d-139">-ParentObject</span></span>
<span data-ttu-id="a149d-140">Az ügynök beviteli objektuma</span><span class="sxs-lookup"><span data-stu-id="a149d-140">The agent input object</span></span>

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

### <span data-ttu-id="a149d-141">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="a149d-141">-ParentResourceId</span></span>
<span data-ttu-id="a149d-142">Az ügynök erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="a149d-142">The agent resource id</span></span>

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

### <span data-ttu-id="a149d-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a149d-143">-ResourceGroupName</span></span>
<span data-ttu-id="a149d-144">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="a149d-144">The resource group name</span></span>

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

### <span data-ttu-id="a149d-145">-RunOnce</span><span class="sxs-lookup"><span data-stu-id="a149d-145">-RunOnce</span></span>
<span data-ttu-id="a149d-146">A feladat jelzésére jelző jelölő egyszer fog futni</span><span class="sxs-lookup"><span data-stu-id="a149d-146">The flag to indicate job will be run once</span></span>

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

### <span data-ttu-id="a149d-147">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a149d-147">-ServerName</span></span>
<span data-ttu-id="a149d-148">A kiszolgáló neve</span><span class="sxs-lookup"><span data-stu-id="a149d-148">The server name</span></span>

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

### <span data-ttu-id="a149d-149">-StartTime</span><span class="sxs-lookup"><span data-stu-id="a149d-149">-StartTime</span></span>
<span data-ttu-id="a149d-150">A munkabeosztás kezdési ideje</span><span class="sxs-lookup"><span data-stu-id="a149d-150">The job schedule start time</span></span>

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

### <span data-ttu-id="a149d-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a149d-151">-Confirm</span></span>
<span data-ttu-id="a149d-152">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a149d-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a149d-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a149d-153">-WhatIf</span></span>
<span data-ttu-id="a149d-154">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a149d-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a149d-155">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a149d-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a149d-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a149d-156">CommonParameters</span></span>
<span data-ttu-id="a149d-157">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a149d-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a149d-158">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a149d-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a149d-159">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a149d-159">INPUTS</span></span>

### <span data-ttu-id="a149d-160">Microsoft.Azure.Commands.Sql.ElasticMods.Model.AzureSqlElasticAgentModel</span><span class="sxs-lookup"><span data-stu-id="a149d-160">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="a149d-161">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a149d-161">OUTPUTS</span></span>

### <span data-ttu-id="a149d-162">Microsoft.Azure.Commands.Sql.ElasticMods.Model.AzureSqlElasticModel</span><span class="sxs-lookup"><span data-stu-id="a149d-162">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="a149d-163">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a149d-163">NOTES</span></span>

## <span data-ttu-id="a149d-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a149d-164">RELATED LINKS</span></span>
