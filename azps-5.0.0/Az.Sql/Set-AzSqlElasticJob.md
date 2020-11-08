---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJob.md
ms.openlocfilehash: 53bd1b1cd1c2f7ba87df8cb5c27f1b2380db04af
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195301"
---
# <span data-ttu-id="f74d5-101">Set-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="f74d5-101">Set-AzSqlElasticJob</span></span>

## <span data-ttu-id="f74d5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f74d5-102">SYNOPSIS</span></span>
<span data-ttu-id="f74d5-103">Feladat frissítése</span><span class="sxs-lookup"><span data-stu-id="f74d5-103">Updates a job</span></span>

## <span data-ttu-id="f74d5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f74d5-104">SYNTAX</span></span>

### <span data-ttu-id="f74d5-105">DefaultSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f74d5-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f74d5-106">Túlfolyás</span><span class="sxs-lookup"><span data-stu-id="f74d5-106">RunOnce</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-RunOnce] [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f74d5-107">Ismétlődő</span><span class="sxs-lookup"><span data-stu-id="f74d5-107">Recurring</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 -IntervalType <String> -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f74d5-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="f74d5-108">ObjectSet</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> [-StartTime <DateTime>] [-EndTime <DateTime>]
 [-Enable] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f74d5-109">RunOnceUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="f74d5-109">RunOnceUsingParentObject</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> [-RunOnce] [-StartTime <DateTime>]
 [-EndTime <DateTime>] [-Enable] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f74d5-110">RecurringUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="f74d5-110">RecurringUsingParentObject</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> -IntervalType <String> -IntervalCount <UInt32>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f74d5-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="f74d5-111">ResourceIdSet</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f74d5-112">RunOnceUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="f74d5-112">RunOnceUsingParentResourceId</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> [-RunOnce] [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f74d5-113">RecurringUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="f74d5-113">RecurringUsingParentResourceId</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> -IntervalType <String> -IntervalCount <UInt32>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f74d5-114">Leírás</span><span class="sxs-lookup"><span data-stu-id="f74d5-114">DESCRIPTION</span></span>
<span data-ttu-id="f74d5-115">A Set-AzSqlElasticJob parancsmag frissíti a feladatot</span><span class="sxs-lookup"><span data-stu-id="f74d5-115">The Set-AzSqlElasticJob cmdlet updates a job</span></span>

## <span data-ttu-id="f74d5-116">Példák</span><span class="sxs-lookup"><span data-stu-id="f74d5-116">EXAMPLES</span></span>

### <span data-ttu-id="f74d5-117">1. példa: a feladat frissítése az óránkénti órák megkezdése után 1 óránként ismételve</span><span class="sxs-lookup"><span data-stu-id="f74d5-117">Example 1: Updates a job to start an hour from now and repeat every 1 hour</span></span>
```powershell
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name job1
$job | Set-AzSqlElasticJob -IntervalType Hour -IntervalCount 1 -StartTime (Get-Date).AddHours(1) -Enable

JobName Version Description StartTime            EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------            -------                ------------ -------- -------
job1    0                   6/1/2018 10:50:15 PM 12/31/9999 11:59:59 AM Recurring    PT1H     True
```

<span data-ttu-id="f74d5-118">Feladat frissítése</span><span class="sxs-lookup"><span data-stu-id="f74d5-118">Updates a job</span></span>

### <span data-ttu-id="f74d5-119">2. példa</span><span class="sxs-lookup"><span data-stu-id="f74d5-119">Example 2</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlElasticJob -AgentName agent -Enable -IntervalCount 1 -IntervalType Hour -Name step1 -ResourceGroupName MyResourceGroup -ServerName s1 -StartTime '9/16/2016 11:31:12'
```

## <span data-ttu-id="f74d5-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f74d5-120">PARAMETERS</span></span>

### <span data-ttu-id="f74d5-121">-AgentName</span><span class="sxs-lookup"><span data-stu-id="f74d5-121">-AgentName</span></span>
<span data-ttu-id="f74d5-122">Az ügynök neve</span><span class="sxs-lookup"><span data-stu-id="f74d5-122">The agent name</span></span>

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

### <span data-ttu-id="f74d5-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f74d5-123">-DefaultProfile</span></span>
<span data-ttu-id="f74d5-124">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f74d5-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f74d5-125">-Leírás</span><span class="sxs-lookup"><span data-stu-id="f74d5-125">-Description</span></span>
<span data-ttu-id="f74d5-126">A munkakör leírása</span><span class="sxs-lookup"><span data-stu-id="f74d5-126">The job description</span></span>

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

### <span data-ttu-id="f74d5-127">– Engedélyezés</span><span class="sxs-lookup"><span data-stu-id="f74d5-127">-Enable</span></span>
<span data-ttu-id="f74d5-128">Annak jelzése, hogy az ügyfél szeretné-e engedélyezni ezt a feladatot.</span><span class="sxs-lookup"><span data-stu-id="f74d5-128">The flag to indicate customer wants this job to be enabled.</span></span>

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

### <span data-ttu-id="f74d5-129">-A befejezési időpont</span><span class="sxs-lookup"><span data-stu-id="f74d5-129">-EndTime</span></span>
<span data-ttu-id="f74d5-130">A projekt ütemtervének befejezési időpontja</span><span class="sxs-lookup"><span data-stu-id="f74d5-130">The job schedule end time</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f74d5-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f74d5-131">-InputObject</span></span>
<span data-ttu-id="f74d5-132">A projekt bemeneti objektuma</span><span class="sxs-lookup"><span data-stu-id="f74d5-132">The job input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel
Parameter Sets: ObjectSet, RunOnceUsingParentObject, RecurringUsingParentObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f74d5-133">-IntervalCount</span><span class="sxs-lookup"><span data-stu-id="f74d5-133">-IntervalCount</span></span>
<span data-ttu-id="f74d5-134">Az ismétlődő ütemezési intervallumok száma</span><span class="sxs-lookup"><span data-stu-id="f74d5-134">The recurring schedule interval count</span></span>

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

### <span data-ttu-id="f74d5-135">-IntervalType</span><span class="sxs-lookup"><span data-stu-id="f74d5-135">-IntervalType</span></span>
<span data-ttu-id="f74d5-136">Az ismétlődő ütemezési intervallum típusa lehet perc, óra, nap, hét, hónap</span><span class="sxs-lookup"><span data-stu-id="f74d5-136">The recurring schedule interval type - Can be Minute, Hour, Day, Week, Month</span></span>

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

### <span data-ttu-id="f74d5-137">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f74d5-137">-Name</span></span>
<span data-ttu-id="f74d5-138">A feladat neve</span><span class="sxs-lookup"><span data-stu-id="f74d5-138">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, RunOnce, Recurring
Aliases: JobName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f74d5-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f74d5-139">-ResourceGroupName</span></span>
<span data-ttu-id="f74d5-140">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="f74d5-140">The resource group name</span></span>

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

### <span data-ttu-id="f74d5-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f74d5-141">-ResourceId</span></span>
<span data-ttu-id="f74d5-142">A projekt erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="f74d5-142">The job resource id</span></span>

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

### <span data-ttu-id="f74d5-143">-Túlfolyás</span><span class="sxs-lookup"><span data-stu-id="f74d5-143">-RunOnce</span></span>
<span data-ttu-id="f74d5-144">A feladat megjelölésére szolgáló jelölő egyszer fog futni</span><span class="sxs-lookup"><span data-stu-id="f74d5-144">The flag to indicate job will be run once</span></span>

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

### <span data-ttu-id="f74d5-145">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="f74d5-145">-ServerName</span></span>
<span data-ttu-id="f74d5-146">A kiszolgáló neve</span><span class="sxs-lookup"><span data-stu-id="f74d5-146">The server name</span></span>

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

### <span data-ttu-id="f74d5-147">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="f74d5-147">-StartTime</span></span>
<span data-ttu-id="f74d5-148">A projekt ütemtervének kezdési időpontja</span><span class="sxs-lookup"><span data-stu-id="f74d5-148">The job schedule start time</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f74d5-149">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f74d5-149">-Confirm</span></span>
<span data-ttu-id="f74d5-150">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f74d5-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f74d5-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f74d5-151">-WhatIf</span></span>
<span data-ttu-id="f74d5-152">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f74d5-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f74d5-153">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f74d5-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f74d5-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f74d5-154">CommonParameters</span></span>
<span data-ttu-id="f74d5-155">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f74d5-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f74d5-156">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f74d5-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f74d5-157">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f74d5-157">INPUTS</span></span>

### <span data-ttu-id="f74d5-158">Microsoft. Azure. Command. SQL. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="f74d5-158">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="f74d5-159">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f74d5-159">OUTPUTS</span></span>

### <span data-ttu-id="f74d5-160">Microsoft. Azure. Command. SQL. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="f74d5-160">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="f74d5-161">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f74d5-161">NOTES</span></span>

## <span data-ttu-id="f74d5-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f74d5-162">RELATED LINKS</span></span>
