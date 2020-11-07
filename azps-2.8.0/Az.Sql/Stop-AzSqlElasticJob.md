---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/stop-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticJob.md
ms.openlocfilehash: 0b7fc702ad331a2ad51e1adfaf4aefd6ae440259
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839514"
---
# <span data-ttu-id="2e7c4-101">Stop-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="2e7c4-101">Stop-AzSqlElasticJob</span></span>

## <span data-ttu-id="2e7c4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2e7c4-102">SYNOPSIS</span></span>
<span data-ttu-id="2e7c4-103">Feladat leállítása az adott tevékenységhez tartozó feladat-végrehajtási azonosítóval</span><span class="sxs-lookup"><span data-stu-id="2e7c4-103">Stops a job given it's job execution id</span></span>

## <span data-ttu-id="2e7c4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2e7c4-104">SYNTAX</span></span>

### <span data-ttu-id="2e7c4-105">DefaultSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2e7c4-105">DefaultSet (Default)</span></span>
```
Stop-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2e7c4-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="2e7c4-106">ObjectSet</span></span>
```
Stop-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobExecutionModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e7c4-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="2e7c4-107">ResourceIdSet</span></span>
```
Stop-AzSqlElasticJob [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e7c4-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="2e7c4-108">DESCRIPTION</span></span>
<span data-ttu-id="2e7c4-109">Az Stop-AzSqlElasticJob parancsmag leállítja a feladatot futó végrehajtással.</span><span class="sxs-lookup"><span data-stu-id="2e7c4-109">The Stop-AzSqlElasticJob cmdlet stops a job's with a running execution.</span></span>
<span data-ttu-id="2e7c4-110">A projekt végrehajtásának aktuális állapotát számítja ki.</span><span class="sxs-lookup"><span data-stu-id="2e7c4-110">Returns the current status of the job execution</span></span>

## <span data-ttu-id="2e7c4-111">Példák</span><span class="sxs-lookup"><span data-stu-id="2e7c4-111">EXAMPLES</span></span>

### <span data-ttu-id="2e7c4-112">Példa 1 – feladat leállítása futó feladatok végrehajtásával</span><span class="sxs-lookup"><span data-stu-id="2e7c4-112">Example 1 - Stops a job with a running job execution</span></span>
```
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId dab0ebe8-fd52-42e9-bacf-e5f27577039b
$je | Stop-AzSqlElasticJob
JobName JobExecutionId                       Lifecycle                    StartTime            EndTime
------- --------------                       ---------                    ---------            -------
job1    dab0ebe8-fd52-42e9-bacf-e5f27577039b WaitingForChildJobExecutions 6/1/2018 10:13:56 PM
```

<span data-ttu-id="2e7c4-113">Futtatja a futási feladatot, és az aktuális állapotát számítja ki.</span><span class="sxs-lookup"><span data-stu-id="2e7c4-113">Stops a running job execution and returns it's current status</span></span>

## <span data-ttu-id="2e7c4-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2e7c4-114">PARAMETERS</span></span>

### <span data-ttu-id="2e7c4-115">-AgentName</span><span class="sxs-lookup"><span data-stu-id="2e7c4-115">-AgentName</span></span>
<span data-ttu-id="2e7c4-116">Az ügynök neve</span><span class="sxs-lookup"><span data-stu-id="2e7c4-116">The agent name</span></span>

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

### <span data-ttu-id="2e7c4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e7c4-117">-DefaultProfile</span></span>
<span data-ttu-id="2e7c4-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2e7c4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e7c4-119">-JobExecutionId</span><span class="sxs-lookup"><span data-stu-id="2e7c4-119">-JobExecutionId</span></span>
<span data-ttu-id="2e7c4-120">A feladat-végrehajtási azonosító.</span><span class="sxs-lookup"><span data-stu-id="2e7c4-120">The job execution id.</span></span>

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

### <span data-ttu-id="2e7c4-121">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="2e7c4-121">-JobName</span></span>
<span data-ttu-id="2e7c4-122">A feladat neve</span><span class="sxs-lookup"><span data-stu-id="2e7c4-122">The job name</span></span>

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

### <span data-ttu-id="2e7c4-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="2e7c4-123">-ParentObject</span></span>
<span data-ttu-id="2e7c4-124">Az Agent Control Database objektum</span><span class="sxs-lookup"><span data-stu-id="2e7c4-124">The Agent Control Database Object</span></span>

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

### <span data-ttu-id="2e7c4-125">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="2e7c4-125">-ParentResourceId</span></span>
<span data-ttu-id="2e7c4-126">A feladat-végrehajtás erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="2e7c4-126">The job execution resource id</span></span>

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

### <span data-ttu-id="2e7c4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e7c4-127">-ResourceGroupName</span></span>
<span data-ttu-id="2e7c4-128">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="2e7c4-128">The resource group name</span></span>

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

### <span data-ttu-id="2e7c4-129">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="2e7c4-129">-ServerName</span></span>
<span data-ttu-id="2e7c4-130">A kiszolgáló neve</span><span class="sxs-lookup"><span data-stu-id="2e7c4-130">The server name</span></span>

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

### <span data-ttu-id="2e7c4-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2e7c4-131">-Confirm</span></span>
<span data-ttu-id="2e7c4-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2e7c4-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e7c4-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e7c4-133">-WhatIf</span></span>
<span data-ttu-id="2e7c4-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2e7c4-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e7c4-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2e7c4-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e7c4-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e7c4-136">CommonParameters</span></span>
<span data-ttu-id="2e7c4-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2e7c4-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e7c4-138">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="2e7c4-138">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e7c4-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2e7c4-139">INPUTS</span></span>

### <span data-ttu-id="2e7c4-140">Microsoft. Azure. Command. SQL. ElasticJobs. Model. AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="2e7c4-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="2e7c4-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2e7c4-141">OUTPUTS</span></span>

### <span data-ttu-id="2e7c4-142">Microsoft. Azure. Command. SQL. ElasticJobs. Model. AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="2e7c4-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="2e7c4-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2e7c4-143">NOTES</span></span>

## <span data-ttu-id="2e7c4-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2e7c4-144">RELATED LINKS</span></span>

## <span data-ttu-id="2e7c4-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2e7c4-145">RELATED LINKS</span></span>
