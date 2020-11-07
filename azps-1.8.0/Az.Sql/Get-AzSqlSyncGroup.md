---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncGroup.md
ms.openlocfilehash: fdee39766c7793b4d326077e5c18e0328a5e4c4c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668917"
---
# <span data-ttu-id="14631-101">Get-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="14631-101">Get-AzSqlSyncGroup</span></span>

## <span data-ttu-id="14631-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="14631-102">SYNOPSIS</span></span>
<span data-ttu-id="14631-103">Információt ad az Azure SQL Database szinkronizálási csoportjairól.</span><span class="sxs-lookup"><span data-stu-id="14631-103">Returns information about Azure SQL Database Sync Groups.</span></span>

## <span data-ttu-id="14631-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="14631-104">SYNTAX</span></span>

```
Get-AzSqlSyncGroup [[-Name] <String>] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14631-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="14631-105">DESCRIPTION</span></span>
<span data-ttu-id="14631-106">A **Get-AzSqlSyncGroup** parancsmag információt ad egy vagy több Azure SQL adatbázis-szinkronizálási csoportról.</span><span class="sxs-lookup"><span data-stu-id="14631-106">The **Get-AzSqlSyncGroup** cmdlet returns information about one or more Azure SQL Database Sync Groups.</span></span>
<span data-ttu-id="14631-107">Adja meg a szinkronizálási csoport nevét, ha csak a szinkronizálási csoport adatait szeretné látni.</span><span class="sxs-lookup"><span data-stu-id="14631-107">Specify the name of a sync group to see information for only that sync group.</span></span>

## <span data-ttu-id="14631-108">Példák</span><span class="sxs-lookup"><span data-stu-id="14631-108">EXAMPLES</span></span>

### <span data-ttu-id="14631-109">Példa 1: az Azure SQL szinkronizálási csoport minden előfordulásának beolvasása Azure SQL-adatbázishoz</span><span class="sxs-lookup"><span data-stu-id="14631-109">Example 1: Get all instances of Azure SQL Sync Group assigned to an Azure SQL Database</span></span>
```
PS C:\>Get-AzSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Format-List
ResourceId                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
IntervalInSeconds           : 100
ConflictResolutionPolicy:   : HubWin
HubDatabaseUserName         : myAccount
HubDatabasePassword         : 
SyncState                   : NotReady
LastSyncTime                : 1/1/0001 12:00:00 AM
Schema                      :  

ResourceId                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup02}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup02
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
IntervalInSeconds           : 100
ConflictResolutionPolicy:   : HubWin
HubDatabaseUserName         : myAccount
HubDatabasePassword         : 
SyncState                   : NotReady
LastSyncTime                : 1/1/0001 12:00:00 AM
Schema                      :
```

<span data-ttu-id="14631-110">Ez a parancs az Azure SQL-adatbázishoz rendelt összes Azure SQL adatbázis-szinkronizálási csoportra vonatkozó információt kap.</span><span class="sxs-lookup"><span data-stu-id="14631-110">This command gets information about all the Azure SQL Database Sync Groups assigned to an Azure SQL Database.</span></span>

### <span data-ttu-id="14631-111">2. példa: információk kérése Azure SQL-adatbázis szinkronizálási csoportjához</span><span class="sxs-lookup"><span data-stu-id="14631-111">Example 2: Get information about an Azure SQL Database Sync Group</span></span>
```
PS C:\>Get-AzSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -Name "SyncGroup01" | Format-List
ResourceId                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup02}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup02
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
IntervalInSeconds           : 100
ConflictResolutionPolicy:   : HubWin
HubDatabaseUserName         : myAccount
HubDatabasePassword         : 
SyncState                   : NotReady
LastSyncTime                : 1/1/0001 12:00:00 AM
Schema                      :
```

<span data-ttu-id="14631-112">Ez a parancs információkat kap az Azure SQL-adatbázis szinkronizálási csoportjához "SyncGroup01" névvel</span><span class="sxs-lookup"><span data-stu-id="14631-112">This command gets information about the Azure SQL Database Sync Group with name "SyncGroup01"</span></span>

### <span data-ttu-id="14631-113">3. példa: az Azure SQL szinkronizálási csoport minden előfordulásának beolvasása a szűrést használó Azure SQL-adatbázisba</span><span class="sxs-lookup"><span data-stu-id="14631-113">Example 3: Get all instances of Azure SQL Sync Group assigned to an Azure SQL Database using filtering</span></span>
```
PS C:\>Get-AzSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -Name "SyncGroup*" | Format-List
ResourceId                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
IntervalInSeconds           : 100
ConflictResolutionPolicy:   : HubWin
HubDatabaseUserName         : myAccount
HubDatabasePassword         : 
SyncState                   : NotReady
LastSyncTime                : 1/1/0001 12:00:00 AM
Schema                      :  

ResourceId                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup02}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup02
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
IntervalInSeconds           : 100
ConflictResolutionPolicy:   : HubWin
HubDatabaseUserName         : myAccount
HubDatabasePassword         : 
SyncState                   : NotReady
LastSyncTime                : 1/1/0001 12:00:00 AM
Schema                      :
```

<span data-ttu-id="14631-114">A parancs a "SyncGroup" kezdetű Azure SQL-adatbázishoz rendelt összes Azure SQL adatbázis-szinkronizálási csoportra vonatkozó információt kap.</span><span class="sxs-lookup"><span data-stu-id="14631-114">This command gets information about all the Azure SQL Database Sync Groups assigned to an Azure SQL Database that start with "SyncGroup".</span></span>

## <span data-ttu-id="14631-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="14631-115">PARAMETERS</span></span>

### <span data-ttu-id="14631-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="14631-116">-DatabaseName</span></span>
<span data-ttu-id="14631-117">Az Azure SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="14631-117">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="14631-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14631-118">-DefaultProfile</span></span>
<span data-ttu-id="14631-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="14631-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="14631-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="14631-120">-Name</span></span>
<span data-ttu-id="14631-121">A szinkronizálási csoport neve.</span><span class="sxs-lookup"><span data-stu-id="14631-121">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="14631-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14631-122">-ResourceGroupName</span></span>
<span data-ttu-id="14631-123">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="14631-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="14631-124">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="14631-124">-ServerName</span></span>
<span data-ttu-id="14631-125">Az Azure SQL Server neve.</span><span class="sxs-lookup"><span data-stu-id="14631-125">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="14631-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14631-126">CommonParameters</span></span>
<span data-ttu-id="14631-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="14631-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14631-128">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="14631-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14631-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="14631-129">INPUTS</span></span>

### <span data-ttu-id="14631-130">System. String</span><span class="sxs-lookup"><span data-stu-id="14631-130">System.String</span></span>

## <span data-ttu-id="14631-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="14631-131">OUTPUTS</span></span>

### <span data-ttu-id="14631-132">Microsoft. Azure. Command. SQL. DataSync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="14631-132">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="14631-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="14631-133">NOTES</span></span>

## <span data-ttu-id="14631-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="14631-134">RELATED LINKS</span></span>

[<span data-ttu-id="14631-135">Új – AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="14631-135">New-AzSqlSyncGroup</span></span>](./New-AzSqlSyncGroup.md)

[<span data-ttu-id="14631-136">Update-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="14631-136">Update-AzSqlSyncGroup</span></span>](./Update-AzSqlSyncGroup.md)

[<span data-ttu-id="14631-137">Remove-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="14631-137">Remove-AzSqlSyncGroup</span></span>](./Remove-AzSqlSyncGroup.md)

