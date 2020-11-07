---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncAgent.md
ms.openlocfilehash: f74a031079ab35e1584d8c7e5536e2605ea665ec
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668920"
---
# <span data-ttu-id="1472d-101">Get-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="1472d-101">Get-AzSqlSyncAgent</span></span>

## <span data-ttu-id="1472d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1472d-102">SYNOPSIS</span></span>
<span data-ttu-id="1472d-103">Információt ad az Azure SQL-szinkronizálási ügynökökről.</span><span class="sxs-lookup"><span data-stu-id="1472d-103">Returns information about Azure SQL Sync Agents.</span></span>

## <span data-ttu-id="1472d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1472d-104">SYNTAX</span></span>

```
Get-AzSqlSyncAgent [[-Name] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1472d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1472d-105">DESCRIPTION</span></span>
<span data-ttu-id="1472d-106">A **Get-AzSqlSyncAgent** parancsmag információt ad egy vagy több Azure SQL-szinkronizálási ügynökről.</span><span class="sxs-lookup"><span data-stu-id="1472d-106">The **Get-AzSqlSyncAgent** cmdlet returns information about one or more Azure SQL Sync Agents.</span></span>
<span data-ttu-id="1472d-107">Adja meg a szinkronizálási ügynök nevét, ha csak a szinkronizálási megbízott adatait szeretné látni.</span><span class="sxs-lookup"><span data-stu-id="1472d-107">Specify the name of a sync agent to see information for only that sync agent.</span></span>

## <span data-ttu-id="1472d-108">Példák</span><span class="sxs-lookup"><span data-stu-id="1472d-108">EXAMPLES</span></span>

### <span data-ttu-id="1472d-109">1. példa: az Azure SQL Serverhez rendelt összes példány beolvasása az Azure SQL Server-kiszolgálóval</span><span class="sxs-lookup"><span data-stu-id="1472d-109">Example 1: Get all instances of Azure SQL Sync Agent assigned to an Azure SQL Server</span></span>
```
PS C:\>Get-AzSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Format-List
ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/syncAgents/{SyncAgent01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncAgentName               : SyncAgent01
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
LastAliveTime:              : 6/1/2017 5:08:48 AM
Version                     : 4.3.6348.1
IsUpToDate                  : False
ExpiryTime                  : 
State                       : Online

ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/syncAgents/{SyncAgent02}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncAgentName               : SyncAgent02
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
LastAliveTime:              : 6/1/2017 5:08:48 AM
Version                     : 4.3.6348.1
IsUpToDate                  : False
ExpiryTime                  : 
State                       : Online
```

<span data-ttu-id="1472d-110">Ez a parancs információt kap az Azure SQL Serverhez rendelt összes Azure SQL-szinkronizálási ügynökről.</span><span class="sxs-lookup"><span data-stu-id="1472d-110">This command gets information about all the Azure SQL Sync Agents assigned to an Azure SQL Server.</span></span>

### <span data-ttu-id="1472d-111">2. példa: információk beszerzése Azure SQL-szinkronizáló ügynökről</span><span class="sxs-lookup"><span data-stu-id="1472d-111">Example 2: Get information about an Azure SQL Sync Agent</span></span>
```
PS C:\>Get-AzSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -Name "SyncAgent01" | Format-List
ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/syncAgents/{SyncAgent01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncAgentName               : SyncAgent01
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
LastAliveTime:              : 6/1/2017 5:08:48 AM
Version                     : 4.3.6348.1
IsUpToDate                  : False
ExpiryTime                  : 
State                       : Online
```

<span data-ttu-id="1472d-112">Ez a parancs információt kap az Azure SQL-adatbázis szinkronizálási ügynökéről a "SyncAgent01" névvel</span><span class="sxs-lookup"><span data-stu-id="1472d-112">This command gets information about the Azure SQL Database Sync Agent with name "SyncAgent01"</span></span>

### <span data-ttu-id="1472d-113">3. példa: az Azure SQL Serverhez rendelt összes példány beolvasása a szűrés segítségével</span><span class="sxs-lookup"><span data-stu-id="1472d-113">Example 3: Get all instances of Azure SQL Sync Agent assigned to an Azure SQL Server using filtering</span></span>
```
PS C:\>Get-AzSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -Name SyncAgent* | Format-List
ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/syncAgents/{SyncAgent01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncAgentName               : SyncAgent01
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
LastAliveTime:              : 6/1/2017 5:08:48 AM
Version                     : 4.3.6348.1
IsUpToDate                  : False
ExpiryTime                  : 
State                       : Online

ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/syncAgents/{SyncAgent02}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncAgentName               : SyncAgent02
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
LastAliveTime:              : 6/1/2017 5:08:48 AM
Version                     : 4.3.6348.1
IsUpToDate                  : False
ExpiryTime                  : 
State                       : Online
```

<span data-ttu-id="1472d-114">Ez a parancs a "SyncAgent" kezdetű Azure SQL Serverhez rendelt összes Azure SQL-szinkronizálási ügynökről kap információkat.</span><span class="sxs-lookup"><span data-stu-id="1472d-114">This command gets information about all the Azure SQL Sync Agents assigned to an Azure SQL Server that start with "SyncAgent".</span></span>

## <span data-ttu-id="1472d-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1472d-115">PARAMETERS</span></span>

### <span data-ttu-id="1472d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1472d-116">-DefaultProfile</span></span>
<span data-ttu-id="1472d-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="1472d-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1472d-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1472d-118">-Name</span></span>
<span data-ttu-id="1472d-119">A Szinkronizáló ügynök neve.</span><span class="sxs-lookup"><span data-stu-id="1472d-119">The sync agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncAgentName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="1472d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1472d-120">-ResourceGroupName</span></span>
<span data-ttu-id="1472d-121">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="1472d-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="1472d-122">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="1472d-122">-ServerName</span></span>
<span data-ttu-id="1472d-123">Annak az Azure SQL Server-kiszolgálónak a neve, amelyen a Szinkronizáló ügynök be van jelentkezve.</span><span class="sxs-lookup"><span data-stu-id="1472d-123">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="1472d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1472d-124">CommonParameters</span></span>
<span data-ttu-id="1472d-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1472d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1472d-126">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1472d-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1472d-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1472d-127">INPUTS</span></span>

### <span data-ttu-id="1472d-128">System. String</span><span class="sxs-lookup"><span data-stu-id="1472d-128">System.String</span></span>

## <span data-ttu-id="1472d-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1472d-129">OUTPUTS</span></span>

### <span data-ttu-id="1472d-130">Microsoft. Azure. Command. SQL. DataSync. Model. AzureSqlSyncAgentModel</span><span class="sxs-lookup"><span data-stu-id="1472d-130">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="1472d-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1472d-131">NOTES</span></span>

## <span data-ttu-id="1472d-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1472d-132">RELATED LINKS</span></span>

[<span data-ttu-id="1472d-133">Remove-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="1472d-133">Remove-AzSqlSyncAgent</span></span>](./Remove-AzSqlSyncAgent.md)

[<span data-ttu-id="1472d-134">Új – AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="1472d-134">New-AzSqlSyncAgent</span></span>](./New-AzSqlSyncAgent.md)

