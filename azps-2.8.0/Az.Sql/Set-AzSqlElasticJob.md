---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJob.md
ms.openlocfilehash: 04f182cb410e77a9ca61aa6f80da14c08e517406
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839286"
---
# <span data-ttu-id="6ebb9-101">Set-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="6ebb9-101">Set-AzSqlElasticJob</span></span>

## <span data-ttu-id="6ebb9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6ebb9-102">SYNOPSIS</span></span>
<span data-ttu-id="6ebb9-103">Feladat frissítése</span><span class="sxs-lookup"><span data-stu-id="6ebb9-103">Updates a job</span></span>

## <span data-ttu-id="6ebb9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6ebb9-104">SYNTAX</span></span>

### <span data-ttu-id="6ebb9-105">DefaultSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6ebb9-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ebb9-106">Túlfolyás</span><span class="sxs-lookup"><span data-stu-id="6ebb9-106">RunOnce</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-RunOnce] [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ebb9-107">Ismétlődő</span><span class="sxs-lookup"><span data-stu-id="6ebb9-107">Recurring</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 -IntervalType <String> -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ebb9-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="6ebb9-108">ObjectSet</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> [-StartTime <DateTime>] [-EndTime <DateTime>]
 [-Enable] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6ebb9-109">RunOnceUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="6ebb9-109">RunOnceUsingParentObject</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> [-RunOnce] [-StartTime <DateTime>]
 [-EndTime <DateTime>] [-Enable] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ebb9-110">RecurringUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="6ebb9-110">RecurringUsingParentObject</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> -IntervalType <String> -IntervalCount <UInt32>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ebb9-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="6ebb9-111">ResourceIdSet</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ebb9-112">RunOnceUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="6ebb9-112">RunOnceUsingParentResourceId</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> [-RunOnce] [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ebb9-113">RecurringUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="6ebb9-113">RecurringUsingParentResourceId</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> -IntervalType <String> -IntervalCount <UInt32>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ebb9-114">Leírás</span><span class="sxs-lookup"><span data-stu-id="6ebb9-114">DESCRIPTION</span></span>
<span data-ttu-id="6ebb9-115">A Set-AzSqlElasticJob parancsmag frissíti a feladatot</span><span class="sxs-lookup"><span data-stu-id="6ebb9-115">The Set-AzSqlElasticJob cmdlet updates a job</span></span>

## <span data-ttu-id="6ebb9-116">Példák</span><span class="sxs-lookup"><span data-stu-id="6ebb9-116">EXAMPLES</span></span>

### <span data-ttu-id="6ebb9-117">Példa 1 – a feladat frissítése az óra megkezdése után 1 óránként ismétlődik</span><span class="sxs-lookup"><span data-stu-id="6ebb9-117">Example 1 - Updates a job to start an hour from now and repeat every 1 hour</span></span>
```
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name job1
$job | Set-AzSqlElasticJob -IntervalType Hour -IntervalCount 1 -StartTime (Get-Date).AddHours(1) -Enable

JobName Version Description StartTime            EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------            -------                ------------ -------- -------
job1    0                   6/1/2018 10:50:15 PM 12/31/9999 11:59:59 AM Recurring    PT1H     True
```

<span data-ttu-id="6ebb9-118">Feladat frissítése</span><span class="sxs-lookup"><span data-stu-id="6ebb9-118">Updates a job</span></span>

## <span data-ttu-id="6ebb9-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6ebb9-119">PARAMETERS</span></span>

### <span data-ttu-id="6ebb9-120">-AgentName</span><span class="sxs-lookup"><span data-stu-id="6ebb9-120">-AgentName</span></span>
<span data-ttu-id="6ebb9-121">Az ügynök neve</span><span class="sxs-lookup"><span data-stu-id="6ebb9-121">The agent name</span></span>

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

### <span data-ttu-id="6ebb9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ebb9-122">-DefaultProfile</span></span>
<span data-ttu-id="6ebb9-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6ebb9-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ebb9-124">-Leírás</span><span class="sxs-lookup"><span data-stu-id="6ebb9-124">-Description</span></span>
<span data-ttu-id="6ebb9-125">A munkakör leírása</span><span class="sxs-lookup"><span data-stu-id="6ebb9-125">The job description</span></span>

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

### <span data-ttu-id="6ebb9-126">– Engedélyezés</span><span class="sxs-lookup"><span data-stu-id="6ebb9-126">-Enable</span></span>
<span data-ttu-id="6ebb9-127">Annak jelzése, hogy az ügyfél szeretné-e engedélyezni ezt a feladatot.</span><span class="sxs-lookup"><span data-stu-id="6ebb9-127">The flag to indicate customer wants this job to be enabled.</span></span>

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

### <span data-ttu-id="6ebb9-128">-A befejezési időpont</span><span class="sxs-lookup"><span data-stu-id="6ebb9-128">-EndTime</span></span>
<span data-ttu-id="6ebb9-129">A projekt ütemtervének befejezési időpontja</span><span class="sxs-lookup"><span data-stu-id="6ebb9-129">The job schedule end time</span></span>

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

### <span data-ttu-id="6ebb9-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6ebb9-130">-InputObject</span></span>
<span data-ttu-id="6ebb9-131">A projekt bemeneti objektuma</span><span class="sxs-lookup"><span data-stu-id="6ebb9-131">The job input object</span></span>

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

### <span data-ttu-id="6ebb9-132">-IntervalCount</span><span class="sxs-lookup"><span data-stu-id="6ebb9-132">-IntervalCount</span></span>
<span data-ttu-id="6ebb9-133">Az ismétlődő ütemezési intervallumok száma</span><span class="sxs-lookup"><span data-stu-id="6ebb9-133">The recurring schedule interval count</span></span>

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

### <span data-ttu-id="6ebb9-134">-IntervalType</span><span class="sxs-lookup"><span data-stu-id="6ebb9-134">-IntervalType</span></span>
<span data-ttu-id="6ebb9-135">Az ismétlődő ütemezési intervallum típusa lehet perc, óra, nap, hét, hónap</span><span class="sxs-lookup"><span data-stu-id="6ebb9-135">The recurring schedule interval type - Can be Minute, Hour, Day, Week, Month</span></span>

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

### <span data-ttu-id="6ebb9-136">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6ebb9-136">-Name</span></span>
<span data-ttu-id="6ebb9-137">A feladat neve</span><span class="sxs-lookup"><span data-stu-id="6ebb9-137">The job name</span></span>

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

### <span data-ttu-id="6ebb9-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ebb9-138">-ResourceGroupName</span></span>
<span data-ttu-id="6ebb9-139">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="6ebb9-139">The resource group name</span></span>

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

### <span data-ttu-id="6ebb9-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6ebb9-140">-ResourceId</span></span>
<span data-ttu-id="6ebb9-141">A projekt erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="6ebb9-141">The job resource id</span></span>

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

### <span data-ttu-id="6ebb9-142">-Túlfolyás</span><span class="sxs-lookup"><span data-stu-id="6ebb9-142">-RunOnce</span></span>
<span data-ttu-id="6ebb9-143">A feladat megjelölésére szolgáló jelölő egyszer fog futni</span><span class="sxs-lookup"><span data-stu-id="6ebb9-143">The flag to indicate job will be run once</span></span>

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

### <span data-ttu-id="6ebb9-144">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="6ebb9-144">-ServerName</span></span>
<span data-ttu-id="6ebb9-145">A kiszolgáló neve</span><span class="sxs-lookup"><span data-stu-id="6ebb9-145">The server name</span></span>

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

### <span data-ttu-id="6ebb9-146">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="6ebb9-146">-StartTime</span></span>
<span data-ttu-id="6ebb9-147">A projekt ütemtervének kezdési időpontja</span><span class="sxs-lookup"><span data-stu-id="6ebb9-147">The job schedule start time</span></span>

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

### <span data-ttu-id="6ebb9-148">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6ebb9-148">-Confirm</span></span>
<span data-ttu-id="6ebb9-149">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6ebb9-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ebb9-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ebb9-150">-WhatIf</span></span>
<span data-ttu-id="6ebb9-151">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6ebb9-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ebb9-152">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6ebb9-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ebb9-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ebb9-153">CommonParameters</span></span>
<span data-ttu-id="6ebb9-154">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6ebb9-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ebb9-155">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="6ebb9-155">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ebb9-156">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6ebb9-156">INPUTS</span></span>

### <span data-ttu-id="6ebb9-157">Microsoft. Azure. Command. SQL. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="6ebb9-157">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="6ebb9-158">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6ebb9-158">OUTPUTS</span></span>

### <span data-ttu-id="6ebb9-159">Microsoft. Azure. Command. SQL. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="6ebb9-159">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="6ebb9-160">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6ebb9-160">NOTES</span></span>

## <span data-ttu-id="6ebb9-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6ebb9-161">RELATED LINKS</span></span>
