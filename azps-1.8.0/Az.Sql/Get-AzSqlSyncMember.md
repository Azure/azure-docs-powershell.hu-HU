---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncMember.md
ms.openlocfilehash: 8b0f67aa8e85ce9123b515f12c2e3a7da84f860d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668918"
---
# <span data-ttu-id="fbb0e-101">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="fbb0e-101">Get-AzSqlSyncMember</span></span>

## <span data-ttu-id="fbb0e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fbb0e-102">SYNOPSIS</span></span>
<span data-ttu-id="fbb0e-103">Információt ad az Azure SQL Database Sync tagjairól.</span><span class="sxs-lookup"><span data-stu-id="fbb0e-103">Returns information about Azure SQL Database Sync Members.</span></span>

## <span data-ttu-id="fbb0e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fbb0e-104">SYNTAX</span></span>

```
Get-AzSqlSyncMember [-Name <String>] [-SyncGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fbb0e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fbb0e-105">DESCRIPTION</span></span>
<span data-ttu-id="fbb0e-106">A **Get-AzSqlSyncMember** parancsmag információt ad egy vagy több Azure SQL-adatbázis szinkronizálási tagjairól.</span><span class="sxs-lookup"><span data-stu-id="fbb0e-106">The **Get-AzSqlSyncMember** cmdlet returns information about one or more Azure SQL Database Sync Members.</span></span>
<span data-ttu-id="fbb0e-107">Adja meg a szinkronizálási tagok nevét, ha csak a szinkronizálási tagok adatait szeretné látni.</span><span class="sxs-lookup"><span data-stu-id="fbb0e-107">Specify the name of a sync member to see information for only that sync member.</span></span>

## <span data-ttu-id="fbb0e-108">Példák</span><span class="sxs-lookup"><span data-stu-id="fbb0e-108">EXAMPLES</span></span>

### <span data-ttu-id="fbb0e-109">Példa 1: az Azure SQL szinkronizálási tagok minden előfordulásának beolvasása szinkronizálási csoportba</span><span class="sxs-lookup"><span data-stu-id="fbb0e-109">Example 1: Get all instances of Azure SQL Sync Member assigned to a sync group</span></span>
```
PS C:\> Get-AzSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" | Format-List
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
SyncState                   : Good 

ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}/syncMembers/{SyncMember02}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncMemberName              : SyncMember02
SyncDirection               : OneWayMemberToHub
MemberDatabaseType:         : AzureSqlDatabase
SyncAgentId                 : 
SqlServerDatabaseId         : 
MemberServerName            : memberServer01.full.dns.name
MemberDatabaseName          : memberDatabase01
MemberDatabaseUserName      : myAccount
MemberDatabasePassword      :  
SyncState                   : Good
```

<span data-ttu-id="fbb0e-110">Ez a parancs információt kap a szinkronizálás csoport SyncGroup01 társított összes Azure SQL-adatbázis szinkronizálási tagjáról.</span><span class="sxs-lookup"><span data-stu-id="fbb0e-110">This command gets information about all the Azure SQL Database Sync Member assigned to the sync group SyncGroup01.</span></span>

### <span data-ttu-id="fbb0e-111">2. példa: információk beszerzése Azure SQL-adatbázis szinkronizálási tagjáról</span><span class="sxs-lookup"><span data-stu-id="fbb0e-111">Example 2: Get information about an Azure SQL Database Sync Member</span></span>
```
PS C:\> Get-AzSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember01" | Format-List
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
SyncState                   : Good
```

<span data-ttu-id="fbb0e-112">Ez a parancs információt kap az Azure SQL-adatbázis szinkronizálási tagjáról a "SyncMember01" névvel</span><span class="sxs-lookup"><span data-stu-id="fbb0e-112">This command gets information about the Azure SQL Database Sync Member with name "SyncMember01"</span></span>

### <span data-ttu-id="fbb0e-113">3. példa: a szinkronizálási csoporthoz rendelt Azure SQL Sync-tagok minden előfordulásának beolvasása szűréssel</span><span class="sxs-lookup"><span data-stu-id="fbb0e-113">Example 3: Get all instances of Azure SQL Sync Member assigned to a sync group using filtering</span></span>
```
PS C:\> Get-AzSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember*" | Format-List
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
SyncState                   : Good 

ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}/syncMembers/{SyncMember02}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncMemberName              : SyncMember02
SyncDirection               : OneWayMemberToHub
MemberDatabaseType:         : AzureSqlDatabase
SyncAgentId                 : 
SqlServerDatabaseId         : 
MemberServerName            : memberServer01.full.dns.name
MemberDatabaseName          : memberDatabase01
MemberDatabaseUserName      : myAccount
MemberDatabasePassword      :  
SyncState                   : Good
```

<span data-ttu-id="fbb0e-114">Ez a parancs a "SyncMember" kezdetű Azure SQL adatbázis-szinkronizálási tagokról szóló információkat kap a szinkronizálás csoport SyncGroup01.</span><span class="sxs-lookup"><span data-stu-id="fbb0e-114">This command gets information about all the Azure SQL Database Sync Member assigned to the sync group SyncGroup01 that start with "SyncMember".</span></span>

## <span data-ttu-id="fbb0e-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fbb0e-115">PARAMETERS</span></span>

### <span data-ttu-id="fbb0e-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fbb0e-116">-DatabaseName</span></span>
<span data-ttu-id="fbb0e-117">Az Azure SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="fbb0e-117">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="fbb0e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbb0e-118">-DefaultProfile</span></span>
<span data-ttu-id="fbb0e-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="fbb0e-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fbb0e-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fbb0e-120">-Name</span></span>
<span data-ttu-id="fbb0e-121">A szinkronizálási tag neve.</span><span class="sxs-lookup"><span data-stu-id="fbb0e-121">The sync member name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncMemberName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="fbb0e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbb0e-122">-ResourceGroupName</span></span>
<span data-ttu-id="fbb0e-123">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="fbb0e-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="fbb0e-124">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="fbb0e-124">-ServerName</span></span>
<span data-ttu-id="fbb0e-125">Az Azure SQL Server neve.</span><span class="sxs-lookup"><span data-stu-id="fbb0e-125">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="fbb0e-126">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="fbb0e-126">-SyncGroupName</span></span>
<span data-ttu-id="fbb0e-127">A szinkronizálási csoport neve.</span><span class="sxs-lookup"><span data-stu-id="fbb0e-127">The sync group name.</span></span>

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

### <span data-ttu-id="fbb0e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbb0e-128">CommonParameters</span></span>
<span data-ttu-id="fbb0e-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fbb0e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbb0e-130">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="fbb0e-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbb0e-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fbb0e-131">INPUTS</span></span>

### <span data-ttu-id="fbb0e-132">System. String</span><span class="sxs-lookup"><span data-stu-id="fbb0e-132">System.String</span></span>

## <span data-ttu-id="fbb0e-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fbb0e-133">OUTPUTS</span></span>

### <span data-ttu-id="fbb0e-134">Microsoft. Azure. Command. SQL. DataSync. Model. AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="fbb0e-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="fbb0e-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fbb0e-135">NOTES</span></span>

## <span data-ttu-id="fbb0e-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fbb0e-136">RELATED LINKS</span></span>

[<span data-ttu-id="fbb0e-137">Új – AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="fbb0e-137">New-AzSqlSyncMember</span></span>](./New-AzSqlSyncMember.md)

[<span data-ttu-id="fbb0e-138">Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="fbb0e-138">Update-AzSqlSyncMember</span></span>](./Update-AzSqlSyncMember.md)

[<span data-ttu-id="fbb0e-139">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="fbb0e-139">Remove-AzSqlSyncMember</span></span>](./Remove-AzSqlSyncMember.md)

