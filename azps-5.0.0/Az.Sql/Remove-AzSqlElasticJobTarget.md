---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobtarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobTarget.md
ms.openlocfilehash: 4bd797528b3656364594f28f72d2b9ce2f7fdfaa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194182"
---
# <span data-ttu-id="86e22-101">Remove-AzSqlElasticJobTarget</span><span class="sxs-lookup"><span data-stu-id="86e22-101">Remove-AzSqlElasticJobTarget</span></span>

## <span data-ttu-id="86e22-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="86e22-102">SYNOPSIS</span></span>
<span data-ttu-id="86e22-103">A cél eltávolítása a cél csoportból</span><span class="sxs-lookup"><span data-stu-id="86e22-103">Removes the target from the target group</span></span>

## <span data-ttu-id="86e22-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="86e22-104">SYNTAX</span></span>

### <span data-ttu-id="86e22-105">SqlDatabase (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="86e22-105">SqlDatabase (Default)</span></span>
```
Remove-AzSqlElasticJobTarget [-ResourceGroupName] <String> [-AgentServerName] <String> [-AgentName] <String>
 [-TargetGroupName] <String> -ServerName <String> -DatabaseName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86e22-106">SqlServerOrElasticPool</span><span class="sxs-lookup"><span data-stu-id="86e22-106">SqlServerOrElasticPool</span></span>
```
Remove-AzSqlElasticJobTarget [-ResourceGroupName] <String> [-AgentServerName] <String> [-AgentName] <String>
 [-TargetGroupName] <String> -ServerName <String> [-ElasticPoolName <String>] -RefreshCredentialName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86e22-107">SqlShardMap</span><span class="sxs-lookup"><span data-stu-id="86e22-107">SqlShardMap</span></span>
```
Remove-AzSqlElasticJobTarget [-ResourceGroupName] <String> [-AgentServerName] <String> [-AgentName] <String>
 [-TargetGroupName] <String> -ServerName <String> -ShardMapName <String> -DatabaseName <String>
 -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="86e22-108">SqlDatabaseUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="86e22-108">SqlDatabaseUsingParentObject</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 -DatabaseName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86e22-109">SqlServerOrElasticPoolUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="86e22-109">SqlServerOrElasticPoolUsingParentObject</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 [-ElasticPoolName <String>] -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86e22-110">SqlShardMapUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="86e22-110">SqlShardMapUsingParentObject</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 -ShardMapName <String> -DatabaseName <String> -RefreshCredentialName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86e22-111">SqlDatabaseUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="86e22-111">SqlDatabaseUsingParentResourceId</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentResourceId] <String> -ServerName <String> -DatabaseName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86e22-112">SqlServerOrElasticPoolUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="86e22-112">SqlServerOrElasticPoolUsingParentResourceId</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentResourceId] <String> -ServerName <String> [-ElasticPoolName <String>]
 -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="86e22-113">SqlShardMapUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="86e22-113">SqlShardMapUsingParentResourceId</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentResourceId] <String> -ServerName <String> -ShardMapName <String>
 -DatabaseName <String> -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86e22-114">Leírás</span><span class="sxs-lookup"><span data-stu-id="86e22-114">DESCRIPTION</span></span>
<span data-ttu-id="86e22-115">A Remove-AzSqlElasticJobTarget parancsmag eltávolítja a cél erőforrást egy célcsoportra</span><span class="sxs-lookup"><span data-stu-id="86e22-115">The Remove-AzSqlElasticJobTarget cmdlet removes a target resource to a target group</span></span>

## <span data-ttu-id="86e22-116">Példák</span><span class="sxs-lookup"><span data-stu-id="86e22-116">EXAMPLES</span></span>

### <span data-ttu-id="86e22-117">1. példa: kiszolgálói cél eltávolítása</span><span class="sxs-lookup"><span data-stu-id="86e22-117">Example 1: Remove a server target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Remove-AzSqlElasticJobTarget -ServerName s1 -RefreshCredentialName cred1

TargetGroupName TargetType TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ---------- ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlServer  s1                                                                           cred1                 Include
```

### <span data-ttu-id="86e22-118">2. példa: adatbázis-tároló eltávolítása</span><span class="sxs-lookup"><span data-stu-id="86e22-118">Example 2: Remove a database target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Remove-AzSqlElasticJobTarget -ServerName s1 -DatabaseName db2

TargetGroupName TargetType  TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------  ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlDatabase s1               db2                                                                               Include
```

### <span data-ttu-id="86e22-119">3. példa: rugalmas Pool-cél eltávolítása</span><span class="sxs-lookup"><span data-stu-id="86e22-119">Example 3: Remove an elastic pool target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Remove-AzSqlElasticJobTarget -ServerName s1 -ElasticPoolName ep1 -RefreshCredentialName cred1

TargetGroupName TargetType     TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------     ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlElasticPool s1                                  ep1                                      cred1                 Include
```

### <span data-ttu-id="86e22-120">4. példa: a Szilánk-Térkép cél eltávolítása</span><span class="sxs-lookup"><span data-stu-id="86e22-120">Example 4: Remove a shard map target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Remove-AzSqlElasticJobTarget -ServerName s1 -ShardMapName sm1 -DatabaseName db1 -RefreshCredentialName cred1

TargetGroupName TargetType  TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------  ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlShardMap s1               db1                                      sm1                cred1                 Include
```

<span data-ttu-id="86e22-121">Cél (kiszolgáló, rugalmas készlet, adatbázis és szilánk-Térkép) eltávolítása a csoportból</span><span class="sxs-lookup"><span data-stu-id="86e22-121">Removes a target (server, elastic pool, database, and shard map) from a target group</span></span>

## <span data-ttu-id="86e22-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="86e22-122">PARAMETERS</span></span>

### <span data-ttu-id="86e22-123">-AgentName</span><span class="sxs-lookup"><span data-stu-id="86e22-123">-AgentName</span></span>
<span data-ttu-id="86e22-124">SQL-adatbázis ügynök neve</span><span class="sxs-lookup"><span data-stu-id="86e22-124">SQL Database Agent Name.</span></span>

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

### <span data-ttu-id="86e22-125">-AgentServerName</span><span class="sxs-lookup"><span data-stu-id="86e22-125">-AgentServerName</span></span>
<span data-ttu-id="86e22-126">SQL-adatbázis ügynök kiszolgálójának neve</span><span class="sxs-lookup"><span data-stu-id="86e22-126">SQL Database Agent Server Name.</span></span>

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

### <span data-ttu-id="86e22-127">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="86e22-127">-DatabaseName</span></span>
<span data-ttu-id="86e22-128">Adatbázis-cél neve</span><span class="sxs-lookup"><span data-stu-id="86e22-128">Database Target Name</span></span>

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

### <span data-ttu-id="86e22-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86e22-129">-DefaultProfile</span></span>
<span data-ttu-id="86e22-130">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="86e22-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="86e22-131">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="86e22-131">-ElasticPoolName</span></span>
<span data-ttu-id="86e22-132">Rugalmas Pool cél neve</span><span class="sxs-lookup"><span data-stu-id="86e22-132">Elastic Pool Target Name</span></span>

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

### <span data-ttu-id="86e22-133">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="86e22-133">-ParentObject</span></span>
<span data-ttu-id="86e22-134">A cél csoport objektum.</span><span class="sxs-lookup"><span data-stu-id="86e22-134">The target group object.</span></span>

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

### <span data-ttu-id="86e22-135">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="86e22-135">-ParentResourceId</span></span>
<span data-ttu-id="86e22-136">A cél csoport erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="86e22-136">The target group resource id.</span></span>

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

### <span data-ttu-id="86e22-137">-RefreshCredentialName</span><span class="sxs-lookup"><span data-stu-id="86e22-137">-RefreshCredentialName</span></span>
<span data-ttu-id="86e22-138">A hitelesítőadat-név frissítése</span><span class="sxs-lookup"><span data-stu-id="86e22-138">Refresh Credential Name</span></span>

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

### <span data-ttu-id="86e22-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86e22-139">-ResourceGroupName</span></span>
<span data-ttu-id="86e22-140">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="86e22-140">Resource Group Name</span></span>

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

### <span data-ttu-id="86e22-141">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="86e22-141">-ServerName</span></span>
<span data-ttu-id="86e22-142">Kiszolgáló cél neve</span><span class="sxs-lookup"><span data-stu-id="86e22-142">Server Target Name</span></span>

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

### <span data-ttu-id="86e22-143">-ShardMapName</span><span class="sxs-lookup"><span data-stu-id="86e22-143">-ShardMapName</span></span>
<span data-ttu-id="86e22-144">A Szilánk-Térkép cél neve</span><span class="sxs-lookup"><span data-stu-id="86e22-144">Shard Map Target Name</span></span>

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

### <span data-ttu-id="86e22-145">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="86e22-145">-TargetGroupName</span></span>
<span data-ttu-id="86e22-146">SQL-adatbázis ügynök neve</span><span class="sxs-lookup"><span data-stu-id="86e22-146">SQL Database Agent Name.</span></span>

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

### <span data-ttu-id="86e22-147">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="86e22-147">-Confirm</span></span>
<span data-ttu-id="86e22-148">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="86e22-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86e22-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86e22-149">-WhatIf</span></span>
<span data-ttu-id="86e22-150">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="86e22-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86e22-151">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="86e22-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86e22-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86e22-152">CommonParameters</span></span>
<span data-ttu-id="86e22-153">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="86e22-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86e22-154">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="86e22-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86e22-155">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="86e22-155">INPUTS</span></span>

### <span data-ttu-id="86e22-156">Microsoft. Azure. Command. SQL. ElasticJobs. Model. AzureSqlElasticJobTargetGroupModel</span><span class="sxs-lookup"><span data-stu-id="86e22-156">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="86e22-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="86e22-157">OUTPUTS</span></span>

### <span data-ttu-id="86e22-158">Microsoft. Azure. Management. SQL. models. JobTarget</span><span class="sxs-lookup"><span data-stu-id="86e22-158">Microsoft.Azure.Management.Sql.Models.JobTarget</span></span>

## <span data-ttu-id="86e22-159">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="86e22-159">NOTES</span></span>

## <span data-ttu-id="86e22-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="86e22-160">RELATED LINKS</span></span>
