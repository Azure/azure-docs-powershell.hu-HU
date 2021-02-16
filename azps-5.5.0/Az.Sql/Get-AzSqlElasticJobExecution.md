---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobexecution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobExecution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobExecution.md
ms.openlocfilehash: d5583e5d7c0984b36679517859cc5a109b808a1a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100165810"
---
# <span data-ttu-id="2bd45-101">Get-AzSqlElasticJobExecution</span><span class="sxs-lookup"><span data-stu-id="2bd45-101">Get-AzSqlElasticJobExecution</span></span>

## <span data-ttu-id="2bd45-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2bd45-102">SYNOPSIS</span></span>
<span data-ttu-id="2bd45-103">Egy vagy több feladatvégrehajtást kap</span><span class="sxs-lookup"><span data-stu-id="2bd45-103">Gets one or more job executions</span></span>

## <span data-ttu-id="2bd45-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2bd45-104">SYNTAX</span></span>

### <span data-ttu-id="2bd45-105">DefaultSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2bd45-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName <String>] [-Count] <Int32> [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>]
 [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2bd45-106">WithCutExecutionId</span><span class="sxs-lookup"><span data-stu-id="2bd45-106">WithJobExecutionId</span></span>
```
Get-AzSqlElasticJobExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 -JobName <String> -JobExecutionId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2bd45-107">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="2bd45-107">ObjectSet</span></span>
```
Get-AzSqlElasticJobExecution [-ParentObject] <AzureSqlElasticJobAgentModel> [-JobName <String>]
 [-Count] <Int32> [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>]
 [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2bd45-108">WithCutExecutionIdUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="2bd45-108">WithJobExecutionIdUsingParentObject</span></span>
```
Get-AzSqlElasticJobExecution [-ParentObject] <AzureSqlElasticJobAgentModel> -JobName <String>
 -JobExecutionId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2bd45-109">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="2bd45-109">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobExecution [-ParentResourceId] <String> [-JobName <String>] [-Count] <Int32>
 [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>]
 [-Active] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2bd45-110">WithCutExecutionIdUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="2bd45-110">WithJobExecutionIdUsingParentResourceId</span></span>
```
Get-AzSqlElasticJobExecution [-ParentResourceId] <String> -JobName <String> -JobExecutionId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2bd45-111">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2bd45-111">DESCRIPTION</span></span>
<span data-ttu-id="2bd45-112">A Get-AzSqlElasticJobExecution parancsmag egy vagy több feladatvégrehajtást kap</span><span class="sxs-lookup"><span data-stu-id="2bd45-112">The Get-AzSqlElasticJobExecution cmdlet gets one or more job executions</span></span>

## <span data-ttu-id="2bd45-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2bd45-113">EXAMPLES</span></span>

### <span data-ttu-id="2bd45-114">1. példa: Egy vagy több feladatvégrehajtást kap minden munkakörben</span><span class="sxs-lookup"><span data-stu-id="2bd45-114">Example 1: Gets one or more job executions across all jobs</span></span>
```powershell
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobExecution -Count 3

JobName JobExecutionId                       Lifecycle StartTime            EndTime
------- --------------                       --------- ---------            -------
job1    dab0ebe8-fd52-42e9-bacf-e5f27577039b Canceled  6/1/2018 10:13:56 PM 6/1/2018 10:13:59 PM
job1    3bcfc912-20b2-411d-a2b7-6265d13fe272 Succeeded 6/1/2018 10:11:43 PM 6/1/2018 10:11:47 PM
job2    433f798e-f35c-41de-a23c-f2b43801d7b4 Succeeded 6/1/2018 10:11:36 PM 6/1/2018 10:11:41 PM
```

### <span data-ttu-id="2bd45-115">2. példa: Egy vagy több feladatvégrehajtást kap egy feladathoz</span><span class="sxs-lookup"><span data-stu-id="2bd45-115">Example 2: Gets one or more job executions for a job</span></span>
```powershell
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobExecution -Count 3 -JobName job2

JobName JobExecutionId                       Lifecycle StartTime            EndTime
------- --------------                       --------- ---------            -------
job2    433f798e-f35c-41de-a23c-f2b43801d7b4 Succeeded 6/1/2018 10:11:36 PM 6/1/2018 10:11:41 PM
```

<span data-ttu-id="2bd45-116">Egy vagy több feladatvégrehajtást kap</span><span class="sxs-lookup"><span data-stu-id="2bd45-116">Gets one or more job executions</span></span>

### <span data-ttu-id="2bd45-117">3. példa</span><span class="sxs-lookup"><span data-stu-id="2bd45-117">Example 3</span></span>

<span data-ttu-id="2bd45-118">Egy vagy több feladatvégrehajtást kap.</span><span class="sxs-lookup"><span data-stu-id="2bd45-118">Gets one or more job executions.</span></span> <span data-ttu-id="2bd45-119">(automatikusan generált)</span><span class="sxs-lookup"><span data-stu-id="2bd45-119">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Get-AzSqlElasticJobExecution -JobExecutionId 00000000-0000-0000-0000-000000000000 -JobName job1
```

## <span data-ttu-id="2bd45-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2bd45-120">PARAMETERS</span></span>

### <span data-ttu-id="2bd45-121">-Aktív</span><span class="sxs-lookup"><span data-stu-id="2bd45-121">-Active</span></span>
<span data-ttu-id="2bd45-122">Szűrés idő szerint</span><span class="sxs-lookup"><span data-stu-id="2bd45-122">Filter by create time min</span></span>

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

### <span data-ttu-id="2bd45-123">-AgentName</span><span class="sxs-lookup"><span data-stu-id="2bd45-123">-AgentName</span></span>
<span data-ttu-id="2bd45-124">Az ügynök neve.</span><span class="sxs-lookup"><span data-stu-id="2bd45-124">The agent name.</span></span>

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

### <span data-ttu-id="2bd45-125">-Count</span><span class="sxs-lookup"><span data-stu-id="2bd45-125">-Count</span></span>
<span data-ttu-id="2bd45-126">A darabszám a végrehajtások legfelső számát adja vissza.</span><span class="sxs-lookup"><span data-stu-id="2bd45-126">Count returns the top number of executions.</span></span>

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

### <span data-ttu-id="2bd45-127">-CreateTimeMax</span><span class="sxs-lookup"><span data-stu-id="2bd45-127">-CreateTimeMax</span></span>
<span data-ttu-id="2bd45-128">Szűrés idő szerint</span><span class="sxs-lookup"><span data-stu-id="2bd45-128">Filter by create time min</span></span>

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

### <span data-ttu-id="2bd45-129">-CreateTimeMin</span><span class="sxs-lookup"><span data-stu-id="2bd45-129">-CreateTimeMin</span></span>
<span data-ttu-id="2bd45-130">Szűrés idő szerint</span><span class="sxs-lookup"><span data-stu-id="2bd45-130">Filter by create time min</span></span>

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

### <span data-ttu-id="2bd45-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bd45-131">-DefaultProfile</span></span>
<span data-ttu-id="2bd45-132">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2bd45-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2bd45-133">-EndTimeMax</span><span class="sxs-lookup"><span data-stu-id="2bd45-133">-EndTimeMax</span></span>
<span data-ttu-id="2bd45-134">Szűrés idő szerint</span><span class="sxs-lookup"><span data-stu-id="2bd45-134">Filter by create time min</span></span>

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

### <span data-ttu-id="2bd45-135">-EndTimeMin</span><span class="sxs-lookup"><span data-stu-id="2bd45-135">-EndTimeMin</span></span>
<span data-ttu-id="2bd45-136">Szűrés idő szerint</span><span class="sxs-lookup"><span data-stu-id="2bd45-136">Filter by create time min</span></span>

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

### <span data-ttu-id="2bd45-137">-JobExecutionId</span><span class="sxs-lookup"><span data-stu-id="2bd45-137">-JobExecutionId</span></span>
<span data-ttu-id="2bd45-138">A feladatvégrehajtás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="2bd45-138">The job execution id.</span></span>

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

### <span data-ttu-id="2bd45-139">-JobName</span><span class="sxs-lookup"><span data-stu-id="2bd45-139">-JobName</span></span>
<span data-ttu-id="2bd45-140">A feladat neve.</span><span class="sxs-lookup"><span data-stu-id="2bd45-140">The job name.</span></span>

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

### <span data-ttu-id="2bd45-141">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="2bd45-141">-ParentObject</span></span>
<span data-ttu-id="2bd45-142">A feladatvégrehajtás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="2bd45-142">The job execution id.</span></span>

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

### <span data-ttu-id="2bd45-143">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="2bd45-143">-ParentResourceId</span></span>
<span data-ttu-id="2bd45-144">Az ügynök erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="2bd45-144">The agent resource id.</span></span>

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

### <span data-ttu-id="2bd45-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2bd45-145">-ResourceGroupName</span></span>
<span data-ttu-id="2bd45-146">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="2bd45-146">The resource group name.</span></span>

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

### <span data-ttu-id="2bd45-147">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2bd45-147">-ServerName</span></span>
<span data-ttu-id="2bd45-148">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="2bd45-148">The server name.</span></span>

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

### <span data-ttu-id="2bd45-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bd45-149">CommonParameters</span></span>
<span data-ttu-id="2bd45-150">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2bd45-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bd45-151">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2bd45-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bd45-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2bd45-152">INPUTS</span></span>

### <span data-ttu-id="2bd45-153">Microsoft.Azure.Commands.Sql.ElasticMods.Model.AzureSqlElasticAgentModel</span><span class="sxs-lookup"><span data-stu-id="2bd45-153">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="2bd45-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2bd45-154">OUTPUTS</span></span>

### <span data-ttu-id="2bd45-155">Microsoft.Azure.Commands.Sql.ElasticMods.Model.AzureSqlElasticAsticAsticExecutionModel</span><span class="sxs-lookup"><span data-stu-id="2bd45-155">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="2bd45-156">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2bd45-156">NOTES</span></span>

## <span data-ttu-id="2bd45-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2bd45-157">RELATED LINKS</span></span>
