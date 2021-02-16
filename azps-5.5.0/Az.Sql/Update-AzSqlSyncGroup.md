---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/update-azsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncGroup.md
ms.openlocfilehash: 9c4a6572a5a2025bba23758160378519524b8ce7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100155178"
---
# <span data-ttu-id="7a872-101">Update-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="7a872-101">Update-AzSqlSyncGroup</span></span>

## <span data-ttu-id="7a872-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a872-102">SYNOPSIS</span></span>
<span data-ttu-id="7a872-103">Frissíti az Azure SQL Database Sync-csoportot.</span><span class="sxs-lookup"><span data-stu-id="7a872-103">Updates an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="7a872-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7a872-104">SYNTAX</span></span>

```
Update-AzSqlSyncGroup [-Name] <String> [-IntervalInSeconds <Int32>] [-DatabaseCredential <PSCredential>]
 [-SchemaFile <String>] [-UsePrivateLinkConnection <Boolean>] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7a872-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7a872-105">DESCRIPTION</span></span>
<span data-ttu-id="7a872-106">Az **Update-AzSqlSyncGroup** parancsmag módosítja egy Azure SQL Database Sync-csoport tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="7a872-106">The **Update-AzSqlSyncGroup** cmdlet modifies properties of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="7a872-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7a872-107">EXAMPLES</span></span>

### <span data-ttu-id="7a872-108">1. példa: Azure SQL-adatbázis szinkronizálási csoportjának frissítése.</span><span class="sxs-lookup"><span data-stu-id="7a872-108">Example 1: Update a sync group for an Azure SQL Database.</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> Update-AzSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -Name "SyncGroup01"
-DatabaseCredential $credential -IntervalInSeconds 100 -Schema ".\schema.json" | Format-List
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

<span data-ttu-id="7a872-109">Ez a parancs frissíti egy Azure SQL-adatbázis szinkronizálási csoportját.</span><span class="sxs-lookup"><span data-stu-id="7a872-109">This command updates a sync group for an Azure SQL Database.</span></span> <span data-ttu-id="7a872-110">A "schema.jsbe" egy helyi lemezen lévő fájl.</span><span class="sxs-lookup"><span data-stu-id="7a872-110">"schema.json" is a file in the local disk.</span></span> <span data-ttu-id="7a872-111">A séma hasznos terhelését tartalmazza json formátumban.</span><span class="sxs-lookup"><span data-stu-id="7a872-111">It contains the schema payload in json format.</span></span> <span data-ttu-id="7a872-112">A json séma példája a következő: {"Tables": [{"Columns": [{"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName": "MayQuotedTable1"}, {"Oszlopok": [{"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName": "MayQuotedTable2"}], "MasterSyncMemberName": null }</span><span class="sxs-lookup"><span data-stu-id="7a872-112">An example of the schema json is: {"Tables":  [{"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable1"}, {"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable2"}], "MasterSyncMemberName":  null }</span></span>

## <span data-ttu-id="7a872-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7a872-113">PARAMETERS</span></span>

### <span data-ttu-id="7a872-114">-DatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="7a872-114">-DatabaseCredential</span></span>
<span data-ttu-id="7a872-115">A központi adatbázis SQL-hitelesítési hitelesítő adatai.</span><span class="sxs-lookup"><span data-stu-id="7a872-115">The SQL authentication credential of the hub database.</span></span>

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

### <span data-ttu-id="7a872-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7a872-116">-DatabaseName</span></span>
<span data-ttu-id="7a872-117">SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="7a872-117">SQL Database name.</span></span>

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

### <span data-ttu-id="7a872-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a872-118">-DefaultProfile</span></span>
<span data-ttu-id="7a872-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="7a872-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7a872-120">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="7a872-120">-IntervalInSeconds</span></span>
<span data-ttu-id="7a872-121">Az adatszinkronizálás gyakorisága (másodpercben).</span><span class="sxs-lookup"><span data-stu-id="7a872-121">The frequency (in seconds) of doing data synchronization.</span></span>
<span data-ttu-id="7a872-122">Az alapértelmezett érték -1, ami azt jelenti, hogy az automatikus szinkronizálás nincs engedélyezve.</span><span class="sxs-lookup"><span data-stu-id="7a872-122">Default is -1, which means the auto synchronization is not enabled.</span></span>

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

### <span data-ttu-id="7a872-123">-Name</span><span class="sxs-lookup"><span data-stu-id="7a872-123">-Name</span></span>
<span data-ttu-id="7a872-124">A szinkronizálási csoport neve.</span><span class="sxs-lookup"><span data-stu-id="7a872-124">The sync group name.</span></span>

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

### <span data-ttu-id="7a872-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a872-125">-ResourceGroupName</span></span>
<span data-ttu-id="7a872-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="7a872-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="7a872-127">-SchemaFile</span><span class="sxs-lookup"><span data-stu-id="7a872-127">-SchemaFile</span></span>
<span data-ttu-id="7a872-128">A sémafájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="7a872-128">The path of the schema file.</span></span>

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

### <span data-ttu-id="7a872-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7a872-129">-ServerName</span></span>
<span data-ttu-id="7a872-130">Az Azure SQL Server neve.</span><span class="sxs-lookup"><span data-stu-id="7a872-130">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="7a872-131">-UsePrivateLinkConnection</span><span class="sxs-lookup"><span data-stu-id="7a872-131">-UsePrivateLinkConnection</span></span>
<span data-ttu-id="7a872-132">Privát kapcsolat használata a szinkronizálási csoport központjához való csatlakozáskor.</span><span class="sxs-lookup"><span data-stu-id="7a872-132">Whether to use a private link connection when connecting to the hub of this sync group.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a872-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7a872-133">-Confirm</span></span>
<span data-ttu-id="7a872-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7a872-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a872-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a872-135">-WhatIf</span></span>
<span data-ttu-id="7a872-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7a872-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a872-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7a872-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a872-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a872-138">CommonParameters</span></span>
<span data-ttu-id="7a872-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a872-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a872-140">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7a872-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a872-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7a872-141">INPUTS</span></span>

### <span data-ttu-id="7a872-142">System.String</span><span class="sxs-lookup"><span data-stu-id="7a872-142">System.String</span></span>

## <span data-ttu-id="7a872-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7a872-143">OUTPUTS</span></span>

### <span data-ttu-id="7a872-144">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="7a872-144">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="7a872-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7a872-145">NOTES</span></span>

## <span data-ttu-id="7a872-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7a872-146">RELATED LINKS</span></span>

[<span data-ttu-id="7a872-147">New-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="7a872-147">New-AzSqlSyncGroup</span></span>](./New-AzSqlSyncGroup.md)

[<span data-ttu-id="7a872-148">Remove-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="7a872-148">Remove-AzSqlSyncGroup</span></span>](./Remove-AzSqlSyncGroup.md)

[<span data-ttu-id="7a872-149">Get-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="7a872-149">Get-AzSqlSyncGroup</span></span>](./Get-AzSqlSyncGroup.md)

