---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/add-azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobStep.md
ms.openlocfilehash: dbc27ec87be3de4c320ad60b7dc204d704fe8f2f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100165819"
---
# <span data-ttu-id="ddab1-101">Add-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="ddab1-101">Add-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="ddab1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ddab1-102">SYNOPSIS</span></span>
<span data-ttu-id="ddab1-103">Feladatlépés hozzáadása egy feladathoz</span><span class="sxs-lookup"><span data-stu-id="ddab1-103">Adds a job step to a job</span></span>

## <span data-ttu-id="ddab1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ddab1-104">SYNTAX</span></span>

### <span data-ttu-id="ddab1-105">DefaultSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ddab1-105">DefaultSet (Default)</span></span>
```
Add-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -TargetGroupName <String> -CredentialName <String> -CommandText <String> -Name <String>
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddab1-106">WithOutputDb</span><span class="sxs-lookup"><span data-stu-id="ddab1-106">WithOutputDb</span></span>
```
Add-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -TargetGroupName <String> -CredentialName <String> -CommandText <String>
 -OutputDatabaseObject <AzureSqlDatabaseModel> -OutputCredentialName <String> -OutputTableName <String>
 -Name <String> [-OutputSchemaName <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ddab1-107">WithOutputDbId</span><span class="sxs-lookup"><span data-stu-id="ddab1-107">WithOutputDbId</span></span>
```
Add-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -TargetGroupName <String> -CredentialName <String> -CommandText <String>
 -OutputDatabaseResourceId <String> -OutputCredentialName <String> -OutputTableName <String> -Name <String>
 [-OutputSchemaName <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>]
 [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ddab1-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="ddab1-108">ObjectSet</span></span>
```
Add-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -TargetGroupName <String>
 -CredentialName <String> -CommandText <String> -Name <String> [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ddab1-109">WithOutputDbUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="ddab1-109">WithOutputDbUsingParentObject</span></span>
```
Add-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -TargetGroupName <String>
 -CredentialName <String> -CommandText <String> -OutputDatabaseObject <AzureSqlDatabaseModel>
 -OutputCredentialName <String> -OutputTableName <String> -Name <String> [-OutputSchemaName <String>]
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddab1-110">WithOutputDbIdUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="ddab1-110">WithOutputDbIdUsingParentObject</span></span>
```
Add-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -TargetGroupName <String>
 -CredentialName <String> -CommandText <String> -OutputDatabaseResourceId <String>
 -OutputCredentialName <String> -OutputTableName <String> -Name <String> [-OutputSchemaName <String>]
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddab1-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="ddab1-111">ResourceIdSet</span></span>
```
Add-AzSqlElasticJobStep [-ParentResourceId] <String> -TargetGroupName <String> -CredentialName <String>
 -CommandText <String> -Name <String> [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>]
 [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ddab1-112">WithOutputDbUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="ddab1-112">WithOutputDbUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobStep [-ParentResourceId] <String> -TargetGroupName <String> -CredentialName <String>
 -CommandText <String> -OutputDatabaseObject <AzureSqlDatabaseModel> -OutputCredentialName <String>
 -OutputTableName <String> -Name <String> [-OutputSchemaName <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddab1-113">WithOutputDbIdUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="ddab1-113">WithOutputDbIdUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobStep [-ParentResourceId] <String> -TargetGroupName <String> -CredentialName <String>
 -CommandText <String> -OutputDatabaseResourceId <String> -OutputCredentialName <String>
 -OutputTableName <String> -Name <String> [-OutputSchemaName <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ddab1-114">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ddab1-114">DESCRIPTION</span></span>
<span data-ttu-id="ddab1-115">A Add-AzSqlElasticJobStep parancsmag hozzáad egy feladatlépést egy feladathoz</span><span class="sxs-lookup"><span data-stu-id="ddab1-115">The Add-AzSqlElasticJobStep cmdlet adds a job step to a job</span></span>

## <span data-ttu-id="ddab1-116">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ddab1-116">EXAMPLES</span></span>

### <span data-ttu-id="ddab1-117">1. példa: Lépés hozzáadása egy feladathoz</span><span class="sxs-lookup"><span data-stu-id="ddab1-117">Example 1: Adds a step to a job</span></span>
```powershell
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -Name job1
$job | Add-AzSqlElasticJobStep -Name step1 -TargetGroupName tg1 -CredentialName cred1 -CommandText "SELECT 1"

JobName StepName StepId TargetGroupName CredentialName Output CommandText
------- -------- ------ --------------- -------------- ------ -----------
job1    step1    1      tg1             cred1                 SELECT 1
```

<span data-ttu-id="ddab1-118">Feladatlépés hozzáadása egy feladathoz</span><span class="sxs-lookup"><span data-stu-id="ddab1-118">Adds a job step to a job</span></span>

## <span data-ttu-id="ddab1-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ddab1-119">PARAMETERS</span></span>

### <span data-ttu-id="ddab1-120">-AgentName</span><span class="sxs-lookup"><span data-stu-id="ddab1-120">-AgentName</span></span>
<span data-ttu-id="ddab1-121">Az ügynök neve</span><span class="sxs-lookup"><span data-stu-id="ddab1-121">The agent name</span></span>

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

### <span data-ttu-id="ddab1-122">-CommandText</span><span class="sxs-lookup"><span data-stu-id="ddab1-122">-CommandText</span></span>
<span data-ttu-id="ddab1-123">A parancs szövege</span><span class="sxs-lookup"><span data-stu-id="ddab1-123">The command text</span></span>

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

### <span data-ttu-id="ddab1-124">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="ddab1-124">-CredentialName</span></span>
<span data-ttu-id="ddab1-125">A hitelesítő adatok neve</span><span class="sxs-lookup"><span data-stu-id="ddab1-125">The credential name</span></span>

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

### <span data-ttu-id="ddab1-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddab1-126">-DefaultProfile</span></span>
<span data-ttu-id="ddab1-127">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ddab1-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ddab1-128">-InitialRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="ddab1-128">-InitialRetryIntervalSeconds</span></span>
<span data-ttu-id="ddab1-129">A kezdeti újrapróbálkozási időköz másodperc</span><span class="sxs-lookup"><span data-stu-id="ddab1-129">The initial retry interval seconds</span></span>

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

### <span data-ttu-id="ddab1-130">-JobName</span><span class="sxs-lookup"><span data-stu-id="ddab1-130">-JobName</span></span>
<span data-ttu-id="ddab1-131">A feladat neve</span><span class="sxs-lookup"><span data-stu-id="ddab1-131">The job name</span></span>

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

### <span data-ttu-id="ddab1-132">-MaximumRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="ddab1-132">-MaximumRetryIntervalSeconds</span></span>
<span data-ttu-id="ddab1-133">A maximális újrapróbálkozási időköz másodperc</span><span class="sxs-lookup"><span data-stu-id="ddab1-133">The maximum retry interval seconds</span></span>

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

### <span data-ttu-id="ddab1-134">-Name</span><span class="sxs-lookup"><span data-stu-id="ddab1-134">-Name</span></span>
<span data-ttu-id="ddab1-135">A feladat lépésének neve</span><span class="sxs-lookup"><span data-stu-id="ddab1-135">The job step name</span></span>

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

### <span data-ttu-id="ddab1-136">-OutputCredentialName</span><span class="sxs-lookup"><span data-stu-id="ddab1-136">-OutputCredentialName</span></span>
<span data-ttu-id="ddab1-137">A kimeneti hitelesítő adatok neve</span><span class="sxs-lookup"><span data-stu-id="ddab1-137">The output credential name</span></span>

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

### <span data-ttu-id="ddab1-138">-OutputDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="ddab1-138">-OutputDatabaseObject</span></span>
<span data-ttu-id="ddab1-139">A kimeneti adatbázis-objektum</span><span class="sxs-lookup"><span data-stu-id="ddab1-139">The output database object</span></span>

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

### <span data-ttu-id="ddab1-140">-OutputDatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="ddab1-140">-OutputDatabaseResourceId</span></span>
<span data-ttu-id="ddab1-141">A kimeneti adatbázis erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="ddab1-141">The output database resource id</span></span>

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

### <span data-ttu-id="ddab1-142">-OutputSchemaName</span><span class="sxs-lookup"><span data-stu-id="ddab1-142">-OutputSchemaName</span></span>
<span data-ttu-id="ddab1-143">A kimeneti séma neve</span><span class="sxs-lookup"><span data-stu-id="ddab1-143">The output schema name</span></span>

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

### <span data-ttu-id="ddab1-144">-OutputTableName</span><span class="sxs-lookup"><span data-stu-id="ddab1-144">-OutputTableName</span></span>
<span data-ttu-id="ddab1-145">A kimeneti tábla neve</span><span class="sxs-lookup"><span data-stu-id="ddab1-145">The output table name</span></span>

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

### <span data-ttu-id="ddab1-146">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="ddab1-146">-ParentObject</span></span>
<span data-ttu-id="ddab1-147">A feladatobjektum</span><span class="sxs-lookup"><span data-stu-id="ddab1-147">The job object</span></span>

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

### <span data-ttu-id="ddab1-148">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="ddab1-148">-ParentResourceId</span></span>
<span data-ttu-id="ddab1-149">A feladaterőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="ddab1-149">The job resource id</span></span>

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

### <span data-ttu-id="ddab1-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddab1-150">-ResourceGroupName</span></span>
<span data-ttu-id="ddab1-151">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="ddab1-151">The resource group name</span></span>

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

### <span data-ttu-id="ddab1-152">-RetryAttempts</span><span class="sxs-lookup"><span data-stu-id="ddab1-152">-RetryAttempts</span></span>
<span data-ttu-id="ddab1-153">Az újrapróbálkozási kísérletek</span><span class="sxs-lookup"><span data-stu-id="ddab1-153">The retry attempts</span></span>

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

### <span data-ttu-id="ddab1-154">-RetryIntervalBackoffMultiplier</span><span class="sxs-lookup"><span data-stu-id="ddab1-154">-RetryIntervalBackoffMultiplier</span></span>
<span data-ttu-id="ddab1-155">Az újrapróbálkozási időköz visszaszorzása</span><span class="sxs-lookup"><span data-stu-id="ddab1-155">The retry interval back off multiplier</span></span>

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

### <span data-ttu-id="ddab1-156">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ddab1-156">-ServerName</span></span>
<span data-ttu-id="ddab1-157">A kiszolgáló neve</span><span class="sxs-lookup"><span data-stu-id="ddab1-157">The server name</span></span>

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

### <span data-ttu-id="ddab1-158">-StepId</span><span class="sxs-lookup"><span data-stu-id="ddab1-158">-StepId</span></span>
<span data-ttu-id="ddab1-159">A lépésazonosító</span><span class="sxs-lookup"><span data-stu-id="ddab1-159">The step id</span></span>

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

### <span data-ttu-id="ddab1-160">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="ddab1-160">-TargetGroupName</span></span>
<span data-ttu-id="ddab1-161">A célcsoport neve</span><span class="sxs-lookup"><span data-stu-id="ddab1-161">The target group name</span></span>

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

### <span data-ttu-id="ddab1-162">-TimeoutSeconds</span><span class="sxs-lookup"><span data-stu-id="ddab1-162">-TimeoutSeconds</span></span>
<span data-ttu-id="ddab1-163">Az időkorrekta másodpercben</span><span class="sxs-lookup"><span data-stu-id="ddab1-163">The time out seconds</span></span>

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

### <span data-ttu-id="ddab1-164">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ddab1-164">-Confirm</span></span>
<span data-ttu-id="ddab1-165">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ddab1-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ddab1-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddab1-166">-WhatIf</span></span>
<span data-ttu-id="ddab1-167">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="ddab1-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ddab1-168">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ddab1-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ddab1-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddab1-169">CommonParameters</span></span>
<span data-ttu-id="ddab1-170">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddab1-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddab1-171">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ddab1-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddab1-172">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ddab1-172">INPUTS</span></span>

### <span data-ttu-id="ddab1-173">Microsoft.Azure.Commands.Sql.Rugasz.Model.AzureSqlElasticModel</span><span class="sxs-lookup"><span data-stu-id="ddab1-173">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="ddab1-174">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ddab1-174">OUTPUTS</span></span>

### <span data-ttu-id="ddab1-175">Microsoft.Azure.Commands.Sql.ElasticMods.Model.AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="ddab1-175">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="ddab1-176">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ddab1-176">NOTES</span></span>

## <span data-ttu-id="ddab1-177">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ddab1-177">RELATED LINKS</span></span>
