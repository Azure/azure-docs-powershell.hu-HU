---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobStep.md
ms.openlocfilehash: 4f6f0471224799e818f9db29e5be5a4c49f9c45e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183878"
---
# <span data-ttu-id="73bd6-101">Set-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="73bd6-101">Set-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="73bd6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="73bd6-102">SYNOPSIS</span></span>
<span data-ttu-id="73bd6-103">Feladat lépésének frissítése</span><span class="sxs-lookup"><span data-stu-id="73bd6-103">Updates a job step</span></span>

## <span data-ttu-id="73bd6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="73bd6-104">SYNTAX</span></span>

### <span data-ttu-id="73bd6-105">DefaultSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="73bd6-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-OutputDatabaseObject <AzureSqlDatabaseModel>]
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73bd6-106">WithRemoveOutput</span><span class="sxs-lookup"><span data-stu-id="73bd6-106">WithRemoveOutput</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-RemoveOutput] [-TargetGroupName <String>] [-CredentialName <String>]
 [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>]
 [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="73bd6-107">WithAddOutput</span><span class="sxs-lookup"><span data-stu-id="73bd6-107">WithAddOutput</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> -OutputDatabaseResourceId <String> [-OutputCredentialName <String>]
 [-OutputTableName <String>] [-OutputSchemaName <String>] [-TargetGroupName <String>]
 [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="73bd6-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="73bd6-108">ObjectSet</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel>
 [-OutputDatabaseObject <AzureSqlDatabaseModel>] [-OutputCredentialName <String>] [-OutputTableName <String>]
 [-OutputSchemaName <String>] [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>]
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73bd6-109">WithRemoveOutputUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="73bd6-109">WithRemoveOutputUsingParentObject</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel> [-RemoveOutput]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73bd6-110">WithAddOutputUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="73bd6-110">WithAddOutputUsingParentObject</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel> -OutputDatabaseResourceId <String>
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73bd6-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="73bd6-111">ResourceIdSet</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> [-OutputDatabaseObject <AzureSqlDatabaseModel>]
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73bd6-112">WithRemoveOutputUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="73bd6-112">WithRemoveOutputUsingParentResourceId</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> [-RemoveOutput] [-TargetGroupName <String>]
 [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="73bd6-113">WithAddOutputUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="73bd6-113">WithAddOutputUsingParentResourceId</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> -OutputDatabaseResourceId <String>
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73bd6-114">Leírás</span><span class="sxs-lookup"><span data-stu-id="73bd6-114">DESCRIPTION</span></span>
<span data-ttu-id="73bd6-115">A Set-AzSqlElasticJobStep parancsmag a feladat lépéseit frissíti</span><span class="sxs-lookup"><span data-stu-id="73bd6-115">The Set-AzSqlElasticJobStep cmdlet updates a job step</span></span>

## <span data-ttu-id="73bd6-116">Példák</span><span class="sxs-lookup"><span data-stu-id="73bd6-116">EXAMPLES</span></span>

### <span data-ttu-id="73bd6-117">1. példa: a projekt egy tevékenységhez tartozó célcsoportjának frissítése</span><span class="sxs-lookup"><span data-stu-id="73bd6-117">Example 1: Updates a job step's target group for a job</span></span>
```powershell
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -StepName step1
$jobStep | Set-AzSqlElasticJobStep -TargetGroupName tg2

JobName StepName StepId TargetGroupName CredentialName Output ExecutionOptions   CommandText
------- -------- ------ --------------- -------------- ------ ----------------   -----------
job1    step1    1      tg2             cred1                 (43200,10,1,120,2) SELECT 1
```

### <span data-ttu-id="73bd6-118">2. példa: egy projekthez tartozó T-SQL-parancsfájl frissítése</span><span class="sxs-lookup"><span data-stu-id="73bd6-118">Example 2: Updates a job step's T-SQL script for a job</span></span>
```powershell
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -StepName step1
$jobStep | Set-AzSqlElasticJobStep -CommandText "SELECT 2"

JobName StepName StepId TargetGroupName CredentialName Output ExecutionOptions   CommandText
------- -------- ------ --------------- -------------- ------ ----------------   -----------
job1    step1    1      tg1             cred1                 (43200,10,1,120,2) SELECT 2
```

<span data-ttu-id="73bd6-119">Feladat lépésének frissítése egy projektből</span><span class="sxs-lookup"><span data-stu-id="73bd6-119">Updates a job step from a job</span></span>

### <span data-ttu-id="73bd6-120">3. példa</span><span class="sxs-lookup"><span data-stu-id="73bd6-120">Example 3</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlElasticJobStep -AgentName agent -CommandText 'SELECT 2' -JobName job1 -Name step1 -ResourceGroupName MyResourceGroup -ServerName s1
```

## <span data-ttu-id="73bd6-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="73bd6-121">PARAMETERS</span></span>

### <span data-ttu-id="73bd6-122">-AgentName</span><span class="sxs-lookup"><span data-stu-id="73bd6-122">-AgentName</span></span>
<span data-ttu-id="73bd6-123">Az ügynök neve</span><span class="sxs-lookup"><span data-stu-id="73bd6-123">The agent name</span></span>

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

### <span data-ttu-id="73bd6-124">-CommandText</span><span class="sxs-lookup"><span data-stu-id="73bd6-124">-CommandText</span></span>
<span data-ttu-id="73bd6-125">A parancs szövege</span><span class="sxs-lookup"><span data-stu-id="73bd6-125">The command text</span></span>

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

### <span data-ttu-id="73bd6-126">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="73bd6-126">-CredentialName</span></span>
<span data-ttu-id="73bd6-127">A hitelesítő adatok neve</span><span class="sxs-lookup"><span data-stu-id="73bd6-127">The credential name</span></span>

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

### <span data-ttu-id="73bd6-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73bd6-128">-DefaultProfile</span></span>
<span data-ttu-id="73bd6-129">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="73bd6-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73bd6-130">-InitialRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="73bd6-130">-InitialRetryIntervalSeconds</span></span>
<span data-ttu-id="73bd6-131">A kezdeti újrapróbálkozás ennyi idő után</span><span class="sxs-lookup"><span data-stu-id="73bd6-131">The initial retry interval seconds</span></span>

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

### <span data-ttu-id="73bd6-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="73bd6-132">-InputObject</span></span>
<span data-ttu-id="73bd6-133">A Job Step objektum</span><span class="sxs-lookup"><span data-stu-id="73bd6-133">The job step object</span></span>

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

### <span data-ttu-id="73bd6-134">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="73bd6-134">-JobName</span></span>
<span data-ttu-id="73bd6-135">A feladat neve</span><span class="sxs-lookup"><span data-stu-id="73bd6-135">The job name</span></span>

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

### <span data-ttu-id="73bd6-136">-MaximumRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="73bd6-136">-MaximumRetryIntervalSeconds</span></span>
<span data-ttu-id="73bd6-137">A maximális újrapróbálkozás ennyi idő után</span><span class="sxs-lookup"><span data-stu-id="73bd6-137">The maximum retry interval seconds</span></span>

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

### <span data-ttu-id="73bd6-138">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="73bd6-138">-Name</span></span>
<span data-ttu-id="73bd6-139">A lépéshez tartozó név</span><span class="sxs-lookup"><span data-stu-id="73bd6-139">The step name</span></span>

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

### <span data-ttu-id="73bd6-140">-OutputCredentialName</span><span class="sxs-lookup"><span data-stu-id="73bd6-140">-OutputCredentialName</span></span>
<span data-ttu-id="73bd6-141">A kimeneti hitelesítő adatok neve</span><span class="sxs-lookup"><span data-stu-id="73bd6-141">The output credential name</span></span>

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

### <span data-ttu-id="73bd6-142">-OutputDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="73bd6-142">-OutputDatabaseObject</span></span>
<span data-ttu-id="73bd6-143">A kimeneti adatbázis-objektum</span><span class="sxs-lookup"><span data-stu-id="73bd6-143">The output database object</span></span>

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

### <span data-ttu-id="73bd6-144">-OutputDatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="73bd6-144">-OutputDatabaseResourceId</span></span>
<span data-ttu-id="73bd6-145">A kimeneti adatbázis erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="73bd6-145">The output database resource id</span></span>

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

### <span data-ttu-id="73bd6-146">-OutputSchemaName</span><span class="sxs-lookup"><span data-stu-id="73bd6-146">-OutputSchemaName</span></span>
<span data-ttu-id="73bd6-147">A kimeneti séma neve</span><span class="sxs-lookup"><span data-stu-id="73bd6-147">The output schema name</span></span>

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

### <span data-ttu-id="73bd6-148">-OutputTableName</span><span class="sxs-lookup"><span data-stu-id="73bd6-148">-OutputTableName</span></span>
<span data-ttu-id="73bd6-149">A Készletrevételi táblázat neve</span><span class="sxs-lookup"><span data-stu-id="73bd6-149">The output table name</span></span>

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

### <span data-ttu-id="73bd6-150">-RemoveOutput</span><span class="sxs-lookup"><span data-stu-id="73bd6-150">-RemoveOutput</span></span>
<span data-ttu-id="73bd6-151">Annak jelzése, hogy el szeretné-e távolítani a kimenetet</span><span class="sxs-lookup"><span data-stu-id="73bd6-151">The flag to indicate whether to remove output</span></span>

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

### <span data-ttu-id="73bd6-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73bd6-152">-ResourceGroupName</span></span>
<span data-ttu-id="73bd6-153">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="73bd6-153">The resource group name</span></span>

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

### <span data-ttu-id="73bd6-154">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="73bd6-154">-ResourceId</span></span>
<span data-ttu-id="73bd6-155">A feladat lépésének erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="73bd6-155">The job step resource id</span></span>

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

### <span data-ttu-id="73bd6-156">-RetryAttempts</span><span class="sxs-lookup"><span data-stu-id="73bd6-156">-RetryAttempts</span></span>
<span data-ttu-id="73bd6-157">Az újrapróbálkozási alkalmaz</span><span class="sxs-lookup"><span data-stu-id="73bd6-157">The retry attemps</span></span>

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

### <span data-ttu-id="73bd6-158">-RetryIntervalBackoffMultiplier</span><span class="sxs-lookup"><span data-stu-id="73bd6-158">-RetryIntervalBackoffMultiplier</span></span>
<span data-ttu-id="73bd6-159">Az újrapróbálkozási intervallum hát szorzója</span><span class="sxs-lookup"><span data-stu-id="73bd6-159">The retry interval backoff multiplier</span></span>

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

### <span data-ttu-id="73bd6-160">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="73bd6-160">-ServerName</span></span>
<span data-ttu-id="73bd6-161">A kiszolgáló neve</span><span class="sxs-lookup"><span data-stu-id="73bd6-161">The server name</span></span>

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

### <span data-ttu-id="73bd6-162">-StepId</span><span class="sxs-lookup"><span data-stu-id="73bd6-162">-StepId</span></span>
<span data-ttu-id="73bd6-163">A Lépésköz szövege</span><span class="sxs-lookup"><span data-stu-id="73bd6-163">The step id text</span></span>

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

### <span data-ttu-id="73bd6-164">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="73bd6-164">-TargetGroupName</span></span>
<span data-ttu-id="73bd6-165">A cél csoport neve</span><span class="sxs-lookup"><span data-stu-id="73bd6-165">The target group name</span></span>

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

### <span data-ttu-id="73bd6-166">-TimeoutSeconds</span><span class="sxs-lookup"><span data-stu-id="73bd6-166">-TimeoutSeconds</span></span>
<span data-ttu-id="73bd6-167">Az időkorlát másodperce</span><span class="sxs-lookup"><span data-stu-id="73bd6-167">The timeout seconds</span></span>

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

### <span data-ttu-id="73bd6-168">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="73bd6-168">-Confirm</span></span>
<span data-ttu-id="73bd6-169">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="73bd6-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73bd6-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73bd6-170">-WhatIf</span></span>
<span data-ttu-id="73bd6-171">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="73bd6-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73bd6-172">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="73bd6-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73bd6-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73bd6-173">CommonParameters</span></span>
<span data-ttu-id="73bd6-174">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="73bd6-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73bd6-175">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="73bd6-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73bd6-176">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="73bd6-176">INPUTS</span></span>

### <span data-ttu-id="73bd6-177">Microsoft. Azure. Command. SQL. ElasticJobs. Model. AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="73bd6-177">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="73bd6-178">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="73bd6-178">OUTPUTS</span></span>

### <span data-ttu-id="73bd6-179">Microsoft. Azure. Command. SQL. ElasticJobs. Model. AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="73bd6-179">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="73bd6-180">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="73bd6-180">NOTES</span></span>

## <span data-ttu-id="73bd6-181">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="73bd6-181">RELATED LINKS</span></span>
