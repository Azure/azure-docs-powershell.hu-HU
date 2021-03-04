---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/remove-Azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobStep.md
ms.openlocfilehash: 788817dd9ca344501dc25bad48b71b7e24b653d9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920209"
---
# <span data-ttu-id="663e5-101">Remove-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="663e5-101">Remove-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="663e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="663e5-102">SYNOPSIS</span></span>
<span data-ttu-id="663e5-103">A feladat lépésének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="663e5-103">Removes the job step</span></span>

## <span data-ttu-id="663e5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="663e5-104">SYNTAX</span></span>

### <span data-ttu-id="663e5-105">DefaultSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="663e5-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="663e5-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="663e5-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="663e5-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="663e5-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobStep [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="663e5-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="663e5-108">DESCRIPTION</span></span>
<span data-ttu-id="663e5-109">A Remove-AzSqlElasticJobStep parancsmag eltávolítja a feladat lépését egy feladatból</span><span class="sxs-lookup"><span data-stu-id="663e5-109">The Remove-AzSqlElasticJobStep cmdlet removes a job step from a job</span></span>

## <span data-ttu-id="663e5-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="663e5-110">EXAMPLES</span></span>

### <span data-ttu-id="663e5-111">1. példa: Egy feladat lépésének eltávolítása egy feladatból</span><span class="sxs-lookup"><span data-stu-id="663e5-111">Example 1: Removes a job step from a job</span></span>
```powershell
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -Name step1
$jobStep | Remove-AzSqlElasticJobStep

JobName StepName StepId TargetGroupName CredentialName Output CommandText
------- -------- ------ --------------- -------------- ------ -----------
job1    step1    1      tg1             cred1                 SELECT 1
```

<span data-ttu-id="663e5-112">Egy feladat lépésének eltávolítása egy feladatból</span><span class="sxs-lookup"><span data-stu-id="663e5-112">Removes a job step from a job</span></span>

### <span data-ttu-id="663e5-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="663e5-113">Example 2</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Remove-AzSqlElasticJobStep -AgentName agent -JobName job1 -Name step1 -ResourceGroupName MyResourceGroup -ServerName s1
```

## <span data-ttu-id="663e5-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="663e5-114">PARAMETERS</span></span>

### <span data-ttu-id="663e5-115">-AgentName</span><span class="sxs-lookup"><span data-stu-id="663e5-115">-AgentName</span></span>
<span data-ttu-id="663e5-116">Az ügynök neve</span><span class="sxs-lookup"><span data-stu-id="663e5-116">The agent name</span></span>

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

### <span data-ttu-id="663e5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="663e5-117">-DefaultProfile</span></span>
<span data-ttu-id="663e5-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="663e5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="663e5-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="663e5-119">-InputObject</span></span>
<span data-ttu-id="663e5-120">The job step input object</span><span class="sxs-lookup"><span data-stu-id="663e5-120">The job step input object</span></span>

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

### <span data-ttu-id="663e5-121">-JobName</span><span class="sxs-lookup"><span data-stu-id="663e5-121">-JobName</span></span>
<span data-ttu-id="663e5-122">A feladat neve</span><span class="sxs-lookup"><span data-stu-id="663e5-122">The job name</span></span>

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

### <span data-ttu-id="663e5-123">-Name</span><span class="sxs-lookup"><span data-stu-id="663e5-123">-Name</span></span>
<span data-ttu-id="663e5-124">A feladat lépésének neve</span><span class="sxs-lookup"><span data-stu-id="663e5-124">The job step name</span></span>

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

### <span data-ttu-id="663e5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="663e5-125">-ResourceGroupName</span></span>
<span data-ttu-id="663e5-126">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="663e5-126">The resource group name</span></span>

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

### <span data-ttu-id="663e5-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="663e5-127">-ResourceId</span></span>
<span data-ttu-id="663e5-128">A feladatlépés erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="663e5-128">The job step resource id</span></span>

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

### <span data-ttu-id="663e5-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="663e5-129">-ServerName</span></span>
<span data-ttu-id="663e5-130">A kiszolgáló neve</span><span class="sxs-lookup"><span data-stu-id="663e5-130">The server name</span></span>

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

### <span data-ttu-id="663e5-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="663e5-131">-Confirm</span></span>
<span data-ttu-id="663e5-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="663e5-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="663e5-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="663e5-133">-WhatIf</span></span>
<span data-ttu-id="663e5-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="663e5-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="663e5-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="663e5-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="663e5-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="663e5-136">CommonParameters</span></span>
<span data-ttu-id="663e5-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="663e5-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="663e5-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="663e5-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="663e5-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="663e5-139">INPUTS</span></span>

### <span data-ttu-id="663e5-140">Microsoft.Azure.Commands.Sql.ElasticMods.Model.AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="663e5-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="663e5-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="663e5-141">OUTPUTS</span></span>

### <span data-ttu-id="663e5-142">Microsoft.Azure.Commands.Sql.ElasticMods.Model.AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="663e5-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="663e5-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="663e5-143">NOTES</span></span>

## <span data-ttu-id="663e5-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="663e5-144">RELATED LINKS</span></span>
