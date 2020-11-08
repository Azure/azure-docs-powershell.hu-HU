---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/add-azsqlelasticjobtarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobTarget.md
ms.openlocfilehash: 6ade592fde11c3bd614f602070fba87b60cdcda3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011271"
---
# <span data-ttu-id="f99eb-101">Add-AzSqlElasticJobTarget</span><span class="sxs-lookup"><span data-stu-id="f99eb-101">Add-AzSqlElasticJobTarget</span></span>

## <span data-ttu-id="f99eb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f99eb-102">SYNOPSIS</span></span>
<span data-ttu-id="f99eb-103">Cél hozzáadása a célcsoporthoz</span><span class="sxs-lookup"><span data-stu-id="f99eb-103">Adds a target to a target group</span></span>

## <span data-ttu-id="f99eb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f99eb-104">SYNTAX</span></span>

### <span data-ttu-id="f99eb-105">SqlDatabase (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f99eb-105">SqlDatabase (Default)</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ResourceGroupName] <String> [-AgentServerName] <String>
 [-AgentName] <String> [-TargetGroupName] <String> -ServerName <String> -DatabaseName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f99eb-106">SqlServerOrElasticPool</span><span class="sxs-lookup"><span data-stu-id="f99eb-106">SqlServerOrElasticPool</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ResourceGroupName] <String> [-AgentServerName] <String>
 [-AgentName] <String> [-TargetGroupName] <String> -ServerName <String> [-ElasticPoolName <String>]
 -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f99eb-107">SqlShardMap</span><span class="sxs-lookup"><span data-stu-id="f99eb-107">SqlShardMap</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ResourceGroupName] <String> [-AgentServerName] <String>
 [-AgentName] <String> [-TargetGroupName] <String> -ServerName <String> -ShardMapName <String>
 -DatabaseName <String> -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f99eb-108">SqlDatabaseUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="f99eb-108">SqlDatabaseUsingParentObject</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 -DatabaseName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f99eb-109">SqlServerOrElasticPoolUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="f99eb-109">SqlServerOrElasticPoolUsingParentObject</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 [-ElasticPoolName <String>] -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f99eb-110">SqlShardMapUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="f99eb-110">SqlShardMapUsingParentObject</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 -ShardMapName <String> -DatabaseName <String> -RefreshCredentialName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f99eb-111">SqlDatabaseUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="f99eb-111">SqlDatabaseUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentResourceId] <String> -ServerName <String> -DatabaseName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f99eb-112">SqlServerOrElasticPoolUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="f99eb-112">SqlServerOrElasticPoolUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentResourceId] <String> -ServerName <String>
 [-ElasticPoolName <String>] -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f99eb-113">SqlShardMapUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="f99eb-113">SqlShardMapUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentResourceId] <String> -ServerName <String> -ShardMapName <String>
 -DatabaseName <String> -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f99eb-114">Leírás</span><span class="sxs-lookup"><span data-stu-id="f99eb-114">DESCRIPTION</span></span>
<span data-ttu-id="f99eb-115">Az Add-AzSqlElasticJobTarget parancsmag a cél erőforrást hozzáadja a célcsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="f99eb-115">The Add-AzSqlElasticJobTarget cmdlet adds a target resource to a target group</span></span>

## <span data-ttu-id="f99eb-116">Példák</span><span class="sxs-lookup"><span data-stu-id="f99eb-116">EXAMPLES</span></span>

### <span data-ttu-id="f99eb-117">Példa 1 – kiszolgálói cél hozzáadása</span><span class="sxs-lookup"><span data-stu-id="f99eb-117">Example 1 - Add a server target</span></span>
```
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Add-AzSqlElasticJobTarget -ServerName s1 -RefreshCredentialName cred1

TargetGroupName TargetType TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ---------- ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlServer  s1                                                                           cred1                 Include
```

### <span data-ttu-id="f99eb-118">Példa 2 – adatbázis-cél hozzáadása</span><span class="sxs-lookup"><span data-stu-id="f99eb-118">Example 2 - Add a database target</span></span>
```
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Add-AzSqlElasticJobTarget -ServerName s1 -DatabaseName db2

TargetGroupName TargetType  TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------  ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlDatabase s1               db2                                                                               Include
```

### <span data-ttu-id="f99eb-119">3 példa – rugalmas Pool-cél hozzáadása</span><span class="sxs-lookup"><span data-stu-id="f99eb-119">Example 3 - Add an elastic pool target</span></span>
```
PS C:\> $tg | Add-AzSqlElasticJobTarget -ServerName s1 -ElasticPoolName ep1 -RefreshCredentialName cred1

TargetGroupName TargetType     TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------     ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlElasticPool s1                                  ep1                                      cred1                 Include
```

### <span data-ttu-id="f99eb-120">Példa 4 – szilánk-térképes cél hozzáadása</span><span class="sxs-lookup"><span data-stu-id="f99eb-120">Example 4 - Add a shard map target</span></span>
```
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Add-AzSqlElasticJobTarget -ServerName s1 -ShardMapName sm1 -DatabaseName db1 -RefreshCredentialName cred1

TargetGroupName TargetType  TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------  ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlShardMap s1               db1                                      sm1                cred1                 Include
```

<span data-ttu-id="f99eb-121">Cél (kiszolgáló, rugalmas készlet, adatbázis és szilánk-Térkép) hozzáadása a célcsoporthoz</span><span class="sxs-lookup"><span data-stu-id="f99eb-121">Adds a target (server, elastic pool, database, and shard map) to a target group</span></span>

## <span data-ttu-id="f99eb-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f99eb-122">PARAMETERS</span></span>

### <span data-ttu-id="f99eb-123">-AgentName</span><span class="sxs-lookup"><span data-stu-id="f99eb-123">-AgentName</span></span>
<span data-ttu-id="f99eb-124">A meghatalmazott neve.</span><span class="sxs-lookup"><span data-stu-id="f99eb-124">The agent name.</span></span>

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

### <span data-ttu-id="f99eb-125">-AgentServerName</span><span class="sxs-lookup"><span data-stu-id="f99eb-125">-AgentServerName</span></span>
<span data-ttu-id="f99eb-126">A kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="f99eb-126">The server name.</span></span>

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

### <span data-ttu-id="f99eb-127">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f99eb-127">-DatabaseName</span></span>
<span data-ttu-id="f99eb-128">Adatbázis-cél neve</span><span class="sxs-lookup"><span data-stu-id="f99eb-128">Database Target Name</span></span>

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

### <span data-ttu-id="f99eb-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f99eb-129">-DefaultProfile</span></span>
<span data-ttu-id="f99eb-130">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f99eb-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f99eb-131">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="f99eb-131">-ElasticPoolName</span></span>
<span data-ttu-id="f99eb-132">Rugalmas Pool cél neve</span><span class="sxs-lookup"><span data-stu-id="f99eb-132">Elastic Pool Target Name</span></span>

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

### <span data-ttu-id="f99eb-133">-Kizár</span><span class="sxs-lookup"><span data-stu-id="f99eb-133">-Exclude</span></span>
<span data-ttu-id="f99eb-134">A cél kihagyása.</span><span class="sxs-lookup"><span data-stu-id="f99eb-134">Excludes a target.</span></span>

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

### <span data-ttu-id="f99eb-135">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f99eb-135">-ParentObject</span></span>
<span data-ttu-id="f99eb-136">A cél csoport objektum.</span><span class="sxs-lookup"><span data-stu-id="f99eb-136">The target group object.</span></span>

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

### <span data-ttu-id="f99eb-137">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="f99eb-137">-ParentResourceId</span></span>
<span data-ttu-id="f99eb-138">A cél csoport erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f99eb-138">The target group resource id.</span></span>

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

### <span data-ttu-id="f99eb-139">-RefreshCredentialName</span><span class="sxs-lookup"><span data-stu-id="f99eb-139">-RefreshCredentialName</span></span>
<span data-ttu-id="f99eb-140">A hitelesítőadat-név frissítése</span><span class="sxs-lookup"><span data-stu-id="f99eb-140">Refresh Credential Name</span></span>

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

### <span data-ttu-id="f99eb-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f99eb-141">-ResourceGroupName</span></span>
<span data-ttu-id="f99eb-142">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="f99eb-142">Resource Group Name</span></span>

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

### <span data-ttu-id="f99eb-143">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="f99eb-143">-ServerName</span></span>
<span data-ttu-id="f99eb-144">Kiszolgáló cél neve</span><span class="sxs-lookup"><span data-stu-id="f99eb-144">Server Target Name</span></span>

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

### <span data-ttu-id="f99eb-145">-ShardMapName</span><span class="sxs-lookup"><span data-stu-id="f99eb-145">-ShardMapName</span></span>
<span data-ttu-id="f99eb-146">A Szilánk-Térkép cél neve</span><span class="sxs-lookup"><span data-stu-id="f99eb-146">Shard Map Target Name</span></span>

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

### <span data-ttu-id="f99eb-147">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="f99eb-147">-TargetGroupName</span></span>
<span data-ttu-id="f99eb-148">A cél csoport neve.</span><span class="sxs-lookup"><span data-stu-id="f99eb-148">The target group name.</span></span>

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

### <span data-ttu-id="f99eb-149">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f99eb-149">-Confirm</span></span>
<span data-ttu-id="f99eb-150">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f99eb-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f99eb-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f99eb-151">-WhatIf</span></span>
<span data-ttu-id="f99eb-152">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f99eb-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f99eb-153">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f99eb-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f99eb-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f99eb-154">CommonParameters</span></span>
<span data-ttu-id="f99eb-155">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f99eb-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f99eb-156">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f99eb-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f99eb-157">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f99eb-157">INPUTS</span></span>

### <span data-ttu-id="f99eb-158">Microsoft. Azure. Command. SQL. ElasticJobs. Model. AzureSqlElasticJobTargetGroupModel</span><span class="sxs-lookup"><span data-stu-id="f99eb-158">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="f99eb-159">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f99eb-159">OUTPUTS</span></span>

### <span data-ttu-id="f99eb-160">Microsoft. Azure. Management. SQL. models. JobTarget</span><span class="sxs-lookup"><span data-stu-id="f99eb-160">Microsoft.Azure.Management.Sql.Models.JobTarget</span></span>

## <span data-ttu-id="f99eb-161">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f99eb-161">NOTES</span></span>

## <span data-ttu-id="f99eb-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f99eb-162">RELATED LINKS</span></span>
