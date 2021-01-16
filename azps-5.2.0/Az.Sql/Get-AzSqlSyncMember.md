---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncMember.md
ms.openlocfilehash: e5bb853d9dd818801298254eac1f120efcc829a4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98364320"
---
# <span data-ttu-id="ebf1d-101">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="ebf1d-101">Get-AzSqlSyncMember</span></span>

## <span data-ttu-id="ebf1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ebf1d-102">SYNOPSIS</span></span>
<span data-ttu-id="ebf1d-103">Információkat ad vissza az Azure SQL Database Sync tagjairól.</span><span class="sxs-lookup"><span data-stu-id="ebf1d-103">Returns information about Azure SQL Database Sync Members.</span></span>

## <span data-ttu-id="ebf1d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ebf1d-104">SYNTAX</span></span>

```
Get-AzSqlSyncMember [-Name <String>] [-SyncGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ebf1d-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ebf1d-105">DESCRIPTION</span></span>
<span data-ttu-id="ebf1d-106">A **Get-AzSqlSyncMember** parancsmag egy vagy több Azure SQL Database Sync-tag adatait adja vissza.</span><span class="sxs-lookup"><span data-stu-id="ebf1d-106">The **Get-AzSqlSyncMember** cmdlet returns information about one or more Azure SQL Database Sync Members.</span></span>
<span data-ttu-id="ebf1d-107">Adja meg a szinkronizálási tag nevét, hogy csak az adott szinkronizálási tag adatai legyenek láthatóak.</span><span class="sxs-lookup"><span data-stu-id="ebf1d-107">Specify the name of a sync member to see information for only that sync member.</span></span>

## <span data-ttu-id="ebf1d-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ebf1d-108">EXAMPLES</span></span>

### <span data-ttu-id="ebf1d-109">1. példa: Az Azure SQL Sync-tag összes példányának hozzárendelése szinkronizálási csoporthoz</span><span class="sxs-lookup"><span data-stu-id="ebf1d-109">Example 1: Get all instances of Azure SQL Sync Member assigned to a sync group</span></span>
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

<span data-ttu-id="ebf1d-110">Ez a parancs információkat kap a SyncGroup01 szinkronizálási csoporthoz rendelt Azure SQL Database Sync tagról.</span><span class="sxs-lookup"><span data-stu-id="ebf1d-110">This command gets information about all the Azure SQL Database Sync Member assigned to the sync group SyncGroup01.</span></span>

### <span data-ttu-id="ebf1d-111">2. példa: Információ az Azure SQL Database Sync tagról</span><span class="sxs-lookup"><span data-stu-id="ebf1d-111">Example 2: Get information about an Azure SQL Database Sync Member</span></span>
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

<span data-ttu-id="ebf1d-112">Ez a parancs "SyncMember01" néven információkat kap az Azure SQL Database Sync Tagról</span><span class="sxs-lookup"><span data-stu-id="ebf1d-112">This command gets information about the Azure SQL Database Sync Member with name "SyncMember01"</span></span>

### <span data-ttu-id="ebf1d-113">3. példa: Azure SQL Sync-tag összes példányának hozzárendelése szinkronizálási csoporthoz szűrés használatával</span><span class="sxs-lookup"><span data-stu-id="ebf1d-113">Example 3: Get all instances of Azure SQL Sync Member assigned to a sync group using filtering</span></span>
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

<span data-ttu-id="ebf1d-114">Ez a parancs információkat kap a SyncGroup01 szinkronizálási csoporthoz rendelt Azure SQL Database Sync Tagról, amely a "SyncMember" kezdettől kezdődik.</span><span class="sxs-lookup"><span data-stu-id="ebf1d-114">This command gets information about all the Azure SQL Database Sync Member assigned to the sync group SyncGroup01 that start with "SyncMember".</span></span>

## <span data-ttu-id="ebf1d-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ebf1d-115">PARAMETERS</span></span>

### <span data-ttu-id="ebf1d-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ebf1d-116">-DatabaseName</span></span>
<span data-ttu-id="ebf1d-117">Az Azure SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="ebf1d-117">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="ebf1d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebf1d-118">-DefaultProfile</span></span>
<span data-ttu-id="ebf1d-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ebf1d-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ebf1d-120">-Name</span><span class="sxs-lookup"><span data-stu-id="ebf1d-120">-Name</span></span>
<span data-ttu-id="ebf1d-121">A szinkronizálási tag neve.</span><span class="sxs-lookup"><span data-stu-id="ebf1d-121">The sync member name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncMemberName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebf1d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebf1d-122">-ResourceGroupName</span></span>
<span data-ttu-id="ebf1d-123">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ebf1d-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="ebf1d-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ebf1d-124">-ServerName</span></span>
<span data-ttu-id="ebf1d-125">Az Azure SQL Server neve.</span><span class="sxs-lookup"><span data-stu-id="ebf1d-125">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="ebf1d-126">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="ebf1d-126">-SyncGroupName</span></span>
<span data-ttu-id="ebf1d-127">A szinkronizálási csoport neve.</span><span class="sxs-lookup"><span data-stu-id="ebf1d-127">The sync group name.</span></span>

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

### <span data-ttu-id="ebf1d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebf1d-128">CommonParameters</span></span>
<span data-ttu-id="ebf1d-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ebf1d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebf1d-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ebf1d-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebf1d-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ebf1d-131">INPUTS</span></span>

### <span data-ttu-id="ebf1d-132">System.String</span><span class="sxs-lookup"><span data-stu-id="ebf1d-132">System.String</span></span>

## <span data-ttu-id="ebf1d-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ebf1d-133">OUTPUTS</span></span>

### <span data-ttu-id="ebf1d-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="ebf1d-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="ebf1d-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ebf1d-135">NOTES</span></span>

## <span data-ttu-id="ebf1d-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ebf1d-136">RELATED LINKS</span></span>

[<span data-ttu-id="ebf1d-137">New-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="ebf1d-137">New-AzSqlSyncMember</span></span>](./New-AzSqlSyncMember.md)

[<span data-ttu-id="ebf1d-138">Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="ebf1d-138">Update-AzSqlSyncMember</span></span>](./Update-AzSqlSyncMember.md)

[<span data-ttu-id="ebf1d-139">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="ebf1d-139">Remove-AzSqlSyncMember</span></span>](./Remove-AzSqlSyncMember.md)

