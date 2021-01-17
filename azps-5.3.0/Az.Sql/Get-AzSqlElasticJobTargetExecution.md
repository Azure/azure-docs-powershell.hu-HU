---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobtargetexecution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobTargetExecution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobTargetExecution.md
ms.openlocfilehash: 6e61a83d843e0ceaa7d7926060da848d80d16eae
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467174"
---
# <span data-ttu-id="b7f60-101">Get-AzSqlElasticJobTargetExecution</span><span class="sxs-lookup"><span data-stu-id="b7f60-101">Get-AzSqlElasticJobTargetExecution</span></span>

## <span data-ttu-id="b7f60-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7f60-102">SYNOPSIS</span></span>
<span data-ttu-id="b7f60-103">Egy vagy több feladatcél végrehajtása</span><span class="sxs-lookup"><span data-stu-id="b7f60-103">Gets one or more job target executions</span></span>

## <span data-ttu-id="b7f60-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b7f60-104">SYNTAX</span></span>

### <span data-ttu-id="b7f60-105">DefaultSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b7f60-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobTargetExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> -Count <Int32> [-StepName <String>] [-CreateTimeMin <DateTime>]
 [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7f60-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="b7f60-106">ObjectSet</span></span>
```
Get-AzSqlElasticJobTargetExecution [-ParentObject] <AzureSqlElasticJobExecutionModel> -Count <Int32>
 [-StepName <String>] [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>]
 [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7f60-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b7f60-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobTargetExecution [-ParentResourceId] <String> -Count <Int32> [-StepName <String>]
 [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>]
 [-Active] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7f60-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b7f60-108">DESCRIPTION</span></span>
<span data-ttu-id="b7f60-109">A Get-AzSqlElasticJobTargetExecution parancsmag egy vagy több feladatvégrehajtást kap egy feladatvégrehajtásból</span><span class="sxs-lookup"><span data-stu-id="b7f60-109">The Get-AzSqlElasticJobTargetExecution cmdlet gets one or more job target executions from a job execution</span></span>

## <span data-ttu-id="b7f60-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b7f60-110">EXAMPLES</span></span>

### <span data-ttu-id="b7f60-111">1. példa: Egy vagy több feladatcél végrehajtását kapja meg egy feladatvégrehajtásból</span><span class="sxs-lookup"><span data-stu-id="b7f60-111">Example 1: Gets one or more job target executions from a job executions</span></span>
```powershell
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId 3bcfc912-20b2-411d-a2b7-6265d13fe272
$je | Get-AzSqlElasticJobTargetExecution -Count 2
JobName JobVersion StepName StepId JobExecutionId                       Lifecycle       TargetServerName TargetDatabaseName StartTime            EndTime
------- ---------- -------- ------ --------------                       ---------       ---------------- ------------------ ---------            -------
job1    1          step2    1      ea0a870b-dfe3-427e-9f95-d229d7815b65 Succeeded       s1               db2                6/1/2018 10:11:47 PM 6/1/2018 10:11:50 PM
job1    1          step1    1      ea0a870b-dfe3-427e-9f95-d229d7815b65 Succeeded       s1               db1                6/1/2018 10:11:44 PM 6/1/2018 10:11:47 PM
```

### <span data-ttu-id="b7f60-112">2. példa: Egy vagy több feladatvégrehajtást kap egy feladatvégrehajtásból – lépésnév alapján végzett szűrés</span><span class="sxs-lookup"><span data-stu-id="b7f60-112">Example 2: Gets one or more job target executions from a job executions - filtering by step name</span></span>
```powershell
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId 3bcfc912-20b2-411d-a2b7-6265d13fe272
$je | Get-AzSqlElasticJobTargetExecution -Count 2 -StepName step2
JobName JobVersion StepName StepId JobExecutionId                       Lifecycle       TargetServerName TargetDatabaseName StartTime            EndTime
------- ---------- -------- ------ --------------                       ---------       ---------------- ------------------ ---------            -------
job1    1          step2    1      ea0a870b-dfe3-427e-9f95-d229d7815b65 Succeeded       s1               db2                6/1/2018 10:11:47 PM 6/1/2018 10:11:50 PM
```

<span data-ttu-id="b7f60-113">Egy vagy több feladatcél végrehajtása</span><span class="sxs-lookup"><span data-stu-id="b7f60-113">Gets one or more job target executions</span></span>

## <span data-ttu-id="b7f60-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b7f60-114">PARAMETERS</span></span>

### <span data-ttu-id="b7f60-115">-Aktív</span><span class="sxs-lookup"><span data-stu-id="b7f60-115">-Active</span></span>
<span data-ttu-id="b7f60-116">Megjelölés aktív végrehajtások szerinti szűréshez.</span><span class="sxs-lookup"><span data-stu-id="b7f60-116">Flag to filter by active executions.</span></span>

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

### <span data-ttu-id="b7f60-117">-AgentName</span><span class="sxs-lookup"><span data-stu-id="b7f60-117">-AgentName</span></span>
<span data-ttu-id="b7f60-118">Az ügynök neve.</span><span class="sxs-lookup"><span data-stu-id="b7f60-118">The agent name.</span></span>

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

### <span data-ttu-id="b7f60-119">-Count</span><span class="sxs-lookup"><span data-stu-id="b7f60-119">-Count</span></span>
<span data-ttu-id="b7f60-120">A darabszám a végrehajtások legfelső számát adja vissza.</span><span class="sxs-lookup"><span data-stu-id="b7f60-120">Count returns the top number of executions.</span></span>

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

### <span data-ttu-id="b7f60-121">-CreateTimeMax</span><span class="sxs-lookup"><span data-stu-id="b7f60-121">-CreateTimeMax</span></span>
<span data-ttu-id="b7f60-122">Szűrés idő létrehozási idő szerint max</span><span class="sxs-lookup"><span data-stu-id="b7f60-122">Filter by create time max</span></span>

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

### <span data-ttu-id="b7f60-123">-CreateTimeMin</span><span class="sxs-lookup"><span data-stu-id="b7f60-123">-CreateTimeMin</span></span>
<span data-ttu-id="b7f60-124">Szűrés idő szerint</span><span class="sxs-lookup"><span data-stu-id="b7f60-124">Filter by create time min</span></span>

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

### <span data-ttu-id="b7f60-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7f60-125">-DefaultProfile</span></span>
<span data-ttu-id="b7f60-126">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b7f60-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7f60-127">-EndTimeMax</span><span class="sxs-lookup"><span data-stu-id="b7f60-127">-EndTimeMax</span></span>
<span data-ttu-id="b7f60-128">Szűrés vége szerint max.</span><span class="sxs-lookup"><span data-stu-id="b7f60-128">Filter by end time max.</span></span>

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

### <span data-ttu-id="b7f60-129">-EndTimeMin</span><span class="sxs-lookup"><span data-stu-id="b7f60-129">-EndTimeMin</span></span>
<span data-ttu-id="b7f60-130">Szűrés a záró időpont szerint</span><span class="sxs-lookup"><span data-stu-id="b7f60-130">Filter by end time min.</span></span>

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

### <span data-ttu-id="b7f60-131">-JobExecutionId</span><span class="sxs-lookup"><span data-stu-id="b7f60-131">-JobExecutionId</span></span>
<span data-ttu-id="b7f60-132">A feladatvégrehajtás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b7f60-132">The job execution id.</span></span>

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

### <span data-ttu-id="b7f60-133">-JobName</span><span class="sxs-lookup"><span data-stu-id="b7f60-133">-JobName</span></span>
<span data-ttu-id="b7f60-134">A feladat neve.</span><span class="sxs-lookup"><span data-stu-id="b7f60-134">The job name.</span></span>

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

### <span data-ttu-id="b7f60-135">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="b7f60-135">-ParentObject</span></span>
<span data-ttu-id="b7f60-136">A feladatvégrehajtási objektum.</span><span class="sxs-lookup"><span data-stu-id="b7f60-136">The job execution object.</span></span>

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

### <span data-ttu-id="b7f60-137">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="b7f60-137">-ParentResourceId</span></span>
<span data-ttu-id="b7f60-138">A feladatvégrehajtás erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b7f60-138">The job execution resource id.</span></span>

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

### <span data-ttu-id="b7f60-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7f60-139">-ResourceGroupName</span></span>
<span data-ttu-id="b7f60-140">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b7f60-140">The resource group name.</span></span>

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

### <span data-ttu-id="b7f60-141">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b7f60-141">-ServerName</span></span>
<span data-ttu-id="b7f60-142">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="b7f60-142">The server name.</span></span>

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

### <span data-ttu-id="b7f60-143">-StepName</span><span class="sxs-lookup"><span data-stu-id="b7f60-143">-StepName</span></span>
<span data-ttu-id="b7f60-144">A feladat lépésének neve.</span><span class="sxs-lookup"><span data-stu-id="b7f60-144">The job step name.</span></span>

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

### <span data-ttu-id="b7f60-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7f60-145">CommonParameters</span></span>
<span data-ttu-id="b7f60-146">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7f60-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7f60-147">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b7f60-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7f60-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b7f60-148">INPUTS</span></span>

### <span data-ttu-id="b7f60-149">Microsoft.Azure.Commands.Sql.ElasticMods.Model.AzureSqlElasticAsticAsticExecutionModel</span><span class="sxs-lookup"><span data-stu-id="b7f60-149">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="b7f60-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b7f60-150">OUTPUTS</span></span>

### <span data-ttu-id="b7f60-151">Microsoft.Azure.Commands.Sql.ElasticMods.Model.AzureSqlElasticAsticAsticExecutionModel</span><span class="sxs-lookup"><span data-stu-id="b7f60-151">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="b7f60-152">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b7f60-152">NOTES</span></span>

## <span data-ttu-id="b7f60-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b7f60-153">RELATED LINKS</span></span>
