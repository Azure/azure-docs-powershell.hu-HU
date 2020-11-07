---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobstepexecution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStepExecution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStepExecution.md
ms.openlocfilehash: 03c4a6dede1f60e782bbfecdec1fb18894b2ca15
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847434"
---
# <span data-ttu-id="2d36f-101">Get-AzSqlElasticJobStepExecution</span><span class="sxs-lookup"><span data-stu-id="2d36f-101">Get-AzSqlElasticJobStepExecution</span></span>

## <span data-ttu-id="2d36f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2d36f-102">SYNOPSIS</span></span>
<span data-ttu-id="2d36f-103">Egy vagy több feladat-végrehajtási lépés végrehajtása</span><span class="sxs-lookup"><span data-stu-id="2d36f-103">Gets one or more job step executions</span></span>

## <span data-ttu-id="2d36f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2d36f-104">SYNTAX</span></span>

### <span data-ttu-id="2d36f-105">DefaultSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2d36f-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobStepExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>]
 [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2d36f-106">WithJobStepName</span><span class="sxs-lookup"><span data-stu-id="2d36f-106">WithJobStepName</span></span>
```
Get-AzSqlElasticJobStepExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> -StepName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2d36f-107">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="2d36f-107">ObjectSet</span></span>
```
Get-AzSqlElasticJobStepExecution [-ParentObject] <AzureSqlElasticJobExecutionModel> [-CreateTimeMin <DateTime>]
 [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2d36f-108">WithJobStepNameUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="2d36f-108">WithJobStepNameUsingParentObject</span></span>
```
Get-AzSqlElasticJobStepExecution [-ParentObject] <AzureSqlElasticJobExecutionModel> -StepName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2d36f-109">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="2d36f-109">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobStepExecution [-ParentResourceId] <String> [-CreateTimeMin <DateTime>]
 [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2d36f-110">WithJobStepNameUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="2d36f-110">WithJobStepNameUsingParentResourceId</span></span>
```
Get-AzSqlElasticJobStepExecution [-ParentResourceId] <String> -StepName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2d36f-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="2d36f-111">DESCRIPTION</span></span>
<span data-ttu-id="2d36f-112">A Get-AzSqlElasticJobStepExecution parancsmag egy vagy több feladat-végrehajtást kap a projekt végrehajtásához</span><span class="sxs-lookup"><span data-stu-id="2d36f-112">The Get-AzSqlElasticJobStepExecution cmdlet gets one or more job step executions from a job execution</span></span>

## <span data-ttu-id="2d36f-113">Példák</span><span class="sxs-lookup"><span data-stu-id="2d36f-113">EXAMPLES</span></span>

### <span data-ttu-id="2d36f-114">Példa 1 – egy vagy több feladat-végrehajtási lépés végrehajtása a projekt végrehajtásában</span><span class="sxs-lookup"><span data-stu-id="2d36f-114">Example 1 - Gets one or more job step executions from a job executions</span></span>
```
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId 3bcfc912-20b2-411d-a2b7-6265d13fe272
$je | Get-AzSqlElasticJobStepExecution

JobName JobVersion StepName StepId JobExecutionId                       Lifecycle StartTime            EndTime
------- ---------- -------- ------ --------------                       --------- ---------            -------
job1    1          step1    1      3bcfc912-20b2-411d-a2b7-6265d13fe272 Succeeded 6/1/2018 10:11:44 PM 6/1/2018 10:11:47 PM
```

### <span data-ttu-id="2d36f-115">Példa: 2 – egy vagy több feladat-végrehajtási lépés végrehajtása a projekt végrehajtásában, a szűrés lépésről lépésre</span><span class="sxs-lookup"><span data-stu-id="2d36f-115">Example 2 - Gets one or more job step executions from a job execution, filtering by step name</span></span>
```
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId 3bcfc912-20b2-411d-a2b7-6265d13fe272
$je | Get-AzSqlElasticJobStepExecution -StepName step1

JobName JobVersion StepName StepId JobExecutionId                       Lifecycle StartTime            EndTime
------- ---------- -------- ------ --------------                       --------- ---------            -------
job1    1          step1    1      3bcfc912-20b2-411d-a2b7-6265d13fe272 Succeeded 6/1/2018 10:11:44 PM 6/1/2018 10:11:47 PM
```

<span data-ttu-id="2d36f-116">Egy vagy több feladat-végrehajtási lépés végrehajtása</span><span class="sxs-lookup"><span data-stu-id="2d36f-116">Gets one or more job step executions</span></span>

## <span data-ttu-id="2d36f-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2d36f-117">PARAMETERS</span></span>

### <span data-ttu-id="2d36f-118">-Aktív</span><span class="sxs-lookup"><span data-stu-id="2d36f-118">-Active</span></span>
<span data-ttu-id="2d36f-119">Megjelölés aktív kivégzéssel való szűrésre</span><span class="sxs-lookup"><span data-stu-id="2d36f-119">Flag to filter by active executions.</span></span>

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

### <span data-ttu-id="2d36f-120">-AgentName</span><span class="sxs-lookup"><span data-stu-id="2d36f-120">-AgentName</span></span>
<span data-ttu-id="2d36f-121">A meghatalmazott neve.</span><span class="sxs-lookup"><span data-stu-id="2d36f-121">The agent name.</span></span>

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

### <span data-ttu-id="2d36f-122">-CreateTimeMax</span><span class="sxs-lookup"><span data-stu-id="2d36f-122">-CreateTimeMax</span></span>
<span data-ttu-id="2d36f-123">Szűrés a maximális idő létrehozásával</span><span class="sxs-lookup"><span data-stu-id="2d36f-123">Filter by create time max</span></span>

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

### <span data-ttu-id="2d36f-124">-CreateTimeMin</span><span class="sxs-lookup"><span data-stu-id="2d36f-124">-CreateTimeMin</span></span>
<span data-ttu-id="2d36f-125">Szűrés a min idő létrehozásával</span><span class="sxs-lookup"><span data-stu-id="2d36f-125">Filter by create time min</span></span>

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

### <span data-ttu-id="2d36f-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d36f-126">-DefaultProfile</span></span>
<span data-ttu-id="2d36f-127">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2d36f-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d36f-128">-EndTimeMax</span><span class="sxs-lookup"><span data-stu-id="2d36f-128">-EndTimeMax</span></span>
<span data-ttu-id="2d36f-129">Szűrés a befejezési idő Max szerint</span><span class="sxs-lookup"><span data-stu-id="2d36f-129">Filter by end time max.</span></span>

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

### <span data-ttu-id="2d36f-130">-EndTimeMin</span><span class="sxs-lookup"><span data-stu-id="2d36f-130">-EndTimeMin</span></span>
<span data-ttu-id="2d36f-131">Szűrés befejezési idő szerint</span><span class="sxs-lookup"><span data-stu-id="2d36f-131">Filter by end time min.</span></span>

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

### <span data-ttu-id="2d36f-132">-JobExecutionId</span><span class="sxs-lookup"><span data-stu-id="2d36f-132">-JobExecutionId</span></span>
<span data-ttu-id="2d36f-133">A feladat-végrehajtási azonosító.</span><span class="sxs-lookup"><span data-stu-id="2d36f-133">The job execution id.</span></span>

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

### <span data-ttu-id="2d36f-134">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="2d36f-134">-JobName</span></span>
<span data-ttu-id="2d36f-135">A feladat neve.</span><span class="sxs-lookup"><span data-stu-id="2d36f-135">The job name.</span></span>

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

### <span data-ttu-id="2d36f-136">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="2d36f-136">-ParentObject</span></span>
<span data-ttu-id="2d36f-137">Az Agent objektum.</span><span class="sxs-lookup"><span data-stu-id="2d36f-137">The agent object.</span></span>

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

### <span data-ttu-id="2d36f-138">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="2d36f-138">-ParentResourceId</span></span>
<span data-ttu-id="2d36f-139">A feladat-végrehajtás erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="2d36f-139">The job execution resource id.</span></span>

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

### <span data-ttu-id="2d36f-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d36f-140">-ResourceGroupName</span></span>
<span data-ttu-id="2d36f-141">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="2d36f-141">The resource group name.</span></span>

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

### <span data-ttu-id="2d36f-142">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="2d36f-142">-ServerName</span></span>
<span data-ttu-id="2d36f-143">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="2d36f-143">The server name.</span></span>

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

### <span data-ttu-id="2d36f-144">-StepName</span><span class="sxs-lookup"><span data-stu-id="2d36f-144">-StepName</span></span>
<span data-ttu-id="2d36f-145">A feladat lépéseinek neve.</span><span class="sxs-lookup"><span data-stu-id="2d36f-145">The job step name.</span></span>

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

### <span data-ttu-id="2d36f-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d36f-146">CommonParameters</span></span>
<span data-ttu-id="2d36f-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2d36f-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d36f-148">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="2d36f-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d36f-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2d36f-149">INPUTS</span></span>

### <span data-ttu-id="2d36f-150">Microsoft. Azure. Command. SQL. ElasticJobs. Model. AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="2d36f-150">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="2d36f-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2d36f-151">OUTPUTS</span></span>

### <span data-ttu-id="2d36f-152">Microsoft. Azure. Command. SQL. ElasticJobs. Model. AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="2d36f-152">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="2d36f-153">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2d36f-153">NOTES</span></span>

## <span data-ttu-id="2d36f-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2d36f-154">RELATED LINKS</span></span>
