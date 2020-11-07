---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJob.md
ms.openlocfilehash: a53a982e13b84bb401389e5edb5294ef1d094a49
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846601"
---
# <span data-ttu-id="cb6ed-101">Set-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="cb6ed-101">Set-AzSqlElasticJob</span></span>

## <span data-ttu-id="cb6ed-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cb6ed-102">SYNOPSIS</span></span>
<span data-ttu-id="cb6ed-103">Feladat frissítése</span><span class="sxs-lookup"><span data-stu-id="cb6ed-103">Updates a job</span></span>

## <span data-ttu-id="cb6ed-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cb6ed-104">SYNTAX</span></span>

### <span data-ttu-id="cb6ed-105">DefaultSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cb6ed-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb6ed-106">Túlfolyás</span><span class="sxs-lookup"><span data-stu-id="cb6ed-106">RunOnce</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-RunOnce] [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb6ed-107">Ismétlődő</span><span class="sxs-lookup"><span data-stu-id="cb6ed-107">Recurring</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 -IntervalType <String> -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb6ed-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="cb6ed-108">ObjectSet</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> [-StartTime <DateTime>] [-EndTime <DateTime>]
 [-Enable] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cb6ed-109">RunOnceUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="cb6ed-109">RunOnceUsingParentObject</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> [-RunOnce] [-StartTime <DateTime>]
 [-EndTime <DateTime>] [-Enable] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb6ed-110">RecurringUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="cb6ed-110">RecurringUsingParentObject</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> -IntervalType <String> -IntervalCount <UInt32>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb6ed-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="cb6ed-111">ResourceIdSet</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb6ed-112">RunOnceUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="cb6ed-112">RunOnceUsingParentResourceId</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> [-RunOnce] [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb6ed-113">RecurringUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="cb6ed-113">RecurringUsingParentResourceId</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> -IntervalType <String> -IntervalCount <UInt32>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb6ed-114">Leírás</span><span class="sxs-lookup"><span data-stu-id="cb6ed-114">DESCRIPTION</span></span>
<span data-ttu-id="cb6ed-115">A Set-AzSqlElasticJob parancsmag frissíti a feladatot</span><span class="sxs-lookup"><span data-stu-id="cb6ed-115">The Set-AzSqlElasticJob cmdlet updates a job</span></span>

## <span data-ttu-id="cb6ed-116">Példák</span><span class="sxs-lookup"><span data-stu-id="cb6ed-116">EXAMPLES</span></span>

### <span data-ttu-id="cb6ed-117">Példa 1 – a feladat frissítése az óra megkezdése után 1 óránként ismétlődik</span><span class="sxs-lookup"><span data-stu-id="cb6ed-117">Example 1 - Updates a job to start an hour from now and repeat every 1 hour</span></span>
```
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name job1
$job | Set-AzSqlElasticJob -IntervalType Hour -IntervalCount 1 -StartTime (Get-Date).AddHours(1) -Enable

JobName Version Description StartTime            EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------            -------                ------------ -------- -------
job1    0                   6/1/2018 10:50:15 PM 12/31/9999 11:59:59 AM Recurring    PT1H     True
```

<span data-ttu-id="cb6ed-118">Feladat frissítése</span><span class="sxs-lookup"><span data-stu-id="cb6ed-118">Updates a job</span></span>

## <span data-ttu-id="cb6ed-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cb6ed-119">PARAMETERS</span></span>

### <span data-ttu-id="cb6ed-120">-AgentName</span><span class="sxs-lookup"><span data-stu-id="cb6ed-120">-AgentName</span></span>
<span data-ttu-id="cb6ed-121">Az ügynök neve</span><span class="sxs-lookup"><span data-stu-id="cb6ed-121">The agent name</span></span>

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

### <span data-ttu-id="cb6ed-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb6ed-122">-DefaultProfile</span></span>
<span data-ttu-id="cb6ed-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cb6ed-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb6ed-124">-Leírás</span><span class="sxs-lookup"><span data-stu-id="cb6ed-124">-Description</span></span>
<span data-ttu-id="cb6ed-125">A munkakör leírása</span><span class="sxs-lookup"><span data-stu-id="cb6ed-125">The job description</span></span>

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

### <span data-ttu-id="cb6ed-126">– Engedélyezés</span><span class="sxs-lookup"><span data-stu-id="cb6ed-126">-Enable</span></span>
<span data-ttu-id="cb6ed-127">Annak jelzése, hogy az ügyfél szeretné-e engedélyezni ezt a feladatot.</span><span class="sxs-lookup"><span data-stu-id="cb6ed-127">The flag to indicate customer wants this job to be enabled.</span></span>

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

### <span data-ttu-id="cb6ed-128">-A befejezési időpont</span><span class="sxs-lookup"><span data-stu-id="cb6ed-128">-EndTime</span></span>
<span data-ttu-id="cb6ed-129">A projekt ütemtervének befejezési időpontja</span><span class="sxs-lookup"><span data-stu-id="cb6ed-129">The job schedule end time</span></span>

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

### <span data-ttu-id="cb6ed-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cb6ed-130">-InputObject</span></span>
<span data-ttu-id="cb6ed-131">A projekt bemeneti objektuma</span><span class="sxs-lookup"><span data-stu-id="cb6ed-131">The job input object</span></span>

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

### <span data-ttu-id="cb6ed-132">-IntervalCount</span><span class="sxs-lookup"><span data-stu-id="cb6ed-132">-IntervalCount</span></span>
<span data-ttu-id="cb6ed-133">Az ismétlődő ütemezési intervallumok száma</span><span class="sxs-lookup"><span data-stu-id="cb6ed-133">The recurring schedule interval count</span></span>

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

### <span data-ttu-id="cb6ed-134">-IntervalType</span><span class="sxs-lookup"><span data-stu-id="cb6ed-134">-IntervalType</span></span>
<span data-ttu-id="cb6ed-135">Az ismétlődő ütemezési intervallum típusa lehet perc, óra, nap, hét, hónap</span><span class="sxs-lookup"><span data-stu-id="cb6ed-135">The recurring schedule interval type - Can be Minute, Hour, Day, Week, Month</span></span>

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

### <span data-ttu-id="cb6ed-136">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cb6ed-136">-Name</span></span>
<span data-ttu-id="cb6ed-137">A feladat neve</span><span class="sxs-lookup"><span data-stu-id="cb6ed-137">The job name</span></span>

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

### <span data-ttu-id="cb6ed-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb6ed-138">-ResourceGroupName</span></span>
<span data-ttu-id="cb6ed-139">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="cb6ed-139">The resource group name</span></span>

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

### <span data-ttu-id="cb6ed-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cb6ed-140">-ResourceId</span></span>
<span data-ttu-id="cb6ed-141">A projekt erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="cb6ed-141">The job resource id</span></span>

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

### <span data-ttu-id="cb6ed-142">-Túlfolyás</span><span class="sxs-lookup"><span data-stu-id="cb6ed-142">-RunOnce</span></span>
<span data-ttu-id="cb6ed-143">A feladat megjelölésére szolgáló jelölő egyszer fog futni</span><span class="sxs-lookup"><span data-stu-id="cb6ed-143">The flag to indicate job will be run once</span></span>

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

### <span data-ttu-id="cb6ed-144">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="cb6ed-144">-ServerName</span></span>
<span data-ttu-id="cb6ed-145">A kiszolgáló neve</span><span class="sxs-lookup"><span data-stu-id="cb6ed-145">The server name</span></span>

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

### <span data-ttu-id="cb6ed-146">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="cb6ed-146">-StartTime</span></span>
<span data-ttu-id="cb6ed-147">A projekt ütemtervének kezdési időpontja</span><span class="sxs-lookup"><span data-stu-id="cb6ed-147">The job schedule start time</span></span>

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

### <span data-ttu-id="cb6ed-148">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cb6ed-148">-Confirm</span></span>
<span data-ttu-id="cb6ed-149">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cb6ed-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb6ed-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb6ed-150">-WhatIf</span></span>
<span data-ttu-id="cb6ed-151">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cb6ed-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb6ed-152">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cb6ed-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb6ed-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb6ed-153">CommonParameters</span></span>
<span data-ttu-id="cb6ed-154">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cb6ed-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb6ed-155">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="cb6ed-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb6ed-156">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cb6ed-156">INPUTS</span></span>

### <span data-ttu-id="cb6ed-157">Microsoft. Azure. Command. SQL. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="cb6ed-157">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="cb6ed-158">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cb6ed-158">OUTPUTS</span></span>

### <span data-ttu-id="cb6ed-159">Microsoft. Azure. Command. SQL. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="cb6ed-159">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="cb6ed-160">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cb6ed-160">NOTES</span></span>

## <span data-ttu-id="cb6ed-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cb6ed-161">RELATED LINKS</span></span>
