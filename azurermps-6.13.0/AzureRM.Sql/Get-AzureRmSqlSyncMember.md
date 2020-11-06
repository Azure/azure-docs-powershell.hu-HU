---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncMember.md
ms.openlocfilehash: 30a73047282508adc0c2aa0d0d64a61f9f70e71a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502872"
---
# <span data-ttu-id="124f9-101">Get-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="124f9-101">Get-AzureRmSqlSyncMember</span></span>

## <span data-ttu-id="124f9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="124f9-102">SYNOPSIS</span></span>
<span data-ttu-id="124f9-103">Információt ad az Azure SQL Database Sync tagjairól.</span><span class="sxs-lookup"><span data-stu-id="124f9-103">Returns information about Azure SQL Database Sync Members.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="124f9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="124f9-104">SYNTAX</span></span>

```
Get-AzureRmSqlSyncMember [-Name <String>] [-SyncGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="124f9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="124f9-105">DESCRIPTION</span></span>
<span data-ttu-id="124f9-106">A **Get-AzureRmSqlSyncMember** parancsmag információt ad egy vagy több Azure SQL-adatbázis szinkronizálási tagjairól.</span><span class="sxs-lookup"><span data-stu-id="124f9-106">The **Get-AzureRmSqlSyncMember** cmdlet returns information about one or more Azure SQL Database Sync Members.</span></span>
<span data-ttu-id="124f9-107">Adja meg a szinkronizálási tagok nevét, ha csak a szinkronizálási tagok adatait szeretné látni.</span><span class="sxs-lookup"><span data-stu-id="124f9-107">Specify the name of a sync member to see information for only that sync member.</span></span>

## <span data-ttu-id="124f9-108">Példák</span><span class="sxs-lookup"><span data-stu-id="124f9-108">EXAMPLES</span></span>

### <span data-ttu-id="124f9-109">Példa 1: az Azure SQL szinkronizálási tagok minden előfordulásának beolvasása szinkronizálási csoportba</span><span class="sxs-lookup"><span data-stu-id="124f9-109">Example 1: Get all instances of Azure SQL Sync Member assigned to a sync group</span></span>
```
PS C:\>Get-AzureRmSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" | Format-List
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

<span data-ttu-id="124f9-110">Ez a parancs információt kap a szinkronizálás csoport SyncGroup01 társított összes Azure SQL-adatbázis szinkronizálási tagjáról.</span><span class="sxs-lookup"><span data-stu-id="124f9-110">This command gets information about all the Azure SQL Database Sync Member assigned to the sync group SyncGroup01.</span></span>

### <span data-ttu-id="124f9-111">2. példa: információk beszerzése Azure SQL-adatbázis szinkronizálási tagjáról</span><span class="sxs-lookup"><span data-stu-id="124f9-111">Example 2: Get information about an Azure SQL Database Sync Member</span></span>
```
PS C:\>Get-AzureRmSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember01" | Format-List
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

<span data-ttu-id="124f9-112">Ez a parancs információt kap az Azure SQL-adatbázis szinkronizálási tagjáról a "SyncMember01" névvel</span><span class="sxs-lookup"><span data-stu-id="124f9-112">This command gets information about the Azure SQL Database Sync Member with name "SyncMember01"</span></span>

## <span data-ttu-id="124f9-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="124f9-113">PARAMETERS</span></span>

### <span data-ttu-id="124f9-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="124f9-114">-DatabaseName</span></span>
<span data-ttu-id="124f9-115">Az Azure SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="124f9-115">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="124f9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="124f9-116">-DefaultProfile</span></span>
<span data-ttu-id="124f9-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="124f9-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="124f9-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="124f9-118">-Name</span></span>
<span data-ttu-id="124f9-119">A szinkronizálási tag neve.</span><span class="sxs-lookup"><span data-stu-id="124f9-119">The sync member name.</span></span>

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

### <span data-ttu-id="124f9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="124f9-120">-ResourceGroupName</span></span>
<span data-ttu-id="124f9-121">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="124f9-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="124f9-122">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="124f9-122">-ServerName</span></span>
<span data-ttu-id="124f9-123">Az Azure SQL Server neve.</span><span class="sxs-lookup"><span data-stu-id="124f9-123">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="124f9-124">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="124f9-124">-SyncGroupName</span></span>
<span data-ttu-id="124f9-125">A szinkronizálási csoport neve.</span><span class="sxs-lookup"><span data-stu-id="124f9-125">The sync group name.</span></span>

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

### <span data-ttu-id="124f9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="124f9-126">CommonParameters</span></span>
<span data-ttu-id="124f9-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="124f9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="124f9-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="124f9-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="124f9-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="124f9-129">INPUTS</span></span>

### <span data-ttu-id="124f9-130">System. String</span><span class="sxs-lookup"><span data-stu-id="124f9-130">System.String</span></span>

## <span data-ttu-id="124f9-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="124f9-131">OUTPUTS</span></span>

### <span data-ttu-id="124f9-132">Microsoft. Azure. Command. SQL. DataSync. Model. AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="124f9-132">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="124f9-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="124f9-133">NOTES</span></span>

## <span data-ttu-id="124f9-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="124f9-134">RELATED LINKS</span></span>

[<span data-ttu-id="124f9-135">Új – AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="124f9-135">New-AzureRmSqlSyncMember</span></span>](./New-AzureRmSqlSyncMember.md)

[<span data-ttu-id="124f9-136">Update-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="124f9-136">Update-AzureRmSqlSyncMember</span></span>](./Update-AzureRmSqlSyncMember.md)

[<span data-ttu-id="124f9-137">Remove-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="124f9-137">Remove-AzureRmSqlSyncMember</span></span>](./Remove-AzureRmSqlSyncMember.md)

