---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/add-azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobStep.md
ms.openlocfilehash: 25c9845d0912374baa0e2219c234f63abe381cfc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011274"
---
# <span data-ttu-id="20b4c-101">Add-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="20b4c-101">Add-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="20b4c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="20b4c-102">SYNOPSIS</span></span>
<span data-ttu-id="20b4c-103">Munkalépés felvétele a projektbe</span><span class="sxs-lookup"><span data-stu-id="20b4c-103">Adds a job step to a job</span></span>

## <span data-ttu-id="20b4c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="20b4c-104">SYNTAX</span></span>

### <span data-ttu-id="20b4c-105">DefaultSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="20b4c-105">DefaultSet (Default)</span></span>
```
Add-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -TargetGroupName <String> -CredentialName <String> -CommandText <String> -Name <String>
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20b4c-106">WithOutputDb</span><span class="sxs-lookup"><span data-stu-id="20b4c-106">WithOutputDb</span></span>
```
Add-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -TargetGroupName <String> -CredentialName <String> -CommandText <String>
 -OutputDatabaseObject <AzureSqlDatabaseModel> -OutputCredentialName <String> -OutputTableName <String>
 -Name <String> [-OutputSchemaName <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="20b4c-107">WithOutputDbId</span><span class="sxs-lookup"><span data-stu-id="20b4c-107">WithOutputDbId</span></span>
```
Add-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -TargetGroupName <String> -CredentialName <String> -CommandText <String>
 -OutputDatabaseResourceId <String> -OutputCredentialName <String> -OutputTableName <String> -Name <String>
 [-OutputSchemaName <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>]
 [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="20b4c-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="20b4c-108">ObjectSet</span></span>
```
Add-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -TargetGroupName <String>
 -CredentialName <String> -CommandText <String> -Name <String> [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="20b4c-109">WithOutputDbUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="20b4c-109">WithOutputDbUsingParentObject</span></span>
```
Add-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -TargetGroupName <String>
 -CredentialName <String> -CommandText <String> -OutputDatabaseObject <AzureSqlDatabaseModel>
 -OutputCredentialName <String> -OutputTableName <String> -Name <String> [-OutputSchemaName <String>]
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20b4c-110">WithOutputDbIdUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="20b4c-110">WithOutputDbIdUsingParentObject</span></span>
```
Add-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -TargetGroupName <String>
 -CredentialName <String> -CommandText <String> -OutputDatabaseResourceId <String>
 -OutputCredentialName <String> -OutputTableName <String> -Name <String> [-OutputSchemaName <String>]
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20b4c-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="20b4c-111">ResourceIdSet</span></span>
```
Add-AzSqlElasticJobStep [-ParentResourceId] <String> -TargetGroupName <String> -CredentialName <String>
 -CommandText <String> -Name <String> [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>]
 [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="20b4c-112">WithOutputDbUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="20b4c-112">WithOutputDbUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobStep [-ParentResourceId] <String> -TargetGroupName <String> -CredentialName <String>
 -CommandText <String> -OutputDatabaseObject <AzureSqlDatabaseModel> -OutputCredentialName <String>
 -OutputTableName <String> -Name <String> [-OutputSchemaName <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20b4c-113">WithOutputDbIdUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="20b4c-113">WithOutputDbIdUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobStep [-ParentResourceId] <String> -TargetGroupName <String> -CredentialName <String>
 -CommandText <String> -OutputDatabaseResourceId <String> -OutputCredentialName <String>
 -OutputTableName <String> -Name <String> [-OutputSchemaName <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20b4c-114">Leírás</span><span class="sxs-lookup"><span data-stu-id="20b4c-114">DESCRIPTION</span></span>
<span data-ttu-id="20b4c-115">Az Add-AzSqlElasticJobStep parancsmag felveszi a feladatot a projekthez</span><span class="sxs-lookup"><span data-stu-id="20b4c-115">The Add-AzSqlElasticJobStep cmdlet adds a job step to a job</span></span>

## <span data-ttu-id="20b4c-116">Példák</span><span class="sxs-lookup"><span data-stu-id="20b4c-116">EXAMPLES</span></span>

### <span data-ttu-id="20b4c-117">Példa 1 – lépés felvétele a projektbe</span><span class="sxs-lookup"><span data-stu-id="20b4c-117">Example 1 - Adds a step to a job</span></span>
```
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -Name job1
$job | Add-AzSqlElasticJobStep -Name step1 -TargetGroupName tg1 -CredentialName cred1 -CommandText "SELECT 1"

JobName StepName StepId TargetGroupName CredentialName Output CommandText
------- -------- ------ --------------- -------------- ------ -----------
job1    step1    1      tg1             cred1                 SELECT 1
```

<span data-ttu-id="20b4c-118">Munkalépés felvétele a projektbe</span><span class="sxs-lookup"><span data-stu-id="20b4c-118">Adds a job step to a job</span></span>

## <span data-ttu-id="20b4c-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="20b4c-119">PARAMETERS</span></span>

### <span data-ttu-id="20b4c-120">-AgentName</span><span class="sxs-lookup"><span data-stu-id="20b4c-120">-AgentName</span></span>
<span data-ttu-id="20b4c-121">Az ügynök neve</span><span class="sxs-lookup"><span data-stu-id="20b4c-121">The agent name</span></span>

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

### <span data-ttu-id="20b4c-122">-CommandText</span><span class="sxs-lookup"><span data-stu-id="20b4c-122">-CommandText</span></span>
<span data-ttu-id="20b4c-123">A parancs szövege</span><span class="sxs-lookup"><span data-stu-id="20b4c-123">The command text</span></span>

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

### <span data-ttu-id="20b4c-124">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="20b4c-124">-CredentialName</span></span>
<span data-ttu-id="20b4c-125">A hitelesítő adatok neve</span><span class="sxs-lookup"><span data-stu-id="20b4c-125">The credential name</span></span>

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

### <span data-ttu-id="20b4c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20b4c-126">-DefaultProfile</span></span>
<span data-ttu-id="20b4c-127">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="20b4c-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20b4c-128">-InitialRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="20b4c-128">-InitialRetryIntervalSeconds</span></span>
<span data-ttu-id="20b4c-129">A kezdeti újrapróbálkozás ennyi idő után</span><span class="sxs-lookup"><span data-stu-id="20b4c-129">The initial retry interval seconds</span></span>

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

### <span data-ttu-id="20b4c-130">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="20b4c-130">-JobName</span></span>
<span data-ttu-id="20b4c-131">A feladat neve</span><span class="sxs-lookup"><span data-stu-id="20b4c-131">The job name</span></span>

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

### <span data-ttu-id="20b4c-132">-MaximumRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="20b4c-132">-MaximumRetryIntervalSeconds</span></span>
<span data-ttu-id="20b4c-133">A maximális újrapróbálkozás ennyi idő után</span><span class="sxs-lookup"><span data-stu-id="20b4c-133">The maximum retry interval seconds</span></span>

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

### <span data-ttu-id="20b4c-134">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="20b4c-134">-Name</span></span>
<span data-ttu-id="20b4c-135">A feladat lépéseinek neve</span><span class="sxs-lookup"><span data-stu-id="20b4c-135">The job step name</span></span>

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

### <span data-ttu-id="20b4c-136">-OutputCredentialName</span><span class="sxs-lookup"><span data-stu-id="20b4c-136">-OutputCredentialName</span></span>
<span data-ttu-id="20b4c-137">A kimeneti hitelesítő adatok neve</span><span class="sxs-lookup"><span data-stu-id="20b4c-137">The output credential name</span></span>

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

### <span data-ttu-id="20b4c-138">-OutputDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="20b4c-138">-OutputDatabaseObject</span></span>
<span data-ttu-id="20b4c-139">A kimeneti adatbázis-objektum</span><span class="sxs-lookup"><span data-stu-id="20b4c-139">The output database object</span></span>

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

### <span data-ttu-id="20b4c-140">-OutputDatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="20b4c-140">-OutputDatabaseResourceId</span></span>
<span data-ttu-id="20b4c-141">A kimeneti adatbázis erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="20b4c-141">The output database resource id</span></span>

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

### <span data-ttu-id="20b4c-142">-OutputSchemaName</span><span class="sxs-lookup"><span data-stu-id="20b4c-142">-OutputSchemaName</span></span>
<span data-ttu-id="20b4c-143">A kimeneti séma neve</span><span class="sxs-lookup"><span data-stu-id="20b4c-143">The output schema name</span></span>

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

### <span data-ttu-id="20b4c-144">-OutputTableName</span><span class="sxs-lookup"><span data-stu-id="20b4c-144">-OutputTableName</span></span>
<span data-ttu-id="20b4c-145">A Készletrevételi táblázat neve</span><span class="sxs-lookup"><span data-stu-id="20b4c-145">The output table name</span></span>

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

### <span data-ttu-id="20b4c-146">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="20b4c-146">-ParentObject</span></span>
<span data-ttu-id="20b4c-147">A Job objektum</span><span class="sxs-lookup"><span data-stu-id="20b4c-147">The job object</span></span>

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

### <span data-ttu-id="20b4c-148">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="20b4c-148">-ParentResourceId</span></span>
<span data-ttu-id="20b4c-149">A projekt erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="20b4c-149">The job resource id</span></span>

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

### <span data-ttu-id="20b4c-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20b4c-150">-ResourceGroupName</span></span>
<span data-ttu-id="20b4c-151">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="20b4c-151">The resource group name</span></span>

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

### <span data-ttu-id="20b4c-152">-RetryAttempts</span><span class="sxs-lookup"><span data-stu-id="20b4c-152">-RetryAttempts</span></span>
<span data-ttu-id="20b4c-153">Az újbóli próbálkozások</span><span class="sxs-lookup"><span data-stu-id="20b4c-153">The retry attempts</span></span>

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

### <span data-ttu-id="20b4c-154">-RetryIntervalBackoffMultiplier</span><span class="sxs-lookup"><span data-stu-id="20b4c-154">-RetryIntervalBackoffMultiplier</span></span>
<span data-ttu-id="20b4c-155">Az Újrapróbálkozások gyakorisága a szorzóból</span><span class="sxs-lookup"><span data-stu-id="20b4c-155">The retry interval back off multiplier</span></span>

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

### <span data-ttu-id="20b4c-156">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="20b4c-156">-ServerName</span></span>
<span data-ttu-id="20b4c-157">A kiszolgáló neve</span><span class="sxs-lookup"><span data-stu-id="20b4c-157">The server name</span></span>

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

### <span data-ttu-id="20b4c-158">-StepId</span><span class="sxs-lookup"><span data-stu-id="20b4c-158">-StepId</span></span>
<span data-ttu-id="20b4c-159">A Lépésköz</span><span class="sxs-lookup"><span data-stu-id="20b4c-159">The step id</span></span>

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

### <span data-ttu-id="20b4c-160">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="20b4c-160">-TargetGroupName</span></span>
<span data-ttu-id="20b4c-161">A cél csoport neve</span><span class="sxs-lookup"><span data-stu-id="20b4c-161">The target group name</span></span>

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

### <span data-ttu-id="20b4c-162">-TimeoutSeconds</span><span class="sxs-lookup"><span data-stu-id="20b4c-162">-TimeoutSeconds</span></span>
<span data-ttu-id="20b4c-163">Az időtúllépés másodpercben</span><span class="sxs-lookup"><span data-stu-id="20b4c-163">The time out seconds</span></span>

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

### <span data-ttu-id="20b4c-164">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="20b4c-164">-Confirm</span></span>
<span data-ttu-id="20b4c-165">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="20b4c-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20b4c-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20b4c-166">-WhatIf</span></span>
<span data-ttu-id="20b4c-167">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="20b4c-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20b4c-168">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="20b4c-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20b4c-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20b4c-169">CommonParameters</span></span>
<span data-ttu-id="20b4c-170">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="20b4c-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20b4c-171">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="20b4c-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20b4c-172">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="20b4c-172">INPUTS</span></span>

### <span data-ttu-id="20b4c-173">Microsoft. Azure. Command. SQL. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="20b4c-173">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="20b4c-174">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="20b4c-174">OUTPUTS</span></span>

### <span data-ttu-id="20b4c-175">Microsoft. Azure. Command. SQL. ElasticJobs. Model. AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="20b4c-175">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="20b4c-176">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="20b4c-176">NOTES</span></span>

## <span data-ttu-id="20b4c-177">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="20b4c-177">RELATED LINKS</span></span>
