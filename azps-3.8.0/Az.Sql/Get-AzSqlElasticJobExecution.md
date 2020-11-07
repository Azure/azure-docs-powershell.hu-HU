---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobexecution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobExecution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobExecution.md
ms.openlocfilehash: 2c4d0865ba1fb904e367857702d1344f5fb210cc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847438"
---
# <span data-ttu-id="82790-101">Get-AzSqlElasticJobExecution</span><span class="sxs-lookup"><span data-stu-id="82790-101">Get-AzSqlElasticJobExecution</span></span>

## <span data-ttu-id="82790-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="82790-102">SYNOPSIS</span></span>
<span data-ttu-id="82790-103">Egy vagy több kiépítési feladatot kap</span><span class="sxs-lookup"><span data-stu-id="82790-103">Gets one or more job executions</span></span>

## <span data-ttu-id="82790-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="82790-104">SYNTAX</span></span>

### <span data-ttu-id="82790-105">DefaultSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="82790-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName <String>] [-Count] <Int32> [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>]
 [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="82790-106">WithJobExecutionId</span><span class="sxs-lookup"><span data-stu-id="82790-106">WithJobExecutionId</span></span>
```
Get-AzSqlElasticJobExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 -JobName <String> -JobExecutionId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="82790-107">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="82790-107">ObjectSet</span></span>
```
Get-AzSqlElasticJobExecution [-ParentObject] <AzureSqlElasticJobAgentModel> [-JobName <String>]
 [-Count] <Int32> [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>]
 [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="82790-108">WithJobExecutionIdUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="82790-108">WithJobExecutionIdUsingParentObject</span></span>
```
Get-AzSqlElasticJobExecution [-ParentObject] <AzureSqlElasticJobAgentModel> -JobName <String>
 -JobExecutionId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="82790-109">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="82790-109">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobExecution [-ParentResourceId] <String> [-JobName <String>] [-Count] <Int32>
 [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>]
 [-Active] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="82790-110">WithJobExecutionIdUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="82790-110">WithJobExecutionIdUsingParentResourceId</span></span>
```
Get-AzSqlElasticJobExecution [-ParentResourceId] <String> -JobName <String> -JobExecutionId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82790-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="82790-111">DESCRIPTION</span></span>
<span data-ttu-id="82790-112">A Get-AzSqlElasticJobExecution parancsmag egy vagy több kiépítési feladatot kap</span><span class="sxs-lookup"><span data-stu-id="82790-112">The Get-AzSqlElasticJobExecution cmdlet gets one or more job executions</span></span>

## <span data-ttu-id="82790-113">Példák</span><span class="sxs-lookup"><span data-stu-id="82790-113">EXAMPLES</span></span>

### <span data-ttu-id="82790-114">Példa 1 – egy vagy több feladat végrehajtása az összes feladaton keresztül</span><span class="sxs-lookup"><span data-stu-id="82790-114">Example 1 - Gets one or more job executions across all jobs</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobExecution -Count 3

JobName JobExecutionId                       Lifecycle StartTime            EndTime
------- --------------                       --------- ---------            -------
job1    dab0ebe8-fd52-42e9-bacf-e5f27577039b Canceled  6/1/2018 10:13:56 PM 6/1/2018 10:13:59 PM
job1    3bcfc912-20b2-411d-a2b7-6265d13fe272 Succeeded 6/1/2018 10:11:43 PM 6/1/2018 10:11:47 PM
job2    433f798e-f35c-41de-a23c-f2b43801d7b4 Succeeded 6/1/2018 10:11:36 PM 6/1/2018 10:11:41 PM
```

### <span data-ttu-id="82790-115">Példa: 2 – egy vagy több kiépítési feladatot kap egy feladathoz.</span><span class="sxs-lookup"><span data-stu-id="82790-115">Example 2 - Gets one or more job executions for a job</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobExecution -Count 3 -JobName job2

JobName JobExecutionId                       Lifecycle StartTime            EndTime
------- --------------                       --------- ---------            -------
job2    433f798e-f35c-41de-a23c-f2b43801d7b4 Succeeded 6/1/2018 10:11:36 PM 6/1/2018 10:11:41 PM
```

<span data-ttu-id="82790-116">Egy vagy több kiépítési feladatot kap</span><span class="sxs-lookup"><span data-stu-id="82790-116">Gets one or more job executions</span></span>

## <span data-ttu-id="82790-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="82790-117">PARAMETERS</span></span>

### <span data-ttu-id="82790-118">-Aktív</span><span class="sxs-lookup"><span data-stu-id="82790-118">-Active</span></span>
<span data-ttu-id="82790-119">Szűrés a min idő létrehozásával</span><span class="sxs-lookup"><span data-stu-id="82790-119">Filter by create time min</span></span>

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

### <span data-ttu-id="82790-120">-AgentName</span><span class="sxs-lookup"><span data-stu-id="82790-120">-AgentName</span></span>
<span data-ttu-id="82790-121">A meghatalmazott neve.</span><span class="sxs-lookup"><span data-stu-id="82790-121">The agent name.</span></span>

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

### <span data-ttu-id="82790-122">-Count</span><span class="sxs-lookup"><span data-stu-id="82790-122">-Count</span></span>
<span data-ttu-id="82790-123">A Count függvény a kivégzések legfelső számát számítja ki.</span><span class="sxs-lookup"><span data-stu-id="82790-123">Count returns the top number of executions.</span></span>

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

### <span data-ttu-id="82790-124">-CreateTimeMax</span><span class="sxs-lookup"><span data-stu-id="82790-124">-CreateTimeMax</span></span>
<span data-ttu-id="82790-125">Szűrés a min idő létrehozásával</span><span class="sxs-lookup"><span data-stu-id="82790-125">Filter by create time min</span></span>

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

### <span data-ttu-id="82790-126">-CreateTimeMin</span><span class="sxs-lookup"><span data-stu-id="82790-126">-CreateTimeMin</span></span>
<span data-ttu-id="82790-127">Szűrés a min idő létrehozásával</span><span class="sxs-lookup"><span data-stu-id="82790-127">Filter by create time min</span></span>

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

### <span data-ttu-id="82790-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82790-128">-DefaultProfile</span></span>
<span data-ttu-id="82790-129">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="82790-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82790-130">-EndTimeMax</span><span class="sxs-lookup"><span data-stu-id="82790-130">-EndTimeMax</span></span>
<span data-ttu-id="82790-131">Szűrés a min idő létrehozásával</span><span class="sxs-lookup"><span data-stu-id="82790-131">Filter by create time min</span></span>

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

### <span data-ttu-id="82790-132">-EndTimeMin</span><span class="sxs-lookup"><span data-stu-id="82790-132">-EndTimeMin</span></span>
<span data-ttu-id="82790-133">Szűrés a min idő létrehozásával</span><span class="sxs-lookup"><span data-stu-id="82790-133">Filter by create time min</span></span>

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

### <span data-ttu-id="82790-134">-JobExecutionId</span><span class="sxs-lookup"><span data-stu-id="82790-134">-JobExecutionId</span></span>
<span data-ttu-id="82790-135">A feladat-végrehajtási azonosító.</span><span class="sxs-lookup"><span data-stu-id="82790-135">The job execution id.</span></span>

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

### <span data-ttu-id="82790-136">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="82790-136">-JobName</span></span>
<span data-ttu-id="82790-137">A feladat neve.</span><span class="sxs-lookup"><span data-stu-id="82790-137">The job name.</span></span>

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

### <span data-ttu-id="82790-138">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="82790-138">-ParentObject</span></span>
<span data-ttu-id="82790-139">A feladat-végrehajtási azonosító.</span><span class="sxs-lookup"><span data-stu-id="82790-139">The job execution id.</span></span>

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

### <span data-ttu-id="82790-140">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="82790-140">-ParentResourceId</span></span>
<span data-ttu-id="82790-141">Az ügynök erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="82790-141">The agent resource id.</span></span>

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

### <span data-ttu-id="82790-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82790-142">-ResourceGroupName</span></span>
<span data-ttu-id="82790-143">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="82790-143">The resource group name.</span></span>

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

### <span data-ttu-id="82790-144">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="82790-144">-ServerName</span></span>
<span data-ttu-id="82790-145">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="82790-145">The server name.</span></span>

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

### <span data-ttu-id="82790-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82790-146">CommonParameters</span></span>
<span data-ttu-id="82790-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="82790-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82790-148">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="82790-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82790-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="82790-149">INPUTS</span></span>

### <span data-ttu-id="82790-150">Microsoft. Azure. Command. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="82790-150">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="82790-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="82790-151">OUTPUTS</span></span>

### <span data-ttu-id="82790-152">Microsoft. Azure. Command. SQL. ElasticJobs. Model. AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="82790-152">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="82790-153">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="82790-153">NOTES</span></span>

## <span data-ttu-id="82790-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="82790-154">RELATED LINKS</span></span>