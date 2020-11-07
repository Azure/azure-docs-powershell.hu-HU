---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAuditing.md
ms.openlocfilehash: ac1057159de6f3028bd599183dc5c411155f14e2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669044"
---
# <span data-ttu-id="ed2f9-101">Get-AzSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="ed2f9-101">Get-AzSqlDatabaseAuditing</span></span>

## <span data-ttu-id="ed2f9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ed2f9-102">SYNOPSIS</span></span>
<span data-ttu-id="ed2f9-103">Egy Azure SQL-adatbázis naplózási beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ed2f9-103">Gets the auditing settings of an Azure SQL database.</span></span>

## <span data-ttu-id="ed2f9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ed2f9-104">SYNTAX</span></span>

### <span data-ttu-id="ed2f9-105">DefaultParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ed2f9-105">DefaultParameterSet (Default)</span></span>
```
Get-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-BlobStorage] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed2f9-106">EventHubSet</span><span class="sxs-lookup"><span data-stu-id="ed2f9-106">EventHubSet</span></span>
```
Get-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-EventHub] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed2f9-107">LogAnalyticsSet</span><span class="sxs-lookup"><span data-stu-id="ed2f9-107">LogAnalyticsSet</span></span>
```
Get-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-LogAnalytics] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed2f9-108">BlobStorageByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="ed2f9-108">BlobStorageByParentResourceSet</span></span>
```
Get-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> [-BlobStorage]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed2f9-109">EventHubByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="ed2f9-109">EventHubByParentResourceSet</span></span>
```
Get-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> [-EventHub]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed2f9-110">LogAnalyticsByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="ed2f9-110">LogAnalyticsByParentResourceSet</span></span>
```
Get-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> [-LogAnalytics]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed2f9-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="ed2f9-111">DESCRIPTION</span></span>
<span data-ttu-id="ed2f9-112">A **Get-AzSqlDatabaseAuditing** parancsmag az Azure SQL-adatbázisok naplózási beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ed2f9-112">The **Get-AzSqlDatabaseAuditing** cmdlet gets the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="ed2f9-113">A parancsmag használatához a *ResourceGroupName* , a *kiszolgálónév* és a *databasename* paraméterrel keresse meg az adatbázist.</span><span class="sxs-lookup"><span data-stu-id="ed2f9-113">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="ed2f9-114">A naplók rendeltetési helyét az alábbi kapcsoló paraméterek egyikének megadásával határozhatja meg: BlobStorage, LogAnalytics vagy EventHub (ha nincs megadva, az alapértelmezett érték a BlobStorage).</span><span class="sxs-lookup"><span data-stu-id="ed2f9-114">The audit logs destination is determined by specifying one of the following switch parameters: BlobStorage, LogAnalytics or EventHub (if none is specified, the default is BlobStorage).</span></span>

## <span data-ttu-id="ed2f9-115">Példák</span><span class="sxs-lookup"><span data-stu-id="ed2f9-115">EXAMPLES</span></span>

### <span data-ttu-id="ed2f9-116">Példa 1: a blob-tároló naplózási beállításainak beszerzése Azure SQL-adatbázisból</span><span class="sxs-lookup"><span data-stu-id="ed2f9-116">Example 1: Get the blob storage auditing settings of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName                 : database01
AuditAction                  : {}
AuditActionGroup             : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                BATCH_COMPLETED_GROUP, ...}
ResourceGroupName            : resourcegroup01
ServerName                   : server01
AuditState                   : Enabled
StorageAccountName           : mystorage
StorageKeyType               : Primary
RetentionInDays              : 0
StorageAccountSubscriptionId : 7fe3301d-31d3-4668-af5e-211a890ba6e3
PredicateExpression          : statement <> 'select 1'
```

### <span data-ttu-id="ed2f9-117">2. példa: a blob-tárterület naplózási beállításainak beszerzése Azure SQL-adatbázisból</span><span class="sxs-lookup"><span data-stu-id="ed2f9-117">Example 2: Get the blob storage auditing settings of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -BlobStorage
DatabaseName                 : database01
AuditAction                  : {}
AuditActionGroup             : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                BATCH_COMPLETED_GROUP, ...}
ResourceGroupName            : resourcegroup01
ServerName                   : server01
AuditState                   : Enabled
StorageAccountName           : mystorage
StorageKeyType               : Primary
RetentionInDays              : 0
StorageAccountSubscriptionId : 7fe3301d-31d3-4668-af5e-211a890ba6e3
PredicateExpression          : statement <> 'select 1'
```

### <span data-ttu-id="ed2f9-118">3. példa: az Azure SQL-adatbázisok blob-tárterületének naplózási beállításainak beolvasása csővezetéken keresztül</span><span class="sxs-lookup"><span data-stu-id="ed2f9-118">Example 3: Get, through pipeline, the blob storage auditing settings of an Azure SQL database</span></span>
```
PS C:\> Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Get-AzSqlDatabaseAuditing
DatabaseName                 : database01
AuditAction                  : {}
AuditActionGroup             : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                BATCH_COMPLETED_GROUP, ...}
ResourceGroupName            : resourcegroup01
ServerName                   : server01
AuditState                   : Enabled
StorageAccountName           : mystorage
StorageKeyType               : Primary
RetentionInDays              : 0
StorageAccountSubscriptionId : 7fe3301d-31d3-4668-af5e-211a890ba6e3
PredicateExpression          : statement <> 'select 1'
```

### <span data-ttu-id="ed2f9-119">Példa 4: az esemény központi naplózási beállításainak beszerzése Azure SQL-adatbázisból</span><span class="sxs-lookup"><span data-stu-id="ed2f9-119">Example 4: Get the event hub auditing settings of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -EventHub
DatabaseName                        : database01
AuditAction                         : {}
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
ResourceGroupName                   : resourcegroup01
ServerName                          : server01
AuditState                          : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
PredicateExpression                 : statement <> 'select 1'
```

### <span data-ttu-id="ed2f9-120">Példa 5: az Azure SQL-adatbázisok esemény-központi naplózási beállításainak beolvasása csővezetéken keresztül</span><span class="sxs-lookup"><span data-stu-id="ed2f9-120">Example 5: Get, through pipeline, the event hub auditing settings of an Azure SQL database</span></span>
```
PS C:\>$database = Get-AzSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\>$database | Get-AzSqlDatabaseAuditing -EventHub
DatabaseName                        : database01
AuditAction                         : {}
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
ResourceGroupName                   : resourcegroup01
ServerName                          : server01
AuditState                          : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
PredicateExpression                 : statement <> 'select 1'
```

### <span data-ttu-id="ed2f9-121">Példa 6: az Azure SQL-adatbázisok naplózási beállításainak beszerzése</span><span class="sxs-lookup"><span data-stu-id="ed2f9-121">Example 6: Get the log analytics auditing settings of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalytics
DatabaseName        : database01
AuditAction         : {}
AuditActionGroup    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                       BATCH_COMPLETED_GROUP, ...}
ResourceGroupName   : resourcegroup01
ServerName          : server01
AuditState          : Enabled
PredicateExpression : statement <> 'select 1'
WorkspaceResourceId : "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

## <span data-ttu-id="ed2f9-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ed2f9-122">PARAMETERS</span></span>

### <span data-ttu-id="ed2f9-123">-BlobStorage</span><span class="sxs-lookup"><span data-stu-id="ed2f9-123">-BlobStorage</span></span>
<span data-ttu-id="ed2f9-124">Megadja, hogy a naplók a blob-tárolók legyenek</span><span class="sxs-lookup"><span data-stu-id="ed2f9-124">Specifies that audit logs destination is blob storage</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameterSet, BlobStorageByParentResourceSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed2f9-125">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ed2f9-125">-DatabaseName</span></span>
<span data-ttu-id="ed2f9-126">SQL-adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="ed2f9-126">SQL Database name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, EventHubSet, LogAnalyticsSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed2f9-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed2f9-127">-DefaultProfile</span></span>
<span data-ttu-id="ed2f9-128">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ed2f9-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed2f9-129">-EventHub</span><span class="sxs-lookup"><span data-stu-id="ed2f9-129">-EventHub</span></span>
<span data-ttu-id="ed2f9-130">Azt adja meg, hogy a naplók cél az esemény középpontja</span><span class="sxs-lookup"><span data-stu-id="ed2f9-130">Specifies that audit logs destination is event hub</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EventHubSet, EventHubByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed2f9-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ed2f9-131">-InputObject</span></span>
<span data-ttu-id="ed2f9-132">Az adatbázis-objektum a naplózási házirend kezeléséhez.</span><span class="sxs-lookup"><span data-stu-id="ed2f9-132">The database object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: BlobStorageByParentResourceSet, EventHubByParentResourceSet, LogAnalyticsByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed2f9-133">-LogAnalytics</span><span class="sxs-lookup"><span data-stu-id="ed2f9-133">-LogAnalytics</span></span>
<span data-ttu-id="ed2f9-134">Azt adja meg, hogy a naplók a naplózási naplókat jelentik</span><span class="sxs-lookup"><span data-stu-id="ed2f9-134">Specifies that audit logs destination is log analytics</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LogAnalyticsSet, LogAnalyticsByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed2f9-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed2f9-135">-ResourceGroupName</span></span>
<span data-ttu-id="ed2f9-136">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ed2f9-136">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, EventHubSet, LogAnalyticsSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed2f9-137">-Kiszolgálónév</span><span class="sxs-lookup"><span data-stu-id="ed2f9-137">-ServerName</span></span>
<span data-ttu-id="ed2f9-138">SQL-kiszolgáló neve.</span><span class="sxs-lookup"><span data-stu-id="ed2f9-138">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, EventHubSet, LogAnalyticsSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed2f9-139">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ed2f9-139">-Confirm</span></span>
<span data-ttu-id="ed2f9-140">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ed2f9-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed2f9-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed2f9-141">-WhatIf</span></span>
<span data-ttu-id="ed2f9-142">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ed2f9-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ed2f9-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ed2f9-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed2f9-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed2f9-144">CommonParameters</span></span>
<span data-ttu-id="ed2f9-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ed2f9-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed2f9-146">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ed2f9-146">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed2f9-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ed2f9-147">INPUTS</span></span>

### <span data-ttu-id="ed2f9-148">System. String</span><span class="sxs-lookup"><span data-stu-id="ed2f9-148">System.String</span></span>

### <span data-ttu-id="ed2f9-149">Microsoft. Azure. Command. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="ed2f9-149">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="ed2f9-150">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ed2f9-150">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ed2f9-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ed2f9-151">OUTPUTS</span></span>

### <span data-ttu-id="ed2f9-152">Microsoft. Azure. Command. SQL. könyvvizsgálat. Model. DatabaseBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="ed2f9-152">Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="ed2f9-153">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ed2f9-153">NOTES</span></span>

## <span data-ttu-id="ed2f9-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ed2f9-154">RELATED LINKS</span></span>
