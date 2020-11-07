---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/stop-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticJob.md
ms.openlocfilehash: ff117dfee7f660845389bd62245be4ecfd53b2f7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846482"
---
# <span data-ttu-id="21d3f-101">Stop-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="21d3f-101">Stop-AzSqlElasticJob</span></span>

## <span data-ttu-id="21d3f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="21d3f-102">SYNOPSIS</span></span>
<span data-ttu-id="21d3f-103">Feladat leállítása az adott tevékenységhez tartozó feladat-végrehajtási azonosítóval</span><span class="sxs-lookup"><span data-stu-id="21d3f-103">Stops a job given it's job execution id</span></span>

## <span data-ttu-id="21d3f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="21d3f-104">SYNTAX</span></span>

### <span data-ttu-id="21d3f-105">DefaultSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="21d3f-105">DefaultSet (Default)</span></span>
```
Stop-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="21d3f-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="21d3f-106">ObjectSet</span></span>
```
Stop-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobExecutionModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21d3f-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="21d3f-107">ResourceIdSet</span></span>
```
Stop-AzSqlElasticJob [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21d3f-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="21d3f-108">DESCRIPTION</span></span>
<span data-ttu-id="21d3f-109">Az Stop-AzSqlElasticJob parancsmag leállítja a feladatot futó végrehajtással.</span><span class="sxs-lookup"><span data-stu-id="21d3f-109">The Stop-AzSqlElasticJob cmdlet stops a job's with a running execution.</span></span>
<span data-ttu-id="21d3f-110">A projekt végrehajtásának aktuális állapotát számítja ki.</span><span class="sxs-lookup"><span data-stu-id="21d3f-110">Returns the current status of the job execution</span></span>

## <span data-ttu-id="21d3f-111">Példák</span><span class="sxs-lookup"><span data-stu-id="21d3f-111">EXAMPLES</span></span>

### <span data-ttu-id="21d3f-112">Példa 1 – feladat leállítása futó feladatok végrehajtásával</span><span class="sxs-lookup"><span data-stu-id="21d3f-112">Example 1 - Stops a job with a running job execution</span></span>
```
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId dab0ebe8-fd52-42e9-bacf-e5f27577039b
$je | Stop-AzSqlElasticJob
JobName JobExecutionId                       Lifecycle                    StartTime            EndTime
------- --------------                       ---------                    ---------            -------
job1    dab0ebe8-fd52-42e9-bacf-e5f27577039b WaitingForChildJobExecutions 6/1/2018 10:13:56 PM
```

<span data-ttu-id="21d3f-113">Futtatja a futási feladatot, és az aktuális állapotát számítja ki.</span><span class="sxs-lookup"><span data-stu-id="21d3f-113">Stops a running job execution and returns it's current status</span></span>

## <span data-ttu-id="21d3f-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="21d3f-114">PARAMETERS</span></span>

### <span data-ttu-id="21d3f-115">-AgentName</span><span class="sxs-lookup"><span data-stu-id="21d3f-115">-AgentName</span></span>
<span data-ttu-id="21d3f-116">Az ügynök neve</span><span class="sxs-lookup"><span data-stu-id="21d3f-116">The agent name</span></span>

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

### <span data-ttu-id="21d3f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21d3f-117">-DefaultProfile</span></span>
<span data-ttu-id="21d3f-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="21d3f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21d3f-119">-JobExecutionId</span><span class="sxs-lookup"><span data-stu-id="21d3f-119">-JobExecutionId</span></span>
<span data-ttu-id="21d3f-120">A feladat-végrehajtási azonosító.</span><span class="sxs-lookup"><span data-stu-id="21d3f-120">The job execution id.</span></span>

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

### <span data-ttu-id="21d3f-121">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="21d3f-121">-JobName</span></span>
<span data-ttu-id="21d3f-122">A feladat neve</span><span class="sxs-lookup"><span data-stu-id="21d3f-122">The job name</span></span>

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

### <span data-ttu-id="21d3f-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="21d3f-123">-ParentObject</span></span>
<span data-ttu-id="21d3f-124">Az Agent Control Database objektum</span><span class="sxs-lookup"><span data-stu-id="21d3f-124">The Agent Control Database Object</span></span>

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

### <span data-ttu-id="21d3f-125">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="21d3f-125">-ParentResourceId</span></span>
<span data-ttu-id="21d3f-126">A feladat-végrehajtás erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="21d3f-126">The job execution resource id</span></span>

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

### <span data-ttu-id="21d3f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21d3f-127">-ResourceGroupName</span></span>
<span data-ttu-id="21d3f-128">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="21d3f-128">The resource group name</span></span>

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

### <span data-ttu-id="21d3f-129">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="21d3f-129">-ServerName</span></span>
<span data-ttu-id="21d3f-130">A kiszolgáló neve</span><span class="sxs-lookup"><span data-stu-id="21d3f-130">The server name</span></span>

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

### <span data-ttu-id="21d3f-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="21d3f-131">-Confirm</span></span>
<span data-ttu-id="21d3f-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="21d3f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21d3f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21d3f-133">-WhatIf</span></span>
<span data-ttu-id="21d3f-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="21d3f-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21d3f-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="21d3f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21d3f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21d3f-136">CommonParameters</span></span>
<span data-ttu-id="21d3f-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="21d3f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21d3f-138">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="21d3f-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21d3f-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="21d3f-139">INPUTS</span></span>

### <span data-ttu-id="21d3f-140">Microsoft. Azure. Command. SQL. ElasticJobs. Model. AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="21d3f-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="21d3f-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="21d3f-141">OUTPUTS</span></span>

### <span data-ttu-id="21d3f-142">Microsoft. Azure. Command. SQL. ElasticJobs. Model. AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="21d3f-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="21d3f-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="21d3f-143">NOTES</span></span>

## <span data-ttu-id="21d3f-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="21d3f-144">RELATED LINKS</span></span>
