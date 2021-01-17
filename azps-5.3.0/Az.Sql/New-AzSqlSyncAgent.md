---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlsyncagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncAgent.md
ms.openlocfilehash: 4a4ce99eb30aaa959eabdc9c1385b567aef2b0fc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467134"
---
# <span data-ttu-id="005ca-101">New-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="005ca-101">New-AzSqlSyncAgent</span></span>

## <span data-ttu-id="005ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="005ca-102">SYNOPSIS</span></span>
<span data-ttu-id="005ca-103">Létrehoz egy Azure SQL Sync-ügynököt.</span><span class="sxs-lookup"><span data-stu-id="005ca-103">Creates an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="005ca-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="005ca-104">SYNTAX</span></span>

### <span data-ttu-id="005ca-105">SyncDatabaseComponent (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="005ca-105">SyncDatabaseComponent (Default)</span></span>
```
New-AzSqlSyncAgent [-Name] <String> -SyncDatabaseName <String> [-SyncDatabaseServerName <String>]
 [-SyncDatabaseResourceGroupName <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="005ca-106">SyncDatabaseResourceID</span><span class="sxs-lookup"><span data-stu-id="005ca-106">SyncDatabaseResourceID</span></span>
```
New-AzSqlSyncAgent [-Name] <String> -SyncDatabaseResourceID <String> [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="005ca-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="005ca-107">DESCRIPTION</span></span>
<span data-ttu-id="005ca-108">A **New-AzSqlSyncAgent** parancsmag létrehoz egy Azure SQL Sync-ügynököt.</span><span class="sxs-lookup"><span data-stu-id="005ca-108">The **New-AzSqlSyncAgent** cmdlet creates an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="005ca-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="005ca-109">EXAMPLES</span></span>

### <span data-ttu-id="005ca-110">1. példa: Szinkronizálási ügynök létrehozása Azure SQL-kiszolgálóhoz.</span><span class="sxs-lookup"><span data-stu-id="005ca-110">Example 1: Create a sync agent for an Azure SQL server.</span></span>
```
PS C:\> New-AzSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -Name "SyncAgent01" -SyncDatabaseServerName "syncDatabaseServer01" 
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

<span data-ttu-id="005ca-111">Ez a parancs szinkronizálási ügynököt hoz létre egy Azure SQL-kiszolgálóhoz.</span><span class="sxs-lookup"><span data-stu-id="005ca-111">This command creates a sync agent for an Azure SQL server.</span></span>

## <span data-ttu-id="005ca-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="005ca-112">PARAMETERS</span></span>

### <span data-ttu-id="005ca-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="005ca-113">-DefaultProfile</span></span>
<span data-ttu-id="005ca-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="005ca-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="005ca-115">-Name</span><span class="sxs-lookup"><span data-stu-id="005ca-115">-Name</span></span>
<span data-ttu-id="005ca-116">A szinkronizálási ügynök neve.</span><span class="sxs-lookup"><span data-stu-id="005ca-116">The sync agent name.</span></span>

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

### <span data-ttu-id="005ca-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="005ca-117">-ResourceGroupName</span></span>
<span data-ttu-id="005ca-118">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="005ca-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="005ca-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="005ca-119">-ServerName</span></span>
<span data-ttu-id="005ca-120">Annak az Azure SQL Servernek a neve, amelyben a szinkronizálási ügynök található.</span><span class="sxs-lookup"><span data-stu-id="005ca-120">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="005ca-121">-SyncDatabaseName</span><span class="sxs-lookup"><span data-stu-id="005ca-121">-SyncDatabaseName</span></span>
<span data-ttu-id="005ca-122">A szinkronizálással kapcsolatos metaadatok tárolására használt adatbázis.</span><span class="sxs-lookup"><span data-stu-id="005ca-122">The database used to store sync related metadata.</span></span>

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

### <span data-ttu-id="005ca-123">-SyncDatabaseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="005ca-123">-SyncDatabaseResourceGroupName</span></span>
<span data-ttu-id="005ca-124">Az erőforráscsoport, amelyhez a szinkronizálási metaadat-adatbázis tartozik.</span><span class="sxs-lookup"><span data-stu-id="005ca-124">The resource group the sync metadata database belongs to.</span></span>

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

### <span data-ttu-id="005ca-125">-SyncDatabaseResourceID</span><span class="sxs-lookup"><span data-stu-id="005ca-125">-SyncDatabaseResourceID</span></span>
<span data-ttu-id="005ca-126">A szinkronizálási metaadat-adatbázis erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="005ca-126">The resource ID of  the sync metadata database.</span></span>

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

### <span data-ttu-id="005ca-127">-SyncDatabaseServerName</span><span class="sxs-lookup"><span data-stu-id="005ca-127">-SyncDatabaseServerName</span></span>
<span data-ttu-id="005ca-128">Az a kiszolgáló, amelyen a szinkronizálási metaadat-adatbázis található.</span><span class="sxs-lookup"><span data-stu-id="005ca-128">The server on which the sync metadata database is hosted.</span></span>

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

### <span data-ttu-id="005ca-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="005ca-129">-Confirm</span></span>
<span data-ttu-id="005ca-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="005ca-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="005ca-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="005ca-131">-WhatIf</span></span>
<span data-ttu-id="005ca-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="005ca-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="005ca-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="005ca-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="005ca-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="005ca-134">CommonParameters</span></span>
<span data-ttu-id="005ca-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="005ca-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="005ca-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="005ca-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="005ca-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="005ca-137">INPUTS</span></span>

### <span data-ttu-id="005ca-138">System.String</span><span class="sxs-lookup"><span data-stu-id="005ca-138">System.String</span></span>

## <span data-ttu-id="005ca-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="005ca-139">OUTPUTS</span></span>

### <span data-ttu-id="005ca-140">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span><span class="sxs-lookup"><span data-stu-id="005ca-140">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="005ca-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="005ca-141">NOTES</span></span>

## <span data-ttu-id="005ca-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="005ca-142">RELATED LINKS</span></span>

[<span data-ttu-id="005ca-143">Remove-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="005ca-143">Remove-AzSqlSyncAgent</span></span>](./Remove-AzSqlSyncAgent.md)

[<span data-ttu-id="005ca-144">Get-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="005ca-144">Get-AzSqlSyncAgent</span></span>](./Get-AzSqlSyncAgent.md)

