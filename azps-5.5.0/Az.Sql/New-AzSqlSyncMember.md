---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncMember.md
ms.openlocfilehash: f7fc860711c5037e6ce6390f9fb7d79ddfa7d6ce
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100163323"
---
# <span data-ttu-id="29f4f-101">New-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="29f4f-101">New-AzSqlSyncMember</span></span>

## <span data-ttu-id="29f4f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29f4f-102">SYNOPSIS</span></span>
<span data-ttu-id="29f4f-103">Létrehoz egy Azure SQL Database Sync- tagot.</span><span class="sxs-lookup"><span data-stu-id="29f4f-103">Creates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="29f4f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="29f4f-104">SYNTAX</span></span>

### <span data-ttu-id="29f4f-105">AzureSqlDatabase (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="29f4f-105">AzureSqlDatabase (Default)</span></span>
```
New-AzSqlSyncMember -Name <String> -MemberDatabaseType <String> -MemberServerName <String>
 -MemberDatabaseName <String> -MemberDatabaseCredential <PSCredential> [-SyncDirection <String>]
 [-UsePrivateLinkConnection] [-SyncMemberAzureDatabaseResourceId <String>] [-SyncGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29f4f-106">OnPremisesDatabaseSyncAgentComponent</span><span class="sxs-lookup"><span data-stu-id="29f4f-106">OnPremisesDatabaseSyncAgentComponent</span></span>
```
New-AzSqlSyncMember -Name <String> -MemberDatabaseType <String> -SyncAgentResourceGroupName <String>
 -SyncAgentServerName <String> -SyncAgentName <String> -SqlServerDatabaseId <String> [-SyncDirection <String>]
 [-UsePrivateLinkConnection] [-SyncMemberAzureDatabaseResourceId <String>] [-SyncGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29f4f-107">OnPremisesDatabaseSyncAgentResourceID</span><span class="sxs-lookup"><span data-stu-id="29f4f-107">OnPremisesDatabaseSyncAgentResourceID</span></span>
```
New-AzSqlSyncMember -Name <String> -MemberDatabaseType <String> -SqlServerDatabaseId <String>
 -SyncAgentResourceID <String> [-SyncDirection <String>] [-UsePrivateLinkConnection]
 [-SyncMemberAzureDatabaseResourceId <String>] [-SyncGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29f4f-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="29f4f-108">DESCRIPTION</span></span>
<span data-ttu-id="29f4f-109">A **New-AzSqlSyncMember** parancsmag létrehoz egy Azure SQL Database Sync- tagot.</span><span class="sxs-lookup"><span data-stu-id="29f4f-109">The **New-AzSqlSyncMember** cmdlet creates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="29f4f-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="29f4f-110">EXAMPLES</span></span>

### <span data-ttu-id="29f4f-111">1. példa: Szinkronizálási tag létrehozása Azure SQL-adatbázishoz.</span><span class="sxs-lookup"><span data-stu-id="29f4f-111">Example 1: Create a sync member for an Azure SQL database.</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> New-AzSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember01" -SyncDirection "OneWayMemberToHub"
-MemberDatabaseType "AzureSqlDatabase" -MemberServerName "memberServer01.full.dns.name" -MemberDatabaseName "memberDatabase01" -MemberDatabaseCredential $credential | Format-List
ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}/syncMembers/{SyncMember01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncMemberName              : SyncMember01
SyncDirection               : OneWayMemberToHub
MemberDatabaseType:         : AzureSqlDatabase
SyncAgentId                 : 
SqlServerDatabaseId         : 
MemberServerName            : memberServer01.full.dns.name
MemberDatabaseName          : memberDatabase01
MemberDatabaseUserName      : myAccount
MemberDatabasePassword      : 
SyncState                   : UnProvisioned
```

<span data-ttu-id="29f4f-112">Ez a parancs szinkronizálási adatokat hoz létre egy Azure SQL-adatbázishoz.</span><span class="sxs-lookup"><span data-stu-id="29f4f-112">This command creates a sync member for an Azure SQL database.</span></span>

### <span data-ttu-id="29f4f-113">2. példa: Szinkronizálási tag létrehozása helyszíni SQL Server-adatbázishoz</span><span class="sxs-lookup"><span data-stu-id="29f4f-113">Example 2: Create a sync member for an on-premises SQL Server database</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> New-AzSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember01" -SyncDirection "OneWayMemberToHub"
-MemberDatabaseType "SqlServerDatabase" -SqlServerDatabaseId "dbId" -syncAgentResourceGroupName "syncAgentResourceGroupName" -syncAgentServerName "syncAgentServerName" 
-syncAgentDatabaseName "syncAgentDatabaseName" -syncAgentName "agentName" | Format-List
ResourceId                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}/syncMembers/{SyncMember01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncMemberName              : SyncMember01
SyncDirection               : OneWayMemberToHub
MemberDatabaseType:         : AzureSqlDatabase
SyncAgentId                 : /subscriptions/{subscriptionId}/resourceGroups/{syncAgentResourceGroupName}/servers/{syncAgentServerName}/syncAgents/{syncAgentId}
SqlServerDatabaseId         : dbId
MemberServerName            : 
MemberDatabaseName          : 
MemberDatabaseUserName      : myAccount
MemberDatabasePassword      : 
SyncState                   : UnProvisioned
```

<span data-ttu-id="29f4f-114">Ez a parancs szinkronizálási adatokat hoz létre egy helyszíni SQL-adatbázishoz.</span><span class="sxs-lookup"><span data-stu-id="29f4f-114">This command creates a sync member for an on-premises SQL database.</span></span>

## <span data-ttu-id="29f4f-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="29f4f-115">PARAMETERS</span></span>

### <span data-ttu-id="29f4f-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="29f4f-116">-DatabaseName</span></span>
<span data-ttu-id="29f4f-117">Az Azure SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="29f4f-117">The name of the Azure SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29f4f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29f4f-118">-DefaultProfile</span></span>
<span data-ttu-id="29f4f-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="29f4f-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="29f4f-120">-MemberDatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="29f4f-120">-MemberDatabaseCredential</span></span>
<span data-ttu-id="29f4f-121">Az Azure SQL-adatbázis hitelesítő adatai (felhasználóneve és jelszava).</span><span class="sxs-lookup"><span data-stu-id="29f4f-121">The credential (username and password) of the Azure SQL Database.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: AzureSqlDatabase
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29f4f-122">-MemberDatabaseName</span><span class="sxs-lookup"><span data-stu-id="29f4f-122">-MemberDatabaseName</span></span>
<span data-ttu-id="29f4f-123">A tagadatbázis Azure SQL-adatbázisának neve.</span><span class="sxs-lookup"><span data-stu-id="29f4f-123">The Azure SQL Database name of the member database.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureSqlDatabase
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29f4f-124">-MemberDatabaseType</span><span class="sxs-lookup"><span data-stu-id="29f4f-124">-MemberDatabaseType</span></span>
<span data-ttu-id="29f4f-125">A tagadatbázis adatbázistípusa.</span><span class="sxs-lookup"><span data-stu-id="29f4f-125">The database type of the member database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: SqlServerDatabase, AzureSqlDatabase

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29f4f-126">-MemberServerName</span><span class="sxs-lookup"><span data-stu-id="29f4f-126">-MemberServerName</span></span>
<span data-ttu-id="29f4f-127">A tagadatbázis Azure SQL Server-neve.</span><span class="sxs-lookup"><span data-stu-id="29f4f-127">The Azure SQL Server Name of the member database.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureSqlDatabase
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29f4f-128">-Name</span><span class="sxs-lookup"><span data-stu-id="29f4f-128">-Name</span></span>
<span data-ttu-id="29f4f-129">A szinkronizálási tag neve.</span><span class="sxs-lookup"><span data-stu-id="29f4f-129">The sync member name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncMemberName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29f4f-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29f4f-130">-ResourceGroupName</span></span>
<span data-ttu-id="29f4f-131">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="29f4f-131">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29f4f-132">-ServerName</span><span class="sxs-lookup"><span data-stu-id="29f4f-132">-ServerName</span></span>
<span data-ttu-id="29f4f-133">Az Azure SQL Server neve.</span><span class="sxs-lookup"><span data-stu-id="29f4f-133">The name of the Azure SQL Server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29f4f-134">-SqlServerDatabaseId</span><span class="sxs-lookup"><span data-stu-id="29f4f-134">-SqlServerDatabaseId</span></span>
<span data-ttu-id="29f4f-135">A szinkronizálási ügynök által csatlakoztatott SQL Server-adatbázis azonosítója.</span><span class="sxs-lookup"><span data-stu-id="29f4f-135">The id of the SQL server database which is connected by the sync agent.</span></span>

```yaml
Type: System.String
Parameter Sets: OnPremisesDatabaseSyncAgentComponent, OnPremisesDatabaseSyncAgentResourceID
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29f4f-136">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="29f4f-136">-SyncAgentName</span></span>
<span data-ttu-id="29f4f-137">A szinkronizálási ügynök neve.</span><span class="sxs-lookup"><span data-stu-id="29f4f-137">The name of the sync agent.</span></span>

```yaml
Type: System.String
Parameter Sets: OnPremisesDatabaseSyncAgentComponent
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29f4f-138">-SyncAgentResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29f4f-138">-SyncAgentResourceGroupName</span></span>
<span data-ttu-id="29f4f-139">Annak az erőforráscsoportnak a neve, amely alatt a szinkronizálási ügynök van.</span><span class="sxs-lookup"><span data-stu-id="29f4f-139">The name of the resource group where the sync agent is under.</span></span>

```yaml
Type: System.String
Parameter Sets: OnPremisesDatabaseSyncAgentComponent
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29f4f-140">-SyncAgentResourceID</span><span class="sxs-lookup"><span data-stu-id="29f4f-140">-SyncAgentResourceID</span></span>
<span data-ttu-id="29f4f-141">A szinkronizálási ügynök erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="29f4f-141">The resource ID of the sync agent.</span></span>

```yaml
Type: System.String
Parameter Sets: OnPremisesDatabaseSyncAgentResourceID
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29f4f-142">-SyncAgentServerName</span><span class="sxs-lookup"><span data-stu-id="29f4f-142">-SyncAgentServerName</span></span>
<span data-ttu-id="29f4f-143">Annak az Azure SQL Servernek a neve, ahol a szinkronizálási ügynök található.</span><span class="sxs-lookup"><span data-stu-id="29f4f-143">The name of the Azure SQL Server where the sync agent is under.</span></span>

```yaml
Type: System.String
Parameter Sets: OnPremisesDatabaseSyncAgentComponent
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29f4f-144">-SyncDirection</span><span class="sxs-lookup"><span data-stu-id="29f4f-144">-SyncDirection</span></span>
<span data-ttu-id="29f4f-145">A szinkronizálási tag szinkronizálási iránya.</span><span class="sxs-lookup"><span data-stu-id="29f4f-145">The sync direction of this sync member.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Bidirectional, OneWayMemberToHub, OneWayHubToMember

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29f4f-146">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="29f4f-146">-SyncGroupName</span></span>
<span data-ttu-id="29f4f-147">A szinkronizálási csoport neve.</span><span class="sxs-lookup"><span data-stu-id="29f4f-147">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29f4f-148">-SyncMemberAzureDatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="29f4f-148">-SyncMemberAzureDatabaseResourceId</span></span>
<span data-ttu-id="29f4f-149">A szinkronizálási tagadatbázis erőforrás-azonosítója, ha a UsePrivateLinkConnection igazra van állítva.</span><span class="sxs-lookup"><span data-stu-id="29f4f-149">The resource ID for the sync member database, used if UsePrivateLinkConnection is set to true.</span></span>

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

### <span data-ttu-id="29f4f-150">-UsePrivateLinkConnection</span><span class="sxs-lookup"><span data-stu-id="29f4f-150">-UsePrivateLinkConnection</span></span>
<span data-ttu-id="29f4f-151">Ha ehhez a szinkronizálási taghoz csatlakozik, használjon privát hivatkozáskapcsolatot.</span><span class="sxs-lookup"><span data-stu-id="29f4f-151">Use a private link connection when connecting to this sync member.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29f4f-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="29f4f-152">-Confirm</span></span>
<span data-ttu-id="29f4f-153">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="29f4f-153">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29f4f-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29f4f-154">-WhatIf</span></span>
<span data-ttu-id="29f4f-155">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="29f4f-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29f4f-156">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="29f4f-156">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29f4f-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29f4f-157">CommonParameters</span></span>
<span data-ttu-id="29f4f-158">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29f4f-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29f4f-159">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="29f4f-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29f4f-160">INPUTS</span><span class="sxs-lookup"><span data-stu-id="29f4f-160">INPUTS</span></span>

### <span data-ttu-id="29f4f-161">System.String</span><span class="sxs-lookup"><span data-stu-id="29f4f-161">System.String</span></span>

## <span data-ttu-id="29f4f-162">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="29f4f-162">OUTPUTS</span></span>

### <span data-ttu-id="29f4f-163">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="29f4f-163">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="29f4f-164">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="29f4f-164">NOTES</span></span>

## <span data-ttu-id="29f4f-165">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="29f4f-165">RELATED LINKS</span></span>

[<span data-ttu-id="29f4f-166">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="29f4f-166">Get-AzSqlSyncMember</span></span>](./Get-AzSqlSyncMember.md)

[<span data-ttu-id="29f4f-167">Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="29f4f-167">Update-AzSqlSyncMember</span></span>](./Update-AzSqlSyncMember.md)

[<span data-ttu-id="29f4f-168">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="29f4f-168">Remove-AzSqlSyncMember</span></span>](./Remove-AzSqlSyncMember.md)

