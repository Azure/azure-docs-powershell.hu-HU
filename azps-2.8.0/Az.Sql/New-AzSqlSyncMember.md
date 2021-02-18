---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncMember.md
ms.openlocfilehash: 5846435df4921e425e12e908539849fda0bd2472
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100405737"
---
# <span data-ttu-id="8c87d-101">New-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="8c87d-101">New-AzSqlSyncMember</span></span>

## <span data-ttu-id="8c87d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c87d-102">SYNOPSIS</span></span>
<span data-ttu-id="8c87d-103">Létrehoz egy Azure SQL Database Sync- tagot.</span><span class="sxs-lookup"><span data-stu-id="8c87d-103">Creates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="8c87d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8c87d-104">SYNTAX</span></span>

### <span data-ttu-id="8c87d-105">AzureSqlDatabase (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8c87d-105">AzureSqlDatabase (Default)</span></span>
```
New-AzSqlSyncMember -Name <String> -MemberDatabaseType <String> -MemberServerName <String>
 -MemberDatabaseName <String> -MemberDatabaseCredential <PSCredential> [-SyncDirection <String>]
 [-SyncGroupName] <String> [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c87d-106">OnPremisesDatabaseSyncAgentComponent</span><span class="sxs-lookup"><span data-stu-id="8c87d-106">OnPremisesDatabaseSyncAgentComponent</span></span>
```
New-AzSqlSyncMember -Name <String> -MemberDatabaseType <String> -SyncAgentResourceGroupName <String>
 -SyncAgentServerName <String> -SyncAgentName <String> -SqlServerDatabaseId <String> [-SyncDirection <String>]
 [-SyncGroupName] <String> [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c87d-107">OnPremisesDatabaseSyncAgentResourceID</span><span class="sxs-lookup"><span data-stu-id="8c87d-107">OnPremisesDatabaseSyncAgentResourceID</span></span>
```
New-AzSqlSyncMember -Name <String> -MemberDatabaseType <String> -SqlServerDatabaseId <String>
 -SyncAgentResourceID <String> [-SyncDirection <String>] [-SyncGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c87d-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8c87d-108">DESCRIPTION</span></span>
<span data-ttu-id="8c87d-109">A **New-AzSqlSyncMember** parancsmag létrehoz egy Azure SQL Database Sync- tagot.</span><span class="sxs-lookup"><span data-stu-id="8c87d-109">The **New-AzSqlSyncMember** cmdlet creates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="8c87d-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8c87d-110">EXAMPLES</span></span>

### <span data-ttu-id="8c87d-111">1. példa: Szinkronizálási tag létrehozása Azure SQL-adatbázishoz.</span><span class="sxs-lookup"><span data-stu-id="8c87d-111">Example 1: Create a sync member for an Azure SQL database.</span></span>
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

<span data-ttu-id="8c87d-112">Ez a parancs szinkronizálási adatokat hoz létre egy Azure SQL-adatbázishoz.</span><span class="sxs-lookup"><span data-stu-id="8c87d-112">This command creates a sync member for an Azure SQL database.</span></span>

### <span data-ttu-id="8c87d-113">2. példa: Szinkronizálási tag létrehozása helyszíni SQL Server-adatbázishoz</span><span class="sxs-lookup"><span data-stu-id="8c87d-113">Example 2: Create a sync member for an on-premises SQL Server database</span></span>
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

<span data-ttu-id="8c87d-114">Ez a parancs szinkronizálási adatokat hoz létre egy helyszíni SQL-adatbázishoz.</span><span class="sxs-lookup"><span data-stu-id="8c87d-114">This command creates a sync member for an on-premises SQL database.</span></span>

## <span data-ttu-id="8c87d-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8c87d-115">PARAMETERS</span></span>

### <span data-ttu-id="8c87d-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8c87d-116">-DatabaseName</span></span>
<span data-ttu-id="8c87d-117">Az Azure SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="8c87d-117">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="8c87d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c87d-118">-DefaultProfile</span></span>
<span data-ttu-id="8c87d-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="8c87d-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8c87d-120">-MemberDatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="8c87d-120">-MemberDatabaseCredential</span></span>
<span data-ttu-id="8c87d-121">Az Azure SQL-adatbázis hitelesítő adatai (felhasználóneve és jelszava).</span><span class="sxs-lookup"><span data-stu-id="8c87d-121">The credential (username and password) of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="8c87d-122">-MemberDatabaseName</span><span class="sxs-lookup"><span data-stu-id="8c87d-122">-MemberDatabaseName</span></span>
<span data-ttu-id="8c87d-123">A tagadatbázis Azure SQL-adatbázisának neve.</span><span class="sxs-lookup"><span data-stu-id="8c87d-123">The Azure SQL Database name of the member database.</span></span>

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

### <span data-ttu-id="8c87d-124">-MemberDatabaseType</span><span class="sxs-lookup"><span data-stu-id="8c87d-124">-MemberDatabaseType</span></span>
<span data-ttu-id="8c87d-125">A tagadatbázis adatbázistípusa.</span><span class="sxs-lookup"><span data-stu-id="8c87d-125">The database type of the member database.</span></span>

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

### <span data-ttu-id="8c87d-126">-MemberServerName</span><span class="sxs-lookup"><span data-stu-id="8c87d-126">-MemberServerName</span></span>
<span data-ttu-id="8c87d-127">A tagadatbázis Azure SQL Server-neve.</span><span class="sxs-lookup"><span data-stu-id="8c87d-127">The Azure SQL Server Name of the member database.</span></span>

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

### <span data-ttu-id="8c87d-128">-Name</span><span class="sxs-lookup"><span data-stu-id="8c87d-128">-Name</span></span>
<span data-ttu-id="8c87d-129">A szinkronizálási tag neve.</span><span class="sxs-lookup"><span data-stu-id="8c87d-129">The sync member name.</span></span>

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

### <span data-ttu-id="8c87d-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c87d-130">-ResourceGroupName</span></span>
<span data-ttu-id="8c87d-131">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="8c87d-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="8c87d-132">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8c87d-132">-ServerName</span></span>
<span data-ttu-id="8c87d-133">Az Azure SQL Server neve.</span><span class="sxs-lookup"><span data-stu-id="8c87d-133">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="8c87d-134">-SqlServerDatabaseId</span><span class="sxs-lookup"><span data-stu-id="8c87d-134">-SqlServerDatabaseId</span></span>
<span data-ttu-id="8c87d-135">A szinkronizálási ügynök által csatlakoztatott SQL Server-adatbázis azonosítója.</span><span class="sxs-lookup"><span data-stu-id="8c87d-135">The id of the SQL server database which is connected by the sync agent.</span></span>

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

### <span data-ttu-id="8c87d-136">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="8c87d-136">-SyncAgentName</span></span>
<span data-ttu-id="8c87d-137">A szinkronizálási ügynök neve.</span><span class="sxs-lookup"><span data-stu-id="8c87d-137">The name of the sync agent.</span></span>

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

### <span data-ttu-id="8c87d-138">-SyncAgentResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c87d-138">-SyncAgentResourceGroupName</span></span>
<span data-ttu-id="8c87d-139">Annak az erőforráscsoportnak a neve, amely alatt a szinkronizálási ügynök van.</span><span class="sxs-lookup"><span data-stu-id="8c87d-139">The name of the resource group where the sync agent is under.</span></span>

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

### <span data-ttu-id="8c87d-140">-SyncAgentResourceID</span><span class="sxs-lookup"><span data-stu-id="8c87d-140">-SyncAgentResourceID</span></span>
<span data-ttu-id="8c87d-141">A szinkronizálási ügynök erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="8c87d-141">The resource ID of the sync agent.</span></span>

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

### <span data-ttu-id="8c87d-142">-SyncAgentServerName</span><span class="sxs-lookup"><span data-stu-id="8c87d-142">-SyncAgentServerName</span></span>
<span data-ttu-id="8c87d-143">Annak az Azure SQL Servernek a neve, ahol a szinkronizálási ügynök található.</span><span class="sxs-lookup"><span data-stu-id="8c87d-143">The name of the Azure SQL Server where the sync agent is under.</span></span>

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

### <span data-ttu-id="8c87d-144">-SyncDirection</span><span class="sxs-lookup"><span data-stu-id="8c87d-144">-SyncDirection</span></span>
<span data-ttu-id="8c87d-145">A szinkronizálási tag szinkronizálási iránya.</span><span class="sxs-lookup"><span data-stu-id="8c87d-145">The sync direction of this sync member.</span></span>

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

### <span data-ttu-id="8c87d-146">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="8c87d-146">-SyncGroupName</span></span>
<span data-ttu-id="8c87d-147">A szinkronizálási csoport neve.</span><span class="sxs-lookup"><span data-stu-id="8c87d-147">The sync group name.</span></span>

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

### <span data-ttu-id="8c87d-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8c87d-148">-Confirm</span></span>
<span data-ttu-id="8c87d-149">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8c87d-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c87d-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c87d-150">-WhatIf</span></span>
<span data-ttu-id="8c87d-151">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8c87d-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c87d-152">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8c87d-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c87d-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c87d-153">CommonParameters</span></span>
<span data-ttu-id="8c87d-154">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c87d-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c87d-155">További információt a [about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8c87d-155">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c87d-156">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8c87d-156">INPUTS</span></span>

### <span data-ttu-id="8c87d-157">System.String</span><span class="sxs-lookup"><span data-stu-id="8c87d-157">System.String</span></span>

## <span data-ttu-id="8c87d-158">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8c87d-158">OUTPUTS</span></span>

### <span data-ttu-id="8c87d-159">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="8c87d-159">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="8c87d-160">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8c87d-160">NOTES</span></span>

## <span data-ttu-id="8c87d-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8c87d-161">RELATED LINKS</span></span>

[<span data-ttu-id="8c87d-162">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="8c87d-162">Get-AzSqlSyncMember</span></span>](./Get-AzSqlSyncMember.md)


[<span data-ttu-id="8c87d-163">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="8c87d-163">Remove-AzSqlSyncMember</span></span>](./Remove-AzSqlSyncMember.md)

