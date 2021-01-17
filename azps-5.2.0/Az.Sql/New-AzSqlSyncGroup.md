---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncGroup.md
ms.openlocfilehash: d6964f076dd1e6882a8031f19101f55d19b9e4d4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361506"
---
# <span data-ttu-id="23d3a-101">New-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="23d3a-101">New-AzSqlSyncGroup</span></span>

## <span data-ttu-id="23d3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23d3a-102">SYNOPSIS</span></span>
<span data-ttu-id="23d3a-103">Létrehoz egy Azure SQL Database Sync-csoportot.</span><span class="sxs-lookup"><span data-stu-id="23d3a-103">Creates an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="23d3a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="23d3a-104">SYNTAX</span></span>

```
New-AzSqlSyncGroup [-Name] <String> -SyncDatabaseName <String> -SyncDatabaseServerName <String>
 -SyncDatabaseResourceGroupName <String> [-IntervalInSeconds <Int32>] [-DatabaseCredential <PSCredential>]
 [-ConflictResolutionPolicy <String>] [-SchemaFile <String>] [-UsePrivateLinkConnection] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23d3a-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="23d3a-105">DESCRIPTION</span></span>
<span data-ttu-id="23d3a-106">A **New-AzSqlSyncGroup** parancsmag létrehoz egy Azure SQL Database Sync-csoportot.</span><span class="sxs-lookup"><span data-stu-id="23d3a-106">The **New-AzSqlSyncGroup** cmdlet creates an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="23d3a-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="23d3a-107">EXAMPLES</span></span>

### <span data-ttu-id="23d3a-108">1. példa: Szinkronizálási csoport létrehozása Azure SQL-adatbázishoz.</span><span class="sxs-lookup"><span data-stu-id="23d3a-108">Example 1: Create a sync group for an Azure SQL Database.</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> New-AzSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -Name "SyncGroup01" -ConflictResolutionPolicy "HubWin"
-DatabaseCredential $credential -IntervalInSeconds 100 -SyncDatabaseServerName "syncDatabaseServer01" -SyncDatabaseName "syncDatabaseName01"
-SyncDatabaseResourceGroupName "syncDatabaseResourceGroup01" -Schema ".\schema.json" | Format-List
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
```

<span data-ttu-id="23d3a-109">Ez a parancs szinkronizálási csoportot hoz létre egy Azure SQL-adatbázishoz.</span><span class="sxs-lookup"><span data-stu-id="23d3a-109">This command creates a sync group for an Azure SQL Database.</span></span> <span data-ttu-id="23d3a-110">A "schema.jsbe" egy helyi lemezen lévő fájl.</span><span class="sxs-lookup"><span data-stu-id="23d3a-110">"schema.json" is a file in the local disk.</span></span> <span data-ttu-id="23d3a-111">A séma hasznos terhelését tartalmazza json formátumban.</span><span class="sxs-lookup"><span data-stu-id="23d3a-111">It contains the schema payload in json format.</span></span> <span data-ttu-id="23d3a-112">A json séma példája a következő: {"Tables": [{"Columns": [{"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName": "MayQuotedTable1"}, {"Oszlopok": [{"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName": "MayQuotedTable2"}], "MasterSyncMemberName": null }</span><span class="sxs-lookup"><span data-stu-id="23d3a-112">An example of the schema json is: {"Tables":  [{"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable1"}, {"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable2"}], "MasterSyncMemberName":  null }</span></span>

## <span data-ttu-id="23d3a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="23d3a-113">PARAMETERS</span></span>

### <span data-ttu-id="23d3a-114">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="23d3a-114">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="23d3a-115">A szinkronizálási csoport központi és tagadatbázisa közötti ütközések feloldására vonatkozó házirend.</span><span class="sxs-lookup"><span data-stu-id="23d3a-115">The policy of resolving conflicts between hub and member database in the sync group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: HubWin, MemberWin

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23d3a-116">-DatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="23d3a-116">-DatabaseCredential</span></span>
<span data-ttu-id="23d3a-117">A központi adatbázis SQL-hitelesítési hitelesítő adatai.</span><span class="sxs-lookup"><span data-stu-id="23d3a-117">The SQL authentication credential of the hub database.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23d3a-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="23d3a-118">-DatabaseName</span></span>
<span data-ttu-id="23d3a-119">Az Azure SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="23d3a-119">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="23d3a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23d3a-120">-DefaultProfile</span></span>
<span data-ttu-id="23d3a-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="23d3a-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="23d3a-122">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="23d3a-122">-IntervalInSeconds</span></span>
<span data-ttu-id="23d3a-123">Az adatszinkronizálás gyakorisága (másodpercben).</span><span class="sxs-lookup"><span data-stu-id="23d3a-123">The frequency (in seconds) of doing data synchronization.</span></span>
<span data-ttu-id="23d3a-124">Az alapértelmezett érték -1, ami azt jelenti, hogy az automatikus szinkronizálás nincs engedélyezve.</span><span class="sxs-lookup"><span data-stu-id="23d3a-124">Default is -1, which means the auto synchronization is not enabled.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23d3a-125">-Name</span><span class="sxs-lookup"><span data-stu-id="23d3a-125">-Name</span></span>
<span data-ttu-id="23d3a-126">A szinkronizálási csoport neve.</span><span class="sxs-lookup"><span data-stu-id="23d3a-126">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23d3a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23d3a-127">-ResourceGroupName</span></span>
<span data-ttu-id="23d3a-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="23d3a-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="23d3a-129">-SchemaFile</span><span class="sxs-lookup"><span data-stu-id="23d3a-129">-SchemaFile</span></span>
<span data-ttu-id="23d3a-130">A sémafájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="23d3a-130">The path of the schema file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23d3a-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="23d3a-131">-ServerName</span></span>
<span data-ttu-id="23d3a-132">Az Azure SQL Server neve.</span><span class="sxs-lookup"><span data-stu-id="23d3a-132">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="23d3a-133">-SyncDatabaseName</span><span class="sxs-lookup"><span data-stu-id="23d3a-133">-SyncDatabaseName</span></span>
<span data-ttu-id="23d3a-134">A szinkronizálással kapcsolatos metaadatok tárolására használt adatbázis.</span><span class="sxs-lookup"><span data-stu-id="23d3a-134">The database used to store sync related metadata.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23d3a-135">-SyncDatabaseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23d3a-135">-SyncDatabaseResourceGroupName</span></span>
<span data-ttu-id="23d3a-136">Az erőforráscsoport, amelyhez a szinkronizálási metaadat-adatbázis tartozik.</span><span class="sxs-lookup"><span data-stu-id="23d3a-136">The resource group the sync metadata database belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23d3a-137">-SyncDatabaseServerName</span><span class="sxs-lookup"><span data-stu-id="23d3a-137">-SyncDatabaseServerName</span></span>
<span data-ttu-id="23d3a-138">Az a kiszolgáló, amelyen a szinkronizálási metaadat-adatbázis található.</span><span class="sxs-lookup"><span data-stu-id="23d3a-138">The server on which the sync metadata database is hosted.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23d3a-139">-UsePrivateLinkConnection</span><span class="sxs-lookup"><span data-stu-id="23d3a-139">-UsePrivateLinkConnection</span></span>
<span data-ttu-id="23d3a-140">Ha a szinkronizálási csoport központjához csatlakozik, használjon privát csatolási kapcsolatot.</span><span class="sxs-lookup"><span data-stu-id="23d3a-140">Use a private link connection when connecting to the hub of this sync group.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23d3a-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="23d3a-141">-Confirm</span></span>
<span data-ttu-id="23d3a-142">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="23d3a-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23d3a-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23d3a-143">-WhatIf</span></span>
<span data-ttu-id="23d3a-144">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="23d3a-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23d3a-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="23d3a-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23d3a-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23d3a-146">CommonParameters</span></span>
<span data-ttu-id="23d3a-147">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23d3a-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23d3a-148">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="23d3a-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23d3a-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="23d3a-149">INPUTS</span></span>

### <span data-ttu-id="23d3a-150">System.String</span><span class="sxs-lookup"><span data-stu-id="23d3a-150">System.String</span></span>

## <span data-ttu-id="23d3a-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="23d3a-151">OUTPUTS</span></span>

### <span data-ttu-id="23d3a-152">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="23d3a-152">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="23d3a-153">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="23d3a-153">NOTES</span></span>

## <span data-ttu-id="23d3a-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="23d3a-154">RELATED LINKS</span></span>

[<span data-ttu-id="23d3a-155">Update-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="23d3a-155">Update-AzSqlSyncGroup</span></span>](./Update-AzSqlSyncGroup.md)

[<span data-ttu-id="23d3a-156">Remove-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="23d3a-156">Remove-AzSqlSyncGroup</span></span>](./Remove-AzSqlSyncGroup.md)

[<span data-ttu-id="23d3a-157">Get-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="23d3a-157">Get-AzSqlSyncGroup</span></span>](./Get-AzSqlSyncGroup.md)

