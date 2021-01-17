---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncAgent.md
ms.openlocfilehash: 8bb031ffa2924ce0cace8d2c7daf94be97713eec
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98374791"
---
# <span data-ttu-id="5a1ab-101">Get-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="5a1ab-101">Get-AzSqlSyncAgent</span></span>

## <span data-ttu-id="5a1ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a1ab-102">SYNOPSIS</span></span>
<span data-ttu-id="5a1ab-103">Információkat ad vissza az Azure SQL Sync-ügynökökről.</span><span class="sxs-lookup"><span data-stu-id="5a1ab-103">Returns information about Azure SQL Sync Agents.</span></span>

## <span data-ttu-id="5a1ab-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5a1ab-104">SYNTAX</span></span>

```
Get-AzSqlSyncAgent [[-Name] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a1ab-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5a1ab-105">DESCRIPTION</span></span>
<span data-ttu-id="5a1ab-106">A **Get-AzSqlSyncAgent** parancsmag egy vagy több Azure SQL Sync-ügynök adatait adja vissza.</span><span class="sxs-lookup"><span data-stu-id="5a1ab-106">The **Get-AzSqlSyncAgent** cmdlet returns information about one or more Azure SQL Sync Agents.</span></span>
<span data-ttu-id="5a1ab-107">Adja meg a szinkronizálási ügynök nevét, hogy csak az adott szinkronizálási ügynök adatai legyenek láthatóak.</span><span class="sxs-lookup"><span data-stu-id="5a1ab-107">Specify the name of a sync agent to see information for only that sync agent.</span></span>

## <span data-ttu-id="5a1ab-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5a1ab-108">EXAMPLES</span></span>

### <span data-ttu-id="5a1ab-109">1. példa: Azure SQL Sync Agent összes példányának hozzárendelése Azure SQL Serverhez</span><span class="sxs-lookup"><span data-stu-id="5a1ab-109">Example 1: Get all instances of Azure SQL Sync Agent assigned to an Azure SQL Server</span></span>
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

<span data-ttu-id="5a1ab-110">Ez a parancs információkat kap az Azure SQL Serverhez rendelt Összes Azure SQL Sync-ügynökről.</span><span class="sxs-lookup"><span data-stu-id="5a1ab-110">This command gets information about all the Azure SQL Sync Agents assigned to an Azure SQL Server.</span></span>

### <span data-ttu-id="5a1ab-111">2. példa: Azure SQL Sync-ügynökkel kapcsolatos információk lekérte</span><span class="sxs-lookup"><span data-stu-id="5a1ab-111">Example 2: Get information about an Azure SQL Sync Agent</span></span>
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

<span data-ttu-id="5a1ab-112">Ez a parancs információt kap az Azure SQL Database Sync Agentről "SyncAgent01" néven</span><span class="sxs-lookup"><span data-stu-id="5a1ab-112">This command gets information about the Azure SQL Database Sync Agent with name "SyncAgent01"</span></span>

### <span data-ttu-id="5a1ab-113">3. példa: Azure SQL Sync Agent összes példányának hozzárendelése egy Azure SQL Serverhez szűrés használatával</span><span class="sxs-lookup"><span data-stu-id="5a1ab-113">Example 3: Get all instances of Azure SQL Sync Agent assigned to an Azure SQL Server using filtering</span></span>
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

<span data-ttu-id="5a1ab-114">Ez a parancs információkat kap az Azure SQL Serverhez rendelt összes Azure SQL Sync Agentsről, amelyek a "SyncAgent" kezdettől indulnak.</span><span class="sxs-lookup"><span data-stu-id="5a1ab-114">This command gets information about all the Azure SQL Sync Agents assigned to an Azure SQL Server that start with "SyncAgent".</span></span>

## <span data-ttu-id="5a1ab-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5a1ab-115">PARAMETERS</span></span>

### <span data-ttu-id="5a1ab-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a1ab-116">-DefaultProfile</span></span>
<span data-ttu-id="5a1ab-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="5a1ab-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5a1ab-118">-Name</span><span class="sxs-lookup"><span data-stu-id="5a1ab-118">-Name</span></span>
<span data-ttu-id="5a1ab-119">A szinkronizálási ügynök neve.</span><span class="sxs-lookup"><span data-stu-id="5a1ab-119">The sync agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncAgentName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a1ab-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a1ab-120">-ResourceGroupName</span></span>
<span data-ttu-id="5a1ab-121">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="5a1ab-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="5a1ab-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5a1ab-122">-ServerName</span></span>
<span data-ttu-id="5a1ab-123">Annak az Azure SQL Servernek a neve, amelyben a szinkronizálási ügynök található.</span><span class="sxs-lookup"><span data-stu-id="5a1ab-123">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="5a1ab-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a1ab-124">CommonParameters</span></span>
<span data-ttu-id="5a1ab-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a1ab-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a1ab-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5a1ab-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a1ab-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5a1ab-127">INPUTS</span></span>

### <span data-ttu-id="5a1ab-128">System.String</span><span class="sxs-lookup"><span data-stu-id="5a1ab-128">System.String</span></span>

## <span data-ttu-id="5a1ab-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5a1ab-129">OUTPUTS</span></span>

### <span data-ttu-id="5a1ab-130">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span><span class="sxs-lookup"><span data-stu-id="5a1ab-130">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="5a1ab-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5a1ab-131">NOTES</span></span>

## <span data-ttu-id="5a1ab-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5a1ab-132">RELATED LINKS</span></span>

[<span data-ttu-id="5a1ab-133">Remove-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="5a1ab-133">Remove-AzSqlSyncAgent</span></span>](./Remove-AzSqlSyncAgent.md)

[<span data-ttu-id="5a1ab-134">New-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="5a1ab-134">New-AzSqlSyncAgent</span></span>](./New-AzSqlSyncAgent.md)

