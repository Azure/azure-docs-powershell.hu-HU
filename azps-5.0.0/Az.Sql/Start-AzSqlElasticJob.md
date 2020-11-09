---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/start-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlElasticJob.md
ms.openlocfilehash: 5ab6b7e6e77fcfcf470c67bfdd8e300ddc4343ea
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300086"
---
# <span data-ttu-id="ca7b7-101">Start-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="ca7b7-101">Start-AzSqlElasticJob</span></span>

## <span data-ttu-id="ca7b7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ca7b7-102">SYNOPSIS</span></span>
<span data-ttu-id="ca7b7-103">Elindít egy feladatot, amely egy olyan feladat-végrehajtási azonosítót ad vissza, amely megkérdezhető az állapotának megtekintéséhez</span><span class="sxs-lookup"><span data-stu-id="ca7b7-103">Starts a job, returning a job execution id that can be polled to view it's status</span></span>

## <span data-ttu-id="ca7b7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ca7b7-104">SYNTAX</span></span>

### <span data-ttu-id="ca7b7-105">DefaultSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ca7b7-105">DefaultSet (Default)</span></span>
```
Start-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> [-Wait] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ca7b7-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="ca7b7-106">ObjectSet</span></span>
```
Start-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobModel> [-Wait] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca7b7-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="ca7b7-107">ResourceIdSet</span></span>
```
Start-AzSqlElasticJob [-ParentResourceId] <String> [-Wait] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca7b7-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="ca7b7-108">DESCRIPTION</span></span>
<span data-ttu-id="ca7b7-109">A Start-AzSqlElasticJob parancsmag új feladat-végrehajtást visszaadó munkát indít</span><span class="sxs-lookup"><span data-stu-id="ca7b7-109">The Start-AzSqlElasticJob cmdlet starts a job returning a new job execution</span></span>

## <span data-ttu-id="ca7b7-110">Példák</span><span class="sxs-lookup"><span data-stu-id="ca7b7-110">EXAMPLES</span></span>

### <span data-ttu-id="ca7b7-111">Példa 1 – új feladat-végrehajtást visszaadó feladat indítása</span><span class="sxs-lookup"><span data-stu-id="ca7b7-111">Example 1 - Starts a job returning a new job execution</span></span>
```
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name job1
$job | Start-AzSqlElasticJob

JobName JobExecutionId                       Lifecycle StartTime EndTime
------- --------------                       --------- --------- -------
job1    b93b3a90-987b-4565-b3d3-5fa1751fa9bc Created
```

<span data-ttu-id="ca7b7-112">Új feladat-végrehajtást visszaadó feladat indítása</span><span class="sxs-lookup"><span data-stu-id="ca7b7-112">Starts a job returning a new job execution</span></span>

## <span data-ttu-id="ca7b7-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ca7b7-113">PARAMETERS</span></span>

### <span data-ttu-id="ca7b7-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="ca7b7-114">-AgentName</span></span>
<span data-ttu-id="ca7b7-115">Az ügynök neve</span><span class="sxs-lookup"><span data-stu-id="ca7b7-115">The agent name</span></span>

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

### <span data-ttu-id="ca7b7-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ca7b7-116">-AsJob</span></span>
<span data-ttu-id="ca7b7-117">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="ca7b7-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ca7b7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca7b7-118">-DefaultProfile</span></span>
<span data-ttu-id="ca7b7-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ca7b7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca7b7-120">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="ca7b7-120">-JobName</span></span>
<span data-ttu-id="ca7b7-121">A feladat neve</span><span class="sxs-lookup"><span data-stu-id="ca7b7-121">The job name</span></span>

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

### <span data-ttu-id="ca7b7-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="ca7b7-122">-ParentObject</span></span>
<span data-ttu-id="ca7b7-123">A Job objektum</span><span class="sxs-lookup"><span data-stu-id="ca7b7-123">The job object</span></span>

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

### <span data-ttu-id="ca7b7-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="ca7b7-124">-ParentResourceId</span></span>
<span data-ttu-id="ca7b7-125">A projekt erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="ca7b7-125">The job resource id</span></span>

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

### <span data-ttu-id="ca7b7-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca7b7-126">-ResourceGroupName</span></span>
<span data-ttu-id="ca7b7-127">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="ca7b7-127">The resource group name</span></span>

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

### <span data-ttu-id="ca7b7-128">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="ca7b7-128">-ServerName</span></span>
<span data-ttu-id="ca7b7-129">A kiszolgáló neve</span><span class="sxs-lookup"><span data-stu-id="ca7b7-129">The server name</span></span>

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

### <span data-ttu-id="ca7b7-130">– Várjon</span><span class="sxs-lookup"><span data-stu-id="ca7b7-130">-Wait</span></span>
<span data-ttu-id="ca7b7-131">Várjon, amíg a várakozási idő megmarad, amíg a feladat végrehajtása meg nem történik</span><span class="sxs-lookup"><span data-stu-id="ca7b7-131">The wait flag to indicate to wait until the job's execution is done</span></span>

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

### <span data-ttu-id="ca7b7-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ca7b7-132">-Confirm</span></span>
<span data-ttu-id="ca7b7-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ca7b7-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca7b7-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca7b7-134">-WhatIf</span></span>
<span data-ttu-id="ca7b7-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ca7b7-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca7b7-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ca7b7-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca7b7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca7b7-137">CommonParameters</span></span>
<span data-ttu-id="ca7b7-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ca7b7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca7b7-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ca7b7-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca7b7-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ca7b7-140">INPUTS</span></span>

### <span data-ttu-id="ca7b7-141">Microsoft. Azure. Command. SQL. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="ca7b7-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="ca7b7-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ca7b7-142">OUTPUTS</span></span>

### <span data-ttu-id="ca7b7-143">Microsoft. Azure. Command. SQL. ElasticJobs. Model. AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="ca7b7-143">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="ca7b7-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ca7b7-144">NOTES</span></span>

## <span data-ttu-id="ca7b7-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ca7b7-145">RELATED LINKS</span></span>
