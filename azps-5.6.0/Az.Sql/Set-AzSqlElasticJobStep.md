---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/set-Azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobStep.md
ms.openlocfilehash: ec2f9174cc0ca8781b56784836a4583b0568128e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933394"
---
# <span data-ttu-id="01755-101">Set-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="01755-101">Set-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="01755-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01755-102">SYNOPSIS</span></span>
<span data-ttu-id="01755-103">Feladatlépés frissítése</span><span class="sxs-lookup"><span data-stu-id="01755-103">Updates a job step</span></span>

## <span data-ttu-id="01755-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="01755-104">SYNTAX</span></span>

### <span data-ttu-id="01755-105">DefaultSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="01755-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-OutputDatabaseObject <AzureSqlDatabaseModel>]
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01755-106">WithRemoveOutput</span><span class="sxs-lookup"><span data-stu-id="01755-106">WithRemoveOutput</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-RemoveOutput] [-TargetGroupName <String>] [-CredentialName <String>]
 [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>]
 [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="01755-107">WithAddOutput</span><span class="sxs-lookup"><span data-stu-id="01755-107">WithAddOutput</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> -OutputDatabaseResourceId <String> [-OutputCredentialName <String>]
 [-OutputTableName <String>] [-OutputSchemaName <String>] [-TargetGroupName <String>]
 [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="01755-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="01755-108">ObjectSet</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel>
 [-OutputDatabaseObject <AzureSqlDatabaseModel>] [-OutputCredentialName <String>] [-OutputTableName <String>]
 [-OutputSchemaName <String>] [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>]
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01755-109">WithRemoveOutputUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="01755-109">WithRemoveOutputUsingParentObject</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel> [-RemoveOutput]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01755-110">WithAddOutputUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="01755-110">WithAddOutputUsingParentObject</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel> -OutputDatabaseResourceId <String>
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01755-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="01755-111">ResourceIdSet</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> [-OutputDatabaseObject <AzureSqlDatabaseModel>]
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01755-112">WithRemoveOutputUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="01755-112">WithRemoveOutputUsingParentResourceId</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> [-RemoveOutput] [-TargetGroupName <String>]
 [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="01755-113">WithAddOutputUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="01755-113">WithAddOutputUsingParentResourceId</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> -OutputDatabaseResourceId <String>
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01755-114">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="01755-114">DESCRIPTION</span></span>
<span data-ttu-id="01755-115">A Set-AzSqlElasticJobStep parancsmag frissíti a feladatlépést</span><span class="sxs-lookup"><span data-stu-id="01755-115">The Set-AzSqlElasticJobStep cmdlet updates a job step</span></span>

## <span data-ttu-id="01755-116">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="01755-116">EXAMPLES</span></span>

### <span data-ttu-id="01755-117">1. példa: Frissíti egy feladat feladatlépésének célcsoportját egy feladathoz</span><span class="sxs-lookup"><span data-stu-id="01755-117">Example 1: Updates a job step's target group for a job</span></span>
```powershell
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -StepName step1
$jobStep | Set-AzSqlElasticJobStep -TargetGroupName tg2

JobName StepName StepId TargetGroupName CredentialName Output ExecutionOptions   CommandText
------- -------- ------ --------------- -------------- ------ ----------------   -----------
job1    step1    1      tg2             cred1                 (43200,10,1,120,2) SELECT 1
```

### <span data-ttu-id="01755-118">2. példa: Egy feladat lépésének T-SQL-parancsfájljának frissítése egy feladathoz</span><span class="sxs-lookup"><span data-stu-id="01755-118">Example 2: Updates a job step's T-SQL script for a job</span></span>
```powershell
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -StepName step1
$jobStep | Set-AzSqlElasticJobStep -CommandText "SELECT 2"

JobName StepName StepId TargetGroupName CredentialName Output ExecutionOptions   CommandText
------- -------- ------ --------------- -------------- ------ ----------------   -----------
job1    step1    1      tg1             cred1                 (43200,10,1,120,2) SELECT 2
```

<span data-ttu-id="01755-119">Egy feladat lépésének frissítése egy feladatból</span><span class="sxs-lookup"><span data-stu-id="01755-119">Updates a job step from a job</span></span>

### <span data-ttu-id="01755-120">3. példa</span><span class="sxs-lookup"><span data-stu-id="01755-120">Example 3</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlElasticJobStep -AgentName agent -CommandText 'SELECT 2' -JobName job1 -Name step1 -ResourceGroupName MyResourceGroup -ServerName s1
```

## <span data-ttu-id="01755-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="01755-121">PARAMETERS</span></span>

### <span data-ttu-id="01755-122">-AgentName</span><span class="sxs-lookup"><span data-stu-id="01755-122">-AgentName</span></span>
<span data-ttu-id="01755-123">Az ügynök neve</span><span class="sxs-lookup"><span data-stu-id="01755-123">The agent name</span></span>

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

### <span data-ttu-id="01755-124">-CommandText</span><span class="sxs-lookup"><span data-stu-id="01755-124">-CommandText</span></span>
<span data-ttu-id="01755-125">A parancs szövege</span><span class="sxs-lookup"><span data-stu-id="01755-125">The command text</span></span>

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

### <span data-ttu-id="01755-126">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="01755-126">-CredentialName</span></span>
<span data-ttu-id="01755-127">A hitelesítő adatok neve</span><span class="sxs-lookup"><span data-stu-id="01755-127">The credential name</span></span>

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

### <span data-ttu-id="01755-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01755-128">-DefaultProfile</span></span>
<span data-ttu-id="01755-129">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="01755-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01755-130">-InitialRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="01755-130">-InitialRetryIntervalSeconds</span></span>
<span data-ttu-id="01755-131">A kezdeti újrapróbálkozási időköz másodperc</span><span class="sxs-lookup"><span data-stu-id="01755-131">The initial retry interval seconds</span></span>

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

### <span data-ttu-id="01755-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="01755-132">-InputObject</span></span>
<span data-ttu-id="01755-133">A feladat lépésobjektuma</span><span class="sxs-lookup"><span data-stu-id="01755-133">The job step object</span></span>

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

### <span data-ttu-id="01755-134">-JobName</span><span class="sxs-lookup"><span data-stu-id="01755-134">-JobName</span></span>
<span data-ttu-id="01755-135">A feladat neve</span><span class="sxs-lookup"><span data-stu-id="01755-135">The job name</span></span>

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

### <span data-ttu-id="01755-136">-MaximumRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="01755-136">-MaximumRetryIntervalSeconds</span></span>
<span data-ttu-id="01755-137">A maximális újrapróbálkozási időköz másodperc</span><span class="sxs-lookup"><span data-stu-id="01755-137">The maximum retry interval seconds</span></span>

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

### <span data-ttu-id="01755-138">-Name</span><span class="sxs-lookup"><span data-stu-id="01755-138">-Name</span></span>
<span data-ttu-id="01755-139">A lépés neve</span><span class="sxs-lookup"><span data-stu-id="01755-139">The step name</span></span>

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

### <span data-ttu-id="01755-140">-OutputCredentialName</span><span class="sxs-lookup"><span data-stu-id="01755-140">-OutputCredentialName</span></span>
<span data-ttu-id="01755-141">A kimeneti hitelesítő adatok neve</span><span class="sxs-lookup"><span data-stu-id="01755-141">The output credential name</span></span>

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

### <span data-ttu-id="01755-142">-OutputDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="01755-142">-OutputDatabaseObject</span></span>
<span data-ttu-id="01755-143">A kimeneti adatbázis-objektum</span><span class="sxs-lookup"><span data-stu-id="01755-143">The output database object</span></span>

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

### <span data-ttu-id="01755-144">-OutputDatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="01755-144">-OutputDatabaseResourceId</span></span>
<span data-ttu-id="01755-145">A kimeneti adatbázis erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="01755-145">The output database resource id</span></span>

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

### <span data-ttu-id="01755-146">-OutputSchemaName</span><span class="sxs-lookup"><span data-stu-id="01755-146">-OutputSchemaName</span></span>
<span data-ttu-id="01755-147">A kimeneti séma neve</span><span class="sxs-lookup"><span data-stu-id="01755-147">The output schema name</span></span>

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

### <span data-ttu-id="01755-148">-OutputTableName</span><span class="sxs-lookup"><span data-stu-id="01755-148">-OutputTableName</span></span>
<span data-ttu-id="01755-149">A kimeneti tábla neve</span><span class="sxs-lookup"><span data-stu-id="01755-149">The output table name</span></span>

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

### <span data-ttu-id="01755-150">-RemoveOutput</span><span class="sxs-lookup"><span data-stu-id="01755-150">-RemoveOutput</span></span>
<span data-ttu-id="01755-151">A kimenet eltávolítását jelző jelölő</span><span class="sxs-lookup"><span data-stu-id="01755-151">The flag to indicate whether to remove output</span></span>

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

### <span data-ttu-id="01755-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01755-152">-ResourceGroupName</span></span>
<span data-ttu-id="01755-153">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="01755-153">The resource group name</span></span>

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

### <span data-ttu-id="01755-154">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="01755-154">-ResourceId</span></span>
<span data-ttu-id="01755-155">A feladatlépés erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="01755-155">The job step resource id</span></span>

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

### <span data-ttu-id="01755-156">-RetryAttempts</span><span class="sxs-lookup"><span data-stu-id="01755-156">-RetryAttempts</span></span>
<span data-ttu-id="01755-157">The retry attemps</span><span class="sxs-lookup"><span data-stu-id="01755-157">The retry attemps</span></span>

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

### <span data-ttu-id="01755-158">-RetryIntervalBackoffMultiplier</span><span class="sxs-lookup"><span data-stu-id="01755-158">-RetryIntervalBackoffMultiplier</span></span>
<span data-ttu-id="01755-159">The retry interval backoff multiplier</span><span class="sxs-lookup"><span data-stu-id="01755-159">The retry interval backoff multiplier</span></span>

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

### <span data-ttu-id="01755-160">-ServerName</span><span class="sxs-lookup"><span data-stu-id="01755-160">-ServerName</span></span>
<span data-ttu-id="01755-161">A kiszolgáló neve</span><span class="sxs-lookup"><span data-stu-id="01755-161">The server name</span></span>

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

### <span data-ttu-id="01755-162">-StepId</span><span class="sxs-lookup"><span data-stu-id="01755-162">-StepId</span></span>
<span data-ttu-id="01755-163">A lépésazonosító szövege</span><span class="sxs-lookup"><span data-stu-id="01755-163">The step id text</span></span>

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

### <span data-ttu-id="01755-164">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="01755-164">-TargetGroupName</span></span>
<span data-ttu-id="01755-165">A célcsoport neve</span><span class="sxs-lookup"><span data-stu-id="01755-165">The target group name</span></span>

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

### <span data-ttu-id="01755-166">-TimeoutSeconds</span><span class="sxs-lookup"><span data-stu-id="01755-166">-TimeoutSeconds</span></span>
<span data-ttu-id="01755-167">Az időkorlát másodpercben</span><span class="sxs-lookup"><span data-stu-id="01755-167">The timeout seconds</span></span>

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

### <span data-ttu-id="01755-168">-Confirm</span><span class="sxs-lookup"><span data-stu-id="01755-168">-Confirm</span></span>
<span data-ttu-id="01755-169">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="01755-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01755-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01755-170">-WhatIf</span></span>
<span data-ttu-id="01755-171">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="01755-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01755-172">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="01755-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01755-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01755-173">CommonParameters</span></span>
<span data-ttu-id="01755-174">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01755-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01755-175">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="01755-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01755-176">INPUTS</span><span class="sxs-lookup"><span data-stu-id="01755-176">INPUTS</span></span>

### <span data-ttu-id="01755-177">Microsoft.Azure.Commands.Sql.ElasticMods.Model.AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="01755-177">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="01755-178">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="01755-178">OUTPUTS</span></span>

### <span data-ttu-id="01755-179">Microsoft.Azure.Commands.Sql.ElasticMods.Model.AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="01755-179">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="01755-180">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="01755-180">NOTES</span></span>

## <span data-ttu-id="01755-181">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="01755-181">RELATED LINKS</span></span>
