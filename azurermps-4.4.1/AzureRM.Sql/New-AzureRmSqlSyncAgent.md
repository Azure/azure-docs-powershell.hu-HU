---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncAgent.md
ms.openlocfilehash: e296e338d519537f688085fc5c142e3c12804b0c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672051"
---
# <span data-ttu-id="b90fb-101">New-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="b90fb-101">New-AzureRmSqlSyncAgent</span></span>

## <span data-ttu-id="b90fb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b90fb-102">SYNOPSIS</span></span>
<span data-ttu-id="b90fb-103">Azure SQL szinkronizáló ügynököt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="b90fb-103">Creates an Azure SQL Sync Agent.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b90fb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b90fb-104">SYNTAX</span></span>

### <span data-ttu-id="b90fb-105">SyncDatabaseComponent (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b90fb-105">SyncDatabaseComponent (Default)</span></span>
```
New-AzureRmSqlSyncAgent [-Name] <String> -SyncDatabaseName <String> [-SyncDatabaseServerName <String>]
 [-SyncDatabaseResourceGroupName <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b90fb-106">SyncDatabaseResourceID</span><span class="sxs-lookup"><span data-stu-id="b90fb-106">SyncDatabaseResourceID</span></span>
```
New-AzureRmSqlSyncAgent [-Name] <String> -SyncDatabaseResourceID <String> [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b90fb-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="b90fb-107">DESCRIPTION</span></span>
<span data-ttu-id="b90fb-108">A **New-AzureRmSqlSyncAgent** parancsmag egy Azure SQL szinkronizáló ügynököt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="b90fb-108">The **New-AzureRmSqlSyncAgent** cmdlet creates an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="b90fb-109">Példák</span><span class="sxs-lookup"><span data-stu-id="b90fb-109">EXAMPLES</span></span>

### <span data-ttu-id="b90fb-110">1. példa: Szinkronizálói ügynök létrehozása Azure SQL Serverhez.</span><span class="sxs-lookup"><span data-stu-id="b90fb-110">Example 1: Create a sync agent for an Azure SQL server.</span></span>
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

<span data-ttu-id="b90fb-111">Ez a parancs létrehoz egy szinkronizáló ügynököt egy Azure SQL Serverhez.</span><span class="sxs-lookup"><span data-stu-id="b90fb-111">This command creates a sync agent for an Azure SQL server.</span></span>

## <span data-ttu-id="b90fb-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b90fb-112">PARAMETERS</span></span>

### <span data-ttu-id="b90fb-113">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b90fb-113">-Confirm</span></span>
<span data-ttu-id="b90fb-114">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b90fb-114">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b90fb-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b90fb-115">-Name</span></span>
<span data-ttu-id="b90fb-116">A Szinkronizáló ügynök neve.</span><span class="sxs-lookup"><span data-stu-id="b90fb-116">The sync agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncAgentName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b90fb-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b90fb-117">-ResourceGroupName</span></span>
<span data-ttu-id="b90fb-118">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b90fb-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="b90fb-119">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="b90fb-119">-ServerName</span></span>
<span data-ttu-id="b90fb-120">Annak az Azure SQL Server-kiszolgálónak a neve, amelyen a Szinkronizáló ügynök be van jelentkezve.</span><span class="sxs-lookup"><span data-stu-id="b90fb-120">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="b90fb-121">-SyncDatabaseName</span><span class="sxs-lookup"><span data-stu-id="b90fb-121">-SyncDatabaseName</span></span>
<span data-ttu-id="b90fb-122">A szinkronizáláshoz kapcsolódó metaadatok tárolására szolgáló adatbázis.</span><span class="sxs-lookup"><span data-stu-id="b90fb-122">The database used to store sync related metadata.</span></span>

```yaml
Type: System.String
Parameter Sets: SyncDatabaseComponent
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b90fb-123">-SyncDatabaseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b90fb-123">-SyncDatabaseResourceGroupName</span></span>
<span data-ttu-id="b90fb-124">Az erőforráscsoport, amelyre a szinkronizálási metaadat-adatbázis tartozik.</span><span class="sxs-lookup"><span data-stu-id="b90fb-124">The resource group the sync metadata database belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: SyncDatabaseComponent
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b90fb-125">-SyncDatabaseResourceID</span><span class="sxs-lookup"><span data-stu-id="b90fb-125">-SyncDatabaseResourceID</span></span>
<span data-ttu-id="b90fb-126">A szinkronizálási metaadat-adatbázis erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b90fb-126">The resource ID of  the sync metadata database.</span></span>

```yaml
Type: System.String
Parameter Sets: SyncDatabaseResourceID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b90fb-127">-SyncDatabaseServerName</span><span class="sxs-lookup"><span data-stu-id="b90fb-127">-SyncDatabaseServerName</span></span>
<span data-ttu-id="b90fb-128">Az a kiszolgáló, amelyen a szinkronizálási metaadat-adatbázis található.</span><span class="sxs-lookup"><span data-stu-id="b90fb-128">The server on which the sync metadata database is hosted.</span></span>

```yaml
Type: System.String
Parameter Sets: SyncDatabaseComponent
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b90fb-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b90fb-129">-WhatIf</span></span>
<span data-ttu-id="b90fb-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b90fb-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b90fb-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b90fb-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b90fb-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b90fb-132">-DefaultProfile</span></span>
<span data-ttu-id="b90fb-133">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b90fb-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b90fb-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b90fb-134">CommonParameters</span></span>
<span data-ttu-id="b90fb-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b90fb-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b90fb-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b90fb-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b90fb-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b90fb-137">INPUTS</span></span>

## <span data-ttu-id="b90fb-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b90fb-138">OUTPUTS</span></span>

### <span data-ttu-id="b90fb-139">Microsoft. Azure. Command. SQL. DataSync. Model. AzureSqlSyncAgentModel</span><span class="sxs-lookup"><span data-stu-id="b90fb-139">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="b90fb-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b90fb-140">NOTES</span></span>

## <span data-ttu-id="b90fb-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b90fb-141">RELATED LINKS</span></span>

[<span data-ttu-id="b90fb-142">Remove-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="b90fb-142">Remove-AzureRmSqlSyncAgent</span></span>](./Remove-AzureRmSqlSyncAgent.md)

[<span data-ttu-id="b90fb-143">Get-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="b90fb-143">Get-AzureRmSqlSyncAgent</span></span>](./Get-AzureRmSqlSyncAgent.md)

