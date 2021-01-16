---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJob.md
ms.openlocfilehash: 53bd1b1cd1c2f7ba87df8cb5c27f1b2380db04af
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468101"
---
# <span data-ttu-id="496cb-101">Set-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="496cb-101">Set-AzSqlElasticJob</span></span>

## <span data-ttu-id="496cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="496cb-102">SYNOPSIS</span></span>
<span data-ttu-id="496cb-103">Feladat frissítése</span><span class="sxs-lookup"><span data-stu-id="496cb-103">Updates a job</span></span>

## <span data-ttu-id="496cb-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="496cb-104">SYNTAX</span></span>

### <span data-ttu-id="496cb-105">DefaultSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="496cb-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="496cb-106">RunOnce</span><span class="sxs-lookup"><span data-stu-id="496cb-106">RunOnce</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-RunOnce] [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="496cb-107">Ismétlődő</span><span class="sxs-lookup"><span data-stu-id="496cb-107">Recurring</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 -IntervalType <String> -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="496cb-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="496cb-108">ObjectSet</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> [-StartTime <DateTime>] [-EndTime <DateTime>]
 [-Enable] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="496cb-109">RunOnceUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="496cb-109">RunOnceUsingParentObject</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> [-RunOnce] [-StartTime <DateTime>]
 [-EndTime <DateTime>] [-Enable] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="496cb-110">RecurringUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="496cb-110">RecurringUsingParentObject</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> -IntervalType <String> -IntervalCount <UInt32>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="496cb-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="496cb-111">ResourceIdSet</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="496cb-112">RunOnceUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="496cb-112">RunOnceUsingParentResourceId</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> [-RunOnce] [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="496cb-113">RecurringUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="496cb-113">RecurringUsingParentResourceId</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> -IntervalType <String> -IntervalCount <UInt32>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="496cb-114">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="496cb-114">DESCRIPTION</span></span>
<span data-ttu-id="496cb-115">A Set-AzSqlElasticJob parancsmag frissíti a feladatot</span><span class="sxs-lookup"><span data-stu-id="496cb-115">The Set-AzSqlElasticJob cmdlet updates a job</span></span>

## <span data-ttu-id="496cb-116">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="496cb-116">EXAMPLES</span></span>

### <span data-ttu-id="496cb-117">1. példa: Frissíti a feladatot úgy, hogy egy óra múlva kezdődjön, és 1 óránként ismétlődjön</span><span class="sxs-lookup"><span data-stu-id="496cb-117">Example 1: Updates a job to start an hour from now and repeat every 1 hour</span></span>
```powershell
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name job1
$job | Set-AzSqlElasticJob -IntervalType Hour -IntervalCount 1 -StartTime (Get-Date).AddHours(1) -Enable

JobName Version Description StartTime            EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------            -------                ------------ -------- -------
job1    0                   6/1/2018 10:50:15 PM 12/31/9999 11:59:59 AM Recurring    PT1H     True
```

<span data-ttu-id="496cb-118">Feladat frissítése</span><span class="sxs-lookup"><span data-stu-id="496cb-118">Updates a job</span></span>

### <span data-ttu-id="496cb-119">2. példa</span><span class="sxs-lookup"><span data-stu-id="496cb-119">Example 2</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlElasticJob -AgentName agent -Enable -IntervalCount 1 -IntervalType Hour -Name step1 -ResourceGroupName MyResourceGroup -ServerName s1 -StartTime '9/16/2016 11:31:12'
```

## <span data-ttu-id="496cb-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="496cb-120">PARAMETERS</span></span>

### <span data-ttu-id="496cb-121">-AgentName</span><span class="sxs-lookup"><span data-stu-id="496cb-121">-AgentName</span></span>
<span data-ttu-id="496cb-122">Az ügynök neve</span><span class="sxs-lookup"><span data-stu-id="496cb-122">The agent name</span></span>

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

### <span data-ttu-id="496cb-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="496cb-123">-DefaultProfile</span></span>
<span data-ttu-id="496cb-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="496cb-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="496cb-125">-Leírás</span><span class="sxs-lookup"><span data-stu-id="496cb-125">-Description</span></span>
<span data-ttu-id="496cb-126">A feladat leírása</span><span class="sxs-lookup"><span data-stu-id="496cb-126">The job description</span></span>

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

### <span data-ttu-id="496cb-127">-Enable</span><span class="sxs-lookup"><span data-stu-id="496cb-127">-Enable</span></span>
<span data-ttu-id="496cb-128">Az ügyfeleket jelző jelölő engedélyezi ezt a feladatot.</span><span class="sxs-lookup"><span data-stu-id="496cb-128">The flag to indicate customer wants this job to be enabled.</span></span>

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

### <span data-ttu-id="496cb-129">-EndTime</span><span class="sxs-lookup"><span data-stu-id="496cb-129">-EndTime</span></span>
<span data-ttu-id="496cb-130">A munkabeosztás záró ideje</span><span class="sxs-lookup"><span data-stu-id="496cb-130">The job schedule end time</span></span>

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

### <span data-ttu-id="496cb-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="496cb-131">-InputObject</span></span>
<span data-ttu-id="496cb-132">A feladat beviteli objektuma</span><span class="sxs-lookup"><span data-stu-id="496cb-132">The job input object</span></span>

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

### <span data-ttu-id="496cb-133">-IntervalCount</span><span class="sxs-lookup"><span data-stu-id="496cb-133">-IntervalCount</span></span>
<span data-ttu-id="496cb-134">Az ismétlődő ütemezési intervallumok száma</span><span class="sxs-lookup"><span data-stu-id="496cb-134">The recurring schedule interval count</span></span>

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

### <span data-ttu-id="496cb-135">-IntervalType</span><span class="sxs-lookup"><span data-stu-id="496cb-135">-IntervalType</span></span>
<span data-ttu-id="496cb-136">Az ismétlődő ütemezési intervallum típusa – Lehet perc, óra, nap, hét, hónap</span><span class="sxs-lookup"><span data-stu-id="496cb-136">The recurring schedule interval type - Can be Minute, Hour, Day, Week, Month</span></span>

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

### <span data-ttu-id="496cb-137">-Name</span><span class="sxs-lookup"><span data-stu-id="496cb-137">-Name</span></span>
<span data-ttu-id="496cb-138">A feladat neve</span><span class="sxs-lookup"><span data-stu-id="496cb-138">The job name</span></span>

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

### <span data-ttu-id="496cb-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="496cb-139">-ResourceGroupName</span></span>
<span data-ttu-id="496cb-140">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="496cb-140">The resource group name</span></span>

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

### <span data-ttu-id="496cb-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="496cb-141">-ResourceId</span></span>
<span data-ttu-id="496cb-142">A feladaterőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="496cb-142">The job resource id</span></span>

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

### <span data-ttu-id="496cb-143">-RunOnce</span><span class="sxs-lookup"><span data-stu-id="496cb-143">-RunOnce</span></span>
<span data-ttu-id="496cb-144">A feladat jelzésére jelző jelölő egyszer fog futni</span><span class="sxs-lookup"><span data-stu-id="496cb-144">The flag to indicate job will be run once</span></span>

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

### <span data-ttu-id="496cb-145">-ServerName</span><span class="sxs-lookup"><span data-stu-id="496cb-145">-ServerName</span></span>
<span data-ttu-id="496cb-146">A kiszolgáló neve</span><span class="sxs-lookup"><span data-stu-id="496cb-146">The server name</span></span>

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

### <span data-ttu-id="496cb-147">-StartTime</span><span class="sxs-lookup"><span data-stu-id="496cb-147">-StartTime</span></span>
<span data-ttu-id="496cb-148">A munkabeosztás kezdési ideje</span><span class="sxs-lookup"><span data-stu-id="496cb-148">The job schedule start time</span></span>

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

### <span data-ttu-id="496cb-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="496cb-149">-Confirm</span></span>
<span data-ttu-id="496cb-150">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="496cb-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="496cb-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="496cb-151">-WhatIf</span></span>
<span data-ttu-id="496cb-152">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="496cb-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="496cb-153">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="496cb-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="496cb-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="496cb-154">CommonParameters</span></span>
<span data-ttu-id="496cb-155">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="496cb-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="496cb-156">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="496cb-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="496cb-157">INPUTS</span><span class="sxs-lookup"><span data-stu-id="496cb-157">INPUTS</span></span>

### <span data-ttu-id="496cb-158">Microsoft.Azure.Commands.Sql.ElasticMods.Model.AzureSqlElasticModel</span><span class="sxs-lookup"><span data-stu-id="496cb-158">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="496cb-159">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="496cb-159">OUTPUTS</span></span>

### <span data-ttu-id="496cb-160">Microsoft.Azure.Commands.Sql.ElasticMods.Model.AzureSqlElasticModel</span><span class="sxs-lookup"><span data-stu-id="496cb-160">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="496cb-161">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="496cb-161">NOTES</span></span>

## <span data-ttu-id="496cb-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="496cb-162">RELATED LINKS</span></span>
