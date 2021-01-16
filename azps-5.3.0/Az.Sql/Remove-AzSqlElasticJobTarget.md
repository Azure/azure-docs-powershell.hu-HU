---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobtarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobTarget.md
ms.openlocfilehash: 4bd797528b3656364594f28f72d2b9ce2f7fdfaa
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98374554"
---
# <span data-ttu-id="d779f-101">Remove-AzSqlElasticJobTarget</span><span class="sxs-lookup"><span data-stu-id="d779f-101">Remove-AzSqlElasticJobTarget</span></span>

## <span data-ttu-id="d779f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d779f-102">SYNOPSIS</span></span>
<span data-ttu-id="d779f-103">A cél eltávolítása a célcsoportból</span><span class="sxs-lookup"><span data-stu-id="d779f-103">Removes the target from the target group</span></span>

## <span data-ttu-id="d779f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d779f-104">SYNTAX</span></span>

### <span data-ttu-id="d779f-105">SqlDatabase (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d779f-105">SqlDatabase (Default)</span></span>
```
Remove-AzSqlElasticJobTarget [-ResourceGroupName] <String> [-AgentServerName] <String> [-AgentName] <String>
 [-TargetGroupName] <String> -ServerName <String> -DatabaseName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d779f-106">SqlServerOrElasticPool</span><span class="sxs-lookup"><span data-stu-id="d779f-106">SqlServerOrElasticPool</span></span>
```
Remove-AzSqlElasticJobTarget [-ResourceGroupName] <String> [-AgentServerName] <String> [-AgentName] <String>
 [-TargetGroupName] <String> -ServerName <String> [-ElasticPoolName <String>] -RefreshCredentialName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d779f-107">SqlShardMap</span><span class="sxs-lookup"><span data-stu-id="d779f-107">SqlShardMap</span></span>
```
Remove-AzSqlElasticJobTarget [-ResourceGroupName] <String> [-AgentServerName] <String> [-AgentName] <String>
 [-TargetGroupName] <String> -ServerName <String> -ShardMapName <String> -DatabaseName <String>
 -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d779f-108">SqlDatabaseUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="d779f-108">SqlDatabaseUsingParentObject</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 -DatabaseName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d779f-109">SqlServerOrElasticPoolUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="d779f-109">SqlServerOrElasticPoolUsingParentObject</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 [-ElasticPoolName <String>] -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d779f-110">SqlShardMapUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="d779f-110">SqlShardMapUsingParentObject</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 -ShardMapName <String> -DatabaseName <String> -RefreshCredentialName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d779f-111">SqlDatabaseUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="d779f-111">SqlDatabaseUsingParentResourceId</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentResourceId] <String> -ServerName <String> -DatabaseName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d779f-112">SqlServerOrElasticPoolUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="d779f-112">SqlServerOrElasticPoolUsingParentResourceId</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentResourceId] <String> -ServerName <String> [-ElasticPoolName <String>]
 -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d779f-113">SqlShardMapUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="d779f-113">SqlShardMapUsingParentResourceId</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentResourceId] <String> -ServerName <String> -ShardMapName <String>
 -DatabaseName <String> -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d779f-114">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d779f-114">DESCRIPTION</span></span>
<span data-ttu-id="d779f-115">A Remove-AzSqlElasticJobTarget parancsmag eltávolítja a célerőforrást a célcsoportba</span><span class="sxs-lookup"><span data-stu-id="d779f-115">The Remove-AzSqlElasticJobTarget cmdlet removes a target resource to a target group</span></span>

## <span data-ttu-id="d779f-116">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d779f-116">EXAMPLES</span></span>

### <span data-ttu-id="d779f-117">1. példa: Kiszolgálói cél eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d779f-117">Example 1: Remove a server target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Remove-AzSqlElasticJobTarget -ServerName s1 -RefreshCredentialName cred1

TargetGroupName TargetType TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ---------- ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlServer  s1                                                                           cred1                 Include
```

### <span data-ttu-id="d779f-118">2. példa: Adatbázis-cél eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d779f-118">Example 2: Remove a database target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Remove-AzSqlElasticJobTarget -ServerName s1 -DatabaseName db2

TargetGroupName TargetType  TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------  ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlDatabase s1               db2                                                                               Include
```

### <span data-ttu-id="d779f-119">3. példa: Rugalmas készlet célértékének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d779f-119">Example 3: Remove an elastic pool target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Remove-AzSqlElasticJobTarget -ServerName s1 -ElasticPoolName ep1 -RefreshCredentialName cred1

TargetGroupName TargetType     TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------     ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlElasticPool s1                                  ep1                                      cred1                 Include
```

### <span data-ttu-id="d779f-120">4. példa: A shard térkép célértékének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d779f-120">Example 4: Remove a shard map target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Remove-AzSqlElasticJobTarget -ServerName s1 -ShardMapName sm1 -DatabaseName db1 -RefreshCredentialName cred1

TargetGroupName TargetType  TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------  ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlShardMap s1               db1                                      sm1                cred1                 Include
```

<span data-ttu-id="d779f-121">Cél (kiszolgáló, rugalmas készlet, adatbázis és szilvatérkép) eltávolítása a célcsoportból</span><span class="sxs-lookup"><span data-stu-id="d779f-121">Removes a target (server, elastic pool, database, and shard map) from a target group</span></span>

## <span data-ttu-id="d779f-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d779f-122">PARAMETERS</span></span>

### <span data-ttu-id="d779f-123">-AgentName</span><span class="sxs-lookup"><span data-stu-id="d779f-123">-AgentName</span></span>
<span data-ttu-id="d779f-124">SQL-adatbázis ügynökének neve.</span><span class="sxs-lookup"><span data-stu-id="d779f-124">SQL Database Agent Name.</span></span>

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

### <span data-ttu-id="d779f-125">-AgentServerName</span><span class="sxs-lookup"><span data-stu-id="d779f-125">-AgentServerName</span></span>
<span data-ttu-id="d779f-126">SQL-adatbázis ügynökkiszolgálójának neve.</span><span class="sxs-lookup"><span data-stu-id="d779f-126">SQL Database Agent Server Name.</span></span>

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

### <span data-ttu-id="d779f-127">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d779f-127">-DatabaseName</span></span>
<span data-ttu-id="d779f-128">Adatbázis célneve</span><span class="sxs-lookup"><span data-stu-id="d779f-128">Database Target Name</span></span>

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

### <span data-ttu-id="d779f-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d779f-129">-DefaultProfile</span></span>
<span data-ttu-id="d779f-130">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d779f-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d779f-131">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="d779f-131">-ElasticPoolName</span></span>
<span data-ttu-id="d779f-132">Rugalmas készlet célneve</span><span class="sxs-lookup"><span data-stu-id="d779f-132">Elastic Pool Target Name</span></span>

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

### <span data-ttu-id="d779f-133">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d779f-133">-ParentObject</span></span>
<span data-ttu-id="d779f-134">A célcsoport-objektum.</span><span class="sxs-lookup"><span data-stu-id="d779f-134">The target group object.</span></span>

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

### <span data-ttu-id="d779f-135">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="d779f-135">-ParentResourceId</span></span>
<span data-ttu-id="d779f-136">A célcsoport erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d779f-136">The target group resource id.</span></span>

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

### <span data-ttu-id="d779f-137">-RefreshCredentialName</span><span class="sxs-lookup"><span data-stu-id="d779f-137">-RefreshCredentialName</span></span>
<span data-ttu-id="d779f-138">A hitelesítő adatok nevének frissítése</span><span class="sxs-lookup"><span data-stu-id="d779f-138">Refresh Credential Name</span></span>

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

### <span data-ttu-id="d779f-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d779f-139">-ResourceGroupName</span></span>
<span data-ttu-id="d779f-140">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="d779f-140">Resource Group Name</span></span>

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

### <span data-ttu-id="d779f-141">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d779f-141">-ServerName</span></span>
<span data-ttu-id="d779f-142">Kiszolgáló célneve</span><span class="sxs-lookup"><span data-stu-id="d779f-142">Server Target Name</span></span>

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

### <span data-ttu-id="d779f-143">-ShardMapName</span><span class="sxs-lookup"><span data-stu-id="d779f-143">-ShardMapName</span></span>
<span data-ttu-id="d779f-144">Shard Map Target Name</span><span class="sxs-lookup"><span data-stu-id="d779f-144">Shard Map Target Name</span></span>

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

### <span data-ttu-id="d779f-145">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="d779f-145">-TargetGroupName</span></span>
<span data-ttu-id="d779f-146">SQL-adatbázis ügynökének neve.</span><span class="sxs-lookup"><span data-stu-id="d779f-146">SQL Database Agent Name.</span></span>

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

### <span data-ttu-id="d779f-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d779f-147">-Confirm</span></span>
<span data-ttu-id="d779f-148">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d779f-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d779f-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d779f-149">-WhatIf</span></span>
<span data-ttu-id="d779f-150">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d779f-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d779f-151">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d779f-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d779f-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d779f-152">CommonParameters</span></span>
<span data-ttu-id="d779f-153">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d779f-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d779f-154">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d779f-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d779f-155">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d779f-155">INPUTS</span></span>

### <span data-ttu-id="d779f-156">Microsoft.Azure.Commands.Sql.ElasticMods.Model.AzureSqlElasticAsticTargetGroupModel</span><span class="sxs-lookup"><span data-stu-id="d779f-156">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="d779f-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d779f-157">OUTPUTS</span></span>

### <span data-ttu-id="d779f-158">Microsoft.Azure.Management.Sql.Models.JobTarget</span><span class="sxs-lookup"><span data-stu-id="d779f-158">Microsoft.Azure.Management.Sql.Models.JobTarget</span></span>

## <span data-ttu-id="d779f-159">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d779f-159">NOTES</span></span>

## <span data-ttu-id="d779f-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d779f-160">RELATED LINKS</span></span>
