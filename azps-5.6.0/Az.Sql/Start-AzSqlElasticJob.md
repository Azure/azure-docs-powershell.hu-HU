---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/start-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlElasticJob.md
ms.openlocfilehash: 6163c7be725d66c7e1f64fced3be0269ffedd32f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011477"
---
# <span data-ttu-id="36482-101">Start-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="36482-101">Start-AzSqlElasticJob</span></span>

## <span data-ttu-id="36482-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36482-102">SYNOPSIS</span></span>
<span data-ttu-id="36482-103">Elindít egy feladatot, és visszaad egy feladatvégrehajtási azonosítót, amely az állapotának megtekintéséhez lekérdezható</span><span class="sxs-lookup"><span data-stu-id="36482-103">Starts a job, returning a job execution id that can be polled to view it's status</span></span>

## <span data-ttu-id="36482-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="36482-104">SYNTAX</span></span>

### <span data-ttu-id="36482-105">DefaultSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="36482-105">DefaultSet (Default)</span></span>
```
Start-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> [-Wait] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="36482-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="36482-106">ObjectSet</span></span>
```
Start-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobModel> [-Wait] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36482-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="36482-107">ResourceIdSet</span></span>
```
Start-AzSqlElasticJob [-ParentResourceId] <String> [-Wait] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36482-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="36482-108">DESCRIPTION</span></span>
<span data-ttu-id="36482-109">A Start-AzSqlElasticJob parancsmag elindít egy feladatot, amely egy új feladatvégrehajtást ad vissza</span><span class="sxs-lookup"><span data-stu-id="36482-109">The Start-AzSqlElasticJob cmdlet starts a job returning a new job execution</span></span>

## <span data-ttu-id="36482-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="36482-110">EXAMPLES</span></span>

### <span data-ttu-id="36482-111">1. példa: Új feladatvégrehajtású feladatot kezd el.</span><span class="sxs-lookup"><span data-stu-id="36482-111">Example 1 - Starts a job returning a new job execution</span></span>
```
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name job1
$job | Start-AzSqlElasticJob

JobName JobExecutionId                       Lifecycle StartTime EndTime
------- --------------                       --------- --------- -------
job1    b93b3a90-987b-4565-b3d3-5fa1751fa9bc Created
```

<span data-ttu-id="36482-112">Új feladat végrehajtását visszavetve elindítja a feladatot</span><span class="sxs-lookup"><span data-stu-id="36482-112">Starts a job returning a new job execution</span></span>

## <span data-ttu-id="36482-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36482-113">PARAMETERS</span></span>

### <span data-ttu-id="36482-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="36482-114">-AgentName</span></span>
<span data-ttu-id="36482-115">Az ügynök neve</span><span class="sxs-lookup"><span data-stu-id="36482-115">The agent name</span></span>

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

### <span data-ttu-id="36482-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="36482-116">-AsJob</span></span>
<span data-ttu-id="36482-117">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="36482-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="36482-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36482-118">-DefaultProfile</span></span>
<span data-ttu-id="36482-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="36482-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36482-120">-JobName</span><span class="sxs-lookup"><span data-stu-id="36482-120">-JobName</span></span>
<span data-ttu-id="36482-121">A feladat neve</span><span class="sxs-lookup"><span data-stu-id="36482-121">The job name</span></span>

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

### <span data-ttu-id="36482-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="36482-122">-ParentObject</span></span>
<span data-ttu-id="36482-123">A feladatobjektum</span><span class="sxs-lookup"><span data-stu-id="36482-123">The job object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="36482-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="36482-124">-ParentResourceId</span></span>
<span data-ttu-id="36482-125">A feladaterőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="36482-125">The job resource id</span></span>

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

### <span data-ttu-id="36482-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36482-126">-ResourceGroupName</span></span>
<span data-ttu-id="36482-127">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="36482-127">The resource group name</span></span>

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

### <span data-ttu-id="36482-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="36482-128">-ServerName</span></span>
<span data-ttu-id="36482-129">A kiszolgáló neve</span><span class="sxs-lookup"><span data-stu-id="36482-129">The server name</span></span>

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

### <span data-ttu-id="36482-130">-Wait</span><span class="sxs-lookup"><span data-stu-id="36482-130">-Wait</span></span>
<span data-ttu-id="36482-131">A várakozási jelölő jelzi, hogy várnia kell, amíg a feladat végrehajtása el nem történik</span><span class="sxs-lookup"><span data-stu-id="36482-131">The wait flag to indicate to wait until the job's execution is done</span></span>

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

### <span data-ttu-id="36482-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="36482-132">-Confirm</span></span>
<span data-ttu-id="36482-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="36482-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36482-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36482-134">-WhatIf</span></span>
<span data-ttu-id="36482-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="36482-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36482-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="36482-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36482-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36482-137">CommonParameters</span></span>
<span data-ttu-id="36482-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36482-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36482-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="36482-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36482-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="36482-140">INPUTS</span></span>

### <span data-ttu-id="36482-141">Microsoft.Azure.Commands.Sql.ElasticMods.Model.AzureSqlElasticModel</span><span class="sxs-lookup"><span data-stu-id="36482-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="36482-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="36482-142">OUTPUTS</span></span>

### <span data-ttu-id="36482-143">Microsoft.Azure.Commands.Sql.ElasticMods.Model.AzureSqlElasticAsticAsticExecutionModel</span><span class="sxs-lookup"><span data-stu-id="36482-143">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="36482-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="36482-144">NOTES</span></span>

## <span data-ttu-id="36482-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="36482-145">RELATED LINKS</span></span>
