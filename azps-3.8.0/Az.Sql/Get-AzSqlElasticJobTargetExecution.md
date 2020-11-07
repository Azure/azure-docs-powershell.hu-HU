---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobtargetexecution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobTargetExecution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobTargetExecution.md
ms.openlocfilehash: 566bfb8caae85c6f4e6ef75a38bdd5363ddb1eaa
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847425"
---
# <span data-ttu-id="0fba9-101">Get-AzSqlElasticJobTargetExecution</span><span class="sxs-lookup"><span data-stu-id="0fba9-101">Get-AzSqlElasticJobTargetExecution</span></span>

## <span data-ttu-id="0fba9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0fba9-102">SYNOPSIS</span></span>
<span data-ttu-id="0fba9-103">Egy vagy több Job Target-végrehajtást kap</span><span class="sxs-lookup"><span data-stu-id="0fba9-103">Gets one or more job target executions</span></span>

## <span data-ttu-id="0fba9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0fba9-104">SYNTAX</span></span>

### <span data-ttu-id="0fba9-105">DefaultSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0fba9-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobTargetExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> -Count <Int32> [-StepName <String>] [-CreateTimeMin <DateTime>]
 [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0fba9-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="0fba9-106">ObjectSet</span></span>
```
Get-AzSqlElasticJobTargetExecution [-ParentObject] <AzureSqlElasticJobExecutionModel> -Count <Int32>
 [-StepName <String>] [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>]
 [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0fba9-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="0fba9-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobTargetExecution [-ParentResourceId] <String> -Count <Int32> [-StepName <String>]
 [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>]
 [-Active] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0fba9-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="0fba9-108">DESCRIPTION</span></span>
<span data-ttu-id="0fba9-109">A Get-AzSqlElasticJobTargetExecution parancsmag egy vagy több projektfeladat-végrehajtási feladatot kap a projekt végrehajtásához</span><span class="sxs-lookup"><span data-stu-id="0fba9-109">The Get-AzSqlElasticJobTargetExecution cmdlet gets one or more job target executions from a job execution</span></span>

## <span data-ttu-id="0fba9-110">Példák</span><span class="sxs-lookup"><span data-stu-id="0fba9-110">EXAMPLES</span></span>

### <span data-ttu-id="0fba9-111">Példa 1 – egy vagy több projektfeladat kivégzése a projekt végrehajtásához</span><span class="sxs-lookup"><span data-stu-id="0fba9-111">Example 1 - Gets one or more job target executions from a job executions</span></span>
```
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId 3bcfc912-20b2-411d-a2b7-6265d13fe272
$je | Get-AzSqlElasticJobTargetExecution -Count 2
JobName JobVersion StepName StepId JobExecutionId                       Lifecycle       TargetServerName TargetDatabaseName StartTime            EndTime
------- ---------- -------- ------ --------------                       ---------       ---------------- ------------------ ---------            -------
job1    1          step2    1      ea0a870b-dfe3-427e-9f95-d229d7815b65 Succeeded       s1               db2                6/1/2018 10:11:47 PM 6/1/2018 10:11:50 PM
job1    1          step1    1      ea0a870b-dfe3-427e-9f95-d229d7815b65 Succeeded       s1               db1                6/1/2018 10:11:44 PM 6/1/2018 10:11:47 PM
```

### <span data-ttu-id="0fba9-112">Példa: 2 – egy vagy több projektfeladat-végrehajtási művelet végrehajtása a projekt végrehajtásában – a szűrés lépésről lépésre</span><span class="sxs-lookup"><span data-stu-id="0fba9-112">Example 2 - Gets one or more job target executions from a job executions - filtering by step name</span></span>
```
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId 3bcfc912-20b2-411d-a2b7-6265d13fe272
$je | Get-AzSqlElasticJobTargetExecution -Count 2 -StepName step2
JobName JobVersion StepName StepId JobExecutionId                       Lifecycle       TargetServerName TargetDatabaseName StartTime            EndTime
------- ---------- -------- ------ --------------                       ---------       ---------------- ------------------ ---------            -------
job1    1          step2    1      ea0a870b-dfe3-427e-9f95-d229d7815b65 Succeeded       s1               db2                6/1/2018 10:11:47 PM 6/1/2018 10:11:50 PM
```

<span data-ttu-id="0fba9-113">Egy vagy több Job Target-végrehajtást kap</span><span class="sxs-lookup"><span data-stu-id="0fba9-113">Gets one or more job target executions</span></span>

## <span data-ttu-id="0fba9-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0fba9-114">PARAMETERS</span></span>

### <span data-ttu-id="0fba9-115">-Aktív</span><span class="sxs-lookup"><span data-stu-id="0fba9-115">-Active</span></span>
<span data-ttu-id="0fba9-116">Megjelölés aktív kivégzéssel való szűrésre</span><span class="sxs-lookup"><span data-stu-id="0fba9-116">Flag to filter by active executions.</span></span>

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

### <span data-ttu-id="0fba9-117">-AgentName</span><span class="sxs-lookup"><span data-stu-id="0fba9-117">-AgentName</span></span>
<span data-ttu-id="0fba9-118">A meghatalmazott neve.</span><span class="sxs-lookup"><span data-stu-id="0fba9-118">The agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fba9-119">-Count</span><span class="sxs-lookup"><span data-stu-id="0fba9-119">-Count</span></span>
<span data-ttu-id="0fba9-120">A Count függvény a kivégzések legfelső számát számítja ki.</span><span class="sxs-lookup"><span data-stu-id="0fba9-120">Count returns the top number of executions.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fba9-121">-CreateTimeMax</span><span class="sxs-lookup"><span data-stu-id="0fba9-121">-CreateTimeMax</span></span>
<span data-ttu-id="0fba9-122">Szűrés a maximális idő létrehozásával</span><span class="sxs-lookup"><span data-stu-id="0fba9-122">Filter by create time max</span></span>

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

### <span data-ttu-id="0fba9-123">-CreateTimeMin</span><span class="sxs-lookup"><span data-stu-id="0fba9-123">-CreateTimeMin</span></span>
<span data-ttu-id="0fba9-124">Szűrés a min idő létrehozásával</span><span class="sxs-lookup"><span data-stu-id="0fba9-124">Filter by create time min</span></span>

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

### <span data-ttu-id="0fba9-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fba9-125">-DefaultProfile</span></span>
<span data-ttu-id="0fba9-126">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0fba9-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0fba9-127">-EndTimeMax</span><span class="sxs-lookup"><span data-stu-id="0fba9-127">-EndTimeMax</span></span>
<span data-ttu-id="0fba9-128">Szűrés a befejezési idő Max szerint</span><span class="sxs-lookup"><span data-stu-id="0fba9-128">Filter by end time max.</span></span>

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

### <span data-ttu-id="0fba9-129">-EndTimeMin</span><span class="sxs-lookup"><span data-stu-id="0fba9-129">-EndTimeMin</span></span>
<span data-ttu-id="0fba9-130">Szűrés befejezési idő szerint</span><span class="sxs-lookup"><span data-stu-id="0fba9-130">Filter by end time min.</span></span>

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

### <span data-ttu-id="0fba9-131">-JobExecutionId</span><span class="sxs-lookup"><span data-stu-id="0fba9-131">-JobExecutionId</span></span>
<span data-ttu-id="0fba9-132">A feladat-végrehajtási azonosító.</span><span class="sxs-lookup"><span data-stu-id="0fba9-132">The job execution id.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fba9-133">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="0fba9-133">-JobName</span></span>
<span data-ttu-id="0fba9-134">A feladat neve.</span><span class="sxs-lookup"><span data-stu-id="0fba9-134">The job name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fba9-135">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="0fba9-135">-ParentObject</span></span>
<span data-ttu-id="0fba9-136">A Job Execution objektum.</span><span class="sxs-lookup"><span data-stu-id="0fba9-136">The job execution object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0fba9-137">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="0fba9-137">-ParentResourceId</span></span>
<span data-ttu-id="0fba9-138">A feladat-végrehajtás erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="0fba9-138">The job execution resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fba9-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fba9-139">-ResourceGroupName</span></span>
<span data-ttu-id="0fba9-140">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="0fba9-140">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fba9-141">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="0fba9-141">-ServerName</span></span>
<span data-ttu-id="0fba9-142">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="0fba9-142">The server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fba9-143">-StepName</span><span class="sxs-lookup"><span data-stu-id="0fba9-143">-StepName</span></span>
<span data-ttu-id="0fba9-144">A feladat lépéseinek neve.</span><span class="sxs-lookup"><span data-stu-id="0fba9-144">The job step name.</span></span>

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

### <span data-ttu-id="0fba9-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fba9-145">CommonParameters</span></span>
<span data-ttu-id="0fba9-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0fba9-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fba9-147">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="0fba9-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fba9-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0fba9-148">INPUTS</span></span>

### <span data-ttu-id="0fba9-149">Microsoft. Azure. Command. SQL. ElasticJobs. Model. AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="0fba9-149">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="0fba9-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0fba9-150">OUTPUTS</span></span>

### <span data-ttu-id="0fba9-151">Microsoft. Azure. Command. SQL. ElasticJobs. Model. AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="0fba9-151">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="0fba9-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0fba9-152">NOTES</span></span>

## <span data-ttu-id="0fba9-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0fba9-153">RELATED LINKS</span></span>
