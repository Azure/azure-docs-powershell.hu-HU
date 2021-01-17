---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/add-azsqlelasticjobtarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobTarget.md
ms.openlocfilehash: cdf50079a08a4ac021e78e210ae574aa978674fe
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98375589"
---
# <span data-ttu-id="30196-101">Add-AzSqlElasticJobTarget</span><span class="sxs-lookup"><span data-stu-id="30196-101">Add-AzSqlElasticJobTarget</span></span>

## <span data-ttu-id="30196-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30196-102">SYNOPSIS</span></span>
<span data-ttu-id="30196-103">Cél hozzáadása egy célcsoporthoz</span><span class="sxs-lookup"><span data-stu-id="30196-103">Adds a target to a target group</span></span>

## <span data-ttu-id="30196-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="30196-104">SYNTAX</span></span>

### <span data-ttu-id="30196-105">SqlDatabase (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="30196-105">SqlDatabase (Default)</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ResourceGroupName] <String> [-AgentServerName] <String>
 [-AgentName] <String> [-TargetGroupName] <String> -ServerName <String> -DatabaseName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30196-106">SqlServerOrElasticPool</span><span class="sxs-lookup"><span data-stu-id="30196-106">SqlServerOrElasticPool</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ResourceGroupName] <String> [-AgentServerName] <String>
 [-AgentName] <String> [-TargetGroupName] <String> -ServerName <String> [-ElasticPoolName <String>]
 -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="30196-107">SqlShardMap</span><span class="sxs-lookup"><span data-stu-id="30196-107">SqlShardMap</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ResourceGroupName] <String> [-AgentServerName] <String>
 [-AgentName] <String> [-TargetGroupName] <String> -ServerName <String> -ShardMapName <String>
 -DatabaseName <String> -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30196-108">SqlDatabaseUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="30196-108">SqlDatabaseUsingParentObject</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 -DatabaseName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30196-109">SqlServerOrElasticPoolUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="30196-109">SqlServerOrElasticPoolUsingParentObject</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 [-ElasticPoolName <String>] -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30196-110">SqlShardMapUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="30196-110">SqlShardMapUsingParentObject</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 -ShardMapName <String> -DatabaseName <String> -RefreshCredentialName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30196-111">SqlDatabaseUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="30196-111">SqlDatabaseUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentResourceId] <String> -ServerName <String> -DatabaseName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30196-112">SqlServerOrElasticPoolUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="30196-112">SqlServerOrElasticPoolUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentResourceId] <String> -ServerName <String>
 [-ElasticPoolName <String>] -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30196-113">SqlShardMapUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="30196-113">SqlShardMapUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentResourceId] <String> -ServerName <String> -ShardMapName <String>
 -DatabaseName <String> -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30196-114">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="30196-114">DESCRIPTION</span></span>
<span data-ttu-id="30196-115">A Add-AzSqlElasticJobTarget parancsmag hozzáad egy célerőforrást egy célcsoporthoz</span><span class="sxs-lookup"><span data-stu-id="30196-115">The Add-AzSqlElasticJobTarget cmdlet adds a target resource to a target group</span></span>

## <span data-ttu-id="30196-116">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="30196-116">EXAMPLES</span></span>

### <span data-ttu-id="30196-117">1. példa: Kiszolgálói cél hozzáadása</span><span class="sxs-lookup"><span data-stu-id="30196-117">Example 1: Add a server target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Add-AzSqlElasticJobTarget -ServerName s1 -RefreshCredentialName cred1

TargetGroupName TargetType TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ---------- ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlServer  s1                                                                           cred1                 Include
```

### <span data-ttu-id="30196-118">2. példa: Adatbázis-cél hozzáadása</span><span class="sxs-lookup"><span data-stu-id="30196-118">Example 2: Add a database target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Add-AzSqlElasticJobTarget -ServerName s1 -DatabaseName db2

TargetGroupName TargetType  TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------  ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlDatabase s1               db2                                                                               Include
```

### <span data-ttu-id="30196-119">3. példa: Rugalmas készletcél hozzáadása</span><span class="sxs-lookup"><span data-stu-id="30196-119">Example 3: Add an elastic pool target</span></span>
```powershell
PS C:\> $tg | Add-AzSqlElasticJobTarget -ServerName s1 -ElasticPoolName ep1 -RefreshCredentialName cred1

TargetGroupName TargetType     TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------     ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlElasticPool s1                                  ep1                                      cred1                 Include
```

### <span data-ttu-id="30196-120">4. példa: Shard térkép célértékének hozzáadása</span><span class="sxs-lookup"><span data-stu-id="30196-120">Example 4: Add a shard map target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Add-AzSqlElasticJobTarget -ServerName s1 -ShardMapName sm1 -DatabaseName db1 -RefreshCredentialName cred1

TargetGroupName TargetType  TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------  ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlShardMap s1               db1                                      sm1                cred1                 Include
```

<span data-ttu-id="30196-121">Cél (kiszolgáló, rugalmas készlet, adatbázis és szilvatérkép) hozzáadása a célcsoporthoz</span><span class="sxs-lookup"><span data-stu-id="30196-121">Adds a target (server, elastic pool, database, and shard map) to a target group</span></span>

## <span data-ttu-id="30196-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="30196-122">PARAMETERS</span></span>

### <span data-ttu-id="30196-123">-AgentName</span><span class="sxs-lookup"><span data-stu-id="30196-123">-AgentName</span></span>
<span data-ttu-id="30196-124">Az ügynök neve.</span><span class="sxs-lookup"><span data-stu-id="30196-124">The agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlDatabase, SqlServerOrElasticPool, SqlShardMap
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30196-125">-AgentServerName</span><span class="sxs-lookup"><span data-stu-id="30196-125">-AgentServerName</span></span>
<span data-ttu-id="30196-126">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="30196-126">The server name.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlDatabase, SqlServerOrElasticPool, SqlShardMap
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30196-127">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="30196-127">-DatabaseName</span></span>
<span data-ttu-id="30196-128">Adatbázis célneve</span><span class="sxs-lookup"><span data-stu-id="30196-128">Database Target Name</span></span>

```yaml
Type: System.String
Parameter Sets: SqlDatabase, SqlShardMap, SqlDatabaseUsingParentObject, SqlShardMapUsingParentObject, SqlDatabaseUsingParentResourceId, SqlShardMapUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30196-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30196-129">-DefaultProfile</span></span>
<span data-ttu-id="30196-130">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="30196-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30196-131">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="30196-131">-ElasticPoolName</span></span>
<span data-ttu-id="30196-132">Rugalmas készlet célneve</span><span class="sxs-lookup"><span data-stu-id="30196-132">Elastic Pool Target Name</span></span>

```yaml
Type: System.String
Parameter Sets: SqlServerOrElasticPool, SqlServerOrElasticPoolUsingParentObject, SqlServerOrElasticPoolUsingParentResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30196-133">-Exclude</span><span class="sxs-lookup"><span data-stu-id="30196-133">-Exclude</span></span>
<span data-ttu-id="30196-134">Egy cél kihagyása.</span><span class="sxs-lookup"><span data-stu-id="30196-134">Excludes a target.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30196-135">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="30196-135">-ParentObject</span></span>
<span data-ttu-id="30196-136">A célcsoport-objektum.</span><span class="sxs-lookup"><span data-stu-id="30196-136">The target group object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel
Parameter Sets: SqlDatabaseUsingParentObject, SqlServerOrElasticPoolUsingParentObject, SqlShardMapUsingParentObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="30196-137">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="30196-137">-ParentResourceId</span></span>
<span data-ttu-id="30196-138">A célcsoport erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="30196-138">The target group resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlDatabaseUsingParentResourceId, SqlServerOrElasticPoolUsingParentResourceId, SqlShardMapUsingParentResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30196-139">-RefreshCredentialName</span><span class="sxs-lookup"><span data-stu-id="30196-139">-RefreshCredentialName</span></span>
<span data-ttu-id="30196-140">A hitelesítő adatok nevének frissítése</span><span class="sxs-lookup"><span data-stu-id="30196-140">Refresh Credential Name</span></span>

```yaml
Type: System.String
Parameter Sets: SqlServerOrElasticPool, SqlShardMap, SqlServerOrElasticPoolUsingParentObject, SqlShardMapUsingParentObject, SqlServerOrElasticPoolUsingParentResourceId, SqlShardMapUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30196-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30196-141">-ResourceGroupName</span></span>
<span data-ttu-id="30196-142">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="30196-142">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SqlDatabase, SqlServerOrElasticPool, SqlShardMap
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30196-143">-ServerName</span><span class="sxs-lookup"><span data-stu-id="30196-143">-ServerName</span></span>
<span data-ttu-id="30196-144">Kiszolgáló célneve</span><span class="sxs-lookup"><span data-stu-id="30196-144">Server Target Name</span></span>

```yaml
Type: System.String
Parameter Sets: SqlDatabase, SqlShardMap, SqlDatabaseUsingParentObject, SqlServerOrElasticPoolUsingParentObject, SqlShardMapUsingParentObject, SqlDatabaseUsingParentResourceId, SqlServerOrElasticPoolUsingParentResourceId, SqlShardMapUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SqlServerOrElasticPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30196-145">-ShardMapName</span><span class="sxs-lookup"><span data-stu-id="30196-145">-ShardMapName</span></span>
<span data-ttu-id="30196-146">Shard Map Target Name</span><span class="sxs-lookup"><span data-stu-id="30196-146">Shard Map Target Name</span></span>

```yaml
Type: System.String
Parameter Sets: SqlShardMap, SqlShardMapUsingParentObject, SqlShardMapUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30196-147">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="30196-147">-TargetGroupName</span></span>
<span data-ttu-id="30196-148">A célcsoport neve.</span><span class="sxs-lookup"><span data-stu-id="30196-148">The target group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlDatabase, SqlServerOrElasticPool, SqlShardMap
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30196-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="30196-149">-Confirm</span></span>
<span data-ttu-id="30196-150">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="30196-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30196-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30196-151">-WhatIf</span></span>
<span data-ttu-id="30196-152">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="30196-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30196-153">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="30196-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30196-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30196-154">CommonParameters</span></span>
<span data-ttu-id="30196-155">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30196-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30196-156">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="30196-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30196-157">INPUTS</span><span class="sxs-lookup"><span data-stu-id="30196-157">INPUTS</span></span>

### <span data-ttu-id="30196-158">Microsoft.Azure.Commands.Sql.ElasticMods.Model.AzureSqlElasticAsticTargetGroupModel</span><span class="sxs-lookup"><span data-stu-id="30196-158">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="30196-159">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="30196-159">OUTPUTS</span></span>

### <span data-ttu-id="30196-160">Microsoft.Azure.Management.Sql.Models.JobTarget</span><span class="sxs-lookup"><span data-stu-id="30196-160">Microsoft.Azure.Management.Sql.Models.JobTarget</span></span>

## <span data-ttu-id="30196-161">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="30196-161">NOTES</span></span>

## <span data-ttu-id="30196-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="30196-162">RELATED LINKS</span></span>
