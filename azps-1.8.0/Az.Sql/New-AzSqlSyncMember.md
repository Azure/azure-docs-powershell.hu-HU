---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncMember.md
ms.openlocfilehash: 503f7be9d4d7f595ac8d337568038d7e7e724d1f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668865"
---
# <span data-ttu-id="877e9-101">New-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="877e9-101">New-AzSqlSyncMember</span></span>

## <span data-ttu-id="877e9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="877e9-102">SYNOPSIS</span></span>
<span data-ttu-id="877e9-103">Azure SQL-adatbázis szinkronizálási tagját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="877e9-103">Creates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="877e9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="877e9-104">SYNTAX</span></span>

### <span data-ttu-id="877e9-105">AzureSqlDatabase (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="877e9-105">AzureSqlDatabase (Default)</span></span>
```
New-AzSqlSyncMember -Name <String> -MemberDatabaseType <String> -MemberServerName <String>
 -MemberDatabaseName <String> -MemberDatabaseCredential <PSCredential> [-SyncDirection <String>]
 [-SyncGroupName] <String> [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="877e9-106">OnPremisesDatabaseSyncAgentComponent</span><span class="sxs-lookup"><span data-stu-id="877e9-106">OnPremisesDatabaseSyncAgentComponent</span></span>
```
New-AzSqlSyncMember -Name <String> -MemberDatabaseType <String> -SyncAgentResourceGroupName <String>
 -SyncAgentServerName <String> -SyncAgentName <String> -SqlServerDatabaseId <String> [-SyncDirection <String>]
 [-SyncGroupName] <String> [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="877e9-107">OnPremisesDatabaseSyncAgentResourceID</span><span class="sxs-lookup"><span data-stu-id="877e9-107">OnPremisesDatabaseSyncAgentResourceID</span></span>
```
New-AzSqlSyncMember -Name <String> -MemberDatabaseType <String> -SqlServerDatabaseId <String>
 -SyncAgentResourceID <String> [-SyncDirection <String>] [-SyncGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="877e9-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="877e9-108">DESCRIPTION</span></span>
<span data-ttu-id="877e9-109">A **New-AzSqlSyncMember** parancsmag egy Azure SQL adatbázis-szinkronizálási tagot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="877e9-109">The **New-AzSqlSyncMember** cmdlet creates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="877e9-110">Példák</span><span class="sxs-lookup"><span data-stu-id="877e9-110">EXAMPLES</span></span>

### <span data-ttu-id="877e9-111">Példa 1: szinkronizálási tag létrehozása Azure SQL-adatbázishoz.</span><span class="sxs-lookup"><span data-stu-id="877e9-111">Example 1: Create a sync member for an Azure SQL database.</span></span>
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

<span data-ttu-id="877e9-112">Ez a parancs létrehoz egy szinkronizálási tagot egy Azure SQL-adatbázishoz.</span><span class="sxs-lookup"><span data-stu-id="877e9-112">This command creates a sync member for an Azure SQL database.</span></span>

### <span data-ttu-id="877e9-113">2. példa: szinkronizálási tag létrehozása helyszíni SQL Server-adatbázishoz</span><span class="sxs-lookup"><span data-stu-id="877e9-113">Example 2: Create a sync member for an on-premises SQL Server database</span></span>
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

<span data-ttu-id="877e9-114">A parancs létrehoz egy szinkronizálási tagot egy helyszíni SQL-adatbázishoz.</span><span class="sxs-lookup"><span data-stu-id="877e9-114">This command creates a sync member for an on-premises SQL database.</span></span>

## <span data-ttu-id="877e9-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="877e9-115">PARAMETERS</span></span>

### <span data-ttu-id="877e9-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="877e9-116">-DatabaseName</span></span>
<span data-ttu-id="877e9-117">Az Azure SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="877e9-117">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="877e9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="877e9-118">-DefaultProfile</span></span>
<span data-ttu-id="877e9-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="877e9-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="877e9-120">-MemberDatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="877e9-120">-MemberDatabaseCredential</span></span>
<span data-ttu-id="877e9-121">Az Azure SQL-adatbázis hitelesítő adatai (Felhasználónév és jelszó).</span><span class="sxs-lookup"><span data-stu-id="877e9-121">The credential (username and password) of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="877e9-122">-MemberDatabaseName</span><span class="sxs-lookup"><span data-stu-id="877e9-122">-MemberDatabaseName</span></span>
<span data-ttu-id="877e9-123">A tag adatbázis Azure SQL-adatbázisának neve.</span><span class="sxs-lookup"><span data-stu-id="877e9-123">The Azure SQL Database name of the member database.</span></span>

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

### <span data-ttu-id="877e9-124">-MemberDatabaseType</span><span class="sxs-lookup"><span data-stu-id="877e9-124">-MemberDatabaseType</span></span>
<span data-ttu-id="877e9-125">A tag adatbázisának adatbázis-típusa.</span><span class="sxs-lookup"><span data-stu-id="877e9-125">The database type of the member database.</span></span>

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

### <span data-ttu-id="877e9-126">-MemberServerName</span><span class="sxs-lookup"><span data-stu-id="877e9-126">-MemberServerName</span></span>
<span data-ttu-id="877e9-127">A tag-adatbázis Azure SQL Server-neve.</span><span class="sxs-lookup"><span data-stu-id="877e9-127">The Azure SQL Server Name of the member database.</span></span>

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

### <span data-ttu-id="877e9-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="877e9-128">-Name</span></span>
<span data-ttu-id="877e9-129">A szinkronizálási tag neve.</span><span class="sxs-lookup"><span data-stu-id="877e9-129">The sync member name.</span></span>

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

### <span data-ttu-id="877e9-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="877e9-130">-ResourceGroupName</span></span>
<span data-ttu-id="877e9-131">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="877e9-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="877e9-132">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="877e9-132">-ServerName</span></span>
<span data-ttu-id="877e9-133">Az Azure SQL Server neve.</span><span class="sxs-lookup"><span data-stu-id="877e9-133">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="877e9-134">-SqlServerDatabaseId</span><span class="sxs-lookup"><span data-stu-id="877e9-134">-SqlServerDatabaseId</span></span>
<span data-ttu-id="877e9-135">A Szinkronizáló ügynök által összekapcsolt SQL Server-adatbázis azonosítója.</span><span class="sxs-lookup"><span data-stu-id="877e9-135">The id of the SQL server database which is connected by the sync agent.</span></span>

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

### <span data-ttu-id="877e9-136">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="877e9-136">-SyncAgentName</span></span>
<span data-ttu-id="877e9-137">A Szinkronizáló ügynök neve.</span><span class="sxs-lookup"><span data-stu-id="877e9-137">The name of the sync agent.</span></span>

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

### <span data-ttu-id="877e9-138">-SyncAgentResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="877e9-138">-SyncAgentResourceGroupName</span></span>
<span data-ttu-id="877e9-139">Annak az erőforráscsoportnek a neve, amelyben a Szinkronizáló ügynök található.</span><span class="sxs-lookup"><span data-stu-id="877e9-139">The name of the resource group where the sync agent is under.</span></span>

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

### <span data-ttu-id="877e9-140">-SyncAgentResourceID</span><span class="sxs-lookup"><span data-stu-id="877e9-140">-SyncAgentResourceID</span></span>
<span data-ttu-id="877e9-141">A Szinkronizáló ügynök erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="877e9-141">The resource ID of the sync agent.</span></span>

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

### <span data-ttu-id="877e9-142">-SyncAgentServerName</span><span class="sxs-lookup"><span data-stu-id="877e9-142">-SyncAgentServerName</span></span>
<span data-ttu-id="877e9-143">Annak az Azure SQL Server-kiszolgálónak a neve, amelyben a Szinkronizáló ügynök található.</span><span class="sxs-lookup"><span data-stu-id="877e9-143">The name of the Azure SQL Server where the sync agent is under.</span></span>

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

### <span data-ttu-id="877e9-144">-SyncDirection</span><span class="sxs-lookup"><span data-stu-id="877e9-144">-SyncDirection</span></span>
<span data-ttu-id="877e9-145">Ennek a szinkronizálási tagnak a szinkronizálási iránya.</span><span class="sxs-lookup"><span data-stu-id="877e9-145">The sync direction of this sync member.</span></span>

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

### <span data-ttu-id="877e9-146">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="877e9-146">-SyncGroupName</span></span>
<span data-ttu-id="877e9-147">A szinkronizálási csoport neve.</span><span class="sxs-lookup"><span data-stu-id="877e9-147">The sync group name.</span></span>

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

### <span data-ttu-id="877e9-148">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="877e9-148">-Confirm</span></span>
<span data-ttu-id="877e9-149">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="877e9-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="877e9-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="877e9-150">-WhatIf</span></span>
<span data-ttu-id="877e9-151">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="877e9-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="877e9-152">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="877e9-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="877e9-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="877e9-153">CommonParameters</span></span>
<span data-ttu-id="877e9-154">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="877e9-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="877e9-155">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="877e9-155">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="877e9-156">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="877e9-156">INPUTS</span></span>

### <span data-ttu-id="877e9-157">System. String</span><span class="sxs-lookup"><span data-stu-id="877e9-157">System.String</span></span>

## <span data-ttu-id="877e9-158">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="877e9-158">OUTPUTS</span></span>

### <span data-ttu-id="877e9-159">Microsoft. Azure. Command. SQL. DataSync. Model. AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="877e9-159">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="877e9-160">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="877e9-160">NOTES</span></span>

## <span data-ttu-id="877e9-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="877e9-161">RELATED LINKS</span></span>

[<span data-ttu-id="877e9-162">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="877e9-162">Get-AzSqlSyncMember</span></span>](./Get-AzSqlSyncMember.md)

[<span data-ttu-id="877e9-163">Set-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="877e9-163">Set-AzSqlSyncMember</span></span>](./Set-AzSqlSyncMember.md)

[<span data-ttu-id="877e9-164">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="877e9-164">Remove-AzSqlSyncMember</span></span>](./Remove-AzSqlSyncMember.md)

