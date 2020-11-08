---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobStep.md
ms.openlocfilehash: c0ebc561a047ffe6a62722012fd7ecd3d42e472a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013188"
---
# <span data-ttu-id="972c3-101">Remove-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="972c3-101">Remove-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="972c3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="972c3-102">SYNOPSIS</span></span>
<span data-ttu-id="972c3-103">A feladat lépésének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="972c3-103">Removes the job step</span></span>

## <span data-ttu-id="972c3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="972c3-104">SYNTAX</span></span>

### <span data-ttu-id="972c3-105">DefaultSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="972c3-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="972c3-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="972c3-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="972c3-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="972c3-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobStep [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="972c3-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="972c3-108">DESCRIPTION</span></span>
<span data-ttu-id="972c3-109">A Remove-AzSqlElasticJobStep parancsmag eltávolítja a feladatot a projektből</span><span class="sxs-lookup"><span data-stu-id="972c3-109">The Remove-AzSqlElasticJobStep cmdlet removes a job step from a job</span></span>

## <span data-ttu-id="972c3-110">Példák</span><span class="sxs-lookup"><span data-stu-id="972c3-110">EXAMPLES</span></span>

### <span data-ttu-id="972c3-111">Példa 1 – feladat lépésének eltávolítása a projektből</span><span class="sxs-lookup"><span data-stu-id="972c3-111">Example 1 - Removes a job step from a job</span></span>
```
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -Name step1
$jobStep | Remove-AzSqlElasticJobStep

JobName StepName StepId TargetGroupName CredentialName Output CommandText
------- -------- ------ --------------- -------------- ------ -----------
job1    step1    1      tg1             cred1                 SELECT 1
```

<span data-ttu-id="972c3-112">Feladat lépésének eltávolítása egy projektből</span><span class="sxs-lookup"><span data-stu-id="972c3-112">Removes a job step from a job</span></span>

## <span data-ttu-id="972c3-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="972c3-113">PARAMETERS</span></span>

### <span data-ttu-id="972c3-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="972c3-114">-AgentName</span></span>
<span data-ttu-id="972c3-115">Az ügynök neve</span><span class="sxs-lookup"><span data-stu-id="972c3-115">The agent name</span></span>

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

### <span data-ttu-id="972c3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="972c3-116">-DefaultProfile</span></span>
<span data-ttu-id="972c3-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="972c3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="972c3-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="972c3-118">-InputObject</span></span>
<span data-ttu-id="972c3-119">A projekt lépésének bemeneti objektuma</span><span class="sxs-lookup"><span data-stu-id="972c3-119">The job step input object</span></span>

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

### <span data-ttu-id="972c3-120">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="972c3-120">-JobName</span></span>
<span data-ttu-id="972c3-121">A feladat neve</span><span class="sxs-lookup"><span data-stu-id="972c3-121">The job name</span></span>

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

### <span data-ttu-id="972c3-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="972c3-122">-Name</span></span>
<span data-ttu-id="972c3-123">A feladat lépéseinek neve</span><span class="sxs-lookup"><span data-stu-id="972c3-123">The job step name</span></span>

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

### <span data-ttu-id="972c3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="972c3-124">-ResourceGroupName</span></span>
<span data-ttu-id="972c3-125">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="972c3-125">The resource group name</span></span>

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

### <span data-ttu-id="972c3-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="972c3-126">-ResourceId</span></span>
<span data-ttu-id="972c3-127">A feladat lépésének erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="972c3-127">The job step resource id</span></span>

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

### <span data-ttu-id="972c3-128">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="972c3-128">-ServerName</span></span>
<span data-ttu-id="972c3-129">A kiszolgáló neve</span><span class="sxs-lookup"><span data-stu-id="972c3-129">The server name</span></span>

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

### <span data-ttu-id="972c3-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="972c3-130">-Confirm</span></span>
<span data-ttu-id="972c3-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="972c3-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="972c3-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="972c3-132">-WhatIf</span></span>
<span data-ttu-id="972c3-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="972c3-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="972c3-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="972c3-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="972c3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="972c3-135">CommonParameters</span></span>
<span data-ttu-id="972c3-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="972c3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="972c3-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="972c3-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="972c3-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="972c3-138">INPUTS</span></span>

### <span data-ttu-id="972c3-139">Microsoft. Azure. Command. SQL. ElasticJobs. Model. AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="972c3-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="972c3-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="972c3-140">OUTPUTS</span></span>

### <span data-ttu-id="972c3-141">Microsoft. Azure. Command. SQL. ElasticJobs. Model. AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="972c3-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="972c3-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="972c3-142">NOTES</span></span>

## <span data-ttu-id="972c3-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="972c3-143">RELATED LINKS</span></span>
