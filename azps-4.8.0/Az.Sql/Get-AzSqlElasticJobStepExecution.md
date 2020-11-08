---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobstepexecution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStepExecution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStepExecution.md
ms.openlocfilehash: 03c4a6dede1f60e782bbfecdec1fb18894b2ca15
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182124"
---
# <span data-ttu-id="9dfbf-101">Get-AzSqlElasticJobStepExecution</span><span class="sxs-lookup"><span data-stu-id="9dfbf-101">Get-AzSqlElasticJobStepExecution</span></span>

## <span data-ttu-id="9dfbf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9dfbf-102">SYNOPSIS</span></span>
<span data-ttu-id="9dfbf-103">Egy vagy több feladat-végrehajtási lépés végrehajtása</span><span class="sxs-lookup"><span data-stu-id="9dfbf-103">Gets one or more job step executions</span></span>

## <span data-ttu-id="9dfbf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9dfbf-104">SYNTAX</span></span>

### <span data-ttu-id="9dfbf-105">DefaultSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9dfbf-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobStepExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>]
 [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9dfbf-106">WithJobStepName</span><span class="sxs-lookup"><span data-stu-id="9dfbf-106">WithJobStepName</span></span>
```
Get-AzSqlElasticJobStepExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> -StepName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9dfbf-107">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="9dfbf-107">ObjectSet</span></span>
```
Get-AzSqlElasticJobStepExecution [-ParentObject] <AzureSqlElasticJobExecutionModel> [-CreateTimeMin <DateTime>]
 [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9dfbf-108">WithJobStepNameUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="9dfbf-108">WithJobStepNameUsingParentObject</span></span>
```
Get-AzSqlElasticJobStepExecution [-ParentObject] <AzureSqlElasticJobExecutionModel> -StepName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9dfbf-109">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="9dfbf-109">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobStepExecution [-ParentResourceId] <String> [-CreateTimeMin <DateTime>]
 [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9dfbf-110">WithJobStepNameUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="9dfbf-110">WithJobStepNameUsingParentResourceId</span></span>
```
Get-AzSqlElasticJobStepExecution [-ParentResourceId] <String> -StepName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9dfbf-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="9dfbf-111">DESCRIPTION</span></span>
<span data-ttu-id="9dfbf-112">A Get-AzSqlElasticJobStepExecution parancsmag egy vagy több feladat-végrehajtást kap a projekt végrehajtásához</span><span class="sxs-lookup"><span data-stu-id="9dfbf-112">The Get-AzSqlElasticJobStepExecution cmdlet gets one or more job step executions from a job execution</span></span>

## <span data-ttu-id="9dfbf-113">Példák</span><span class="sxs-lookup"><span data-stu-id="9dfbf-113">EXAMPLES</span></span>

### <span data-ttu-id="9dfbf-114">Példa 1 – egy vagy több feladat-végrehajtási lépés végrehajtása a projekt végrehajtásában</span><span class="sxs-lookup"><span data-stu-id="9dfbf-114">Example 1 - Gets one or more job step executions from a job executions</span></span>
```
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId 3bcfc912-20b2-411d-a2b7-6265d13fe272
$je | Get-AzSqlElasticJobStepExecution

JobName JobVersion StepName StepId JobExecutionId                       Lifecycle StartTime            EndTime
------- ---------- -------- ------ --------------                       --------- ---------            -------
job1    1          step1    1      3bcfc912-20b2-411d-a2b7-6265d13fe272 Succeeded 6/1/2018 10:11:44 PM 6/1/2018 10:11:47 PM
```

### <span data-ttu-id="9dfbf-115">Példa: 2 – egy vagy több feladat-végrehajtási lépés végrehajtása a projekt végrehajtásában, a szűrés lépésről lépésre</span><span class="sxs-lookup"><span data-stu-id="9dfbf-115">Example 2 - Gets one or more job step executions from a job execution, filtering by step name</span></span>
```
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId 3bcfc912-20b2-411d-a2b7-6265d13fe272
$je | Get-AzSqlElasticJobStepExecution -StepName step1

JobName JobVersion StepName StepId JobExecutionId                       Lifecycle StartTime            EndTime
------- ---------- -------- ------ --------------                       --------- ---------            -------
job1    1          step1    1      3bcfc912-20b2-411d-a2b7-6265d13fe272 Succeeded 6/1/2018 10:11:44 PM 6/1/2018 10:11:47 PM
```

<span data-ttu-id="9dfbf-116">Egy vagy több feladat-végrehajtási lépés végrehajtása</span><span class="sxs-lookup"><span data-stu-id="9dfbf-116">Gets one or more job step executions</span></span>

## <span data-ttu-id="9dfbf-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9dfbf-117">PARAMETERS</span></span>

### <span data-ttu-id="9dfbf-118">-Aktív</span><span class="sxs-lookup"><span data-stu-id="9dfbf-118">-Active</span></span>
<span data-ttu-id="9dfbf-119">Megjelölés aktív kivégzéssel való szűrésre</span><span class="sxs-lookup"><span data-stu-id="9dfbf-119">Flag to filter by active executions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dfbf-120">-AgentName</span><span class="sxs-lookup"><span data-stu-id="9dfbf-120">-AgentName</span></span>
<span data-ttu-id="9dfbf-121">A meghatalmazott neve.</span><span class="sxs-lookup"><span data-stu-id="9dfbf-121">The agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobStepName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dfbf-122">-CreateTimeMax</span><span class="sxs-lookup"><span data-stu-id="9dfbf-122">-CreateTimeMax</span></span>
<span data-ttu-id="9dfbf-123">Szűrés a maximális idő létrehozásával</span><span class="sxs-lookup"><span data-stu-id="9dfbf-123">Filter by create time max</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dfbf-124">-CreateTimeMin</span><span class="sxs-lookup"><span data-stu-id="9dfbf-124">-CreateTimeMin</span></span>
<span data-ttu-id="9dfbf-125">Szűrés a min idő létrehozásával</span><span class="sxs-lookup"><span data-stu-id="9dfbf-125">Filter by create time min</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dfbf-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9dfbf-126">-DefaultProfile</span></span>
<span data-ttu-id="9dfbf-127">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9dfbf-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9dfbf-128">-EndTimeMax</span><span class="sxs-lookup"><span data-stu-id="9dfbf-128">-EndTimeMax</span></span>
<span data-ttu-id="9dfbf-129">Szűrés a befejezési idő Max szerint</span><span class="sxs-lookup"><span data-stu-id="9dfbf-129">Filter by end time max.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dfbf-130">-EndTimeMin</span><span class="sxs-lookup"><span data-stu-id="9dfbf-130">-EndTimeMin</span></span>
<span data-ttu-id="9dfbf-131">Szűrés befejezési idő szerint</span><span class="sxs-lookup"><span data-stu-id="9dfbf-131">Filter by end time min.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dfbf-132">-JobExecutionId</span><span class="sxs-lookup"><span data-stu-id="9dfbf-132">-JobExecutionId</span></span>
<span data-ttu-id="9dfbf-133">A feladat-végrehajtási azonosító.</span><span class="sxs-lookup"><span data-stu-id="9dfbf-133">The job execution id.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobStepName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dfbf-134">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="9dfbf-134">-JobName</span></span>
<span data-ttu-id="9dfbf-135">A feladat neve.</span><span class="sxs-lookup"><span data-stu-id="9dfbf-135">The job name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobStepName
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dfbf-136">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="9dfbf-136">-ParentObject</span></span>
<span data-ttu-id="9dfbf-137">Az Agent objektum.</span><span class="sxs-lookup"><span data-stu-id="9dfbf-137">The agent object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel
Parameter Sets: ObjectSet, WithJobStepNameUsingParentObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9dfbf-138">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="9dfbf-138">-ParentResourceId</span></span>
<span data-ttu-id="9dfbf-139">A feladat-végrehajtás erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="9dfbf-139">The job execution resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet, WithJobStepNameUsingParentResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9dfbf-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9dfbf-140">-ResourceGroupName</span></span>
<span data-ttu-id="9dfbf-141">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="9dfbf-141">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobStepName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dfbf-142">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="9dfbf-142">-ServerName</span></span>
<span data-ttu-id="9dfbf-143">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="9dfbf-143">The server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobStepName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dfbf-144">-StepName</span><span class="sxs-lookup"><span data-stu-id="9dfbf-144">-StepName</span></span>
<span data-ttu-id="9dfbf-145">A feladat lépéseinek neve.</span><span class="sxs-lookup"><span data-stu-id="9dfbf-145">The job step name.</span></span>

```yaml
Type: System.String
Parameter Sets: WithJobStepName, WithJobStepNameUsingParentObject, WithJobStepNameUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dfbf-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dfbf-146">CommonParameters</span></span>
<span data-ttu-id="9dfbf-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9dfbf-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dfbf-148">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="9dfbf-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dfbf-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9dfbf-149">INPUTS</span></span>

### <span data-ttu-id="9dfbf-150">Microsoft. Azure. Command. SQL. ElasticJobs. Model. AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="9dfbf-150">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="9dfbf-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9dfbf-151">OUTPUTS</span></span>

### <span data-ttu-id="9dfbf-152">Microsoft. Azure. Command. SQL. ElasticJobs. Model. AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="9dfbf-152">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="9dfbf-153">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9dfbf-153">NOTES</span></span>

## <span data-ttu-id="9dfbf-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9dfbf-154">RELATED LINKS</span></span>
