---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/stop-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticJob.md
ms.openlocfilehash: ec5ab9706bd459a07c91e7060d3bf6da30f76ed5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468021"
---
# <span data-ttu-id="012b1-101">Stop-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="012b1-101">Stop-AzSqlElasticJob</span></span>

## <span data-ttu-id="012b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="012b1-102">SYNOPSIS</span></span>
<span data-ttu-id="012b1-103">Leállít egy feladatot, mert az feladatvégrehajtási azonosítója</span><span class="sxs-lookup"><span data-stu-id="012b1-103">Stops a job given it's job execution id</span></span>

## <span data-ttu-id="012b1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="012b1-104">SYNTAX</span></span>

### <span data-ttu-id="012b1-105">DefaultSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="012b1-105">DefaultSet (Default)</span></span>
```
Stop-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="012b1-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="012b1-106">ObjectSet</span></span>
```
Stop-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobExecutionModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="012b1-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="012b1-107">ResourceIdSet</span></span>
```
Stop-AzSqlElasticJob [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="012b1-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="012b1-108">DESCRIPTION</span></span>
<span data-ttu-id="012b1-109">A Stop-AzSqlElasticJob parancsmag futásvégrehajtással leállítja a feladatok végrehajtását.</span><span class="sxs-lookup"><span data-stu-id="012b1-109">The Stop-AzSqlElasticJob cmdlet stops a job's with a running execution.</span></span>
<span data-ttu-id="012b1-110">A feladat végrehajtásának aktuális állapotát adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="012b1-110">Returns the current status of the job execution</span></span>

## <span data-ttu-id="012b1-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="012b1-111">EXAMPLES</span></span>

### <span data-ttu-id="012b1-112">1. példa: Egy futó feladatvégrehajtással végzett feladat leállítja</span><span class="sxs-lookup"><span data-stu-id="012b1-112">Example 1: Stops a job with a running job execution</span></span>
```powershell
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId dab0ebe8-fd52-42e9-bacf-e5f27577039b
$je | Stop-AzSqlElasticJob
JobName JobExecutionId                       Lifecycle                    StartTime            EndTime
------- --------------                       ---------                    ---------            -------
job1    dab0ebe8-fd52-42e9-bacf-e5f27577039b WaitingForChildJobExecutions 6/1/2018 10:13:56 PM
```

<span data-ttu-id="012b1-113">Leállít egy futó feladatvégrehajtást, és visszaadja az aktuális állapotát.</span><span class="sxs-lookup"><span data-stu-id="012b1-113">Stops a running job execution and returns it's current status</span></span>

### <span data-ttu-id="012b1-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="012b1-114">Example 2</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Stop-AzSqlElasticJob -AgentName agent -JobExecutionId 00000000-0000-0000-0000-000000000000 -JobName job1 -ResourceGroupName MyResourceGroup -ServerName s1
```

## <span data-ttu-id="012b1-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="012b1-115">PARAMETERS</span></span>

### <span data-ttu-id="012b1-116">-AgentName</span><span class="sxs-lookup"><span data-stu-id="012b1-116">-AgentName</span></span>
<span data-ttu-id="012b1-117">Az ügynök neve</span><span class="sxs-lookup"><span data-stu-id="012b1-117">The agent name</span></span>

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

### <span data-ttu-id="012b1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="012b1-118">-DefaultProfile</span></span>
<span data-ttu-id="012b1-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="012b1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="012b1-120">-JobExecutionId</span><span class="sxs-lookup"><span data-stu-id="012b1-120">-JobExecutionId</span></span>
<span data-ttu-id="012b1-121">A feladatvégrehajtás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="012b1-121">The job execution id.</span></span>

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

### <span data-ttu-id="012b1-122">-JobName</span><span class="sxs-lookup"><span data-stu-id="012b1-122">-JobName</span></span>
<span data-ttu-id="012b1-123">A feladat neve</span><span class="sxs-lookup"><span data-stu-id="012b1-123">The job name</span></span>

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

### <span data-ttu-id="012b1-124">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="012b1-124">-ParentObject</span></span>
<span data-ttu-id="012b1-125">The Agent Control Database Object</span><span class="sxs-lookup"><span data-stu-id="012b1-125">The Agent Control Database Object</span></span>

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

### <span data-ttu-id="012b1-126">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="012b1-126">-ParentResourceId</span></span>
<span data-ttu-id="012b1-127">A feladatvégrehajtás erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="012b1-127">The job execution resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="012b1-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="012b1-128">-ResourceGroupName</span></span>
<span data-ttu-id="012b1-129">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="012b1-129">The resource group name</span></span>

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

### <span data-ttu-id="012b1-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="012b1-130">-ServerName</span></span>
<span data-ttu-id="012b1-131">A kiszolgáló neve</span><span class="sxs-lookup"><span data-stu-id="012b1-131">The server name</span></span>

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

### <span data-ttu-id="012b1-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="012b1-132">-Confirm</span></span>
<span data-ttu-id="012b1-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="012b1-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="012b1-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="012b1-134">-WhatIf</span></span>
<span data-ttu-id="012b1-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="012b1-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="012b1-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="012b1-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="012b1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="012b1-137">CommonParameters</span></span>
<span data-ttu-id="012b1-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="012b1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="012b1-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="012b1-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="012b1-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="012b1-140">INPUTS</span></span>

### <span data-ttu-id="012b1-141">Microsoft.Azure.Commands.Sql.ElasticMods.Model.AzureSqlElasticAsticAsticExecutionModel</span><span class="sxs-lookup"><span data-stu-id="012b1-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="012b1-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="012b1-142">OUTPUTS</span></span>

### <span data-ttu-id="012b1-143">Microsoft.Azure.Commands.Sql.ElasticMods.Model.AzureSqlElasticAsticAsticExecutionModel</span><span class="sxs-lookup"><span data-stu-id="012b1-143">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="012b1-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="012b1-144">NOTES</span></span>

## <span data-ttu-id="012b1-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="012b1-145">RELATED LINKS</span></span>
