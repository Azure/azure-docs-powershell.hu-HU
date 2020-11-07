---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/update-azsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncGroup.md
ms.openlocfilehash: cef62c85f42c2c9f0e6fbda776c58d6818659474
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846441"
---
# <span data-ttu-id="2d9b9-101">Update-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="2d9b9-101">Update-AzSqlSyncGroup</span></span>

## <span data-ttu-id="2d9b9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2d9b9-102">SYNOPSIS</span></span>
<span data-ttu-id="2d9b9-103">Egy Azure SQL-adatbázis szinkronizálási csoportjának frissítése</span><span class="sxs-lookup"><span data-stu-id="2d9b9-103">Updates an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="2d9b9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2d9b9-104">SYNTAX</span></span>

```
Update-AzSqlSyncGroup [-Name] <String> [-IntervalInSeconds <Int32>] [-DatabaseCredential <PSCredential>]
 [-SchemaFile <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d9b9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2d9b9-105">DESCRIPTION</span></span>
<span data-ttu-id="2d9b9-106">Az **Update-AzSqlSyncGroup** parancsmag az Azure SQL-adatbázisok szinkronizálási csoportjának tulajdonságait módosítja.</span><span class="sxs-lookup"><span data-stu-id="2d9b9-106">The **Update-AzSqlSyncGroup** cmdlet modifies properties of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="2d9b9-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2d9b9-107">EXAMPLES</span></span>

### <span data-ttu-id="2d9b9-108">1. példa: az Azure SQL-adatbázisok szinkronizálási csoportjának frissítése.</span><span class="sxs-lookup"><span data-stu-id="2d9b9-108">Example 1: Update a sync group for an Azure SQL Database.</span></span>
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

<span data-ttu-id="2d9b9-109">Ez a parancs frissíti az Azure SQL-adatbázisok szinkronizálási csoportját.</span><span class="sxs-lookup"><span data-stu-id="2d9b9-109">This command updates a sync group for an Azure SQL Database.</span></span> <span data-ttu-id="2d9b9-110">A "schema.jsbe" szó a helyi lemezen lévő fájl.</span><span class="sxs-lookup"><span data-stu-id="2d9b9-110">"schema.json" is a file in the local disk.</span></span> <span data-ttu-id="2d9b9-111">A séma tartalma JSON formátumban található.</span><span class="sxs-lookup"><span data-stu-id="2d9b9-111">It contains the schema payload in json format.</span></span> <span data-ttu-id="2d9b9-112">A JSON-as séma példája: {"Tables": [{"Columns": [{"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}]; "QuotedName": "MayQuotedTable1"}; {"Columns": [{"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}; {"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"</span><span class="sxs-lookup"><span data-stu-id="2d9b9-112">An example of the schema json is: {"Tables":  [{"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable1"}, {"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable2"}], "MasterSyncMemberName":  null }</span></span>

## <span data-ttu-id="2d9b9-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2d9b9-113">PARAMETERS</span></span>

### <span data-ttu-id="2d9b9-114">-DatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="2d9b9-114">-DatabaseCredential</span></span>
<span data-ttu-id="2d9b9-115">A hub-adatbázis SQL-hitelesítési hitelesítő adatai.</span><span class="sxs-lookup"><span data-stu-id="2d9b9-115">The SQL authentication credential of the hub database.</span></span>

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

### <span data-ttu-id="2d9b9-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2d9b9-116">-DatabaseName</span></span>
<span data-ttu-id="2d9b9-117">SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="2d9b9-117">SQL Database name.</span></span>

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

### <span data-ttu-id="2d9b9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d9b9-118">-DefaultProfile</span></span>
<span data-ttu-id="2d9b9-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="2d9b9-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2d9b9-120">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="2d9b9-120">-IntervalInSeconds</span></span>
<span data-ttu-id="2d9b9-121">Az adatok szinkronizálásának gyakorisága (másodpercben).</span><span class="sxs-lookup"><span data-stu-id="2d9b9-121">The frequency (in seconds) of doing data synchronization.</span></span>
<span data-ttu-id="2d9b9-122">Az alapértelmezett érték a-1, ami azt jelenti, hogy az automatikus szinkronizálás nincs engedélyezve.</span><span class="sxs-lookup"><span data-stu-id="2d9b9-122">Default is -1, which means the auto synchronization is not enabled.</span></span>

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

### <span data-ttu-id="2d9b9-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2d9b9-123">-Name</span></span>
<span data-ttu-id="2d9b9-124">A szinkronizálási csoport neve.</span><span class="sxs-lookup"><span data-stu-id="2d9b9-124">The sync group name.</span></span>

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

### <span data-ttu-id="2d9b9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d9b9-125">-ResourceGroupName</span></span>
<span data-ttu-id="2d9b9-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="2d9b9-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="2d9b9-127">-SchemaFile</span><span class="sxs-lookup"><span data-stu-id="2d9b9-127">-SchemaFile</span></span>
<span data-ttu-id="2d9b9-128">A sémafájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="2d9b9-128">The path of the schema file.</span></span>

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

### <span data-ttu-id="2d9b9-129">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="2d9b9-129">-ServerName</span></span>
<span data-ttu-id="2d9b9-130">Az Azure SQL Server neve.</span><span class="sxs-lookup"><span data-stu-id="2d9b9-130">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="2d9b9-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2d9b9-131">-Confirm</span></span>
<span data-ttu-id="2d9b9-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2d9b9-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d9b9-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d9b9-133">-WhatIf</span></span>
<span data-ttu-id="2d9b9-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2d9b9-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d9b9-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2d9b9-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d9b9-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d9b9-136">CommonParameters</span></span>
<span data-ttu-id="2d9b9-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2d9b9-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d9b9-138">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="2d9b9-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d9b9-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2d9b9-139">INPUTS</span></span>

### <span data-ttu-id="2d9b9-140">System. String</span><span class="sxs-lookup"><span data-stu-id="2d9b9-140">System.String</span></span>

## <span data-ttu-id="2d9b9-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2d9b9-141">OUTPUTS</span></span>

### <span data-ttu-id="2d9b9-142">Microsoft. Azure. Command. SQL. DataSync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="2d9b9-142">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="2d9b9-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2d9b9-143">NOTES</span></span>

## <span data-ttu-id="2d9b9-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2d9b9-144">RELATED LINKS</span></span>

[<span data-ttu-id="2d9b9-145">Új – AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="2d9b9-145">New-AzSqlSyncGroup</span></span>](./New-AzSqlSyncGroup.md)

[<span data-ttu-id="2d9b9-146">Remove-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="2d9b9-146">Remove-AzSqlSyncGroup</span></span>](./Remove-AzSqlSyncGroup.md)

[<span data-ttu-id="2d9b9-147">Get-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="2d9b9-147">Get-AzSqlSyncGroup</span></span>](./Get-AzSqlSyncGroup.md)

