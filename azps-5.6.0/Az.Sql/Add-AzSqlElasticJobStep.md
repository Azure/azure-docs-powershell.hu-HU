---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/add-azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobStep.md
ms.openlocfilehash: 41314cb2a65912e2973e91b27036fc099d2cbca6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923385"
---
# <span data-ttu-id="152e7-101">Add-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="152e7-101">Add-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="152e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="152e7-102">SYNOPSIS</span></span>
<span data-ttu-id="152e7-103">Feladatlépés hozzáadása egy feladathoz</span><span class="sxs-lookup"><span data-stu-id="152e7-103">Adds a job step to a job</span></span>

## <span data-ttu-id="152e7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="152e7-104">SYNTAX</span></span>

### <span data-ttu-id="152e7-105">DefaultSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="152e7-105">DefaultSet (Default)</span></span>
```
Add-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -TargetGroupName <String> -CredentialName <String> -CommandText <String> -Name <String>
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="152e7-106">WithOutputDb</span><span class="sxs-lookup"><span data-stu-id="152e7-106">WithOutputDb</span></span>
```
Add-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -TargetGroupName <String> -CredentialName <String> -CommandText <String>
 -OutputDatabaseObject <AzureSqlDatabaseModel> -OutputCredentialName <String> -OutputTableName <String>
 -Name <String> [-OutputSchemaName <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="152e7-107">WithOutputDbId</span><span class="sxs-lookup"><span data-stu-id="152e7-107">WithOutputDbId</span></span>
```
Add-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -TargetGroupName <String> -CredentialName <String> -CommandText <String>
 -OutputDatabaseResourceId <String> -OutputCredentialName <String> -OutputTableName <String> -Name <String>
 [-OutputSchemaName <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>]
 [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="152e7-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="152e7-108">ObjectSet</span></span>
```
Add-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -TargetGroupName <String>
 -CredentialName <String> -CommandText <String> -Name <String> [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="152e7-109">WithOutputDbUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="152e7-109">WithOutputDbUsingParentObject</span></span>
```
Add-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -TargetGroupName <String>
 -CredentialName <String> -CommandText <String> -OutputDatabaseObject <AzureSqlDatabaseModel>
 -OutputCredentialName <String> -OutputTableName <String> -Name <String> [-OutputSchemaName <String>]
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="152e7-110">WithOutputDbIdUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="152e7-110">WithOutputDbIdUsingParentObject</span></span>
```
Add-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -TargetGroupName <String>
 -CredentialName <String> -CommandText <String> -OutputDatabaseResourceId <String>
 -OutputCredentialName <String> -OutputTableName <String> -Name <String> [-OutputSchemaName <String>]
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="152e7-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="152e7-111">ResourceIdSet</span></span>
```
Add-AzSqlElasticJobStep [-ParentResourceId] <String> -TargetGroupName <String> -CredentialName <String>
 -CommandText <String> -Name <String> [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>]
 [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="152e7-112">WithOutputDbUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="152e7-112">WithOutputDbUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobStep [-ParentResourceId] <String> -TargetGroupName <String> -CredentialName <String>
 -CommandText <String> -OutputDatabaseObject <AzureSqlDatabaseModel> -OutputCredentialName <String>
 -OutputTableName <String> -Name <String> [-OutputSchemaName <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="152e7-113">WithOutputDbIdUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="152e7-113">WithOutputDbIdUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobStep [-ParentResourceId] <String> -TargetGroupName <String> -CredentialName <String>
 -CommandText <String> -OutputDatabaseResourceId <String> -OutputCredentialName <String>
 -OutputTableName <String> -Name <String> [-OutputSchemaName <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="152e7-114">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="152e7-114">DESCRIPTION</span></span>
<span data-ttu-id="152e7-115">A Add-AzSqlElasticJobStep parancsmag hozzáad egy feladatlépést egy feladathoz</span><span class="sxs-lookup"><span data-stu-id="152e7-115">The Add-AzSqlElasticJobStep cmdlet adds a job step to a job</span></span>

## <span data-ttu-id="152e7-116">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="152e7-116">EXAMPLES</span></span>

### <span data-ttu-id="152e7-117">1. példa: Lépés hozzáadása egy feladathoz</span><span class="sxs-lookup"><span data-stu-id="152e7-117">Example 1: Adds a step to a job</span></span>
```powershell
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -Name job1
$job | Add-AzSqlElasticJobStep -Name step1 -TargetGroupName tg1 -CredentialName cred1 -CommandText "SELECT 1"

JobName StepName StepId TargetGroupName CredentialName Output CommandText
------- -------- ------ --------------- -------------- ------ -----------
job1    step1    1      tg1             cred1                 SELECT 1
```

<span data-ttu-id="152e7-118">Feladatlépés hozzáadása egy feladathoz</span><span class="sxs-lookup"><span data-stu-id="152e7-118">Adds a job step to a job</span></span>

## <span data-ttu-id="152e7-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="152e7-119">PARAMETERS</span></span>

### <span data-ttu-id="152e7-120">-AgentName</span><span class="sxs-lookup"><span data-stu-id="152e7-120">-AgentName</span></span>
<span data-ttu-id="152e7-121">Az ügynök neve</span><span class="sxs-lookup"><span data-stu-id="152e7-121">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithOutputDb, WithOutputDbId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="152e7-122">-CommandText</span><span class="sxs-lookup"><span data-stu-id="152e7-122">-CommandText</span></span>
<span data-ttu-id="152e7-123">A parancs szövege</span><span class="sxs-lookup"><span data-stu-id="152e7-123">The command text</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="152e7-124">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="152e7-124">-CredentialName</span></span>
<span data-ttu-id="152e7-125">A hitelesítő adatok neve</span><span class="sxs-lookup"><span data-stu-id="152e7-125">The credential name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="152e7-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="152e7-126">-DefaultProfile</span></span>
<span data-ttu-id="152e7-127">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="152e7-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="152e7-128">-InitialRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="152e7-128">-InitialRetryIntervalSeconds</span></span>
<span data-ttu-id="152e7-129">A kezdeti újrapróbálkozási időköz másodperc</span><span class="sxs-lookup"><span data-stu-id="152e7-129">The initial retry interval seconds</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="152e7-130">-JobName</span><span class="sxs-lookup"><span data-stu-id="152e7-130">-JobName</span></span>
<span data-ttu-id="152e7-131">A feladat neve</span><span class="sxs-lookup"><span data-stu-id="152e7-131">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithOutputDb, WithOutputDbId
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="152e7-132">-MaximumRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="152e7-132">-MaximumRetryIntervalSeconds</span></span>
<span data-ttu-id="152e7-133">A maximális újrapróbálkozási időköz másodperc</span><span class="sxs-lookup"><span data-stu-id="152e7-133">The maximum retry interval seconds</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="152e7-134">-Name</span><span class="sxs-lookup"><span data-stu-id="152e7-134">-Name</span></span>
<span data-ttu-id="152e7-135">A feladat lépésének neve</span><span class="sxs-lookup"><span data-stu-id="152e7-135">The job step name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StepName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="152e7-136">-OutputCredentialName</span><span class="sxs-lookup"><span data-stu-id="152e7-136">-OutputCredentialName</span></span>
<span data-ttu-id="152e7-137">A kimeneti hitelesítő adatok neve</span><span class="sxs-lookup"><span data-stu-id="152e7-137">The output credential name</span></span>

```yaml
Type: System.String
Parameter Sets: WithOutputDb, WithOutputDbId, WithOutputDbUsingParentObject, WithOutputDbIdUsingParentObject, WithOutputDbUsingParentResourceId, WithOutputDbIdUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="152e7-138">-OutputDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="152e7-138">-OutputDatabaseObject</span></span>
<span data-ttu-id="152e7-139">A kimeneti adatbázis-objektum</span><span class="sxs-lookup"><span data-stu-id="152e7-139">The output database object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: WithOutputDb, WithOutputDbUsingParentObject, WithOutputDbUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="152e7-140">-OutputDatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="152e7-140">-OutputDatabaseResourceId</span></span>
<span data-ttu-id="152e7-141">A kimeneti adatbázis erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="152e7-141">The output database resource id</span></span>

```yaml
Type: System.String
Parameter Sets: WithOutputDbId, WithOutputDbIdUsingParentObject, WithOutputDbIdUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="152e7-142">-OutputSchemaName</span><span class="sxs-lookup"><span data-stu-id="152e7-142">-OutputSchemaName</span></span>
<span data-ttu-id="152e7-143">A kimeneti séma neve</span><span class="sxs-lookup"><span data-stu-id="152e7-143">The output schema name</span></span>

```yaml
Type: System.String
Parameter Sets: WithOutputDb, WithOutputDbId, WithOutputDbUsingParentObject, WithOutputDbIdUsingParentObject, WithOutputDbUsingParentResourceId, WithOutputDbIdUsingParentResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="152e7-144">-OutputTableName</span><span class="sxs-lookup"><span data-stu-id="152e7-144">-OutputTableName</span></span>
<span data-ttu-id="152e7-145">A kimeneti tábla neve</span><span class="sxs-lookup"><span data-stu-id="152e7-145">The output table name</span></span>

```yaml
Type: System.String
Parameter Sets: WithOutputDb, WithOutputDbId, WithOutputDbUsingParentObject, WithOutputDbIdUsingParentObject, WithOutputDbUsingParentResourceId, WithOutputDbIdUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="152e7-146">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="152e7-146">-ParentObject</span></span>
<span data-ttu-id="152e7-147">A feladatobjektum</span><span class="sxs-lookup"><span data-stu-id="152e7-147">The job object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel
Parameter Sets: ObjectSet, WithOutputDbUsingParentObject, WithOutputDbIdUsingParentObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="152e7-148">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="152e7-148">-ParentResourceId</span></span>
<span data-ttu-id="152e7-149">A feladaterőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="152e7-149">The job resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet, WithOutputDbUsingParentResourceId, WithOutputDbIdUsingParentResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="152e7-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="152e7-150">-ResourceGroupName</span></span>
<span data-ttu-id="152e7-151">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="152e7-151">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithOutputDb, WithOutputDbId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="152e7-152">-RetryAttempts</span><span class="sxs-lookup"><span data-stu-id="152e7-152">-RetryAttempts</span></span>
<span data-ttu-id="152e7-153">Az újrapróbálkozási kísérletek</span><span class="sxs-lookup"><span data-stu-id="152e7-153">The retry attempts</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="152e7-154">-RetryIntervalBackoffMultiplier</span><span class="sxs-lookup"><span data-stu-id="152e7-154">-RetryIntervalBackoffMultiplier</span></span>
<span data-ttu-id="152e7-155">Az újrapróbálkozási időköz visszaszorzása</span><span class="sxs-lookup"><span data-stu-id="152e7-155">The retry interval back off multiplier</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="152e7-156">-ServerName</span><span class="sxs-lookup"><span data-stu-id="152e7-156">-ServerName</span></span>
<span data-ttu-id="152e7-157">A kiszolgáló neve</span><span class="sxs-lookup"><span data-stu-id="152e7-157">The server name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithOutputDb, WithOutputDbId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="152e7-158">-StepId</span><span class="sxs-lookup"><span data-stu-id="152e7-158">-StepId</span></span>
<span data-ttu-id="152e7-159">A lépésazonosító</span><span class="sxs-lookup"><span data-stu-id="152e7-159">The step id</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="152e7-160">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="152e7-160">-TargetGroupName</span></span>
<span data-ttu-id="152e7-161">A célcsoport neve</span><span class="sxs-lookup"><span data-stu-id="152e7-161">The target group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithOutputDb, WithOutputDbId, ObjectSet, WithOutputDbUsingParentObject, WithOutputDbIdUsingParentObject, ResourceIdSet, WithOutputDbIdUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WithOutputDbUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="152e7-162">-TimeoutSeconds</span><span class="sxs-lookup"><span data-stu-id="152e7-162">-TimeoutSeconds</span></span>
<span data-ttu-id="152e7-163">Az időkorrekta másodpercben</span><span class="sxs-lookup"><span data-stu-id="152e7-163">The time out seconds</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="152e7-164">-Confirm</span><span class="sxs-lookup"><span data-stu-id="152e7-164">-Confirm</span></span>
<span data-ttu-id="152e7-165">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="152e7-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="152e7-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="152e7-166">-WhatIf</span></span>
<span data-ttu-id="152e7-167">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="152e7-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="152e7-168">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="152e7-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="152e7-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="152e7-169">CommonParameters</span></span>
<span data-ttu-id="152e7-170">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="152e7-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="152e7-171">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="152e7-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="152e7-172">INPUTS</span><span class="sxs-lookup"><span data-stu-id="152e7-172">INPUTS</span></span>

### <span data-ttu-id="152e7-173">Microsoft.Azure.Commands.Sql.ElasticMods.Model.AzureSqlElasticModel</span><span class="sxs-lookup"><span data-stu-id="152e7-173">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="152e7-174">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="152e7-174">OUTPUTS</span></span>

### <span data-ttu-id="152e7-175">Microsoft.Azure.Commands.Sql.ElasticMods.Model.AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="152e7-175">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="152e7-176">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="152e7-176">NOTES</span></span>

## <span data-ttu-id="152e7-177">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="152e7-177">RELATED LINKS</span></span>
