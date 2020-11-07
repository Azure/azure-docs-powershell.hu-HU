---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobStep.md
ms.openlocfilehash: 83d5733144c07c229cf8b5321ee9d3417ab112ad
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839389"
---
# <span data-ttu-id="1e747-101">Remove-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="1e747-101">Remove-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="1e747-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1e747-102">SYNOPSIS</span></span>
<span data-ttu-id="1e747-103">A feladat lépésének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="1e747-103">Removes the job step</span></span>

## <span data-ttu-id="1e747-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1e747-104">SYNTAX</span></span>

### <span data-ttu-id="1e747-105">DefaultSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1e747-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1e747-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="1e747-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e747-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="1e747-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobStep [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e747-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="1e747-108">DESCRIPTION</span></span>
<span data-ttu-id="1e747-109">A Remove-AzSqlElasticJobStep parancsmag eltávolítja a feladatot a projektből</span><span class="sxs-lookup"><span data-stu-id="1e747-109">The Remove-AzSqlElasticJobStep cmdlet removes a job step from a job</span></span>

## <span data-ttu-id="1e747-110">Példák</span><span class="sxs-lookup"><span data-stu-id="1e747-110">EXAMPLES</span></span>

### <span data-ttu-id="1e747-111">Példa 1 – feladat lépésének eltávolítása a projektből</span><span class="sxs-lookup"><span data-stu-id="1e747-111">Example 1 - Removes a job step from a job</span></span>
```
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -Name step1
$jobStep | Remove-AzSqlElasticJobStep

JobName StepName StepId TargetGroupName CredentialName Output CommandText
------- -------- ------ --------------- -------------- ------ -----------
job1    step1    1      tg1             cred1                 SELECT 1
```

<span data-ttu-id="1e747-112">Feladat lépésének eltávolítása egy projektből</span><span class="sxs-lookup"><span data-stu-id="1e747-112">Removes a job step from a job</span></span>

## <span data-ttu-id="1e747-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1e747-113">PARAMETERS</span></span>

### <span data-ttu-id="1e747-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="1e747-114">-AgentName</span></span>
<span data-ttu-id="1e747-115">Az ügynök neve</span><span class="sxs-lookup"><span data-stu-id="1e747-115">The agent name</span></span>

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

### <span data-ttu-id="1e747-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e747-116">-DefaultProfile</span></span>
<span data-ttu-id="1e747-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1e747-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e747-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1e747-118">-InputObject</span></span>
<span data-ttu-id="1e747-119">A projekt lépésének bemeneti objektuma</span><span class="sxs-lookup"><span data-stu-id="1e747-119">The job step input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1e747-120">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="1e747-120">-JobName</span></span>
<span data-ttu-id="1e747-121">A feladat neve</span><span class="sxs-lookup"><span data-stu-id="1e747-121">The job name</span></span>

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

### <span data-ttu-id="1e747-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1e747-122">-Name</span></span>
<span data-ttu-id="1e747-123">A feladat lépéseinek neve</span><span class="sxs-lookup"><span data-stu-id="1e747-123">The job step name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases: StepName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e747-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e747-124">-ResourceGroupName</span></span>
<span data-ttu-id="1e747-125">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="1e747-125">The resource group name</span></span>

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

### <span data-ttu-id="1e747-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1e747-126">-ResourceId</span></span>
<span data-ttu-id="1e747-127">A feladat lépésének erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="1e747-127">The job step resource id</span></span>

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

### <span data-ttu-id="1e747-128">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="1e747-128">-ServerName</span></span>
<span data-ttu-id="1e747-129">A kiszolgáló neve</span><span class="sxs-lookup"><span data-stu-id="1e747-129">The server name</span></span>

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

### <span data-ttu-id="1e747-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1e747-130">-Confirm</span></span>
<span data-ttu-id="1e747-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1e747-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e747-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e747-132">-WhatIf</span></span>
<span data-ttu-id="1e747-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1e747-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e747-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1e747-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e747-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e747-135">CommonParameters</span></span>
<span data-ttu-id="1e747-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1e747-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e747-137">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1e747-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e747-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1e747-138">INPUTS</span></span>

### <span data-ttu-id="1e747-139">Microsoft. Azure. Command. SQL. ElasticJobs. Model. AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="1e747-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="1e747-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1e747-140">OUTPUTS</span></span>

### <span data-ttu-id="1e747-141">Microsoft. Azure. Command. SQL. ElasticJobs. Model. AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="1e747-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="1e747-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1e747-142">NOTES</span></span>

## <span data-ttu-id="1e747-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1e747-143">RELATED LINKS</span></span>
