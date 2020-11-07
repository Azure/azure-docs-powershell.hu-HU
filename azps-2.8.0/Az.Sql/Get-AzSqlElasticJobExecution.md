---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobexecution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobExecution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobExecution.md
ms.openlocfilehash: 5b5837fb0c5fa56e8e8f9887b6d85bfc3a3a559c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839206"
---
# <span data-ttu-id="795f9-101">Get-AzSqlElasticJobExecution</span><span class="sxs-lookup"><span data-stu-id="795f9-101">Get-AzSqlElasticJobExecution</span></span>

## <span data-ttu-id="795f9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="795f9-102">SYNOPSIS</span></span>
<span data-ttu-id="795f9-103">Egy vagy több kiépítési feladatot kap</span><span class="sxs-lookup"><span data-stu-id="795f9-103">Gets one or more job executions</span></span>

## <span data-ttu-id="795f9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="795f9-104">SYNTAX</span></span>

### <span data-ttu-id="795f9-105">DefaultSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="795f9-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName <String>] [-Count] <Int32> [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>]
 [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="795f9-106">WithJobExecutionId</span><span class="sxs-lookup"><span data-stu-id="795f9-106">WithJobExecutionId</span></span>
```
Get-AzSqlElasticJobExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 -JobName <String> -JobExecutionId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="795f9-107">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="795f9-107">ObjectSet</span></span>
```
Get-AzSqlElasticJobExecution [-ParentObject] <AzureSqlElasticJobAgentModel> [-JobName <String>]
 [-Count] <Int32> [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>]
 [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="795f9-108">WithJobExecutionIdUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="795f9-108">WithJobExecutionIdUsingParentObject</span></span>
```
Get-AzSqlElasticJobExecution [-ParentObject] <AzureSqlElasticJobAgentModel> -JobName <String>
 -JobExecutionId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="795f9-109">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="795f9-109">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobExecution [-ParentResourceId] <String> [-JobName <String>] [-Count] <Int32>
 [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>]
 [-Active] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="795f9-110">WithJobExecutionIdUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="795f9-110">WithJobExecutionIdUsingParentResourceId</span></span>
```
Get-AzSqlElasticJobExecution [-ParentResourceId] <String> -JobName <String> -JobExecutionId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="795f9-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="795f9-111">DESCRIPTION</span></span>
<span data-ttu-id="795f9-112">A Get-AzSqlElasticJobExecution parancsmag egy vagy több kiépítési feladatot kap</span><span class="sxs-lookup"><span data-stu-id="795f9-112">The Get-AzSqlElasticJobExecution cmdlet gets one or more job executions</span></span>

## <span data-ttu-id="795f9-113">Példák</span><span class="sxs-lookup"><span data-stu-id="795f9-113">EXAMPLES</span></span>

### <span data-ttu-id="795f9-114">Példa 1 – egy vagy több feladat végrehajtása az összes feladaton keresztül</span><span class="sxs-lookup"><span data-stu-id="795f9-114">Example 1 - Gets one or more job executions across all jobs</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobExecution -Count 3

JobName JobExecutionId                       Lifecycle StartTime            EndTime
------- --------------                       --------- ---------            -------
job1    dab0ebe8-fd52-42e9-bacf-e5f27577039b Canceled  6/1/2018 10:13:56 PM 6/1/2018 10:13:59 PM
job1    3bcfc912-20b2-411d-a2b7-6265d13fe272 Succeeded 6/1/2018 10:11:43 PM 6/1/2018 10:11:47 PM
job2    433f798e-f35c-41de-a23c-f2b43801d7b4 Succeeded 6/1/2018 10:11:36 PM 6/1/2018 10:11:41 PM
```

### <span data-ttu-id="795f9-115">Példa: 2 – egy vagy több kiépítési feladatot kap egy feladathoz.</span><span class="sxs-lookup"><span data-stu-id="795f9-115">Example 2 - Gets one or more job executions for a job</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobExecution -Count 3 -JobName job2

JobName JobExecutionId                       Lifecycle StartTime            EndTime
------- --------------                       --------- ---------            -------
job2    433f798e-f35c-41de-a23c-f2b43801d7b4 Succeeded 6/1/2018 10:11:36 PM 6/1/2018 10:11:41 PM
```

<span data-ttu-id="795f9-116">Egy vagy több kiépítési feladatot kap</span><span class="sxs-lookup"><span data-stu-id="795f9-116">Gets one or more job executions</span></span>

## <span data-ttu-id="795f9-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="795f9-117">PARAMETERS</span></span>

### <span data-ttu-id="795f9-118">-Aktív</span><span class="sxs-lookup"><span data-stu-id="795f9-118">-Active</span></span>
<span data-ttu-id="795f9-119">Szűrés a min idő létrehozásával</span><span class="sxs-lookup"><span data-stu-id="795f9-119">Filter by create time min</span></span>

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

### <span data-ttu-id="795f9-120">-AgentName</span><span class="sxs-lookup"><span data-stu-id="795f9-120">-AgentName</span></span>
<span data-ttu-id="795f9-121">A meghatalmazott neve.</span><span class="sxs-lookup"><span data-stu-id="795f9-121">The agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobExecutionId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="795f9-122">-Count</span><span class="sxs-lookup"><span data-stu-id="795f9-122">-Count</span></span>
<span data-ttu-id="795f9-123">A Count függvény a kivégzések legfelső számát számítja ki.</span><span class="sxs-lookup"><span data-stu-id="795f9-123">Count returns the top number of executions.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="795f9-124">-CreateTimeMax</span><span class="sxs-lookup"><span data-stu-id="795f9-124">-CreateTimeMax</span></span>
<span data-ttu-id="795f9-125">Szűrés a min idő létrehozásával</span><span class="sxs-lookup"><span data-stu-id="795f9-125">Filter by create time min</span></span>

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

### <span data-ttu-id="795f9-126">-CreateTimeMin</span><span class="sxs-lookup"><span data-stu-id="795f9-126">-CreateTimeMin</span></span>
<span data-ttu-id="795f9-127">Szűrés a min idő létrehozásával</span><span class="sxs-lookup"><span data-stu-id="795f9-127">Filter by create time min</span></span>

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

### <span data-ttu-id="795f9-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="795f9-128">-DefaultProfile</span></span>
<span data-ttu-id="795f9-129">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="795f9-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="795f9-130">-EndTimeMax</span><span class="sxs-lookup"><span data-stu-id="795f9-130">-EndTimeMax</span></span>
<span data-ttu-id="795f9-131">Szűrés a min idő létrehozásával</span><span class="sxs-lookup"><span data-stu-id="795f9-131">Filter by create time min</span></span>

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

### <span data-ttu-id="795f9-132">-EndTimeMin</span><span class="sxs-lookup"><span data-stu-id="795f9-132">-EndTimeMin</span></span>
<span data-ttu-id="795f9-133">Szűrés a min idő létrehozásával</span><span class="sxs-lookup"><span data-stu-id="795f9-133">Filter by create time min</span></span>

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

### <span data-ttu-id="795f9-134">-JobExecutionId</span><span class="sxs-lookup"><span data-stu-id="795f9-134">-JobExecutionId</span></span>
<span data-ttu-id="795f9-135">A feladat-végrehajtási azonosító.</span><span class="sxs-lookup"><span data-stu-id="795f9-135">The job execution id.</span></span>

```yaml
Type: System.String
Parameter Sets: WithJobExecutionId, WithJobExecutionIdUsingParentObject, WithJobExecutionIdUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="795f9-136">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="795f9-136">-JobName</span></span>
<span data-ttu-id="795f9-137">A feladat neve.</span><span class="sxs-lookup"><span data-stu-id="795f9-137">The job name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WithJobExecutionId, WithJobExecutionIdUsingParentObject, WithJobExecutionIdUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="795f9-138">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="795f9-138">-ParentObject</span></span>
<span data-ttu-id="795f9-139">A feladat-végrehajtási azonosító.</span><span class="sxs-lookup"><span data-stu-id="795f9-139">The job execution id.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel
Parameter Sets: ObjectSet, WithJobExecutionIdUsingParentObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="795f9-140">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="795f9-140">-ParentResourceId</span></span>
<span data-ttu-id="795f9-141">Az ügynök erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="795f9-141">The agent resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet, WithJobExecutionIdUsingParentResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="795f9-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="795f9-142">-ResourceGroupName</span></span>
<span data-ttu-id="795f9-143">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="795f9-143">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobExecutionId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="795f9-144">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="795f9-144">-ServerName</span></span>
<span data-ttu-id="795f9-145">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="795f9-145">The server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobExecutionId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="795f9-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="795f9-146">CommonParameters</span></span>
<span data-ttu-id="795f9-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="795f9-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="795f9-148">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="795f9-148">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="795f9-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="795f9-149">INPUTS</span></span>

### <span data-ttu-id="795f9-150">Microsoft. Azure. Command. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="795f9-150">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="795f9-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="795f9-151">OUTPUTS</span></span>

### <span data-ttu-id="795f9-152">Microsoft. Azure. Command. SQL. ElasticJobs. Model. AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="795f9-152">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="795f9-153">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="795f9-153">NOTES</span></span>

## <span data-ttu-id="795f9-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="795f9-154">RELATED LINKS</span></span>
