---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Update-AzureRmSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Update-AzureRmSqlSyncGroup.md
ms.openlocfilehash: a530a9e99c698ca6b827df94b1966e4df065790d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499935"
---
# <span data-ttu-id="e3fb2-101">Update-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="e3fb2-101">Update-AzureRmSqlSyncGroup</span></span>

## <span data-ttu-id="e3fb2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e3fb2-102">SYNOPSIS</span></span>
<span data-ttu-id="e3fb2-103">Egy Azure SQL-adatbázis szinkronizálási csoportjának frissítése</span><span class="sxs-lookup"><span data-stu-id="e3fb2-103">Updates an Azure SQL Database Sync Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3fb2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e3fb2-104">SYNTAX</span></span>

```
Update-AzureRmSqlSyncGroup [-Name] <String> [-IntervalInSeconds <Int32>] [-DatabaseCredential <PSCredential>]
 [-SchemaFile <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3fb2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e3fb2-105">DESCRIPTION</span></span>
<span data-ttu-id="e3fb2-106">Az **Update-AzureRmSqlSyncGroup** parancsmag az Azure SQL-adatbázisok szinkronizálási csoportjának tulajdonságait módosítja.</span><span class="sxs-lookup"><span data-stu-id="e3fb2-106">The **Update-AzureRmSqlSyncGroup** cmdlet modifies properties of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="e3fb2-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e3fb2-107">EXAMPLES</span></span>

### <span data-ttu-id="e3fb2-108">1. példa: az Azure SQL-adatbázisok szinkronizálási csoportjának frissítése.</span><span class="sxs-lookup"><span data-stu-id="e3fb2-108">Example 1: Update a sync group for an Azure SQL Database.</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> Update-AzureRmSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -Name "SyncGroup01"
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

<span data-ttu-id="e3fb2-109">Ez a parancs frissíti az Azure SQL-adatbázisok szinkronizálási csoportját.</span><span class="sxs-lookup"><span data-stu-id="e3fb2-109">This command updates a sync group for an Azure SQL Database.</span></span> <span data-ttu-id="e3fb2-110">A "schema.jsbe" szó a helyi lemezen lévő fájl.</span><span class="sxs-lookup"><span data-stu-id="e3fb2-110">"schema.json" is a file in the local disk.</span></span> <span data-ttu-id="e3fb2-111">A shema-adattartalmat JSON formátumban tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="e3fb2-111">It contains the shema payload in json format.</span></span> <span data-ttu-id="e3fb2-112">A JSON-as séma példája: {"Tables": [{"Columns": [{"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}]; "QuotedName": "MayQuotedTable1"}; {"Columns": [{"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}; {"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"</span><span class="sxs-lookup"><span data-stu-id="e3fb2-112">An example of the schema json is: {"Tables":  [{"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable1"}, {"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable2"}], "MasterSyncMemberName":  null }</span></span>

## <span data-ttu-id="e3fb2-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e3fb2-113">PARAMETERS</span></span>

### <span data-ttu-id="e3fb2-114">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e3fb2-114">-Confirm</span></span>
<span data-ttu-id="e3fb2-115">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e3fb2-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3fb2-116">-DatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="e3fb2-116">-DatabaseCredential</span></span>
<span data-ttu-id="e3fb2-117">A hub-adatbázis SQL-hitelesítési hitelesítő adatai.</span><span class="sxs-lookup"><span data-stu-id="e3fb2-117">The SQL authentication credential of the hub database.</span></span>

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

### <span data-ttu-id="e3fb2-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e3fb2-118">-DatabaseName</span></span>
<span data-ttu-id="e3fb2-119">SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="e3fb2-119">SQL Database name.</span></span>

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

### <span data-ttu-id="e3fb2-120">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="e3fb2-120">-IntervalInSeconds</span></span>
<span data-ttu-id="e3fb2-121">Az adatok szinkronizálásának gyakorisága (másodpercben).</span><span class="sxs-lookup"><span data-stu-id="e3fb2-121">The frequency (in seconds) of doing data synchronization.</span></span>
<span data-ttu-id="e3fb2-122">Az alapértelmezett érték a-1, ami azt jelenti, hogy az automatikus szinkronizálás nincs engedélyezve.</span><span class="sxs-lookup"><span data-stu-id="e3fb2-122">Default is -1, which means the auto synchronization is not enabled.</span></span>

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

### <span data-ttu-id="e3fb2-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e3fb2-123">-Name</span></span>
<span data-ttu-id="e3fb2-124">A szinkronizálási csoport neve.</span><span class="sxs-lookup"><span data-stu-id="e3fb2-124">The sync group name.</span></span>

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

### <span data-ttu-id="e3fb2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3fb2-125">-ResourceGroupName</span></span>
<span data-ttu-id="e3fb2-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e3fb2-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="e3fb2-127">-SchemaFile</span><span class="sxs-lookup"><span data-stu-id="e3fb2-127">-SchemaFile</span></span>
<span data-ttu-id="e3fb2-128">A sémafájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="e3fb2-128">The path of the schema file.</span></span>

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

### <span data-ttu-id="e3fb2-129">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="e3fb2-129">-ServerName</span></span>
<span data-ttu-id="e3fb2-130">Az Azure SQL Server neve.</span><span class="sxs-lookup"><span data-stu-id="e3fb2-130">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="e3fb2-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3fb2-131">-WhatIf</span></span>
<span data-ttu-id="e3fb2-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e3fb2-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3fb2-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e3fb2-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3fb2-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3fb2-134">-DefaultProfile</span></span>
<span data-ttu-id="e3fb2-135">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e3fb2-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3fb2-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3fb2-136">CommonParameters</span></span>
<span data-ttu-id="e3fb2-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e3fb2-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3fb2-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3fb2-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3fb2-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e3fb2-139">INPUTS</span></span>

## <span data-ttu-id="e3fb2-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e3fb2-140">OUTPUTS</span></span>

### <span data-ttu-id="e3fb2-141">Microsoft. Azure. Command. SQL. DataSync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="e3fb2-141">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="e3fb2-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e3fb2-142">NOTES</span></span>

## <span data-ttu-id="e3fb2-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e3fb2-143">RELATED LINKS</span></span>

[<span data-ttu-id="e3fb2-144">Új – AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="e3fb2-144">New-AzureRmSqlSyncGroup</span></span>](./New-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="e3fb2-145">Remove-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="e3fb2-145">Remove-AzureRmSqlSyncGroup</span></span>](./Remove-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="e3fb2-146">Get-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="e3fb2-146">Get-AzureRmSqlSyncGroup</span></span>](./Get-AzureRmSqlSyncGroup.md)

