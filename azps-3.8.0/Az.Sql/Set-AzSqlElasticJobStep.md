---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobStep.md
ms.openlocfilehash: f39554dacdaabfc42fe44d55a7f3034c1c8b54df
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846746"
---
# <span data-ttu-id="f4044-101">Set-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="f4044-101">Set-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="f4044-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f4044-102">SYNOPSIS</span></span>
<span data-ttu-id="f4044-103">Feladat lépésének frissítése</span><span class="sxs-lookup"><span data-stu-id="f4044-103">Updates a job step</span></span>

## <span data-ttu-id="f4044-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f4044-104">SYNTAX</span></span>

### <span data-ttu-id="f4044-105">DefaultSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f4044-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-OutputDatabaseObject <AzureSqlDatabaseModel>]
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4044-106">WithRemoveOutput</span><span class="sxs-lookup"><span data-stu-id="f4044-106">WithRemoveOutput</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-RemoveOutput] [-TargetGroupName <String>] [-CredentialName <String>]
 [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>]
 [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f4044-107">WithAddOutput</span><span class="sxs-lookup"><span data-stu-id="f4044-107">WithAddOutput</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> -OutputDatabaseResourceId <String> [-OutputCredentialName <String>]
 [-OutputTableName <String>] [-OutputSchemaName <String>] [-TargetGroupName <String>]
 [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f4044-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="f4044-108">ObjectSet</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel>
 [-OutputDatabaseObject <AzureSqlDatabaseModel>] [-OutputCredentialName <String>] [-OutputTableName <String>]
 [-OutputSchemaName <String>] [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>]
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4044-109">WithRemoveOutputUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="f4044-109">WithRemoveOutputUsingParentObject</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel> [-RemoveOutput]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4044-110">WithAddOutputUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="f4044-110">WithAddOutputUsingParentObject</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel> -OutputDatabaseResourceId <String>
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4044-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="f4044-111">ResourceIdSet</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> [-OutputDatabaseObject <AzureSqlDatabaseModel>]
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4044-112">WithRemoveOutputUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="f4044-112">WithRemoveOutputUsingParentResourceId</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> [-RemoveOutput] [-TargetGroupName <String>]
 [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f4044-113">WithAddOutputUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="f4044-113">WithAddOutputUsingParentResourceId</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> -OutputDatabaseResourceId <String>
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4044-114">Leírás</span><span class="sxs-lookup"><span data-stu-id="f4044-114">DESCRIPTION</span></span>
<span data-ttu-id="f4044-115">A Set-AzSqlElasticJobStep parancsmag a feladat lépéseit frissíti</span><span class="sxs-lookup"><span data-stu-id="f4044-115">The Set-AzSqlElasticJobStep cmdlet updates a job step</span></span>

## <span data-ttu-id="f4044-116">Példák</span><span class="sxs-lookup"><span data-stu-id="f4044-116">EXAMPLES</span></span>

### <span data-ttu-id="f4044-117">Példa 1 – a projekt egy tevékenységhez tartozó célcsoportjának frissítése</span><span class="sxs-lookup"><span data-stu-id="f4044-117">Example 1 - Updates a job step's target group for a job</span></span>
```
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -StepName step1
$jobStep | Set-AzSqlElasticJobStep -TargetGroupName tg2

JobName StepName StepId TargetGroupName CredentialName Output ExecutionOptions   CommandText
------- -------- ------ --------------- -------------- ------ ----------------   -----------
job1    step1    1      tg2             cred1                 (43200,10,1,120,2) SELECT 1
```

### <span data-ttu-id="f4044-118">2. példa – egy projekthez tartozó T-SQL-parancsfájl frissítése</span><span class="sxs-lookup"><span data-stu-id="f4044-118">Example 2 - Updates a job step's T-SQL script for a job</span></span>
```
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -StepName step1
$jobStep | Set-AzSqlElasticJobStep -CommandText "SELECT 2"

JobName StepName StepId TargetGroupName CredentialName Output ExecutionOptions   CommandText
------- -------- ------ --------------- -------------- ------ ----------------   -----------
job1    step1    1      tg1             cred1                 (43200,10,1,120,2) SELECT 2
```

<span data-ttu-id="f4044-119">Feladat lépésének frissítése egy projektből</span><span class="sxs-lookup"><span data-stu-id="f4044-119">Updates a job step from a job</span></span>

## <span data-ttu-id="f4044-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f4044-120">PARAMETERS</span></span>

### <span data-ttu-id="f4044-121">-AgentName</span><span class="sxs-lookup"><span data-stu-id="f4044-121">-AgentName</span></span>
<span data-ttu-id="f4044-122">Az ügynök neve</span><span class="sxs-lookup"><span data-stu-id="f4044-122">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithRemoveOutput, WithAddOutput
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4044-123">-CommandText</span><span class="sxs-lookup"><span data-stu-id="f4044-123">-CommandText</span></span>
<span data-ttu-id="f4044-124">A parancs szövege</span><span class="sxs-lookup"><span data-stu-id="f4044-124">The command text</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4044-125">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="f4044-125">-CredentialName</span></span>
<span data-ttu-id="f4044-126">A hitelesítő adatok neve</span><span class="sxs-lookup"><span data-stu-id="f4044-126">The credential name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4044-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4044-127">-DefaultProfile</span></span>
<span data-ttu-id="f4044-128">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f4044-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4044-129">-InitialRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="f4044-129">-InitialRetryIntervalSeconds</span></span>
<span data-ttu-id="f4044-130">A kezdeti újrapróbálkozás ennyi idő után</span><span class="sxs-lookup"><span data-stu-id="f4044-130">The initial retry interval seconds</span></span>

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

### <span data-ttu-id="f4044-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f4044-131">-InputObject</span></span>
<span data-ttu-id="f4044-132">A Job Step objektum</span><span class="sxs-lookup"><span data-stu-id="f4044-132">The job step object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel
Parameter Sets: ObjectSet, WithRemoveOutputUsingParentObject, WithAddOutputUsingParentObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f4044-133">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="f4044-133">-JobName</span></span>
<span data-ttu-id="f4044-134">A feladat neve</span><span class="sxs-lookup"><span data-stu-id="f4044-134">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithRemoveOutput, WithAddOutput
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4044-135">-MaximumRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="f4044-135">-MaximumRetryIntervalSeconds</span></span>
<span data-ttu-id="f4044-136">A maximális újrapróbálkozás ennyi idő után</span><span class="sxs-lookup"><span data-stu-id="f4044-136">The maximum retry interval seconds</span></span>

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

### <span data-ttu-id="f4044-137">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f4044-137">-Name</span></span>
<span data-ttu-id="f4044-138">A lépéshez tartozó név</span><span class="sxs-lookup"><span data-stu-id="f4044-138">The step name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithRemoveOutput, WithAddOutput
Aliases: StepName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4044-139">-OutputCredentialName</span><span class="sxs-lookup"><span data-stu-id="f4044-139">-OutputCredentialName</span></span>
<span data-ttu-id="f4044-140">A kimeneti hitelesítő adatok neve</span><span class="sxs-lookup"><span data-stu-id="f4044-140">The output credential name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithAddOutput, ObjectSet, WithAddOutputUsingParentObject, ResourceIdSet, WithAddOutputUsingParentResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4044-141">-OutputDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="f4044-141">-OutputDatabaseObject</span></span>
<span data-ttu-id="f4044-142">A kimeneti adatbázis-objektum</span><span class="sxs-lookup"><span data-stu-id="f4044-142">The output database object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4044-143">-OutputDatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="f4044-143">-OutputDatabaseResourceId</span></span>
<span data-ttu-id="f4044-144">A kimeneti adatbázis erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="f4044-144">The output database resource id</span></span>

```yaml
Type: System.String
Parameter Sets: WithAddOutput, WithAddOutputUsingParentObject, WithAddOutputUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4044-145">-OutputSchemaName</span><span class="sxs-lookup"><span data-stu-id="f4044-145">-OutputSchemaName</span></span>
<span data-ttu-id="f4044-146">A kimeneti séma neve</span><span class="sxs-lookup"><span data-stu-id="f4044-146">The output schema name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithAddOutput, ObjectSet, WithAddOutputUsingParentObject, ResourceIdSet, WithAddOutputUsingParentResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4044-147">-OutputTableName</span><span class="sxs-lookup"><span data-stu-id="f4044-147">-OutputTableName</span></span>
<span data-ttu-id="f4044-148">A Készletrevételi táblázat neve</span><span class="sxs-lookup"><span data-stu-id="f4044-148">The output table name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithAddOutput, ObjectSet, WithAddOutputUsingParentObject, ResourceIdSet, WithAddOutputUsingParentResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4044-149">-RemoveOutput</span><span class="sxs-lookup"><span data-stu-id="f4044-149">-RemoveOutput</span></span>
<span data-ttu-id="f4044-150">Annak jelzése, hogy el szeretné-e távolítani a kimenetet</span><span class="sxs-lookup"><span data-stu-id="f4044-150">The flag to indicate whether to remove output</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WithRemoveOutput, WithRemoveOutputUsingParentObject, WithRemoveOutputUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4044-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4044-151">-ResourceGroupName</span></span>
<span data-ttu-id="f4044-152">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="f4044-152">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithRemoveOutput, WithAddOutput
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4044-153">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f4044-153">-ResourceId</span></span>
<span data-ttu-id="f4044-154">A feladat lépésének erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="f4044-154">The job step resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet, WithRemoveOutputUsingParentResourceId, WithAddOutputUsingParentResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4044-155">-RetryAttempts</span><span class="sxs-lookup"><span data-stu-id="f4044-155">-RetryAttempts</span></span>
<span data-ttu-id="f4044-156">Az újrapróbálkozási alkalmaz</span><span class="sxs-lookup"><span data-stu-id="f4044-156">The retry attemps</span></span>

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

### <span data-ttu-id="f4044-157">-RetryIntervalBackoffMultiplier</span><span class="sxs-lookup"><span data-stu-id="f4044-157">-RetryIntervalBackoffMultiplier</span></span>
<span data-ttu-id="f4044-158">Az újrapróbálkozási intervallum hát szorzója</span><span class="sxs-lookup"><span data-stu-id="f4044-158">The retry interval backoff multiplier</span></span>

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

### <span data-ttu-id="f4044-159">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="f4044-159">-ServerName</span></span>
<span data-ttu-id="f4044-160">A kiszolgáló neve</span><span class="sxs-lookup"><span data-stu-id="f4044-160">The server name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithRemoveOutput, WithAddOutput
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4044-161">-StepId</span><span class="sxs-lookup"><span data-stu-id="f4044-161">-StepId</span></span>
<span data-ttu-id="f4044-162">A Lépésköz szövege</span><span class="sxs-lookup"><span data-stu-id="f4044-162">The step id text</span></span>

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

### <span data-ttu-id="f4044-163">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="f4044-163">-TargetGroupName</span></span>
<span data-ttu-id="f4044-164">A cél csoport neve</span><span class="sxs-lookup"><span data-stu-id="f4044-164">The target group name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4044-165">-TimeoutSeconds</span><span class="sxs-lookup"><span data-stu-id="f4044-165">-TimeoutSeconds</span></span>
<span data-ttu-id="f4044-166">Az időkorlát másodperce</span><span class="sxs-lookup"><span data-stu-id="f4044-166">The timeout seconds</span></span>

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

### <span data-ttu-id="f4044-167">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f4044-167">-Confirm</span></span>
<span data-ttu-id="f4044-168">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f4044-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4044-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4044-169">-WhatIf</span></span>
<span data-ttu-id="f4044-170">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f4044-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4044-171">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f4044-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4044-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4044-172">CommonParameters</span></span>
<span data-ttu-id="f4044-173">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f4044-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4044-174">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f4044-174">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4044-175">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f4044-175">INPUTS</span></span>

### <span data-ttu-id="f4044-176">Microsoft. Azure. Command. SQL. ElasticJobs. Model. AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="f4044-176">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="f4044-177">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f4044-177">OUTPUTS</span></span>

### <span data-ttu-id="f4044-178">Microsoft. Azure. Command. SQL. ElasticJobs. Model. AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="f4044-178">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="f4044-179">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f4044-179">NOTES</span></span>

## <span data-ttu-id="f4044-180">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f4044-180">RELATED LINKS</span></span>
