---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobStep.md
ms.openlocfilehash: b097c95f45700afabd3317a1014641da061d410d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186533"
---
# <span data-ttu-id="b4be6-101">Remove-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="b4be6-101">Remove-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="b4be6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b4be6-102">SYNOPSIS</span></span>
<span data-ttu-id="b4be6-103">A feladat lépésének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="b4be6-103">Removes the job step</span></span>

## <span data-ttu-id="b4be6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b4be6-104">SYNTAX</span></span>

### <span data-ttu-id="b4be6-105">DefaultSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b4be6-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b4be6-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="b4be6-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4be6-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b4be6-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobStep [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4be6-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="b4be6-108">DESCRIPTION</span></span>
<span data-ttu-id="b4be6-109">A Remove-AzSqlElasticJobStep parancsmag eltávolítja a feladatot a projektből</span><span class="sxs-lookup"><span data-stu-id="b4be6-109">The Remove-AzSqlElasticJobStep cmdlet removes a job step from a job</span></span>

## <span data-ttu-id="b4be6-110">Példák</span><span class="sxs-lookup"><span data-stu-id="b4be6-110">EXAMPLES</span></span>

### <span data-ttu-id="b4be6-111">1. példa: a feladat lépésének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="b4be6-111">Example 1: Removes a job step from a job</span></span>
```powershell
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -Name step1
$jobStep | Remove-AzSqlElasticJobStep

JobName StepName StepId TargetGroupName CredentialName Output CommandText
------- -------- ------ --------------- -------------- ------ -----------
job1    step1    1      tg1             cred1                 SELECT 1
```

<span data-ttu-id="b4be6-112">Feladat lépésének eltávolítása egy projektből</span><span class="sxs-lookup"><span data-stu-id="b4be6-112">Removes a job step from a job</span></span>

### <span data-ttu-id="b4be6-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="b4be6-113">Example 2</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Remove-AzSqlElasticJobStep -AgentName agent -JobName job1 -Name step1 -ResourceGroupName MyResourceGroup -ServerName s1
```

## <span data-ttu-id="b4be6-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b4be6-114">PARAMETERS</span></span>

### <span data-ttu-id="b4be6-115">-AgentName</span><span class="sxs-lookup"><span data-stu-id="b4be6-115">-AgentName</span></span>
<span data-ttu-id="b4be6-116">Az ügynök neve</span><span class="sxs-lookup"><span data-stu-id="b4be6-116">The agent name</span></span>

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

### <span data-ttu-id="b4be6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4be6-117">-DefaultProfile</span></span>
<span data-ttu-id="b4be6-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b4be6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4be6-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b4be6-119">-InputObject</span></span>
<span data-ttu-id="b4be6-120">A projekt lépésének bemeneti objektuma</span><span class="sxs-lookup"><span data-stu-id="b4be6-120">The job step input object</span></span>

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

### <span data-ttu-id="b4be6-121">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="b4be6-121">-JobName</span></span>
<span data-ttu-id="b4be6-122">A feladat neve</span><span class="sxs-lookup"><span data-stu-id="b4be6-122">The job name</span></span>

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

### <span data-ttu-id="b4be6-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b4be6-123">-Name</span></span>
<span data-ttu-id="b4be6-124">A feladat lépéseinek neve</span><span class="sxs-lookup"><span data-stu-id="b4be6-124">The job step name</span></span>

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

### <span data-ttu-id="b4be6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4be6-125">-ResourceGroupName</span></span>
<span data-ttu-id="b4be6-126">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="b4be6-126">The resource group name</span></span>

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

### <span data-ttu-id="b4be6-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b4be6-127">-ResourceId</span></span>
<span data-ttu-id="b4be6-128">A feladat lépésének erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="b4be6-128">The job step resource id</span></span>

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

### <span data-ttu-id="b4be6-129">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="b4be6-129">-ServerName</span></span>
<span data-ttu-id="b4be6-130">A kiszolgáló neve</span><span class="sxs-lookup"><span data-stu-id="b4be6-130">The server name</span></span>

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

### <span data-ttu-id="b4be6-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b4be6-131">-Confirm</span></span>
<span data-ttu-id="b4be6-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b4be6-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4be6-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4be6-133">-WhatIf</span></span>
<span data-ttu-id="b4be6-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b4be6-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4be6-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b4be6-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4be6-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4be6-136">CommonParameters</span></span>
<span data-ttu-id="b4be6-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b4be6-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4be6-138">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b4be6-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4be6-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b4be6-139">INPUTS</span></span>

### <span data-ttu-id="b4be6-140">Microsoft. Azure. Command. SQL. ElasticJobs. Model. AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="b4be6-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="b4be6-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b4be6-141">OUTPUTS</span></span>

### <span data-ttu-id="b4be6-142">Microsoft. Azure. Command. SQL. ElasticJobs. Model. AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="b4be6-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="b4be6-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b4be6-143">NOTES</span></span>

## <span data-ttu-id="b4be6-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b4be6-144">RELATED LINKS</span></span>
