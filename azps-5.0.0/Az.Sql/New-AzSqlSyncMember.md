---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncMember.md
ms.openlocfilehash: f7fc860711c5037e6ce6390f9fb7d79ddfa7d6ce
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186650"
---
# <span data-ttu-id="ce1de-101">New-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="ce1de-101">New-AzSqlSyncMember</span></span>

## <span data-ttu-id="ce1de-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ce1de-102">SYNOPSIS</span></span>
<span data-ttu-id="ce1de-103">Azure SQL-adatbázis szinkronizálási tagját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="ce1de-103">Creates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="ce1de-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ce1de-104">SYNTAX</span></span>

### <span data-ttu-id="ce1de-105">AzureSqlDatabase (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ce1de-105">AzureSqlDatabase (Default)</span></span>
```
New-AzSqlSyncMember -Name <String> -MemberDatabaseType <String> -MemberServerName <String>
 -MemberDatabaseName <String> -MemberDatabaseCredential <PSCredential> [-SyncDirection <String>]
 [-UsePrivateLinkConnection] [-SyncMemberAzureDatabaseResourceId <String>] [-SyncGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce1de-106">OnPremisesDatabaseSyncAgentComponent</span><span class="sxs-lookup"><span data-stu-id="ce1de-106">OnPremisesDatabaseSyncAgentComponent</span></span>
```
New-AzSqlSyncMember -Name <String> -MemberDatabaseType <String> -SyncAgentResourceGroupName <String>
 -SyncAgentServerName <String> -SyncAgentName <String> -SqlServerDatabaseId <String> [-SyncDirection <String>]
 [-UsePrivateLinkConnection] [-SyncMemberAzureDatabaseResourceId <String>] [-SyncGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce1de-107">OnPremisesDatabaseSyncAgentResourceID</span><span class="sxs-lookup"><span data-stu-id="ce1de-107">OnPremisesDatabaseSyncAgentResourceID</span></span>
```
New-AzSqlSyncMember -Name <String> -MemberDatabaseType <String> -SqlServerDatabaseId <String>
 -SyncAgentResourceID <String> [-SyncDirection <String>] [-UsePrivateLinkConnection]
 [-SyncMemberAzureDatabaseResourceId <String>] [-SyncGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce1de-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="ce1de-108">DESCRIPTION</span></span>
<span data-ttu-id="ce1de-109">A **New-AzSqlSyncMember** parancsmag egy Azure SQL adatbázis-szinkronizálási tagot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="ce1de-109">The **New-AzSqlSyncMember** cmdlet creates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="ce1de-110">Példák</span><span class="sxs-lookup"><span data-stu-id="ce1de-110">EXAMPLES</span></span>

### <span data-ttu-id="ce1de-111">Példa 1: szinkronizálási tag létrehozása Azure SQL-adatbázishoz.</span><span class="sxs-lookup"><span data-stu-id="ce1de-111">Example 1: Create a sync member for an Azure SQL database.</span></span>
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

<span data-ttu-id="ce1de-112">Ez a parancs létrehoz egy szinkronizálási tagot egy Azure SQL-adatbázishoz.</span><span class="sxs-lookup"><span data-stu-id="ce1de-112">This command creates a sync member for an Azure SQL database.</span></span>

### <span data-ttu-id="ce1de-113">2. példa: szinkronizálási tag létrehozása helyszíni SQL Server-adatbázishoz</span><span class="sxs-lookup"><span data-stu-id="ce1de-113">Example 2: Create a sync member for an on-premises SQL Server database</span></span>
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

<span data-ttu-id="ce1de-114">A parancs létrehoz egy szinkronizálási tagot egy helyszíni SQL-adatbázishoz.</span><span class="sxs-lookup"><span data-stu-id="ce1de-114">This command creates a sync member for an on-premises SQL database.</span></span>

## <span data-ttu-id="ce1de-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ce1de-115">PARAMETERS</span></span>

### <span data-ttu-id="ce1de-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ce1de-116">-DatabaseName</span></span>
<span data-ttu-id="ce1de-117">Az Azure SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="ce1de-117">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="ce1de-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce1de-118">-DefaultProfile</span></span>
<span data-ttu-id="ce1de-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ce1de-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ce1de-120">-MemberDatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="ce1de-120">-MemberDatabaseCredential</span></span>
<span data-ttu-id="ce1de-121">Az Azure SQL-adatbázis hitelesítő adatai (Felhasználónév és jelszó).</span><span class="sxs-lookup"><span data-stu-id="ce1de-121">The credential (username and password) of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="ce1de-122">-MemberDatabaseName</span><span class="sxs-lookup"><span data-stu-id="ce1de-122">-MemberDatabaseName</span></span>
<span data-ttu-id="ce1de-123">A tag adatbázis Azure SQL-adatbázisának neve.</span><span class="sxs-lookup"><span data-stu-id="ce1de-123">The Azure SQL Database name of the member database.</span></span>

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

### <span data-ttu-id="ce1de-124">-MemberDatabaseType</span><span class="sxs-lookup"><span data-stu-id="ce1de-124">-MemberDatabaseType</span></span>
<span data-ttu-id="ce1de-125">A tag adatbázisának adatbázis-típusa.</span><span class="sxs-lookup"><span data-stu-id="ce1de-125">The database type of the member database.</span></span>

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

### <span data-ttu-id="ce1de-126">-MemberServerName</span><span class="sxs-lookup"><span data-stu-id="ce1de-126">-MemberServerName</span></span>
<span data-ttu-id="ce1de-127">A tag-adatbázis Azure SQL Server-neve.</span><span class="sxs-lookup"><span data-stu-id="ce1de-127">The Azure SQL Server Name of the member database.</span></span>

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

### <span data-ttu-id="ce1de-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ce1de-128">-Name</span></span>
<span data-ttu-id="ce1de-129">A szinkronizálási tag neve.</span><span class="sxs-lookup"><span data-stu-id="ce1de-129">The sync member name.</span></span>

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

### <span data-ttu-id="ce1de-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce1de-130">-ResourceGroupName</span></span>
<span data-ttu-id="ce1de-131">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ce1de-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="ce1de-132">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="ce1de-132">-ServerName</span></span>
<span data-ttu-id="ce1de-133">Az Azure SQL Server neve.</span><span class="sxs-lookup"><span data-stu-id="ce1de-133">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="ce1de-134">-SqlServerDatabaseId</span><span class="sxs-lookup"><span data-stu-id="ce1de-134">-SqlServerDatabaseId</span></span>
<span data-ttu-id="ce1de-135">A Szinkronizáló ügynök által összekapcsolt SQL Server-adatbázis azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ce1de-135">The id of the SQL server database which is connected by the sync agent.</span></span>

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

### <span data-ttu-id="ce1de-136">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="ce1de-136">-SyncAgentName</span></span>
<span data-ttu-id="ce1de-137">A Szinkronizáló ügynök neve.</span><span class="sxs-lookup"><span data-stu-id="ce1de-137">The name of the sync agent.</span></span>

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

### <span data-ttu-id="ce1de-138">-SyncAgentResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce1de-138">-SyncAgentResourceGroupName</span></span>
<span data-ttu-id="ce1de-139">Annak az erőforráscsoportnek a neve, amelyben a Szinkronizáló ügynök található.</span><span class="sxs-lookup"><span data-stu-id="ce1de-139">The name of the resource group where the sync agent is under.</span></span>

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

### <span data-ttu-id="ce1de-140">-SyncAgentResourceID</span><span class="sxs-lookup"><span data-stu-id="ce1de-140">-SyncAgentResourceID</span></span>
<span data-ttu-id="ce1de-141">A Szinkronizáló ügynök erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ce1de-141">The resource ID of the sync agent.</span></span>

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

### <span data-ttu-id="ce1de-142">-SyncAgentServerName</span><span class="sxs-lookup"><span data-stu-id="ce1de-142">-SyncAgentServerName</span></span>
<span data-ttu-id="ce1de-143">Annak az Azure SQL Server-kiszolgálónak a neve, amelyben a Szinkronizáló ügynök található.</span><span class="sxs-lookup"><span data-stu-id="ce1de-143">The name of the Azure SQL Server where the sync agent is under.</span></span>

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

### <span data-ttu-id="ce1de-144">-SyncDirection</span><span class="sxs-lookup"><span data-stu-id="ce1de-144">-SyncDirection</span></span>
<span data-ttu-id="ce1de-145">Ennek a szinkronizálási tagnak a szinkronizálási iránya.</span><span class="sxs-lookup"><span data-stu-id="ce1de-145">The sync direction of this sync member.</span></span>

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

### <span data-ttu-id="ce1de-146">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="ce1de-146">-SyncGroupName</span></span>
<span data-ttu-id="ce1de-147">A szinkronizálási csoport neve.</span><span class="sxs-lookup"><span data-stu-id="ce1de-147">The sync group name.</span></span>

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

### <span data-ttu-id="ce1de-148">-SyncMemberAzureDatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="ce1de-148">-SyncMemberAzureDatabaseResourceId</span></span>
<span data-ttu-id="ce1de-149">A szinkronizálási tag adatbázisának azonosítója, amelyet akkor kell használni, ha a UsePrivateLinkConnection értéke igaz.</span><span class="sxs-lookup"><span data-stu-id="ce1de-149">The resource ID for the sync member database, used if UsePrivateLinkConnection is set to true.</span></span>

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

### <span data-ttu-id="ce1de-150">-UsePrivateLinkConnection</span><span class="sxs-lookup"><span data-stu-id="ce1de-150">-UsePrivateLinkConnection</span></span>
<span data-ttu-id="ce1de-151">A szinkronizálási tagra való csatlakozáskor használjon privát kapcsolati kapcsolatot.</span><span class="sxs-lookup"><span data-stu-id="ce1de-151">Use a private link connection when connecting to this sync member.</span></span>

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

### <span data-ttu-id="ce1de-152">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ce1de-152">-Confirm</span></span>
<span data-ttu-id="ce1de-153">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ce1de-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce1de-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce1de-154">-WhatIf</span></span>
<span data-ttu-id="ce1de-155">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ce1de-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce1de-156">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ce1de-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce1de-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce1de-157">CommonParameters</span></span>
<span data-ttu-id="ce1de-158">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ce1de-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce1de-159">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ce1de-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce1de-160">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ce1de-160">INPUTS</span></span>

### <span data-ttu-id="ce1de-161">System. String</span><span class="sxs-lookup"><span data-stu-id="ce1de-161">System.String</span></span>

## <span data-ttu-id="ce1de-162">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ce1de-162">OUTPUTS</span></span>

### <span data-ttu-id="ce1de-163">Microsoft. Azure. Command. SQL. DataSync. Model. AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="ce1de-163">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="ce1de-164">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ce1de-164">NOTES</span></span>

## <span data-ttu-id="ce1de-165">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ce1de-165">RELATED LINKS</span></span>

[<span data-ttu-id="ce1de-166">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="ce1de-166">Get-AzSqlSyncMember</span></span>](./Get-AzSqlSyncMember.md)

[<span data-ttu-id="ce1de-167">Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="ce1de-167">Update-AzSqlSyncMember</span></span>](./Update-AzSqlSyncMember.md)

[<span data-ttu-id="ce1de-168">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="ce1de-168">Remove-AzSqlSyncMember</span></span>](./Remove-AzSqlSyncMember.md)

