---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlsyncagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncAgent.md
ms.openlocfilehash: 6e1d647c390d8d0f92192a63c3a395005074cfa6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498716"
---
# <span data-ttu-id="c4e9a-101">New-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="c4e9a-101">New-AzureRmSqlSyncAgent</span></span>

## <span data-ttu-id="c4e9a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c4e9a-102">SYNOPSIS</span></span>
<span data-ttu-id="c4e9a-103">Azure SQL szinkronizáló ügynököt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="c4e9a-103">Creates an Azure SQL Sync Agent.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c4e9a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c4e9a-104">SYNTAX</span></span>

### <span data-ttu-id="c4e9a-105">SyncDatabaseComponent (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c4e9a-105">SyncDatabaseComponent (Default)</span></span>
```
New-AzureRmSqlSyncAgent [-Name] <String> -SyncDatabaseName <String> [-SyncDatabaseServerName <String>]
 [-SyncDatabaseResourceGroupName <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4e9a-106">SyncDatabaseResourceID</span><span class="sxs-lookup"><span data-stu-id="c4e9a-106">SyncDatabaseResourceID</span></span>
```
New-AzureRmSqlSyncAgent [-Name] <String> -SyncDatabaseResourceID <String> [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c4e9a-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="c4e9a-107">DESCRIPTION</span></span>
<span data-ttu-id="c4e9a-108">A **New-AzureRmSqlSyncAgent** parancsmag egy Azure SQL szinkronizáló ügynököt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="c4e9a-108">The **New-AzureRmSqlSyncAgent** cmdlet creates an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="c4e9a-109">Példák</span><span class="sxs-lookup"><span data-stu-id="c4e9a-109">EXAMPLES</span></span>

### <span data-ttu-id="c4e9a-110">1. példa: Szinkronizálói ügynök létrehozása Azure SQL Serverhez.</span><span class="sxs-lookup"><span data-stu-id="c4e9a-110">Example 1: Create a sync agent for an Azure SQL server.</span></span>
```
PS C:\> New-AzureRmSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -Name "SyncAgent01" -SyncDatabaseServerName "syncDatabaseServer01" 
-SyncDatabaseName "syncDatabaseName01" -SyncDatabaseResourceGroupName "syncDatabaseResourceGroup01" | Format-List
ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/syncAgents/{SyncAgent01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncAgentName               : SyncAgent01
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
LastAliveTime:              : 
Version                     : 4.2.0.0
IsUpToDate                  : True
ExpiryTime                  : 12/31/9999 11:59:59 PM
State                       : NeverConnected
```

<span data-ttu-id="c4e9a-111">Ez a parancs létrehoz egy szinkronizáló ügynököt egy Azure SQL Serverhez.</span><span class="sxs-lookup"><span data-stu-id="c4e9a-111">This command creates a sync agent for an Azure SQL server.</span></span>

## <span data-ttu-id="c4e9a-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c4e9a-112">PARAMETERS</span></span>

### <span data-ttu-id="c4e9a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4e9a-113">-DefaultProfile</span></span>
<span data-ttu-id="c4e9a-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="c4e9a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c4e9a-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c4e9a-115">-Name</span></span>
<span data-ttu-id="c4e9a-116">A Szinkronizáló ügynök neve.</span><span class="sxs-lookup"><span data-stu-id="c4e9a-116">The sync agent name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SyncAgentName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4e9a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4e9a-117">-ResourceGroupName</span></span>
<span data-ttu-id="c4e9a-118">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c4e9a-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="c4e9a-119">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="c4e9a-119">-ServerName</span></span>
<span data-ttu-id="c4e9a-120">Annak az Azure SQL Server-kiszolgálónak a neve, amelyen a Szinkronizáló ügynök be van jelentkezve.</span><span class="sxs-lookup"><span data-stu-id="c4e9a-120">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="c4e9a-121">-SyncDatabaseName</span><span class="sxs-lookup"><span data-stu-id="c4e9a-121">-SyncDatabaseName</span></span>
<span data-ttu-id="c4e9a-122">A szinkronizáláshoz kapcsolódó metaadatok tárolására szolgáló adatbázis.</span><span class="sxs-lookup"><span data-stu-id="c4e9a-122">The database used to store sync related metadata.</span></span>

```yaml
Type: String
Parameter Sets: SyncDatabaseComponent
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4e9a-123">-SyncDatabaseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4e9a-123">-SyncDatabaseResourceGroupName</span></span>
<span data-ttu-id="c4e9a-124">Az erőforráscsoport, amelyre a szinkronizálási metaadat-adatbázis tartozik.</span><span class="sxs-lookup"><span data-stu-id="c4e9a-124">The resource group the sync metadata database belongs to.</span></span>

```yaml
Type: String
Parameter Sets: SyncDatabaseComponent
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4e9a-125">-SyncDatabaseResourceID</span><span class="sxs-lookup"><span data-stu-id="c4e9a-125">-SyncDatabaseResourceID</span></span>
<span data-ttu-id="c4e9a-126">A szinkronizálási metaadat-adatbázis erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="c4e9a-126">The resource ID of  the sync metadata database.</span></span>

```yaml
Type: String
Parameter Sets: SyncDatabaseResourceID
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4e9a-127">-SyncDatabaseServerName</span><span class="sxs-lookup"><span data-stu-id="c4e9a-127">-SyncDatabaseServerName</span></span>
<span data-ttu-id="c4e9a-128">Az a kiszolgáló, amelyen a szinkronizálási metaadat-adatbázis található.</span><span class="sxs-lookup"><span data-stu-id="c4e9a-128">The server on which the sync metadata database is hosted.</span></span>

```yaml
Type: String
Parameter Sets: SyncDatabaseComponent
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4e9a-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c4e9a-129">-Confirm</span></span>
<span data-ttu-id="c4e9a-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c4e9a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4e9a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4e9a-131">-WhatIf</span></span>
<span data-ttu-id="c4e9a-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c4e9a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4e9a-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c4e9a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4e9a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4e9a-134">CommonParameters</span></span>
<span data-ttu-id="c4e9a-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c4e9a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4e9a-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4e9a-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4e9a-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c4e9a-137">INPUTS</span></span>

### <span data-ttu-id="c4e9a-138">Nincs</span><span class="sxs-lookup"><span data-stu-id="c4e9a-138">None</span></span>
<span data-ttu-id="c4e9a-139">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="c4e9a-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c4e9a-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c4e9a-140">OUTPUTS</span></span>

### <span data-ttu-id="c4e9a-141">Microsoft. Azure. Command. SQL. DataSync. Model. AzureSqlSyncAgentModel</span><span class="sxs-lookup"><span data-stu-id="c4e9a-141">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="c4e9a-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c4e9a-142">NOTES</span></span>

## <span data-ttu-id="c4e9a-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c4e9a-143">RELATED LINKS</span></span>

[<span data-ttu-id="c4e9a-144">Remove-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="c4e9a-144">Remove-AzureRmSqlSyncAgent</span></span>](./Remove-AzureRmSqlSyncAgent.md)

[<span data-ttu-id="c4e9a-145">Get-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="c4e9a-145">Get-AzureRmSqlSyncAgent</span></span>](./Get-AzureRmSqlSyncAgent.md)

