---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlsyncagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncAgent.md
ms.openlocfilehash: 8b590e6ba8329ba6e0c45d30f7163c637d90f79e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495596"
---
# <span data-ttu-id="8af29-101">Get-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="8af29-101">Get-AzureRmSqlSyncAgent</span></span>

## <span data-ttu-id="8af29-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8af29-102">SYNOPSIS</span></span>
<span data-ttu-id="8af29-103">Információt ad az Azure SQL-szinkronizálási ügynökökről.</span><span class="sxs-lookup"><span data-stu-id="8af29-103">Returns information about Azure SQL Sync Agents.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8af29-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8af29-104">SYNTAX</span></span>

```
Get-AzureRmSqlSyncAgent [[-Name] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8af29-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8af29-105">DESCRIPTION</span></span>
<span data-ttu-id="8af29-106">A **Get-AzureRmSqlSyncAgent** parancsmag információt ad egy vagy több Azure SQL-szinkronizálási ügynökről.</span><span class="sxs-lookup"><span data-stu-id="8af29-106">The **Get-AzureRmSqlSyncAgent** cmdlet returns information about one or more Azure SQL Sync Agents.</span></span>
<span data-ttu-id="8af29-107">Adja meg a szinkronizálási ügynök nevét, ha csak a szinkronizálási megbízott adatait szeretné látni.</span><span class="sxs-lookup"><span data-stu-id="8af29-107">Specify the name of a sync agent to see information for only that sync agent.</span></span>

## <span data-ttu-id="8af29-108">Példák</span><span class="sxs-lookup"><span data-stu-id="8af29-108">EXAMPLES</span></span>

### <span data-ttu-id="8af29-109">1. példa: az Azure SQL Serverhez rendelt összes példány beolvasása az Azure SQL Server-kiszolgálóval</span><span class="sxs-lookup"><span data-stu-id="8af29-109">Example 1: Get all instances of Azure SQL Sync Agent assigned to an Azure SQL Server</span></span>
```
PS C:\>Get-AzureRmSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Format-List
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

<span data-ttu-id="8af29-110">Ez a parancs információt kap az Azure SQL Serverhez rendelt összes Azure SQL-szinkronizálási ügynökről.</span><span class="sxs-lookup"><span data-stu-id="8af29-110">This command gets information about all the Azure SQL Sync Agents assigned to an Azure SQL Server.</span></span>

### <span data-ttu-id="8af29-111">2. példa: információk beszerzése Azure SQL-szinkronizáló ügynökről</span><span class="sxs-lookup"><span data-stu-id="8af29-111">Example 2: Get information about an Azure SQL Sync Agent</span></span>
```
PS C:\>Get-AzureRmSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -Name "SyncAgent01" | Format-List
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

<span data-ttu-id="8af29-112">Ez a parancs információt kap az Azure SQL-adatbázis szinkronizálási ügynökéről a "SyncAgent01" névvel</span><span class="sxs-lookup"><span data-stu-id="8af29-112">This command gets information about the Azure SQL Database Sync Agent with name "SyncAgent01"</span></span>

## <span data-ttu-id="8af29-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8af29-113">PARAMETERS</span></span>

### <span data-ttu-id="8af29-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8af29-114">-DefaultProfile</span></span>
<span data-ttu-id="8af29-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="8af29-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8af29-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8af29-116">-Name</span></span>
<span data-ttu-id="8af29-117">A Szinkronizáló ügynök neve.</span><span class="sxs-lookup"><span data-stu-id="8af29-117">The sync agent name.</span></span>

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

### <span data-ttu-id="8af29-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8af29-118">-ResourceGroupName</span></span>
<span data-ttu-id="8af29-119">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="8af29-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="8af29-120">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="8af29-120">-ServerName</span></span>
<span data-ttu-id="8af29-121">Annak az Azure SQL Server-kiszolgálónak a neve, amelyen a Szinkronizáló ügynök be van jelentkezve.</span><span class="sxs-lookup"><span data-stu-id="8af29-121">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="8af29-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8af29-122">CommonParameters</span></span>
<span data-ttu-id="8af29-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8af29-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8af29-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8af29-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8af29-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8af29-125">INPUTS</span></span>

### <span data-ttu-id="8af29-126">System. String</span><span class="sxs-lookup"><span data-stu-id="8af29-126">System.String</span></span>

## <span data-ttu-id="8af29-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8af29-127">OUTPUTS</span></span>

### <span data-ttu-id="8af29-128">Microsoft. Azure. Command. SQL. DataSync. Model. AzureSqlSyncAgentModel</span><span class="sxs-lookup"><span data-stu-id="8af29-128">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="8af29-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8af29-129">NOTES</span></span>

## <span data-ttu-id="8af29-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8af29-130">RELATED LINKS</span></span>

[<span data-ttu-id="8af29-131">Remove-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="8af29-131">Remove-AzureRmSqlSyncAgent</span></span>](./Remove-AzureRmSqlSyncAgent.md)

[<span data-ttu-id="8af29-132">Új – AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="8af29-132">New-AzureRmSqlSyncAgent</span></span>](./New-AzureRmSqlSyncAgent.md)

