---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncGroup.md
ms.openlocfilehash: bc4a547ec216cc4c88837f48eadc1c1e80c9087a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502879"
---
# <span data-ttu-id="67656-101">Get-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="67656-101">Get-AzureRmSqlSyncGroup</span></span>

## <span data-ttu-id="67656-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="67656-102">SYNOPSIS</span></span>
<span data-ttu-id="67656-103">Információt ad az Azure SQL Database szinkronizálási csoportjairól.</span><span class="sxs-lookup"><span data-stu-id="67656-103">Returns information about Azure SQL Database Sync Groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67656-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="67656-104">SYNTAX</span></span>

```
Get-AzureRmSqlSyncGroup [[-Name] <String>] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67656-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="67656-105">DESCRIPTION</span></span>
<span data-ttu-id="67656-106">A **Get-AzureRmSqlSyncGroup** parancsmag információt ad egy vagy több Azure SQL adatbázis-szinkronizálási csoportról.</span><span class="sxs-lookup"><span data-stu-id="67656-106">The **Get-AzureRmSqlSyncGroup** cmdlet returns information about one or more Azure SQL Database Sync Groups.</span></span>
<span data-ttu-id="67656-107">Adja meg a szinkronizálási csoport nevét, ha csak a szinkronizálási csoport adatait szeretné látni.</span><span class="sxs-lookup"><span data-stu-id="67656-107">Specify the name of a sync group to see information for only that sync group.</span></span>

## <span data-ttu-id="67656-108">Példák</span><span class="sxs-lookup"><span data-stu-id="67656-108">EXAMPLES</span></span>

### <span data-ttu-id="67656-109">Példa 1: az Azure SQL szinkronizálási csoport minden előfordulásának beolvasása Azure SQL-adatbázishoz</span><span class="sxs-lookup"><span data-stu-id="67656-109">Example 1: Get all instances of Azure SQL Sync Group assigned to an Azure SQL Database</span></span>
```
PS C:\>Get-AzureRmSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Format-List
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

<span data-ttu-id="67656-110">Ez a parancs az Azure SQL-adatbázishoz rendelt összes Azure SQL adatbázis-szinkronizálási csoportra vonatkozó információt kap.</span><span class="sxs-lookup"><span data-stu-id="67656-110">This command gets information about all the Azure SQL Database Sync Groups assigned to an Azure SQL Database.</span></span>

### <span data-ttu-id="67656-111">2. példa: információk kérése Azure SQL-adatbázis szinkronizálási csoportjához</span><span class="sxs-lookup"><span data-stu-id="67656-111">Example 2: Get information about an Azure SQL Database Sync Group</span></span>
```
PS C:\>Get-AzureRmSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -Name "SyncGroup01" | Format-List
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

<span data-ttu-id="67656-112">Ez a parancs információkat kap az Azure SQL-adatbázis szinkronizálási csoportjához "SyncGroup01" névvel</span><span class="sxs-lookup"><span data-stu-id="67656-112">This command gets information about the Azure SQL Database Sync Group with name "SyncGroup01"</span></span>

## <span data-ttu-id="67656-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="67656-113">PARAMETERS</span></span>

### <span data-ttu-id="67656-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="67656-114">-DatabaseName</span></span>
<span data-ttu-id="67656-115">Az Azure SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="67656-115">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="67656-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67656-116">-DefaultProfile</span></span>
<span data-ttu-id="67656-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="67656-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="67656-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="67656-118">-Name</span></span>
<span data-ttu-id="67656-119">A szinkronizálási csoport neve.</span><span class="sxs-lookup"><span data-stu-id="67656-119">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67656-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67656-120">-ResourceGroupName</span></span>
<span data-ttu-id="67656-121">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="67656-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="67656-122">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="67656-122">-ServerName</span></span>
<span data-ttu-id="67656-123">Az Azure SQL Server neve.</span><span class="sxs-lookup"><span data-stu-id="67656-123">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="67656-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67656-124">CommonParameters</span></span>
<span data-ttu-id="67656-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="67656-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67656-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67656-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67656-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="67656-127">INPUTS</span></span>

### <span data-ttu-id="67656-128">System. String</span><span class="sxs-lookup"><span data-stu-id="67656-128">System.String</span></span>

## <span data-ttu-id="67656-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="67656-129">OUTPUTS</span></span>

### <span data-ttu-id="67656-130">Microsoft. Azure. Command. SQL. DataSync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="67656-130">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="67656-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="67656-131">NOTES</span></span>

## <span data-ttu-id="67656-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="67656-132">RELATED LINKS</span></span>

[<span data-ttu-id="67656-133">Új – AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="67656-133">New-AzureRmSqlSyncGroup</span></span>](./New-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="67656-134">Update-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="67656-134">Update-AzureRmSqlSyncGroup</span></span>](./Update-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="67656-135">Remove-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="67656-135">Remove-AzureRmSqlSyncGroup</span></span>](./Remove-AzureRmSqlSyncGroup.md)

