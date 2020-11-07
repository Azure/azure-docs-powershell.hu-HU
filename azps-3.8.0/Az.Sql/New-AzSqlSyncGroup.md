---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncGroup.md
ms.openlocfilehash: 7dc408b757c2bce197fcc6dd366c4ef64484eccf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845181"
---
# <span data-ttu-id="6be51-101">New-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="6be51-101">New-AzSqlSyncGroup</span></span>

## <span data-ttu-id="6be51-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6be51-102">SYNOPSIS</span></span>
<span data-ttu-id="6be51-103">Azure SQL-adatbázis szinkronizálási csoportját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="6be51-103">Creates an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="6be51-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6be51-104">SYNTAX</span></span>

```
New-AzSqlSyncGroup [-Name] <String> -SyncDatabaseName <String> -SyncDatabaseServerName <String>
 -SyncDatabaseResourceGroupName <String> [-IntervalInSeconds <Int32>] [-DatabaseCredential <PSCredential>]
 [-ConflictResolutionPolicy <String>] [-SchemaFile <String>] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6be51-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6be51-105">DESCRIPTION</span></span>
<span data-ttu-id="6be51-106">A **New-AzSqlSyncGroup** parancsmag egy Azure SQL-adatbázis szinkronizálási csoportját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="6be51-106">The **New-AzSqlSyncGroup** cmdlet creates an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="6be51-107">Példák</span><span class="sxs-lookup"><span data-stu-id="6be51-107">EXAMPLES</span></span>

### <span data-ttu-id="6be51-108">1. példa: szinkronizálási csoport létrehozása Azure SQL-adatbázishoz.</span><span class="sxs-lookup"><span data-stu-id="6be51-108">Example 1: Create a sync group for an Azure SQL Database.</span></span>
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

<span data-ttu-id="6be51-109">Ez a parancs létrehoz egy szinkronizálási csoportot egy Azure SQL-adatbázishoz.</span><span class="sxs-lookup"><span data-stu-id="6be51-109">This command creates a sync group for an Azure SQL Database.</span></span> <span data-ttu-id="6be51-110">A "schema.jsbe" szó a helyi lemezen lévő fájl.</span><span class="sxs-lookup"><span data-stu-id="6be51-110">"schema.json" is a file in the local disk.</span></span> <span data-ttu-id="6be51-111">A séma tartalma JSON formátumban található.</span><span class="sxs-lookup"><span data-stu-id="6be51-111">It contains the schema payload in json format.</span></span> <span data-ttu-id="6be51-112">A JSON-as séma példája: {"Tables": [{"Columns": [{"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}]; "QuotedName": "MayQuotedTable1"}; {"Columns": [{"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}; {"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"</span><span class="sxs-lookup"><span data-stu-id="6be51-112">An example of the schema json is: {"Tables":  [{"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable1"}, {"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable2"}], "MasterSyncMemberName":  null }</span></span>

## <span data-ttu-id="6be51-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6be51-113">PARAMETERS</span></span>

### <span data-ttu-id="6be51-114">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="6be51-114">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="6be51-115">A szinkronizálás csoport központi és tagsági adatbázisa közötti ütközések feloldására szolgáló házirend.</span><span class="sxs-lookup"><span data-stu-id="6be51-115">The policy of resolving conflicts between hub and member database in the sync group.</span></span>

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

### <span data-ttu-id="6be51-116">-DatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="6be51-116">-DatabaseCredential</span></span>
<span data-ttu-id="6be51-117">A hub-adatbázis SQL-hitelesítési hitelesítő adatai.</span><span class="sxs-lookup"><span data-stu-id="6be51-117">The SQL authentication credential of the hub database.</span></span>

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

### <span data-ttu-id="6be51-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6be51-118">-DatabaseName</span></span>
<span data-ttu-id="6be51-119">Az Azure SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="6be51-119">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="6be51-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6be51-120">-DefaultProfile</span></span>
<span data-ttu-id="6be51-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="6be51-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6be51-122">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="6be51-122">-IntervalInSeconds</span></span>
<span data-ttu-id="6be51-123">Az adatok szinkronizálásának gyakorisága (másodpercben).</span><span class="sxs-lookup"><span data-stu-id="6be51-123">The frequency (in seconds) of doing data synchronization.</span></span>
<span data-ttu-id="6be51-124">Az alapértelmezett érték a-1, ami azt jelenti, hogy az automatikus szinkronizálás nincs engedélyezve.</span><span class="sxs-lookup"><span data-stu-id="6be51-124">Default is -1, which means the auto synchronization is not enabled.</span></span>

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

### <span data-ttu-id="6be51-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6be51-125">-Name</span></span>
<span data-ttu-id="6be51-126">A szinkronizálási csoport neve.</span><span class="sxs-lookup"><span data-stu-id="6be51-126">The sync group name.</span></span>

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

### <span data-ttu-id="6be51-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6be51-127">-ResourceGroupName</span></span>
<span data-ttu-id="6be51-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6be51-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="6be51-129">-SchemaFile</span><span class="sxs-lookup"><span data-stu-id="6be51-129">-SchemaFile</span></span>
<span data-ttu-id="6be51-130">A sémafájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="6be51-130">The path of the schema file.</span></span>

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

### <span data-ttu-id="6be51-131">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="6be51-131">-ServerName</span></span>
<span data-ttu-id="6be51-132">Az Azure SQL Server neve.</span><span class="sxs-lookup"><span data-stu-id="6be51-132">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="6be51-133">-SyncDatabaseName</span><span class="sxs-lookup"><span data-stu-id="6be51-133">-SyncDatabaseName</span></span>
<span data-ttu-id="6be51-134">A szinkronizáláshoz kapcsolódó metaadatok tárolására szolgáló adatbázis.</span><span class="sxs-lookup"><span data-stu-id="6be51-134">The database used to store sync related metadata.</span></span>

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

### <span data-ttu-id="6be51-135">-SyncDatabaseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6be51-135">-SyncDatabaseResourceGroupName</span></span>
<span data-ttu-id="6be51-136">Az erőforráscsoport, amelyre a szinkronizálási metaadat-adatbázis tartozik.</span><span class="sxs-lookup"><span data-stu-id="6be51-136">The resource group the sync metadata database belongs to.</span></span>

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

### <span data-ttu-id="6be51-137">-SyncDatabaseServerName</span><span class="sxs-lookup"><span data-stu-id="6be51-137">-SyncDatabaseServerName</span></span>
<span data-ttu-id="6be51-138">Az a kiszolgáló, amelyen a szinkronizálási metaadat-adatbázis található.</span><span class="sxs-lookup"><span data-stu-id="6be51-138">The server on which the sync metadata database is hosted.</span></span>

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

### <span data-ttu-id="6be51-139">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6be51-139">-Confirm</span></span>
<span data-ttu-id="6be51-140">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6be51-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6be51-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6be51-141">-WhatIf</span></span>
<span data-ttu-id="6be51-142">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6be51-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6be51-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6be51-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6be51-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6be51-144">CommonParameters</span></span>
<span data-ttu-id="6be51-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6be51-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6be51-146">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="6be51-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6be51-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6be51-147">INPUTS</span></span>

### <span data-ttu-id="6be51-148">System. String</span><span class="sxs-lookup"><span data-stu-id="6be51-148">System.String</span></span>

## <span data-ttu-id="6be51-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6be51-149">OUTPUTS</span></span>

### <span data-ttu-id="6be51-150">Microsoft. Azure. Command. SQL. DataSync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="6be51-150">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="6be51-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6be51-151">NOTES</span></span>

## <span data-ttu-id="6be51-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6be51-152">RELATED LINKS</span></span>

[<span data-ttu-id="6be51-153">Set-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="6be51-153">Set-AzSqlSyncGroup</span></span>](./Set-AzSqlSyncGroup.md)

[<span data-ttu-id="6be51-154">Remove-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="6be51-154">Remove-AzSqlSyncGroup</span></span>](./Remove-AzSqlSyncGroup.md)

[<span data-ttu-id="6be51-155">Get-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="6be51-155">Get-AzSqlSyncGroup</span></span>](./Get-AzSqlSyncGroup.md)

