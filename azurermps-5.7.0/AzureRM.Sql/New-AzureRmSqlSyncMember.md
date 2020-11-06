---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncMember.md
ms.openlocfilehash: d2df78cc4cbf7bea7918653e310193bf013d7495
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498708"
---
# <span data-ttu-id="153ec-101">New-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="153ec-101">New-AzureRmSqlSyncMember</span></span>

## <span data-ttu-id="153ec-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="153ec-102">SYNOPSIS</span></span>
<span data-ttu-id="153ec-103">Azure SQL-adatbázis szinkronizálási tagját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="153ec-103">Creates an Azure SQL Database Sync Member.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="153ec-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="153ec-104">SYNTAX</span></span>

### <span data-ttu-id="153ec-105">AzureSqlDatabase (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="153ec-105">AzureSqlDatabase (Default)</span></span>
```
New-AzureRmSqlSyncMember -Name <String> -MemberDatabaseType <String> -MemberServerName <String>
 -MemberDatabaseName <String> -MemberDatabaseCredential <PSCredential> [-SyncDirection <String>]
 [-SyncGroupName] <String> [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="153ec-106">OnPremisesDatabaseSyncAgentComponent</span><span class="sxs-lookup"><span data-stu-id="153ec-106">OnPremisesDatabaseSyncAgentComponent</span></span>
```
New-AzureRmSqlSyncMember -Name <String> -MemberDatabaseType <String> -SyncAgentResourceGroupName <String>
 -SyncAgentServerName <String> -SyncAgentName <String> -SqlServerDatabaseId <String> [-SyncDirection <String>]
 [-SyncGroupName] <String> [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="153ec-107">OnPremisesDatabaseSyncAgentResourceID</span><span class="sxs-lookup"><span data-stu-id="153ec-107">OnPremisesDatabaseSyncAgentResourceID</span></span>
```
New-AzureRmSqlSyncMember -Name <String> -MemberDatabaseType <String> -SqlServerDatabaseId <String>
 -SyncAgentResourceID <String> [-SyncDirection <String>] [-SyncGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="153ec-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="153ec-108">DESCRIPTION</span></span>
<span data-ttu-id="153ec-109">A **New-AzureRmSqlSyncMember** parancsmag egy Azure SQL adatbázis-szinkronizálási tagot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="153ec-109">The **New-AzureRmSqlSyncMember** cmdlet creates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="153ec-110">Példák</span><span class="sxs-lookup"><span data-stu-id="153ec-110">EXAMPLES</span></span>

### <span data-ttu-id="153ec-111">Példa 1: szinkronizálási tag létrehozása Azure SQL-adatbázishoz.</span><span class="sxs-lookup"><span data-stu-id="153ec-111">Example 1: Create a sync member for an Azure SQL database.</span></span>
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

<span data-ttu-id="153ec-112">Ez a parancs létrehoz egy szinkronizálási tagot egy Azure SQL-adatbázishoz.</span><span class="sxs-lookup"><span data-stu-id="153ec-112">This command creates a sync member for an Azure SQL database.</span></span>

### <span data-ttu-id="153ec-113">2. példa: szinkronizálási tag létrehozása helyszíni SQL Server-adatbázishoz</span><span class="sxs-lookup"><span data-stu-id="153ec-113">Example 2: Create a sync member for an on-premises SQL Server database</span></span>
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

<span data-ttu-id="153ec-114">A parancs létrehoz egy szinkronizálási tagot egy helyszíni SQL-adatbázishoz.</span><span class="sxs-lookup"><span data-stu-id="153ec-114">This command creates a sync member for an on-premises SQL database.</span></span>

## <span data-ttu-id="153ec-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="153ec-115">PARAMETERS</span></span>

### <span data-ttu-id="153ec-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="153ec-116">-DatabaseName</span></span>
<span data-ttu-id="153ec-117">Az Azure SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="153ec-117">The name of the Azure SQL Database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="153ec-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="153ec-118">-DefaultProfile</span></span>
<span data-ttu-id="153ec-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="153ec-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="153ec-120">-MemberDatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="153ec-120">-MemberDatabaseCredential</span></span>
<span data-ttu-id="153ec-121">Az Azure SQL-adatbázis hitelesítő adatai (Felhasználónév és jelszó).</span><span class="sxs-lookup"><span data-stu-id="153ec-121">The credential (username and password) of the Azure SQL Database.</span></span>

```yaml
Type: PSCredential
Parameter Sets: AzureSqlDatabase
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="153ec-122">-MemberDatabaseName</span><span class="sxs-lookup"><span data-stu-id="153ec-122">-MemberDatabaseName</span></span>
<span data-ttu-id="153ec-123">A tag adatbázis Azure SQL-adatbázisának neve.</span><span class="sxs-lookup"><span data-stu-id="153ec-123">The Azure SQL Database name of the member database.</span></span>

```yaml
Type: String
Parameter Sets: AzureSqlDatabase
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="153ec-124">-MemberDatabaseType</span><span class="sxs-lookup"><span data-stu-id="153ec-124">-MemberDatabaseType</span></span>
<span data-ttu-id="153ec-125">A tag adatbázisának adatbázis-típusa.</span><span class="sxs-lookup"><span data-stu-id="153ec-125">The database type of the member database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: SqlServerDatabase, AzureSqlDatabase

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="153ec-126">-MemberServerName</span><span class="sxs-lookup"><span data-stu-id="153ec-126">-MemberServerName</span></span>
<span data-ttu-id="153ec-127">A tag-adatbázis Azure SQL Server-neve.</span><span class="sxs-lookup"><span data-stu-id="153ec-127">The Azure SQL Server Name of the member database.</span></span>

```yaml
Type: String
Parameter Sets: AzureSqlDatabase
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="153ec-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="153ec-128">-Name</span></span>
<span data-ttu-id="153ec-129">A szinkronizálási tag neve.</span><span class="sxs-lookup"><span data-stu-id="153ec-129">The sync member name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SyncMemberName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="153ec-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="153ec-130">-ResourceGroupName</span></span>
<span data-ttu-id="153ec-131">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="153ec-131">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="153ec-132">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="153ec-132">-ServerName</span></span>
<span data-ttu-id="153ec-133">Az Azure SQL Server neve.</span><span class="sxs-lookup"><span data-stu-id="153ec-133">The name of the Azure SQL Server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="153ec-134">-SqlServerDatabaseId</span><span class="sxs-lookup"><span data-stu-id="153ec-134">-SqlServerDatabaseId</span></span>
<span data-ttu-id="153ec-135">A Szinkronizáló ügynök által összekapcsolt SQL Server-adatbázis azonosítója.</span><span class="sxs-lookup"><span data-stu-id="153ec-135">The id of the SQL server database which is connected by the sync agent.</span></span>

```yaml
Type: String
Parameter Sets: OnPremisesDatabaseSyncAgentComponent, OnPremisesDatabaseSyncAgentResourceID
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="153ec-136">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="153ec-136">-SyncAgentName</span></span>
<span data-ttu-id="153ec-137">A Szinkronizáló ügynök neve.</span><span class="sxs-lookup"><span data-stu-id="153ec-137">The name of the sync agent.</span></span>

```yaml
Type: String
Parameter Sets: OnPremisesDatabaseSyncAgentComponent
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="153ec-138">-SyncAgentResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="153ec-138">-SyncAgentResourceGroupName</span></span>
<span data-ttu-id="153ec-139">Annak az erőforráscsoportnek a neve, amelyben a Szinkronizáló ügynök található.</span><span class="sxs-lookup"><span data-stu-id="153ec-139">The name of the resource group where the sync agent is under.</span></span>

```yaml
Type: String
Parameter Sets: OnPremisesDatabaseSyncAgentComponent
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="153ec-140">-SyncAgentResourceID</span><span class="sxs-lookup"><span data-stu-id="153ec-140">-SyncAgentResourceID</span></span>
<span data-ttu-id="153ec-141">A Szinkronizáló ügynök erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="153ec-141">The resource ID of the sync agent.</span></span>

```yaml
Type: String
Parameter Sets: OnPremisesDatabaseSyncAgentResourceID
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="153ec-142">-SyncAgentServerName</span><span class="sxs-lookup"><span data-stu-id="153ec-142">-SyncAgentServerName</span></span>
<span data-ttu-id="153ec-143">Annak az Azure SQL Server-kiszolgálónak a neve, amelyben a Szinkronizáló ügynök található.</span><span class="sxs-lookup"><span data-stu-id="153ec-143">The name of the Azure SQL Server where the sync agent is under.</span></span>

```yaml
Type: String
Parameter Sets: OnPremisesDatabaseSyncAgentComponent
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="153ec-144">-SyncDirection</span><span class="sxs-lookup"><span data-stu-id="153ec-144">-SyncDirection</span></span>
<span data-ttu-id="153ec-145">Ennek a szinkronizálási tagnak a szinkronizálási iránya.</span><span class="sxs-lookup"><span data-stu-id="153ec-145">The sync direction of this sync member.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Bidirectional, OneWayMemberToHub, OneWayHubToMember

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="153ec-146">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="153ec-146">-SyncGroupName</span></span>
<span data-ttu-id="153ec-147">A szinkronizálási csoport neve.</span><span class="sxs-lookup"><span data-stu-id="153ec-147">The sync group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="153ec-148">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="153ec-148">-Confirm</span></span>
<span data-ttu-id="153ec-149">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="153ec-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="153ec-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="153ec-150">-WhatIf</span></span>
<span data-ttu-id="153ec-151">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="153ec-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="153ec-152">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="153ec-152">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="153ec-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="153ec-153">CommonParameters</span></span>
<span data-ttu-id="153ec-154">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="153ec-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="153ec-155">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="153ec-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="153ec-156">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="153ec-156">INPUTS</span></span>

### <span data-ttu-id="153ec-157">Nincs</span><span class="sxs-lookup"><span data-stu-id="153ec-157">None</span></span>
<span data-ttu-id="153ec-158">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="153ec-158">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="153ec-159">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="153ec-159">OUTPUTS</span></span>

### <span data-ttu-id="153ec-160">Microsoft. Azure. Command. SQL. DataSync. Model. AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="153ec-160">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="153ec-161">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="153ec-161">NOTES</span></span>

## <span data-ttu-id="153ec-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="153ec-162">RELATED LINKS</span></span>

[<span data-ttu-id="153ec-163">Get-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="153ec-163">Get-AzureRmSqlSyncMember</span></span>](./Get-AzureRmSqlSyncMember.md)

[<span data-ttu-id="153ec-164">Set-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="153ec-164">Set-AzureRmSqlSyncMember</span></span>](./Set-AzureRmSqlSyncMember.md)

[<span data-ttu-id="153ec-165">Remove-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="153ec-165">Remove-AzureRmSqlSyncMember</span></span>](./Remove-AzureRmSqlSyncMember.md)

