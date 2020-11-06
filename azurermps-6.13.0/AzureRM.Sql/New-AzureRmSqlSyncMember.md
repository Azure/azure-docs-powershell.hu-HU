---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncMember.md
ms.openlocfilehash: a779217b67cc73f25223661ae8671b4588a8cd2b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498188"
---
# <span data-ttu-id="22281-101">New-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="22281-101">New-AzureRmSqlSyncMember</span></span>

## <span data-ttu-id="22281-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="22281-102">SYNOPSIS</span></span>
<span data-ttu-id="22281-103">Azure SQL-adatbázis szinkronizálási tagját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="22281-103">Creates an Azure SQL Database Sync Member.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22281-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="22281-104">SYNTAX</span></span>

### <span data-ttu-id="22281-105">AzureSqlDatabase (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="22281-105">AzureSqlDatabase (Default)</span></span>
```
New-AzureRmSqlSyncMember -Name <String> -MemberDatabaseType <String> -MemberServerName <String>
 -MemberDatabaseName <String> -MemberDatabaseCredential <PSCredential> [-SyncDirection <String>]
 [-SyncGroupName] <String> [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22281-106">OnPremisesDatabaseSyncAgentComponent</span><span class="sxs-lookup"><span data-stu-id="22281-106">OnPremisesDatabaseSyncAgentComponent</span></span>
```
New-AzureRmSqlSyncMember -Name <String> -MemberDatabaseType <String> -SyncAgentResourceGroupName <String>
 -SyncAgentServerName <String> -SyncAgentName <String> -SqlServerDatabaseId <String> [-SyncDirection <String>]
 [-SyncGroupName] <String> [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22281-107">OnPremisesDatabaseSyncAgentResourceID</span><span class="sxs-lookup"><span data-stu-id="22281-107">OnPremisesDatabaseSyncAgentResourceID</span></span>
```
New-AzureRmSqlSyncMember -Name <String> -MemberDatabaseType <String> -SqlServerDatabaseId <String>
 -SyncAgentResourceID <String> [-SyncDirection <String>] [-SyncGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22281-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="22281-108">DESCRIPTION</span></span>
<span data-ttu-id="22281-109">A **New-AzureRmSqlSyncMember** parancsmag egy Azure SQL adatbázis-szinkronizálási tagot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="22281-109">The **New-AzureRmSqlSyncMember** cmdlet creates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="22281-110">Példák</span><span class="sxs-lookup"><span data-stu-id="22281-110">EXAMPLES</span></span>

### <span data-ttu-id="22281-111">Példa 1: szinkronizálási tag létrehozása Azure SQL-adatbázishoz.</span><span class="sxs-lookup"><span data-stu-id="22281-111">Example 1: Create a sync member for an Azure SQL database.</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> New-AzureRmSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember01" -SyncDirection "OneWayMemberToHub"
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

<span data-ttu-id="22281-112">Ez a parancs létrehoz egy szinkronizálási tagot egy Azure SQL-adatbázishoz.</span><span class="sxs-lookup"><span data-stu-id="22281-112">This command creates a sync member for an Azure SQL database.</span></span>

### <span data-ttu-id="22281-113">2. példa: szinkronizálási tag létrehozása helyszíni SQL Server-adatbázishoz</span><span class="sxs-lookup"><span data-stu-id="22281-113">Example 2: Create a sync member for an on-premises SQL Server database</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> New-AzureRmSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember01" -SyncDirection "OneWayMemberToHub"
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

<span data-ttu-id="22281-114">A parancs létrehoz egy szinkronizálási tagot egy helyszíni SQL-adatbázishoz.</span><span class="sxs-lookup"><span data-stu-id="22281-114">This command creates a sync member for an on-premises SQL database.</span></span>

## <span data-ttu-id="22281-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="22281-115">PARAMETERS</span></span>

### <span data-ttu-id="22281-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="22281-116">-DatabaseName</span></span>
<span data-ttu-id="22281-117">Az Azure SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="22281-117">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="22281-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22281-118">-DefaultProfile</span></span>
<span data-ttu-id="22281-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="22281-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22281-120">-MemberDatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="22281-120">-MemberDatabaseCredential</span></span>
<span data-ttu-id="22281-121">Az Azure SQL-adatbázis hitelesítő adatai (Felhasználónév és jelszó).</span><span class="sxs-lookup"><span data-stu-id="22281-121">The credential (username and password) of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="22281-122">-MemberDatabaseName</span><span class="sxs-lookup"><span data-stu-id="22281-122">-MemberDatabaseName</span></span>
<span data-ttu-id="22281-123">A tag adatbázis Azure SQL-adatbázisának neve.</span><span class="sxs-lookup"><span data-stu-id="22281-123">The Azure SQL Database name of the member database.</span></span>

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

### <span data-ttu-id="22281-124">-MemberDatabaseType</span><span class="sxs-lookup"><span data-stu-id="22281-124">-MemberDatabaseType</span></span>
<span data-ttu-id="22281-125">A tag adatbázisának adatbázis-típusa.</span><span class="sxs-lookup"><span data-stu-id="22281-125">The database type of the member database.</span></span>

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

### <span data-ttu-id="22281-126">-MemberServerName</span><span class="sxs-lookup"><span data-stu-id="22281-126">-MemberServerName</span></span>
<span data-ttu-id="22281-127">A tag-adatbázis Azure SQL Server-neve.</span><span class="sxs-lookup"><span data-stu-id="22281-127">The Azure SQL Server Name of the member database.</span></span>

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

### <span data-ttu-id="22281-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="22281-128">-Name</span></span>
<span data-ttu-id="22281-129">A szinkronizálási tag neve.</span><span class="sxs-lookup"><span data-stu-id="22281-129">The sync member name.</span></span>

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

### <span data-ttu-id="22281-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22281-130">-ResourceGroupName</span></span>
<span data-ttu-id="22281-131">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="22281-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="22281-132">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="22281-132">-ServerName</span></span>
<span data-ttu-id="22281-133">Az Azure SQL Server neve.</span><span class="sxs-lookup"><span data-stu-id="22281-133">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="22281-134">-SqlServerDatabaseId</span><span class="sxs-lookup"><span data-stu-id="22281-134">-SqlServerDatabaseId</span></span>
<span data-ttu-id="22281-135">A Szinkronizáló ügynök által összekapcsolt SQL Server-adatbázis azonosítója.</span><span class="sxs-lookup"><span data-stu-id="22281-135">The id of the SQL server database which is connected by the sync agent.</span></span>

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

### <span data-ttu-id="22281-136">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="22281-136">-SyncAgentName</span></span>
<span data-ttu-id="22281-137">A Szinkronizáló ügynök neve.</span><span class="sxs-lookup"><span data-stu-id="22281-137">The name of the sync agent.</span></span>

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

### <span data-ttu-id="22281-138">-SyncAgentResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22281-138">-SyncAgentResourceGroupName</span></span>
<span data-ttu-id="22281-139">Annak az erőforráscsoportnek a neve, amelyben a Szinkronizáló ügynök található.</span><span class="sxs-lookup"><span data-stu-id="22281-139">The name of the resource group where the sync agent is under.</span></span>

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

### <span data-ttu-id="22281-140">-SyncAgentResourceID</span><span class="sxs-lookup"><span data-stu-id="22281-140">-SyncAgentResourceID</span></span>
<span data-ttu-id="22281-141">A Szinkronizáló ügynök erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="22281-141">The resource ID of the sync agent.</span></span>

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

### <span data-ttu-id="22281-142">-SyncAgentServerName</span><span class="sxs-lookup"><span data-stu-id="22281-142">-SyncAgentServerName</span></span>
<span data-ttu-id="22281-143">Annak az Azure SQL Server-kiszolgálónak a neve, amelyben a Szinkronizáló ügynök található.</span><span class="sxs-lookup"><span data-stu-id="22281-143">The name of the Azure SQL Server where the sync agent is under.</span></span>

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

### <span data-ttu-id="22281-144">-SyncDirection</span><span class="sxs-lookup"><span data-stu-id="22281-144">-SyncDirection</span></span>
<span data-ttu-id="22281-145">Ennek a szinkronizálási tagnak a szinkronizálási iránya.</span><span class="sxs-lookup"><span data-stu-id="22281-145">The sync direction of this sync member.</span></span>

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

### <span data-ttu-id="22281-146">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="22281-146">-SyncGroupName</span></span>
<span data-ttu-id="22281-147">A szinkronizálási csoport neve.</span><span class="sxs-lookup"><span data-stu-id="22281-147">The sync group name.</span></span>

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

### <span data-ttu-id="22281-148">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="22281-148">-Confirm</span></span>
<span data-ttu-id="22281-149">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="22281-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22281-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22281-150">-WhatIf</span></span>
<span data-ttu-id="22281-151">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="22281-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22281-152">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="22281-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22281-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22281-153">CommonParameters</span></span>
<span data-ttu-id="22281-154">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="22281-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22281-155">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22281-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22281-156">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="22281-156">INPUTS</span></span>

### <span data-ttu-id="22281-157">System. String</span><span class="sxs-lookup"><span data-stu-id="22281-157">System.String</span></span>

## <span data-ttu-id="22281-158">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="22281-158">OUTPUTS</span></span>

### <span data-ttu-id="22281-159">Microsoft. Azure. Command. SQL. DataSync. Model. AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="22281-159">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="22281-160">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="22281-160">NOTES</span></span>

## <span data-ttu-id="22281-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="22281-161">RELATED LINKS</span></span>

[<span data-ttu-id="22281-162">Get-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="22281-162">Get-AzureRmSqlSyncMember</span></span>](./Get-AzureRmSqlSyncMember.md)

[<span data-ttu-id="22281-163">Set-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="22281-163">Set-AzureRmSqlSyncMember</span></span>](./Set-AzureRmSqlSyncMember.md)

[<span data-ttu-id="22281-164">Remove-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="22281-164">Remove-AzureRmSqlSyncMember</span></span>](./Remove-AzureRmSqlSyncMember.md)

