---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJob.md
ms.openlocfilehash: e6853c3b4fa32a10e93ee281aab0b97755403671
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186685"
---
# <span data-ttu-id="1641e-101">New-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="1641e-101">New-AzSqlElasticJob</span></span>

## <span data-ttu-id="1641e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1641e-102">SYNOPSIS</span></span>
<span data-ttu-id="1641e-103">Új feladat létrehozása</span><span class="sxs-lookup"><span data-stu-id="1641e-103">Creates a new job</span></span>

## <span data-ttu-id="1641e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1641e-104">SYNTAX</span></span>

### <span data-ttu-id="1641e-105">DefaultSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1641e-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1641e-106">Túlfolyás</span><span class="sxs-lookup"><span data-stu-id="1641e-106">RunOnce</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-RunOnce] [-StartTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1641e-107">Ismétlődő</span><span class="sxs-lookup"><span data-stu-id="1641e-107">Recurring</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 -IntervalType <String> -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>]
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1641e-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="1641e-108">ObjectSet</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> [-Description <String>]
 [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1641e-109">RunOnceUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="1641e-109">RunOnceUsingParentObject</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> [-RunOnce]
 [-StartTime <DateTime>] [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1641e-110">RecurringUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="1641e-110">RecurringUsingParentObject</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> -IntervalType <String>
 -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1641e-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="1641e-111">ResourceIdSet</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1641e-112">RunOnceUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="1641e-112">RunOnceUsingParentResourceId</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> [-RunOnce] [-StartTime <DateTime>]
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1641e-113">RecurringUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="1641e-113">RecurringUsingParentResourceId</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> -IntervalType <String>
 -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1641e-114">Leírás</span><span class="sxs-lookup"><span data-stu-id="1641e-114">DESCRIPTION</span></span>
<span data-ttu-id="1641e-115">A New-AzSqlElasticJob parancsmag új feladatot hoz létre</span><span class="sxs-lookup"><span data-stu-id="1641e-115">The New-AzSqlElasticJob cmdlet creates a new job</span></span>

## <span data-ttu-id="1641e-116">Példák</span><span class="sxs-lookup"><span data-stu-id="1641e-116">EXAMPLES</span></span>

### <span data-ttu-id="1641e-117">1. példa: új feladat létrehozása</span><span class="sxs-lookup"><span data-stu-id="1641e-117">Example 1: Creates a new job</span></span>
```powershell
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | New-AzSqlElasticJob -Name job1

JobName Version Description StartTime           EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------           -------                ------------ -------- -------
job1    0                   6/1/2018 9:46:29 PM 12/31/9999 11:59:59 AM Once                  False
```

<span data-ttu-id="1641e-118">Új feladat létrehozása</span><span class="sxs-lookup"><span data-stu-id="1641e-118">Creates a new job</span></span>

### <span data-ttu-id="1641e-119">2. példa</span><span class="sxs-lookup"><span data-stu-id="1641e-119">Example 2</span></span>

<span data-ttu-id="1641e-120">Új feladatot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="1641e-120">Creates a new job.</span></span> <span data-ttu-id="1641e-121">autogenerated</span><span class="sxs-lookup"><span data-stu-id="1641e-121">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzSqlElasticJob -Name job1 -RunOnce
```

## <span data-ttu-id="1641e-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1641e-122">PARAMETERS</span></span>

### <span data-ttu-id="1641e-123">-AgentName</span><span class="sxs-lookup"><span data-stu-id="1641e-123">-AgentName</span></span>
<span data-ttu-id="1641e-124">Az ügynök neve</span><span class="sxs-lookup"><span data-stu-id="1641e-124">The agent name</span></span>

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

### <span data-ttu-id="1641e-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1641e-125">-DefaultProfile</span></span>
<span data-ttu-id="1641e-126">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1641e-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1641e-127">-Leírás</span><span class="sxs-lookup"><span data-stu-id="1641e-127">-Description</span></span>
<span data-ttu-id="1641e-128">A munkakör leírása</span><span class="sxs-lookup"><span data-stu-id="1641e-128">The job description</span></span>

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

### <span data-ttu-id="1641e-129">– Engedélyezés</span><span class="sxs-lookup"><span data-stu-id="1641e-129">-Enable</span></span>
<span data-ttu-id="1641e-130">Annak jelzése, hogy az ügyfél szeretné-e engedélyezni ezt a feladatot.</span><span class="sxs-lookup"><span data-stu-id="1641e-130">The flag to indicate customer wants this job to be enabled.</span></span>

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

### <span data-ttu-id="1641e-131">-A befejezési időpont</span><span class="sxs-lookup"><span data-stu-id="1641e-131">-EndTime</span></span>
<span data-ttu-id="1641e-132">A projekt ütemtervének befejezési időpontja</span><span class="sxs-lookup"><span data-stu-id="1641e-132">The job schedule end time</span></span>

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

### <span data-ttu-id="1641e-133">-IntervalCount</span><span class="sxs-lookup"><span data-stu-id="1641e-133">-IntervalCount</span></span>
<span data-ttu-id="1641e-134">Az ismétlődő ütemezési intervallumok száma</span><span class="sxs-lookup"><span data-stu-id="1641e-134">The recurring schedule interval count</span></span>

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

### <span data-ttu-id="1641e-135">-IntervalType</span><span class="sxs-lookup"><span data-stu-id="1641e-135">-IntervalType</span></span>
<span data-ttu-id="1641e-136">Az ismétlődő ütemezési intervallum típusa lehet perc, óra, nap, hét, hónap</span><span class="sxs-lookup"><span data-stu-id="1641e-136">The recurring schedule interval type - Can be Minute, Hour, Day, Week, Month</span></span>

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

### <span data-ttu-id="1641e-137">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1641e-137">-Name</span></span>
<span data-ttu-id="1641e-138">A feladat neve</span><span class="sxs-lookup"><span data-stu-id="1641e-138">The job name</span></span>

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

### <span data-ttu-id="1641e-139">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="1641e-139">-ParentObject</span></span>
<span data-ttu-id="1641e-140">Ügynök beviteli objektuma</span><span class="sxs-lookup"><span data-stu-id="1641e-140">The agent input object</span></span>

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

### <span data-ttu-id="1641e-141">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="1641e-141">-ParentResourceId</span></span>
<span data-ttu-id="1641e-142">Az ügynök erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="1641e-142">The agent resource id</span></span>

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

### <span data-ttu-id="1641e-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1641e-143">-ResourceGroupName</span></span>
<span data-ttu-id="1641e-144">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="1641e-144">The resource group name</span></span>

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

### <span data-ttu-id="1641e-145">-Túlfolyás</span><span class="sxs-lookup"><span data-stu-id="1641e-145">-RunOnce</span></span>
<span data-ttu-id="1641e-146">A feladat megjelölésére szolgáló jelölő egyszer fog futni</span><span class="sxs-lookup"><span data-stu-id="1641e-146">The flag to indicate job will be run once</span></span>

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

### <span data-ttu-id="1641e-147">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="1641e-147">-ServerName</span></span>
<span data-ttu-id="1641e-148">A kiszolgáló neve</span><span class="sxs-lookup"><span data-stu-id="1641e-148">The server name</span></span>

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

### <span data-ttu-id="1641e-149">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="1641e-149">-StartTime</span></span>
<span data-ttu-id="1641e-150">A projekt ütemtervének kezdési időpontja</span><span class="sxs-lookup"><span data-stu-id="1641e-150">The job schedule start time</span></span>

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

### <span data-ttu-id="1641e-151">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1641e-151">-Confirm</span></span>
<span data-ttu-id="1641e-152">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1641e-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1641e-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1641e-153">-WhatIf</span></span>
<span data-ttu-id="1641e-154">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1641e-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1641e-155">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1641e-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1641e-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1641e-156">CommonParameters</span></span>
<span data-ttu-id="1641e-157">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1641e-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1641e-158">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1641e-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1641e-159">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1641e-159">INPUTS</span></span>

### <span data-ttu-id="1641e-160">Microsoft. Azure. Command. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="1641e-160">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="1641e-161">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1641e-161">OUTPUTS</span></span>

### <span data-ttu-id="1641e-162">Microsoft. Azure. Command. SQL. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="1641e-162">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="1641e-163">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1641e-163">NOTES</span></span>

## <span data-ttu-id="1641e-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1641e-164">RELATED LINKS</span></span>
