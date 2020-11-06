---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncGroup.md
ms.openlocfilehash: 9df59edf3b73597e639e49a13265468b495fe4d3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498187"
---
# <span data-ttu-id="a5443-101">New-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="a5443-101">New-AzureRmSqlSyncGroup</span></span>

## <span data-ttu-id="a5443-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a5443-102">SYNOPSIS</span></span>
<span data-ttu-id="a5443-103">Azure SQL-adatbázis szinkronizálási csoportját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="a5443-103">Creates an Azure SQL Database Sync Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5443-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a5443-104">SYNTAX</span></span>

```
New-AzureRmSqlSyncGroup [-Name] <String> -SyncDatabaseName <String> -SyncDatabaseServerName <String>
 -SyncDatabaseResourceGroupName <String> [-IntervalInSeconds <Int32>] [-DatabaseCredential <PSCredential>]
 [-ConflictResolutionPolicy <String>] [-SchemaFile <String>] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a5443-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a5443-105">DESCRIPTION</span></span>
<span data-ttu-id="a5443-106">A **New-AzureRmSqlSyncGroup** parancsmag egy Azure SQL-adatbázis szinkronizálási csoportját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="a5443-106">The **New-AzureRmSqlSyncGroup** cmdlet creates an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="a5443-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a5443-107">EXAMPLES</span></span>

### <span data-ttu-id="a5443-108">1. példa: szinkronizálási csoport létrehozása Azure SQL-adatbázishoz.</span><span class="sxs-lookup"><span data-stu-id="a5443-108">Example 1: Create a sync group for an Azure SQL Database.</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> New-AzureRmSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -Name "SyncGroup01" -ConflictResolutionPolicy "HubWin"
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

<span data-ttu-id="a5443-109">Ez a parancs létrehoz egy szinkronizálási csoportot egy Azure SQL-adatbázishoz.</span><span class="sxs-lookup"><span data-stu-id="a5443-109">This command creates a sync group for an Azure SQL Database.</span></span> <span data-ttu-id="a5443-110">A "schema.jsbe" szó a helyi lemezen lévő fájl.</span><span class="sxs-lookup"><span data-stu-id="a5443-110">"schema.json" is a file in the local disk.</span></span> <span data-ttu-id="a5443-111">A shema-adattartalmat JSON formátumban tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="a5443-111">It contains the shema payload in json format.</span></span> <span data-ttu-id="a5443-112">A JSON-as séma példája: {"Tables": [{"Columns": [{"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}]; "QuotedName": "MayQuotedTable1"}; {"Columns": [{"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}; {"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"</span><span class="sxs-lookup"><span data-stu-id="a5443-112">An example of the schema json is: {"Tables":  [{"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable1"}, {"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable2"}], "MasterSyncMemberName":  null }</span></span>

## <span data-ttu-id="a5443-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a5443-113">PARAMETERS</span></span>

### <span data-ttu-id="a5443-114">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="a5443-114">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="a5443-115">A csomópont és a tagok adatbázisa közötti ütközés feloldására szolgáló házirend a szinkronizálás csoportban.</span><span class="sxs-lookup"><span data-stu-id="a5443-115">The policy of resolving confliction between hub and member database in the sync group.</span></span>

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

### <span data-ttu-id="a5443-116">-DatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="a5443-116">-DatabaseCredential</span></span>
<span data-ttu-id="a5443-117">A hub-adatbázis SQL-hitelesítési hitelesítő adatai.</span><span class="sxs-lookup"><span data-stu-id="a5443-117">The SQL authentication credential of the hub database.</span></span>

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

### <span data-ttu-id="a5443-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a5443-118">-DatabaseName</span></span>
<span data-ttu-id="a5443-119">Az Azure SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="a5443-119">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="a5443-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5443-120">-DefaultProfile</span></span>
<span data-ttu-id="a5443-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a5443-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a5443-122">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="a5443-122">-IntervalInSeconds</span></span>
<span data-ttu-id="a5443-123">Az adatok szinkronizálásának gyakorisága (másodpercben).</span><span class="sxs-lookup"><span data-stu-id="a5443-123">The frequency (in seconds) of doing data synchronization.</span></span>
<span data-ttu-id="a5443-124">Az alapértelmezett érték a-1, ami azt jelenti, hogy az automatikus szinkronizálás nincs engedélyezve.</span><span class="sxs-lookup"><span data-stu-id="a5443-124">Default is -1, which means the auto synchronization is not enabled.</span></span>

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

### <span data-ttu-id="a5443-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a5443-125">-Name</span></span>
<span data-ttu-id="a5443-126">A szinkronizálási csoport neve.</span><span class="sxs-lookup"><span data-stu-id="a5443-126">The sync group name.</span></span>

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

### <span data-ttu-id="a5443-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5443-127">-ResourceGroupName</span></span>
<span data-ttu-id="a5443-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a5443-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="a5443-129">-SchemaFile</span><span class="sxs-lookup"><span data-stu-id="a5443-129">-SchemaFile</span></span>
<span data-ttu-id="a5443-130">A sémafájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="a5443-130">The path of the schema file.</span></span>

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

### <span data-ttu-id="a5443-131">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="a5443-131">-ServerName</span></span>
<span data-ttu-id="a5443-132">Az Azure SQL Server neve.</span><span class="sxs-lookup"><span data-stu-id="a5443-132">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="a5443-133">-SyncDatabaseName</span><span class="sxs-lookup"><span data-stu-id="a5443-133">-SyncDatabaseName</span></span>
<span data-ttu-id="a5443-134">A szinkronizáláshoz kapcsolódó metaadatok tárolására szolgáló adatbázis.</span><span class="sxs-lookup"><span data-stu-id="a5443-134">The database used to store sync related metadata.</span></span>

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

### <span data-ttu-id="a5443-135">-SyncDatabaseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5443-135">-SyncDatabaseResourceGroupName</span></span>
<span data-ttu-id="a5443-136">Az erőforráscsoport, amelyre a szinkronizálási metaadat-adatbázis tartozik.</span><span class="sxs-lookup"><span data-stu-id="a5443-136">The resource group the sync metadata database belongs to.</span></span>

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

### <span data-ttu-id="a5443-137">-SyncDatabaseServerName</span><span class="sxs-lookup"><span data-stu-id="a5443-137">-SyncDatabaseServerName</span></span>
<span data-ttu-id="a5443-138">Az a kiszolgáló, amelyen a szinkronizálási metaadat-adatbázis található.</span><span class="sxs-lookup"><span data-stu-id="a5443-138">The server on which the sync metadata database is hosted.</span></span>

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

### <span data-ttu-id="a5443-139">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a5443-139">-Confirm</span></span>
<span data-ttu-id="a5443-140">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a5443-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5443-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5443-141">-WhatIf</span></span>
<span data-ttu-id="a5443-142">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a5443-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5443-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a5443-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5443-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5443-144">CommonParameters</span></span>
<span data-ttu-id="a5443-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a5443-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5443-146">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5443-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5443-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a5443-147">INPUTS</span></span>

### <span data-ttu-id="a5443-148">System. String</span><span class="sxs-lookup"><span data-stu-id="a5443-148">System.String</span></span>

## <span data-ttu-id="a5443-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a5443-149">OUTPUTS</span></span>

### <span data-ttu-id="a5443-150">Microsoft. Azure. Command. SQL. DataSync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="a5443-150">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="a5443-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a5443-151">NOTES</span></span>

## <span data-ttu-id="a5443-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a5443-152">RELATED LINKS</span></span>

[<span data-ttu-id="a5443-153">Set-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="a5443-153">Set-AzureRmSqlSyncGroup</span></span>](./Set-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="a5443-154">Remove-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="a5443-154">Remove-AzureRmSqlSyncGroup</span></span>](./Remove-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="a5443-155">Get-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="a5443-155">Get-AzureRmSqlSyncGroup</span></span>](./Get-AzureRmSqlSyncGroup.md)

